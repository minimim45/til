## gettr(ゲッター)のルール　フィールドの数分存在している（取得）

- **private （フィールドにしかつかない）フィールドの値の取り出し**

```java
public String getName(){
  return this.name;
  
}
public フィールドの型 getフィールド名(){//フィールド名()は大文字
  return this.フィールド名;  
}
**戻り値がboolean型のみいis~()というようになる```java

## setter(セッター)のルール（代入）
ある特定のフィールドに指定された値を代入するだけのメゾット（ゲッター）をは逆の働きをしている
Heroクラスの外から名前（値）ができるようになった。

```java
  public void setName(String name) {
     this.name = name;
  }
  
  public void getフィールド名(フィールド名 変数名){//フィールド名()は大文字//変数名はフィールド名になる
　　 this.変数名 = 変数名  
}```java

- もともとアクセス修飾子がついていたが困るからゲッターセッターを使えば代入も取得もできるようになってしまった
- メリット
- setだけを取ってgetだけにして読みとりのみＯＫにする
-将来的にgetter・setterを準備せずに開発の場で、new nameのフィールド名を変えてもほかのクラスに影響を及ぼすことは無い
-
