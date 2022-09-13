public class Main9_11{//神様クラス//newを引数を渡す
  public static void main(String[] args){
    Hero h = new Hero("ミナト");//インスタント生成後、ＪＶＭがコンストラクタを呼び出す際に「ミナト」を渡してもらえる


		System.out.println(h.hp);//コンストラクタで100
		System.out.println(h.name);//コンストラクタの引数に入れてJVMに渡すミナト
	}
}
