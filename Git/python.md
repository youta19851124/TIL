# python基礎知識
- 拡張子は.py
- 機能をまとめたものを「関数」と呼ぶ
- 関数を使うことで計算や処理を簡単に行い作業を進められる
- pythonには便利な関数がたくさん用意されている
- 例：len関数　文字列の文字数をか数えてくれる (半角スペースも1文字としてカウントされる)
- 例：str関数　数値を文字列に変換してくれる str(20)  出力結果：'20'
- 例：int関数　文字列を数値に変換してくれる int("30") 出力結果：30
- 文字同士の連結はPythonのf文字列を使えばより綺麗に書ける
- 例：f"今日で{19 + 1}歳になりました" 出力結果："今日で20歳になりました"
- 例：f"タロウさん、{5}分は{5 * 60}秒です！“ 出力結果： 'タロウさん、5分は300秒です！'
- pythonもrubyやjavascriptと同様に変数が使える 例：pi = 3.14159 変数piは数値と同様に計算式に使うことができる
- print関数 pythonに用意された値を出力するための関数 printの後ろに()の中に値を入力すると値が出力される　rubyでいうputs javaでいうconsole.log
- 例：name = "Taro"  print(name) 出力結果： "Taro"
- 変数には再代入が何度でも可能 例：pi = 3.15 pi = 3.142
- 変数を使った計算式例： number = 7,  number = number + 1,  print(number) 出力結果：8
- number += 1 はnumber = number + 1 と同じ意味である。 自己代入演算子(+=,-=,/=,*=)を使えば記述量も少なくて済む
- 変数の命名規則： 変数の中身が何かわかる, 小文字で始める, 数字で始めない, 日本語を使わない, スペースを含めない, 予約語を使用しない(Pythonには文法などで使うことがあらかじめ決まっている単語があり、それを予約語と呼ぶ。これらを使うとエラーが生じる)
- 以下の例は直径が10の円の、面積と円周を計算して変数に代入している
  直径10の場合
  menseki = (10 / 2) * (10/ 2) * 3.14   面積
  print (menseki)
  ensyu = 10 * 3.14   円周
  print (ensyu)   31.400000000000002
- このソースコード上では直径を示す「10」が3回も出ている。もし直径を20に変更する場合、10と書いてある箇所をすべて20に訂正するのは大変なうえ、訂正し忘れる可能性もある。
  また、ただ「10」とだけ書かれても何の値かわかりづらいので、上のソースコードを以下のように変更する。
