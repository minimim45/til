##String クラスに備わる文字列**検索** メゾット
- 文字列の中に含まれているか否かだけを判定するもの
- 「文字列のどこにふくまれているか」という位置情報を返すもno
- blooeanはあるかどうか
一部に文字列Sを含むかを調べる　public blooean contains(String s)
文字列Sで始まっているかを調べる　　public blooean startsWith(String s)
文字列Sで終わっっているかを調べる　　public blooean endsWith(String s)
- どこにあるか
- **先頭文字は0文字目と評す-1が帰ってきたら文字列の中に無かったということ
文字ch(または文字列str) が最初に登場する位置を調べる　public int　indexOf(int ch)
                                                       public int　indexOf(String str)
文字ch(または文字列str) が最後に登場する位置を調べる   public int　lastIndexOf(int ch)  
　　　　　　　　　　　　　　　　　　　　　　　　　　　public int　lastIndexOf(String str) 
                           
                       
 ```java
 public class Main15_2 {
  public static void main(String[] aregs) {
    String s1 = "Java and JavaScript";

    if(s2.contains("Java")) {
      System.out.println("文字列s1とJavaを含んでいます");
    }
    if(s2.containsWith("Java")) {
     System.out.println("文字列s1は、Javaが末尾にあります");
    }
     System.out.println("文字列s1は、最初にJavaが登場する位置は" + s1.indexOf("Java"));

    System.out.println("文字列s1は、最後にJavaが登場する位置は" + s1.lastIndexOf("Java"));


  }
}
