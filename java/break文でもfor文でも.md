
class Main {
  public static void main(String[] args) {
    System.out.println("=== while文 ===");
    int i = 1;
    while (i < 10) {　//for文でもオッケー
     if(i % 5 ==0) {
     break;
     }
      // iが5の倍数のとき、繰り返し処理を終了してください
      
      
      System.out.println("i" + i);
      i++;
    }
    
    System.out.println("=== for文 ===");
    for (int j = 1; j < 10; j++) {
      // jが3の倍数のとき、処理をスキップしてください
      if (j % 3 == 0) {
        continue;
      }
      
      System.out.println("j" + j);
    }
  }
}
i１、２、３、４、
ｊ１、２、４、５、７、８、
