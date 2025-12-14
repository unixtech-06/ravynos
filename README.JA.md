# ravynOSとは？ [![Build Status](https://api.cirrus-ci.com/github/ravynsoft/ravynos.svg?branch=main)](https://cirrus-ci.com/github/ravynsoft/ravynos) [![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.1-4baaaa.svg)](CODE_OF_CONDUCT.md)
### 他の言語で読む: [English](README.md), [Italiano](README.IT.md), [Türkçe](README.TR.md), [Deutsch](README.DE.md), [Indonesia](README.ID.md), [简体中文](README.zh_CN.md), [繁體中文](README.zh_TW.md), [Português do Brasil](README.pt_BR.md), [한국어](README.KR.md), [فارسی](README.FA.md), [Magyar](README.HU.md), [日本語](README.JA.md)

ravynOSは、x86-64（および将来的にはARM）システム上でmacOSと同様の体験と一定の互換性を提供することを目指す、新しいオープンソースOSプロジェクトです。FreeBSDの強固な基盤、同じ領域の既存のオープンソースパッケージ、そしてそのギャップを埋めるための新しいコードの上に構築されています。

主な設計目標は以下の通りです：
- macOSアプリケーションとのソース互換性（つまり、ravynOS上でMacアプリケーションをコンパイルして実行できること）
- 同様のGUIメタファーと使い慣れたUX（ファイルマネージャ、アプリケーションランチャ、開いているアプリケーションを反映するトップメニューバーなど）
- macOSのフォルダ構成（/Library, /System, /Users, /Volumesなど）との互換性、そしておそらくファイルシステム（HFS+, APFS）との互換性、さらにZFSの完全サポート
- [App Bundles](https://developer.apple.com/documentation/foundation/bundle)、[AppDirs](https://github.com/AppImage/AppImageKit/wiki/AppDir)、および[AppImage](https://github.com/AppImage)ファイルによる自己完結型アプリケーション - /Applicationsへのインストーラー不要の体験
- FreeBSDベースシステムおよびX11との大部分の互換性維持 - 内部は標準的なUnix環境
- FreeBSDのLinuxサポートを通じたLinuxバイナリとの互換性
- 将来的なx86-64/arm64 macOSバイナリ（Mach-O）およびライブラリとの互換性
- 快適な使用感、セキュリティ、安定性、そしてパフォーマンス

詳細については [ravynos.com](https://ravynos.com/) をご覧ください: [リリースノート](https://ravynos.com/releases.html) | [スクリーンショット](https://ravynos.com/screenshots.html) | [FAQ](https://ravynos.com/faq.html)

### 参加しよう！

* 夢の構築を手伝ってくれませんか？ [CONTRIBUTING.md](CONTRIBUTING.md) で現在のプロジェクト/ニーズを確認してください！
* 我々の [Discord](https://discord.com/invite/8caJbAGNwY) サーバー。
* `#ravynOS-general:matrix.org` - [Element.io](https://app.element.io/#/room/%23ravynOS-general:matrix.org) 経由で参加

[![Packages hosted by: Cloudsmith](https://img.shields.io/badge/OSS%20hosting%20by-cloudsmith-blue?logo=cloudsmith&style=flat-square)](https://cloudsmith.com)

---

FreeBSD ソース:
---------------
これはFreeBSDソースディレクトリのトップレベルです。

FreeBSDは、現代のサーバー、デスクトップ、組み込みプラットフォームを動かすために使用されているオペレーティングシステムです。
大規模なコミュニティにより、30年以上にわたって継続的に開発されてきました。
その高度なネットワーク、セキュリティ、ストレージ機能により、FreeBSDは多くの最も忙しいWebサイトや、最も普及している組み込みネットワークおよびストレージデバイスに選ばれるプラットフォームとなっています。

著作権情報については、このディレクトリ内の [ファイル COPYRIGHT](COPYRIGHT) をご覧ください。
追加の著作権情報は、このツリーの一部のソースにも存在します - 詳細については、特定のソースディレクトリをご覧ください。

このディレクトリのMakefileは、FreeBSDソースツリーのコンポーネント（またはすべて）を構築するための多数のターゲットをサポートしています。
make(1)変数の設定を含む詳細については、build(7)、config(8)、[FreeBSDハンドブックのユーザーランドの構築](https://docs.freebsd.org/en/books/handbook/cutting-edge/#makeworld)、および[カーネルに関するハンドブック](https://docs.freebsd.org/en/books/handbook/kernelconfig/)をご覧ください。

FreeBSDがサポートしているCPUアーキテクチャとプラットフォームに関する情報については、[FreeBSD Webサイトのプラットフォームページ](https://www.freebsd.org/platforms/)をご覧ください。

公式のFreeBSDブータブルイメージについては、[リリースページ](https://download.freebsd.org/ftp/releases/ISO-IMAGES/)をご覧ください。

ソースロードマップ:
---------------
| ディレクトリ | 説明 |
| --------- | ----------- |
| bin | システム/ユーザーコマンド。 |
| cddl | Common Development and Distribution License (CDDL) 下の様々なコマンドとライブラリ。 |
| contrib | サードパーティによって寄贈されたパッケージ。 |
| crypto | 暗号化関連（[crypto/README](crypto/README)を参照）。 |
| etc | /etc 用のテンプレートファイル。 |
| gnu | GNU General Public License (GPL) または Lesser General Public License (LGPL) 下のコマンドとライブラリ。詳細については [gnu/COPYING](gnu/COPYING) および [gnu/COPYING.LIB](gnu/COPYING.LIB) をご覧ください。 |
| include | システムインクルードファイル。 |
| kerberos5 | Kerberos5 (Heimdal) パッケージ。 |
| lib | システムライブラリ。 |
| libexec | システムデーモン。 |
| release | リリース構築用 Makefile と関連ツール。 |
| rescue | 静的リンクされた /rescue ユーティリティのビルドシステム。 |
| sbin | システムコマンド。 |
| secure | 暗号ライブラリとコマンド。 |
| share | 共有リソース。 |
| stand | ブートローダーのソース。 |
| sys | カーネルソース（[sys/README.md](sys/README.md)を参照）。 |
| targets | 実験的な `DIRDEPS_BUILD` のサポート。 |
| tests | Kyua で実行可能なリグレッションテスト。詳細については [tests/README](tests/README) をご覧ください。 |
| tools | リグレッションテストやその他のタスクのためのユーティリティ。 |
| usr.bin | ユーザーコマンド。 |
| usr.sbin | システム管理コマンド。 |

FreeBSDプロジェクトの開発ブランチの1つ以上とソースツリーを同期する方法に関する情報については、[FreeBSDハンドブック](https://docs.freebsd.org/en/books/handbook/cutting-edge/#current-stable)をご覧ください。
