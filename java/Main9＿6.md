```java
public class Main9_6{
  public static void main(String[] args){
    Hero h1 = new Hero();
    h1.name = "ミナト";
    h1.hp = 100;
    Hero h2 = new Hero();
    h2.name = "アサカ";
		h2.hp = 100;
		Wizard w = new Wizard();
		w.hp = 50;
		w.heal(h1);	//ミナトを回復させる（HP:１００→１１０）Wizardクラスからミナトを１０回復させるさせている
		w.heal(h2);	//アサカを回復させる（HP：１００→１１０）
		w.heal(h2);	//アサカを回復させる（HP:１００→１２０）
	}
}
