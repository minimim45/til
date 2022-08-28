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
