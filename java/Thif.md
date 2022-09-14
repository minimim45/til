```java
public class Thif {
  String name;
  int hp;
  int mp;
	public void Thif(String name,int hp, int mp) {
	  this.name =name;
	  this.hp = hp;
	  this.mp = mp;
	}
	public Thif (String name, int hp) {
  //this name = name
  //this hp = 35;
  //this mp = 5;

  
  this(name,hp,5);
}
	public Thif (String name) {//上から持ってくる
	  //this name = name
	  //this hp = 40;
	  //this mp = 5;
	  this(name, 40,/*5*/);


	}
}
