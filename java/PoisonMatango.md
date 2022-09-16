public class PoisonMatango extends Matango {
  int poisonCount = 5;

  public PoisonMatango(char suffix) {//識別をする
    super(suffix);//親から呼び出し
  }

  public void attack(Hero h) {//攻撃する
    super.attack(h);
    if (this.poisonCount > 0) {
      System.out.println("さらに毒胞子をバラまいた！");
      int damage = h.hp / 5;
      h.hp -= damage;
      System.out.println(h.hp + "ポイントダメージ！");
      this.poisonCount--;
    }
  }
}
