 ```java
 
 public String toString() {
    return "名前：" + this.name + "/HP：" + this.hp;
  }
}
**とするとオーバーライドしているのでtoStringメゾットが呼び出されるので、勇者のインスタントをMain14＿4にわたすことができる**

public class Main14_4{//
  public static void main(String[] args){
    Hero h = new Hero();
    h.setName ("ミナト");
    h.setHp(100);
    System.out.println(h.toString());//toString()なくてよい
  }
}　toString  System.out.println(h.toString());に入る

toString　はインスタンス化するクラスにオーバーライドさせることが必要
Mainクラスはインスタンス化させる必要がないためtoStringする必要がない
インスタンスわたして終了となる
