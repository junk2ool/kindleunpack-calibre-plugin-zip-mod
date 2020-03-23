/*
 KindleUnpack - The Plugin + ZIP mod v.0.1
   Copyright (C) 2020 junk2ool
 */

■概要
calibre用KindleUnpackプラグインを改造してazwを画像のみのzipでも出力可能にしたものです。
ついでに個人的なことで、
・画像のファイル名の連番の開始を00001に変更。(DumpAZW6の出力ファイルと同じ連番に)
・JPEG画像の拡張子をjpegからjpgに変更。
・zipは画像だけだとどうせ大して縮まないので無圧縮で作成されるように。
をしています。

■変更部分
action.py
dialogs.py
mobi_stuff.py
mobi_cover.py
kindleunpack.py
unpack_structure.py
上記を主にZIPで出力できるようにコードを修正、追加しています。

■使用したもの等
KindleUnpack - The Plugin Version: 0.82.1 Released: 18 Dec, 2019
https://plugins.calibre-ebook.com/
ついでに、
http://rio2016.5ch.net/test/read.cgi/ebooks/1526467330/395
の>>395さんの修正も取り込んでいます。

■ライセンス
元がGPL v3なのでこれもGPL v3に基づきます。

■履歴
2020/03/14 v.0.1
・なんとなく形になったので公開
