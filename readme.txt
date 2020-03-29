/*
 KindleUnpack - The Plugin + ZIP mod v.0.3
   Copyright (C) 2020 junk2ool
 */

■概要
calibre用KindleUnpackプラグインを改造してazw3を画像のみのzipでも出力可能にしたものです。
DumpAZW6も取り込んであるのでresがあれば中にあるHD画像を差し替えて出力します。(要設定)
ついでに個人的なことで、
・画像のファイル名の連番の開始を00001に変更。(DumpAZW6の出力ファイルと同じ連番に)
・JPEG画像の拡張子をjpegからjpgに変更。
・zipは画像だけだとどうせ大して縮まないので無圧縮で作成されるように。(設定で圧縮するように変更可能)
・ファイル変換後に書籍毎に一時ファイルをすべて消すように。(設定で変更可能)
　(大量のファイルを変換した場合calibreを終了するまでTEMPディレクトリの容量を圧迫するため)
をしています。

■使用方法
KindleUnpackのメニューにzipで出力する項目が出来ているのでそれを実行してください。
DumpAZW6を使用したHD画像の差し替え機能を使うには、KindleUnpackのメニューの設定からKindle Contentのディレクトリの位置を設定してください。
その中の書籍のディレクトリ(*_EBOK)にresファイルがあれば自動的に差し替えてepubやzipを作成します。
上記の場所に見つからない場合は、calibreライブラリの書籍のディレクトリからresファイルを探して差し替えます。

■変更部分
__init__.py
action.py
config.py
dialogs.py
mobi_stuff.py
utilities.py
kindleunpackcore/DumpAZW6_v01.py
kindleunpackcore/kindleunpack.py
kindleunpackcore/mobi_cover.py
kindleunpackcore/unpack_structure.py
kindleunpackcore/DumpAZW6_v01.py
上記を主にzipで出力できるようにコードを修正、追加しています。

■使用したもの等
KindleUnpack - The Plugin Version: 0.82.1 Released: 18 Dec, 2019
https://www.mobileread.com/forums/showthread.php?t=171529
https://github.com/dougmassay/kindleunpack-calibre-plugin
DumpAZW6_v01.py
https://gist.github.com/fireattack/99b7d9f6b2896cfa33944555d9e2a158
ついでに、
http://rio2016.5ch.net/test/read.cgi/ebooks/1526467330/395
の>>395さんの修正も取り込んでいます。

■ライセンス
GNU General Public License v3.0

■履歴
2020/03/29 v.0.3
・設定ダイアログにzipの圧縮タイプを追加。(デフォルトは無圧縮)
・設定ダイアログに一時ファイルを常に削除するを追加。(デフォルトはオン)
・上記に伴い設定ダイアログを整理。
・テキストの一部日本語表示に対応。
・nav.xhtmlに存在しない表紙が登録され、表紙が二重になってしまうことがあったのを修正。

2020/03/17 v.0.2
・設定にKindle Contentディレクトリを設定する項目を追加。
・DumpAZW6の機能を追加。(上記の位置かcalibreライブラリの書籍のディレクトリにresがあればHD画像と差し替えるように)
・epub出力のデフォルトバージョンをAuto-detectに変更。
・ファイル変換後に書籍毎に一時ファイルをすべて消すように変更。
・配布ファイルの構造を変更。

2020/03/14 v.0.1
・なんとなく形になったので公開
