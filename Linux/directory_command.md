# Linux【ディレクトリコマンド】

# はじめに
これは学習用のメモになります。

* ディレクトリとはフォルダのことです。ファイルを格納するフォルダのこと。

##1.cd(change directory）
```
cd [ディレクトリ]
```
ディレクトリを移動するコマンド

###特別なディレクトリの指定
カレントディレクトリ、親ディレクトリ、ホームディレクトリには特別な指定方法がある

|ディレクトリ| 意味　|指定方法　
|:------:|:------:|:------|
|カレントディレクトリ | 現在自分がいるディレクトリ| 「.」|
|親ディレクトリ | 一つ上の階層のディレクトリ| 「..」|
|ホームディレクトリ| 「/home/ユーザー名」ディレクトリ| 「~」|
|ルートディレクトリ | 「/」ディレクトリ|「/」|


##2.pwd
```
pwd [オプション]　　　#ほとんどオプションをつけることはない
```
カレントディレクトリを表示するコマンド
今どこのディレクトリにいるのか教えてくれるコマンド

##3.ls
```
ls [オプション][ディレクトリ・ファイル名]　
```
ファイルやディレクトリの一覧を表示するコマンド
今いるディレクトリの中に入っているフォルダ/ファイルがわかる


###便利なパス名展開
パス名展開を使うと複数のファイルを一度に指定できる

####パス名展開

|記号| 意味
|:------:|:------:|
|* | 任意の文字列| 
|？| 任意の1文字|

```
具体例
#拡張子がhtmlのファイルの一覧を表示
$ls *.html
index.html home.html job.html

#zから始まり4文字で終わるファイルを表示
$ls /bin/z???
/bin/zcat /bin/zcmp /bin/znew
```

###よく使うオプション

#####ls -l
ファイルの詳細情報を表示する

#####ls -a 
隠しファイルも含めた全てのファイルを表示する

#####ls -F
ファイルの種別を表示


##4.mkdir(make directory)
```
mkdir [オプション]<作成するディレクトリ名>
```
ディレクトリを作成するコマンド

###よく使うオプション

####-p
深いディレクトリを一度に作成する
-pオプションをつけるとtest,2019というディレクトリを事前に作らなくていい

```
$mkdir -p test/2019/08
```

##5.rmdir(remove directory)
```
rmdir <ディレクトリ名>
```
空のディレクトリを削除するコマンド(空でないディレクトリを削除しようとするとエラーになります）
あまり使うことはない（ほとんどrmコマンドを使うことが多い）

##6.パス
パスはディレクトリやファイルの住所情報。
ディレクトリの階層の区切りを「/」で表現する

###パスの種類
####1)絶対パス
絶対パスはルートディレクトリ（「/」)から始まるパス。

```
/home/kume/code/README.md
```
####2)相対パス
相対パスはカレントディレクトリから始まるパス。

```
code/README.md
```
