# Active Recordメソッドとは
- モデルがテーブル操作に関して使用できるメソッドの総称である
- テーブルに情報を保存したり取得するために使用する
- コードの入力方法は モデル名.メソッド名となる
- 例：Post.allでpostsテーブルの全てのデータを取得する
- 例:Posst.newでpostsテーブルにクラスのインスタンス（レコード）を生成する
- 例：Post.saveでpostsテーブルにクラスのインスタンスを保存する
- 例：Post.find(2)でpostsテーブルの2番目のデータを取得する（2）はidカラムの番号
- 例：post = Post.find(2)でpostという変数にpostsテーブルのidカラム2のデータを代入できる
- 例：post.contentsでpostsテーブルのidカラム2のデータの中のcontentsカラムの情報だけを取得する
