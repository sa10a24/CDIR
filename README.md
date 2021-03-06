# cdir-collector

[English](README_en.md)

cdir-collectorは初動対応時のデータ保全を支援するためのツールです。Windows PC上の以下のデータを取得することが可能です。

* メモリ
* MFT
* UsnJrnl
* プリフェッチ
* イベントログ
* レジストリ
* Web(履歴、クッキー)

## ダウンロード

バイナリ版は以下から入手可能です。

https://github.com/CyberDefenseInstitute/CDIR/releases

## ビルド

ソースコードはVisual Studio 2015で読み込みビルドすることができます。cdir-collectorの構成ファイルは以下の通りです。

* cdir.ini
* cdir-collector.exe
* NTFSParserDLL.dll
* libcrypto-38.dll
* libssl-39.dll
* winpmem.exe

## 使い方

cdir-collector.exeを含む関連ファイル一式をUSBメモリやファイルサーバ上に配置してから実行することを想定しています。cdir-collector.exeをダブルクリックして実行してください。実行には管理者権限が必要です。実行場所に"コンピュータ名_年月日時分秒"フォルダを作成し、そのフォルダ配下にデータを保存します。

cdir.iniファイルを編集することにより、それぞれのデータを取得する、しないを切り替えることができます。

## サードパーティ

cdir-collectorは以下のライブラリ、ツールを活用しています。

* ライブラリ: NTFSParserDLL, LibreSSL
* ツール: winpmem

winpmem.exeはrekallプロジェクト (https://github.com/google/rekall) で提供されているWindows用のメモリ保全プログラムです。
