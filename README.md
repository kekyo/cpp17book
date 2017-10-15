# C++17の新機能の差分本

著者：江添亮

ブログ: https://cpplover.blogspot.jp/

とりあえず書く。

[GitHub Pageで閲覧:C++17の新機能](https://ezoeryou.github.io/cpp17book/index.html)

# 参考書の構成

参考書のソースコードはPandoc markdownで記述されている。

ソースコードのファイル名は、"3文字の数字-記述内容の概要.md"となっている。ファイル名でソートした順番で結合される。

C++のコード例のうち、すべての標準ヘッダーファイルが#includeされていればwell-formedなものは、

~~~~
~~~cpp
C++のコード例
~~~
~~~~

で囲む。

C++のコード例のうち、意図的にill-formedなものは、

~~~~
~~~c++
C++のコード例
~~~
~~~~

で囲む。


# 参考書のビルド

参考書はmarkdownからpandocを使って目的のフォーマットに変換される。

pandocを呼び出すためにMakefileを使っている。これはGNU Makeで使うことを前提として記述されている。

参考書をHTMLファイルにするには、makeを使う。index.htmlが生成される。

~~~
make
~~~

参考書を単一のmarkdownファイルにするにはmakeを使う。index.mdが生成される。

~~~
make index.md
~~~



# 参考書を紙の本で印刷する工程

参考書を紙の本で印刷する場合、想定される工程は以下のようになる。

## アスキードワンゴから出版される場合

1. pandocを使ってmarkdownからtexに変換
1. 生成されたtexを編集者が手で編集

## その他の製本方法

以下は、大多数の出版社で想定される方法である。

+ pandocを使ってmarkdownからInDesign ICMLに変換。生成されたInDesignを手で編集。
+ markdownを編集者が目で読み、手でInDesignに入力。
