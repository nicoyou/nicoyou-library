# nlib3

ちょっと便利な関数やクラスを使用できます。


# Release Notes
```text
----------------------------------------------------------------------------------------------------------
ver.1.17.0 (2022/12/10)
属性を文字列として扱う列挙子を定義できる StrEnum クラスを追加
JsonData クラスに file_exists メソッドと __str__ メソッドを追加
イテラブルな型のエイリアスを 4 種類追加
get_datatime_now 関数にオーバーロードを追加

一部関数の型ヒントが間違っていた不具合を修正
format構文を f文字列 に、文字列で定義されているファイルパスを pathlib にリファクタリング

----------------------------------------------------------------------------------------------------------
ver.1.16.0 (2022/11/12)
Url クラスを追加
Vector2 クラスに set メソッドを追加

インデントをタブからスペースに変更

----------------------------------------------------------------------------------------------------------
ver.1.15.0 (2022/09/09)
型ヒントを Python 3.10 で追加された書き方に変更 ( Python 3.9 以下では実行不可 )
Vector2 クラスに比較演算子、算術演算子、単項演算子のオーバーロードを追加
Vector2 クラスに 6 つの関数を追加
Vector2 クラスのコンストラクタにリスト、タプル、自クラスを指定できる機能を追加

----------------------------------------------------------------------------------------------------------
ver.1.14.0 (2022/07/12)
ライブラリ名を nlib に変更、PyPIに公開
load_json() 関数と save_json() 関数を追加
JsonData() クラス内のファイルIO処理を全て新規追加した関数に変更
ファイルIO時の標準エンコードを定数に追加

----------------------------------------------------------------------------------------------------------
ver.1.13.0 (2022/07/05)
get_check_digit() 関数を追加
サードパーティー製ライブラリを使用していた convert_file_encoding() 関数を削除
download_file() 関数と、download_and_check_file() 関数で対応できるエラーを追加
download_and_check_file() 関数に再試行に関するパラメーターを指定できる引数を追加、返り値の型を変更
エラーコード名 LibErrorCode.file を LibErrorCode.file_not_found に変更

----------------------------------------------------------------------------------------------------------
ver.1.12.0 (2022/06/07)
全クラスと関数に引数の型と返り値の型を追加、トップのコメントをdocstringに書き換え
Vector2 クラスの仕様を変更し、コンストラクタで x しか値が与えられなかった場合は y が 0 で初期化されるように変更
print_log() 関数にログを出力するファイル名を指定する事ができる引数を追加
マルチスレッドのデコレータ関数がスレットを返すように変更

関数内のデバッグ出力で print_debug() 関数を使用せずに print() 関数を使用していた箇所がいくつかあった不具合を修正
ファイルをダウンロードする関数が 302 エラーを稀に起こす対策としてユーザーエージェントを追加

----------------------------------------------------------------------------------------------------------
ver.1.11.0 (2021/10/03)
ファイルパスの指定した階層をリネームする関数を追加
OSのコマンドを実行する関数を追加
print_debug 関数に引数 end を追加

----------------------------------------------------------------------------------------------------------
ver.1.10.1 (2021/07/16)
JsonData()クラスで、同時に同じファイルを更新しようとすると、ファイルのデータが初期化される不具合を修正
返り値の値を調整、JsonData.incrementをリファクタリング

----------------------------------------------------------------------------------------------------------
ver.1.10.0 (2021/06/06)
JSON文字列を整形して print 出力する関数を JsonData クラスに追加
関数をマルチスレッドで実行するためのデコレーターを追加
print_log関数でクラス名が存在しないときにクラッシュすることがある不具合を修正
PyLintを使用して、プログラムをリファクタリング

----------------------------------------------------------------------------------------------------------
ver.1.9.0 (2021/04/24)
２次元ベクトルの値を保存する構造体を追加
read_tail 関数で encoding を指定できるように引数を追加
print_log 関数のエラーログを出力する際の引数を bool 値のフラグを指定するだけで出力できるように簡略化

----------------------------------------------------------------------------------------------------------
ver.1.8.0 (2021/04/09)
エラーログに出力されるソースコードの情報にファイル名とクラス名を追加
エラーログが複数行の場合は、２行目以降の左の空白に日時が出力されるように変更
ログファイルの最大容量を 10MB から 50MB まで増加

----------------------------------------------------------------------------------------------------------
ver.1.7.0 (2021/03/13)
スタックされているエラーを表示する関数を追加
指定されたファイルが指定された文字コードでなければ指定された文字コードに変換する関数を追加
ネストされた辞書内の特定の値のみを再帰で変更する関数を JsonData クラス内からライブラリの関数に移動
ログを出力する際に OS のデフォルト文字コードで出力していたのを utf-8 で出力するように変更
JsonData クラスに値をインクリメントしてファイルに保存する関数を追加
JsonData クラスで扱うファイルの文字コードを OS のデフォルト文字コードから utf-8 に変更 ( 過去verで保存したファイルの読み込み不可 )
JsonData クラスで読み込んだJsonファイルに文法エラーがあった場合に、データを新しく上書き保存できない不具合を修正

----------------------------------------------------------------------------------------------------------
ver.1.6.0 (2021/03/07)
Jsonデータを読み込んで保持するクラスで、自由な数のキーを指定できる用に変更
キャストできるかどうかを確認する関数を追加

----------------------------------------------------------------------------------------------------------
ver.1.5.0 (2021/02/15)
ファイルを後ろから指定した行だけ読み込む関数を追加
16進数の文字列を圧縮、展開する関数を追加

----------------------------------------------------------------------------------------------------------
ver.1.4.0 (2021/01/12)
Pythonのバージョン情報を文字列で取得する関数を追加
デバッグログを出力する関数を追加
ログに出力する日付の計算に get_datatime_now 関数を使うように変更

----------------------------------------------------------------------------------------------------------
ver.1.3.1 (2020/12/24)
get_datatime 関数の名前を get_datatime_now に変更、文字列に変換した際のフォーマットを変更

----------------------------------------------------------------------------------------------------------
ver.1.3.0 (2020/12/01)
日本の現在の datetime を取得する関数を追加
Jsonデータを読み込んで保持するクラスを追加
初期化関数をライブラリ内で使用するディレクトリを作成する関数に名前を変更

----------------------------------------------------------------------------------------------------------
ver.1.2.1 (2020/11/24)
ログを出力する際に、元のメッセージの最後に改行が含まれていた場合は改行を削除するように調整
エラーログを出力する関数を複数行のログに対応
起動時の初期化処理を行う関数を作成

----------------------------------------------------------------------------------------------------------
ver.1.2.0 (2020/10/29)
条件に一致する文字が入力されるまで再入力を求める入力関数を追加

----------------------------------------------------------------------------------------------------------
ver.1.1.1 (2020/10/20)
download_file関数とdownload_and_check_file関数でファイルが既に存在する場合に上書きするかどうかを指定できる引数を追加

----------------------------------------------------------------------------------------------------------
ver.1.1.0 (2020/10/17)
通常のログを出力する関数を追加
プログラム終了時に一時停止する関数を追加
リンク先が存在するかどうかを確認する関数を追加
ライブラリ内エラーコードからエラーメッセージを取得する関数を追加
列挙型のライブラリ内エラーコードを追加

インターネット上からファイルをダウンロードする関数で、存在しないURLを指定するとクラッシュする不具合を修正
print_log関数に文字列以外のものを渡した際にクラッシュする不具合を修正

----------------------------------------------------------------------------------------------------------
ver.1.0.0 (2020/10/15)
初版
エラーログを出力する関数を実装
インターネット上からファイルをダウンロードする関数を追加
ファイルをダウンロードして、失敗時に再ダウンロードを試みる関数
```


# Author

Nicoyou
