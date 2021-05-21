# Week3
# クラス
今週は、クラスについて学習していきます。
クラスは直感的に説明すると、構造体＋関数です。構造体に関数を追加した概念です。

極端に言えば、関数・構造体・クラスはソースコードの保守性向上と直感的な理解度向上のためのツールみたいなものです。
なので、これらを使用しなくても、勿論コーディングは可能です。
しかし、大規模なプログラミング開発になればなるほど、これらの概念は非常に重要になってきます。
皆も卒業研究をしていくうちに気がついていくと思います。
<p align="center"><a href="http://cpp-lang.sevendays-study.com/day2.html">参考ウェブサイト(クラス)</a></p>

## 一問目
### ①簡単なクラスを作る
<p align="left"><a href="https://github.com/ERiC-Labo/C_Journal_club/blob/main/Week3/numbler.hpp">number.hpp</a></p>

実行結果が
```
数字を入力してください
342
あなたが入力した数字は num = 342 です。
```
になるようにクラスを定義するためのファイルnumber.cppファイルを作成してみてください。
### ②名前空間を追加する
##### rikuken_number.hpp
```
数字を入力してください
342
あなたが入力した数字は num = 342 です。
```
になるようにrikuken_number.cppファイルを作成してみてください。


## 二問目
Week2で作成したソースコードをクラス化してください。(行列クラスを作って下さい。)
アクセス演算子・カプセル化等を用いて、どのようにすればユーザフレンドリーになるか工夫してクラス化してみてください。

## 三問目
"start"という文字を出力する処理をコンストラクタに設定して下さい。"finish"という文字を出力する処理をデストラクタに設定してください。
そして、作成したクラスを使用して、行列の足し算を行ってください。

(ターミナル実行例)

------start-------

matrix1:[[],[],...]

matrix2:[[],[],...]

add_result:[[],[],...]

------finish-------

<p><a href="https://github.com/ERiC-Labo/C_Journal_club/tree/main/Week2">Week2のリンク</a></p>
<p align="right"><a href="https://github.com/ERiC-Labo/C_Journal_club/tree/main/Week4">Week4のリンク</a></p>