　　　　例：chokkei = 10　, menseki =(chokkei/ 2) *(chokkei/ 2) * 3.14, print (menseki)
- ensyu = chokkei * 3.14, print (ensyu),  31.400000000000002
- これなら直径を20に変える場合も、変数の値を変更すれば良いだでけで済む
- 例：chokkei = 20, menseki = (chokkei / 2) * (chokkei / 2) * 3.14, print (menseki) 314.0, ensyu = chokkei * 3.14, print (ensyu)  62.800000000000004
- 可読性も柔軟性も一気に向上した。このように、できるだけ変数を使ってわかりやすいコードを書くよう心がける。
- name = "takashi" 文字数を調べる, name_ length = len (name), print (name_ length) 出力結果：7, print (name) 出力結果：'takashi'
- 変数を使うことで、文字列の意味もわかりやすくなり、値を再利用することも簡単になった。
- "ようこそ！名前を入力してください", name ゠ “タロウ", 秒数を知りたい時間を分単位で入力してください", 5 minutes = 5, f"{name}さん、{minutes}分は{minutes * 60}秒です！"
- 名前、分単位の時間を変数で定義して置き換えました。これによって、たとえば秒数を知りたい時間に変更があっても、minutesを定義している5行目を変更するだけで済みます。変更に強いコードになりましたが、 minutes * 60 としている部分は、計算内容はわかっても、その計算結果が何をあらわしているのか理解しづらいです。コード量が増えると、こうした記述はミスを生むおそれがあるため、避けるべきです。このコードを少し工夫しましょう。
- "ようこそ！名前を入力してください", name ゠ "タロウ", "秒数を知りたい時間を分単位で入力してください" minutes = 5, seconds = minutes * 60, f"{name}さん、{minutes}分は{seconds}秒です！
- 秒数をあらわす「seconds」という変数を定義しました。変更前と比べても、文字列にどのような意味の値が含まれているかわかりゃすくなりました。
- コードをpythonで実行すると出力結果は： 'タロウさん、5分は300秒です！！'となる。
- input関数　ターミナルが入力待ちになり、入力された値は文字列として返される　例： name = input ( ), print (name)
- 例：　text = input ( ), print(f"入力した値は「text」です")
- バックスラッシュ記法　　Macの場合 option + ¥ でバックスラッシュを打つことができる。
- 記法：　\n 意味：　改行, 　例：　text = input ( ), print(f"入力した値は「text」です"), print(f"入力した値はftext}です\n"), print(f"入力した値はftextトです")
- 記法：　\t 意味：　タブ, 　記法：　\b 意味：　バックスペース, 記法：　\ 意味：　バックスラッシュ
- 例：print(“ようこそ！\n名前を入力してください"), name = input (), print(“秒数を知りたい時間を分単位で入力してください"), minutes = input ( ), seconds = minutes * 60, print(f"fname」さん、fminutes}分は「seconds}秒です！"),　 okamotoさん、5分は555555555555555555555555555555555555555555555555555555555555秒です！, 表示がおかしい。
- minutes = int(input ( )) 文字列ではなく数値に変換することで直る。　okaotoさん、5分は300秒です！
- 配列：　箱の中に要素を順番に格納する。　配列の宣言例：　変数 = []
- pencil_case =["ペン"，"消しゴム"，"定規"], print (pencil_case), 出力結果：　［ペン，消しゴム，定規]
- appendメソッド：　生成した配列に新しい要素を追加したいときに使用する。　例：　pencil_case =［"ペン"，"消しゴム"，“定規"], pencil_case. append ("えんぴつ"), print (pencil_case)
出力結果：　［'ペン'，'消しゴム'，'定規'，'えんぴつ']
- 配列の要素数をlen関数を用いて数える方法
- 例：　pencil_case = 【ペン"，"消しゴム"，“定規"］, print(len (pencil_case)), pencil_case.append("えんぴつ"), pencil_case.append("付箋"), print (len(pencil_case)) 出力結果：　3 5
- ミニアプリを作成
- 名前、身長の情報を配列に追加します。 また、乗車できる人数を管理する変数ride_countも用意します。
- 入力の案内も出力しておきましょう。
- ride_count = 0
- friends = []
- print("お友達の名前は？")
- friends. append(input ())
- print("お友達の身長は？")
- friends.append(int(input () ) )
- ride_count += 1
- print("お友達の名前は？")
- friends.append(input () )
- print(“お友達の身長は？“)
- friends.append(int(input () ) )
- ride_count += 1
- print("お友達の名前は？")
- friends. append(input ( ))
- print("お友達の身長は？")
- friends.append(int(input ( )) )
- ride_count += 1
- print(f"乗車するのは{ride_count}人です"）
- 実行すると、合計6回のinputによる入力を経た後に、乗車人数が出力されることを確認しましょう。
- お友達の名前は？
taro
お友達の身長は?
120
お友達の名前は？
jiro
お友達の身長は?
130
お友達の名前は？
saburo
お友達の身長は?
100
乗車するのは3人です
- まとめ：　配列は、1つの変数で複数の値を持つことのできる値, 配列の中のデータは「要素」と呼ばれる, appendメソッドは、生成した配列に新しい要素を追加できる, 添字は、配列の各要素に割り振られた番号、添字は「0」から始まる, len関数は配列の要素数を返す
- 配列だと名前と身長の関係性（誰の身長？）の管理が難しい。そこで、辞書で管理することが好ましい。辞書においては、データを バリュー、それに対応する名前をキーと呼びます。rubyでいうハッシュのこと。
- 辞書を定義する例：　変数 = { キー1 ： バリュー1, キー2 ： バリュー2, キー3 ： バリュー3 }
- student = {"name": "John", "age": 10 } , teacher = {"name": "Mike", "age": 25 }
- print (student)　出力結果：　{'name': 'John', 'age': 10 }
- print(teacher)　出力結果：　{'name': 'Mike', 'age': 25 }
- 辞書にデータを追加する：　[]を用いて追加できる, 例： teacher = {"name": "Mike", "age": 25 }, teacher["subject"] = "English", print (teacher), 出力結果：　{'name': 'Mike',
'age': 25, 'subject': 'English"}
- 辞書で値を取得するには 辞書［取得したい値のキー］といった形で取得できる。（配列の場合は添字）
- 例：　print(teacher ["name"])　, 出力結果：　Mike
- 辞書の値を変更するには 辞書［変更したい値のキー］ = 値　　といった形で変更できる
- 例：　teacher ["name"] = "Emma", print(teacher["name"]), 出力結果：　Emma
- 辞書で管理する際のデメリットとして、複数の辞書（teacher1, teacher2, teacher3、、、)を管理する際に名前とデータが一致しない場合が出てくる。そこで、配列と辞書を組み合わせることで管理がしやすくなる
- 例：teachers[{ name: "Mike", age: 25 }, {name: "Emma", age: 28 }], print(teachers)[1], 出力結果： {name: "Emma", age: 28 }
- 配列と辞書を組み合わせることで、別々の意味を持つ複数の値のまとまり自体を複数管理できる
- friend = {}
- print("お友達の名前は？“)
- friend ["name"] = input ( )
- print("お友達の身長は？”)
- friend ["height"] = int(input ( ) )
- friends append(friend)
- ride_count += 1
- friend = {}
- print(“お友達の名前は？")
- friend ["name"] = input ( )
- print("お友達の身長は?")
- friend["height"] = int(input () )
- friends.append(friend)
- ride_count += 1
- friend = {}
- print(“お友達の名前は？")
- friend ["name"] = input ()
- print("お友達の身長は？")
- friend ["height"] = int(input ( ))
- friends.append(friend)
- ride_count += 1
- 条件分岐と比較演算子を用いて身長制限をしてみる
- Rubyと同じif文を使うが、pythonではendではなくインデントの変化で処理の終了を判断する
- 例：　if(条件式):
- ____(インデント4つ）処理1
- ____(インデント4つ）処理2
- print(インデントが4つから0に変わっているのでブロック終了)
