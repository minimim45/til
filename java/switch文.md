
public class Main {
  public static void main(String[] args) {
    System.out.println("あなたの運気を占います");
    int fortune = new java.util.Random().nextInt(5) + 1;
    switch (fortune){
      case 1:

      case 2:
       System.out.println("いいね");
       break;
      case 3:
       System.out.println("普通です");
       break;
      case 4:

      case 5:
        System.out.println("うーん...");
     }
  }
}

//switch文に書き換えることができる条件
①左辺＝＝右辺が一致するか比較式の時。
②整数、文字列または文字であり少数や真偽型ではない
//switch文記述の際の注意点
fortune＝変数名
caseの横には値を書きその後ろに：をつけるcase値（数字）：
caseの末尾にはbreak文を記述する
default:を書くとどの条件に合わない場合にデフォルトで処理する

