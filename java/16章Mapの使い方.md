## Mapとは2つの情報をキーと値のペアとして格納売ることができるデータ構造
Map＜キーの値、値の型＞マップ変数＝newHashMap＜キーの値、値の型＞（）；

|  操作 |  戻り値  |  メゾット  |  意味  |
| ---- | ---- | ---- | ---- |
|  追加  | ■|  put(●,■) |  マップに●と■のペアを格納する |
|  取得 |  ■  |  get(●)  |  キーの値●に対応する値の取得 |
|  調査 |  int  |  size() |  格納されているペア数を数える  |
| 調査 |  boolean  |  isEmpty()  |  要素数がゼロであるかを判定する  |
| 調査 |  boolean  |  containsKey(●)  |  指定データがキーに含まれるかを判定  |
| 調査 |  boolean  |  containsValue(■)  |  指定データが値に含まれているかを判定  |
| 削除 |  void  |  clear()  |  要素をすべて削除する  |
| 削除 |  ■  |  remove(●)  |  指定した内容を削除する  |
| その他 |  Set<●>  |  keySet()  |  格納さているキーの一覧を返す  |

**マップに格納された情報を1つずつ取り出す**
for(キーの型key :マップ変数.keySet()) {
値の型valeue = マップ変数.get(key);
//keyとvaleueを用いて何らかの処理を行う//
**格納順を保証しない
```java
import java.util.*;

public class Main16_7{
  public static void main(String [] args) {
    //HashMapwoをインスタント化させる
    Map<String,Integer> prefs = new HashMap<String,Integer>();//<String,Integer>省略できる//2つある
    //要素を追加
    prefs.put("京都府",255);
    prefs.put("東京都",1261);
    prefs.put("熊本県",181);
    //キーを指定して値を1つずつ取得する
    for(String key : prefs.keySet()) {
      int value = prefs.get(key);
      System.out.println(key + "の人口は、" + value);
    }
  }
}
