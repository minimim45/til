# for文
## for文の基本
- 記述方法
  1. 初期化式
      - ループを開始するたびに評価され、”true”のときに"{}"内のブロックの処理を行う
  2. 条件式
      - for文の最初に一度だけ実行される
      - この条件式でループ処理を行う回数を指定する事ができる
  3. 変化式
      - ループ処理が終わるたびに実行される式です

```java
for (初期化式; 条件式; 変化式) {
    // 条件式がtrueのときに繰り返す処理
}
```
## for文を「スキップ」「抜ける」方法
1. break
    - for文の中でbreak文が実行されると、for文の残りの処理を終了して次の処理に移る
2. continue
    - for文全体を終わらせるのではなく、現在のループ処理の残りをスキップして次のループ処理を開始したい場合にはcontinue文を使う


## 様々なfor文の使い方
### 基本
```java
import java.util.ArrayList;
import java.util.List;
 
public class Main {
    
    public static void main(String args[]) {
        List<String> list = new ArrayList<>();
        list.add("a");
        list.add("b");
        list.add("c");
     
        for (int i = 0; i < list.size(); i++) {
            System.out.println(i + " : " + list.get(i));
        }
    }
    
}

// 結果
// 0 : a
// 1 : b
// 2 : c
```

### 省略形のfor(;;)
- for文の外で変数の初期化を行う場合は初期化式を省略できる
- for文の中で変数を増減させる場合は変化式を省略できる
- ただし、条件式を省略すると常に”true”となり無限ループになるので注意
```java
public class Main {
    public static void main(String[] args) {
 
        String[] strArray = { "s", "a", "m", "u", "r", "a", "i" };
 
        // 省略なし
        for (int i = 0; i < strArray.length; i++) {
            System.out.print(strArray[i] + " ");
        }
        System.out.println();
 
        // 初期化式を省略
        int i = 0;
        for (; i < strArray.length; i++) {
            System.out.print(strArray[i] + " ");
        }
        System.out.println();
 
        // 初期化式と変化式を省略
        i = 0;
        for (; i < strArray.length;) {
            System.out.print(strArray[i] + " ");
            i++;
        }
        System.out.println();
 
        // 条件式を省略すると常にtrueになる
        i = 0;
        for (;;) {
            System.out.print(strArray[i] + " ");
            i++;
            if (i == strArray.length) {
                break;
            }
        }
    }
}

// 結果
// s a m u r a i 
// s a m u r a i 
// s a m u r a i 
// s a m u r a i
```

### 2重ループ
- 2重ループは二次元配列のすべての要素を表示したい場合などに使われ
```java
public class Main {
    public static void main(String[] args) {
 
        String[][] strArray = { { "s", "a", "m", "u", "r", "a", "i" }, { "S", "A", "M", "U", "R", "A", "I" } };
 
        for (int i = 0; i < 2; i++) {
            for (int j = 0; j < 7; j++) {
                System.out.print(strArray[i][j] + " ");
            }
            System.out.println();
        }
    }
}

// 結果
// s a m u r a i 
// S A M U R A I
```

### 拡張for文
- 配列やListなどのコレクションのすべての要素に対して順番に処理を行うために使う
- 拡張for文は通常のfor文と違って条件式と変化式が無いため、簡潔にコードが記述できる
```java
public class Main {
    public static void main(String[] args) {
 
        String[] strArray = { "s", "a", "m", "u", "r", "a", "i" };
 
        for (String str : strArray) {
            System.out.print(str);
        }
    }
}

// 結果
// samurai
```

### forEachメソッド
- Java8でforEachメソッドとラムダ式が追加されました。これにより、さらに簡潔にコードが書けるようになりました
- [詳しくはコチラ](https://www.sejuku.net/blog/22232)
```java
import java.util.Arrays;
 
public class Main {
    public static void main(String[] args) {
 
        String[] strArray = { "s", "a", "m", "u", "r", "a", "i" };
 
        Arrays.stream(strArray).forEach(str -> System.out.print(str));
    }
}

// 結果
// samurai
```
