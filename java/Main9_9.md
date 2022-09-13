ublic class Main9_9{//神様クラス//newを引数を渡す
  public static void main(String[] args){
    Hero h = new Hero();//インスタント生成後、ＪＶＭがコンストラクタを呼び出す際に「ミナト」を渡してもらえる


		System.out.println(h.hp);//100．これはコンパイルできなくなる引数がnameが入っているから//
	}
}
