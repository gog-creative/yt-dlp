<!-- MANPAGE: BEGIN EXCLUDED SECTION -->
<div align="center">

[![YT-DLP](https://raw.githubusercontent.com/yt-dlp/yt-dlp/master/.github/banner.svg)](#readme)

[![Release version](https://img.shields.io/github/v/release/yt-dlp/yt-dlp?color=brightgreen&label=Download&style=for-the-badge)](#installation "インストール")
[![PyPI](https://img.shields.io/badge/-PyPI-blue.svg?logo=pypi&labelColor=555555&style=for-the-badge)](https://pypi.org/project/yt-dlp "PyPI")
[![Donate](https://img.shields.io/badge/_-Donate-red.svg?logo=githubsponsors&labelColor=555555&style=for-the-badge)](Collaborators.md#collaborators "寄付")
[![Discord](https://img.shields.io/discord/807245652072857610?color=blue&labelColor=555555&label=&logo=discord&style=for-the-badge)](https://discord.gg/H5MNcFW63r "Discord")
[![Supported Sites](https://img.shields.io/badge/-Supported_Sites-brightgreen.svg?style=for-the-badge)](supportedsites.md "対応サイト")
[![License: Unlicense](https://img.shields.io/badge/-Unlicense-blue.svg?style=for-the-badge)](LICENSE "ライセンス")
[![CI Status](https://img.shields.io/github/actions/workflow/status/yt-dlp/yt-dlp/core.yml?branch=master&label=Tests&style=for-the-badge)](https://github.com/yt-dlp/yt-dlp/actions "CIステータス")
[![Commits](https://img.shields.io/github/commit-activity/m/yt-dlp/yt-dlp?label=commits&style=for-the-badge)](https://github.com/yt-dlp/yt-dlp/commits "コミット履歴")
[![Last Commit](https://img.shields.io/github/last-commit/yt-dlp/yt-dlp/master?label=&style=for-the-badge&display_timestamp=committer)](https://github.com/yt-dlp/yt-dlp/pulse/monthly "最終アクティビティ")

</div>
<!-- MANPAGE: END EXCLUDED SECTION -->

yt-dlpは、[数千のサイト](supportedsites.md)に対応した、多機能なコマンドラインの音声/動画ダウンローダーです。このプロジェクトは[youtube-dl](https://github.com/ytdl-org/youtube-dl)のフォークであり、現在は活動を停止している[youtube-dlc](https://github.com/blackjack4494/yt-dlc)をベースにしています。

<!-- MANPAGE: MOVE "USAGE AND OPTIONS" SECTION HERE -->

<!-- MANPAGE: BEGIN EXCLUDED SECTION -->
* [インストール](#installation)
    * [詳細な手順](https://github.com/yt-dlp/yt-dlp/wiki/Installation)
    * [リリースファイル](#release-files)
    * [アップデート](#update)
    * [依存関係](#dependencies)
    * [コンパイル](#compile)
* [使い方とオプション](#usage-and-options)
    * [一般オプション](#general-options)
    * [ネットワークオプション](#network-options)
    * [地域制限](#geo-restriction)
    * [動画の選択](#video-selection)
    * [ダウンロードオプション](#download-options)
    * [ファイルシステムオプション](#filesystem-options)
    * [サムネイルオプション](#thumbnail-options)
    * [インターネットショートカットオプション](#internet-shortcut-options)
    * [詳細表示とシミュレーションオプション](#verbosity-and-simulation-options)
    * [回避策](#workarounds)
    * [動画フォーマットオプション](#video-format-options)
    * [字幕オプション](#subtitle-options)
    * [認証オプション](#authentication-options)
    * [ポストプロセッシングオプション](#post-processing-options)
    * [SponsorBlockオプション](#sponsorblock-options)
    * [エクストラクタオプション](#extractor-options)
    * [プリセットエイリアス](#preset-aliases)
* [設定](#configuration)
    * [設定ファイルのエンコーディング](#configuration-file-encoding)
    * [netrcによる認証](#authentication-with-netrc)
    * [環境変数に関する注意](#notes-about-environment-variables)
* [出力テンプレート](#output-template)
    * [出力テンプレートの例](#output-template-examples)
* [フォーマットの選択](#format-selection)
    * [フォーマットのフィルタリング](#filtering-formats)
    * [フォーマットのソート](#sorting-formats)
    * [フォーマット選択の例](#format-selection-examples)
* [メタデータの変更](#modifying-metadata)
    * [メタデータ変更の例](#modifying-metadata-examples)
* [エクストラクタ引数](#extractor-arguments)
* [プラグイン](#plugins)
    * [プラグインのインストール](#installing-plugins)
    * [プラグインの開発](#developing-plugins)
* [YT-DLPの埋め込み](#embedding-yt-dlp)
    * [埋め込みの例](#embedding-examples)
* [YOUTUBE-DLからの変更点](#changes-from-youtube-dl)
    * [新機能](#new-features)
    * [デフォルトの挙動の違い](#differences-in-default-behavior)
    * [非推奨のオプション](#deprecated-options)
* [貢献する](CONTRIBUTING.md#contributing-to-yt-dlp)
    * [Issueを立てる](CONTRIBUTING.md#opening-an-issue)
    * [開発者向けの手順](CONTRIBUTING.md#developer-instructions)
* [WIKI](https://github.com/yt-dlp/yt-dlp/wiki)
    * [FAQ](https://github.com/yt-dlp/yt-dlp/wiki/FAQ)
<!-- MANPAGE: END EXCLUDED SECTION -->


# インストール

<!-- MANPAGE: BEGIN EXCLUDED SECTION -->
[![Windows](https://img.shields.io/badge/-Windows_x64-blue.svg?style=for-the-badge&logo=windows)](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp.exe)
[![Unix](https://img.shields.io/badge/-Linux/BSD-red.svg?style=for-the-badge&logo=linux)](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp)
[![MacOS](https://img.shields.io/badge/-MacOS-lightblue.svg?style=for-the-badge&logo=apple)](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_macos)
[![PyPI](https://img.shields.io/badge/-PyPI-blue.svg?logo=pypi&labelColor=555555&style=for-the-badge)](https://pypi.org/project/yt-dlp)
[![Source Tarball](https://img.shields.io/badge/-Source_tar-green.svg?style=for-the-badge)](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp.tar.gz)
[![Other variants](https://img.shields.io/badge/-Other-grey.svg?style=for-the-badge)](#release-files)
[![All versions](https://img.shields.io/badge/-All_Versions-lightgrey.svg?style=for-the-badge)](https://github.com/yt-dlp/yt-dlp/releases)
<!-- MANPAGE: END EXCLUDED SECTION -->

yt-dlpは[バイナリ](#release-files)や[pip](https://pypi.org/project/yt-dlp)、またはサードパーティのパッケージマネージャを使ってインストールできます。詳細な手順については[Wiki](https://github.com/yt-dlp/yt-dlp/wiki/Installation)を参照してください。


<!-- MANPAGE: BEGIN EXCLUDED SECTION -->
## リリースファイル

#### 推奨

ファイル|説明
:---|:---
[yt-dlp](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp)|プラットフォーム非依存の[zipimport](https://docs.python.org/3/library/zipimport.html)バイナリ。Pythonが必要（**Linux/BSD**に推奨）
[yt-dlp.exe](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp.exe)|Windows (Win8+) 向けのスタンドアロンx64バイナリ（**Windows**に推奨）
[yt-dlp_macos](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_macos)|Universal MacOS (10.15+) 向けのスタンドアロン実行ファイル（**MacOS**に推奨）

#### 代替

ファイル|説明
:---|:---
[yt-dlp_linux](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_linux)|Linux (glibc 2.17+) 向けのスタンドアロンx86_64バイナリ
[yt-dlp_linux.zip](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_linux.zip)|パッケージ化されていないLinux (glibc 2.17+) x86_64実行ファイル（自動更新なし）
[yt-dlp_linux_aarch64](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_linux_aarch64)|Linux (glibc 2.17+) 向けのスタンドアロンaarch64バイナリ
[yt-dlp_linux_aarch64.zip](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_linux_aarch64.zip)|パッケージ化されていないLinux (glibc 2.17+) aarch64実行ファイル（自動更新なし）
[yt-dlp_linux_armv7l.zip](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_linux_armv7l.zip)|パッケージ化されていないLinux (glibc 2.31+) armv7l実行ファイル（自動更新なし）
[yt-dlp_musllinux](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_musllinux)|Linux (musl 1.2+) 向けのスタンドアロンx86_64バイナリ
[yt-dlp_musllinux.zip](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_musllinux.zip)|パッケージ化されていないLinux (musl 1.2+) x86_64実行ファイル（自動更新なし）
[yt-dlp_musllinux_aarch64](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_musllinux_aarch64)|Linux (musl 1.2+) 向けのスタンドアロンaarch64バイナリ
[yt-dlp_musllinux_aarch64.zip](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_musllinux_aarch64.zip)|パッケージ化されていないLinux (musl 1.2+) aarch64実行ファイル（自動更新なし）
[yt-dlp_x86.exe](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_x86.exe)|Windows (Win8+) 向けのスタンドアロンx86 (32-bit) バイナリ
[yt-dlp_win_x86.zip](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_win_x86.zip)|パッケージ化されていないWindows (Win8+) x86 (32-bit) 実行ファイル（自動更新なし）
[yt-dlp_arm64.exe](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_arm64.exe)|Windows (Win10+) 向けのスタンドアロンARM64バイナリ
[yt-dlp_win_arm64.zip](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_win_arm64.zip)|パッケージ化されていないWindows (Win10+) ARM64実行ファイル（自動更新なし）
[yt-dlp_win.zip](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_win.zip)|パッケージ化されていないWindows (Win8+) x64実行ファイル（自動更新なし）
[yt-dlp_macos.zip](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_macos.zip)|パッケージ化されていないMacOS (10.15+) 実行ファイル（自動更新なし）

#### その他

ファイル|説明
:---|:---
[yt-dlp.tar.gz](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp.tar.gz)|ソースコードのtarball
[SHA2-512SUMS](https://github.com/yt-dlp/yt-dlp/releases/latest/download/SHA2-512SUMS)|GNUスタイルのSHA512サム
[SHA2-512SUMS.sig](https://github.com/yt-dlp/yt-dlp/releases/latest/download/SHA2-512SUMS.sig)|SHA512サム用のGPG署名ファイル
[SHA2-256SUMS](https://github.com/yt-dlp/yt-dlp/releases/latest/download/SHA2-256SUMS)|GNUスタイルのSHA256サム
[SHA2-256SUMS.sig](https://github.com/yt-dlp/yt-dlp/releases/latest/download/SHA2-256SUMS.sig)|SHA256サム用のGPG署名ファイル

GPG署名の検証に使用できる公開鍵は[こちら](https://github.com/yt-dlp/yt-dlp/blob/master/public.key)で入手できます。
使用例：
```
curl -L https://github.com/yt-dlp/yt-dlp/raw/master/public.key | gpg --import
gpg --verify SHA2-256SUMS.sig SHA2-256SUMS
gpg --verify SHA2-512SUMS.sig SHA2-512SUMS
```

#### ライセンス

yt-dlpは[Unlicense](LICENSE)でライセンスされていますが、多くのリリースファイルには異なるライセンスを持つ他のプロジェクトのコードが含まれています。

特に、PyInstallerでバンドルされた実行ファイルにはGPLv3+ライセンスのコードが含まれており、そのため結合された成果物は[GPLv3+](https://www.gnu.org/licenses/gpl-3.0.html)でライセンスされます。

詳細は[THIRD_PARTY_LICENSES.txt](THIRD_PARTY_LICENSES.txt)を参照してください。

zipimportバイナリ (`yt-dlp`)、ソースtarball (`yt-dlp.tar.gz`)、PyPIのソースディストリビューションおよびホイールには、[Unlicense](LICENSE)でライセンスされたコードのみが含まれています。

<!-- MANPAGE: END EXCLUDED SECTION -->

**注**: manページ、シェル補完（オートコンプリート）ファイルなどは、[ソースtarball](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp.tar.gz)内にあります。


## アップデート
[リリースバイナリ](#release-files)を使用している場合は、`yt-dlp -U` でアップデートできます。

[pipでインストールした場合](https://github.com/yt-dlp/yt-dlp/wiki/Installation#with-pip)は、プログラムのインストールに使用したのと同じコマンドを再実行してください。

他のサードパーティのパッケージマネージャについては、[Wiki](https://github.com/yt-dlp/yt-dlp/wiki/Installation#third-party-package-managers)を参照するか、それぞれのドキュメントを参照してください。

<a id="update-channels"></a>

現在、バイナリには`stable`、`nightly`、`master`の3つのリリースチャンネルがあります。

* `stable`はデフォルトのチャンネルで、その変更点の多くは`nightly`および`master`チャンネルのユーザーによってテストされています。
* `nightly`チャンネルは、毎日午前0時（UTC）頃にビルドがスケジュールされており、プロジェクトの新しいパッチや変更のスナップショットを提供します。これはyt-dlpの**一般ユーザーに推奨されるチャンネル**です。`nightly`リリースは[yt-dlp/yt-dlp-nightly-builds](https://github.com/yt-dlp/yt-dlp-nightly-builds/releases)から、または`yt-dlp` PyPIパッケージの開発リリースとして入手できます（pipの`--pre`フラグでインストール可能）。
* `master`チャンネルは、masterブランチへの各プッシュ後にビルドされるリリースを特徴とし、最新の修正や追加が含まれますが、リグレッションが発生しやすい可能性もあります。これらは[yt-dlp/yt-dlp-master-builds](https://github.com/yt-dlp/yt-dlp-master-builds/releases)から入手できます。

`--update`/`-U`を使用する場合、リリースバイナリは現在のチャンネルにのみアップデートします。
`--update-to CHANNEL`を使用すると、新しいバージョンが利用可能な場合に別のチャンネルに切り替えることができます。`--update-to [CHANNEL@]TAG`は、特定のチャンネルの特定のタグにアップグレードまたはダウングレードするためにも使用できます。

また、`--update-to <repository>`（`<owner>/<repository>`）を使用して、全く異なるリポジトリのチャンネルにアップデートすることもできます。ただし、アップデート先のリポジトリには注意してください。異なるリポジトリからのバイナリに対する検証は行われません。

使用例：

* `yt-dlp --update-to master` `master`チャンネルに切り替え、その最新リリースにアップデートします。
* `yt-dlp --update-to stable@2023.07.06` `stable`チャンネルのタグ`2023.07.06`にアップグレード/ダウングレードします。
* `yt-dlp --update-to 2023.10.07` 現在のチャンネルにタグ`2023.10.07`が存在する場合、それにアップグレード/ダウングレードします。
* `yt-dlp --update-to example/yt-dlp@2023.09.24` `example/yt-dlp`リポジトリのタグ`2023.09.24`のリリースにアップグレード/ダウングレードします。

**重要**: `stable`リリースで問題が発生したユーザーは、バグレポートを提出する前に`nightly`リリースをインストールまたはアップデートしてください。
```
# stableの実行ファイル/バイナリからnightlyにアップデートする場合：
yt-dlp --update-to nightly

# pipでnightlyをインストールする場合：
python3 -m pip install -U --pre "yt-dlp[default]"
```

90日以上古いyt-dlpバージョンを実行すると、最新バージョンへのアップデートを促す警告メッセージが表示されます。
この警告を抑制するには、コマンドまたは設定ファイルに`--no-update`を追加します。

## 依存関係
Pythonバージョン3.9以上（CPython）および3.11以上（PyPy）がサポートされています。他のバージョンや実装は正しく動作しない可能性があります。

<!-- Python 3.5+ uses VC++14 and it is already embedded in the binary created
<!x-- https://www.microsoft.com/en-us/download/details.aspx?id=26999 --x>
On Windows, [Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://download.microsoft.com/download/1/6/5/165255E7-1014-4D0A-B094-B6A430A6BFFC/vcredist_x86.exe) is also necessary to run yt-dlp. You probably already have this, but if the executable throws an error due to missing `MSVCR100.dll` you need to install it manually.
-->

他のすべての依存関係はオプションですが、`ffmpeg`と`ffprobe`は強く推奨されます。

### 強く推奨

* [**ffmpeg** と **ffprobe**](https://www.ffmpeg.org) - [動画と音声ファイルを別々にマージする](#format-selection)ため、また様々な[ポストプロセッシング](#post-processing-options)タスクに必要です。ライセンスは[ビルドによります](https://www.ffmpeg.org/legal.html)。

    ffmpegには、yt-dlpと併用すると様々な問題を引き起こすバグがあります。ffmpegは非常に重要な依存関係であるため、これらの問題のいくつかにパッチを当てた[カスタムビルド](https://github.com/yt-dlp/FFmpeg-Builds#ffmpeg-static-auto-builds)を[yt-dlp/FFmpeg-Builds](https://github.com/yt-dlp/FFmpeg-Builds)で提供しています。これらのビルドで解決される具体的な問題については、[readme](https://github.com/yt-dlp/FFmpeg-Builds#patches-applied)を参照してください。

    **重要**: 必要なのはffmpegの*バイナリ*であり、[同名のPythonパッケージ](https://pypi.org/project/ffmpeg)では**ありません**。

### ネットワーク
* [**certifi**](https://github.com/certifi/python-certifi)\* - Mozillaのルート証明書バンドルを提供します。[MPLv2](https://github.com/certifi/python-certifi/blob/master/LICENSE)ライセンスです。
* [**brotli**](https://github.com/google/brotli)\* または [**brotlicffi**](https://github.com/python-hyper/brotlicffi) - [Brotli](https://en.wikipedia.org/wiki/Brotli)コンテンツエンコーディングをサポートします。両方ともMITライセンスです <sup>(https://github.com/google/brotli/blob/master/LICENSE)(https://github.com/python-hyper/brotlicffi/blob/master/LICENSE) </sup>
* [**websockets**](https://github.com/aaugustin/websockets)\* - websocket経由でのダウンロード用。[BSD-3-Clause](https://github.com/aaugustin/websockets/blob/main/LICENSE)ライセンスです。
* [**requests**](https://github.com/psf/requests)\* - HTTPライブラリ。HTTPSプロキシと持続的接続をサポートします。[Apache-2.0](https://github.com/psf/requests/blob/main/LICENSE)ライセンスです。

#### 偽装

以下は、ブラウザリクエストを偽装するためのサポートを提供します。これはTLSフィンガープリンティングを使用する一部のサイトで必要になる場合があります。

* [**curl_cffi**](https://github.com/lexiforest/curl_cffi) (推奨) - [curl-impersonate](https://github.com/lexiforest/curl-impersonate)のPythonバインディング。Chrome、Edge、Safariの偽装ターゲットを提供します。[MIT](https://github.com/lexiforest/curl_cffi/blob/main/LICENSE)ライセンスです。
  * `curl-cffi`グループでインストールできます。例：`pip install "yt-dlp[default,curl-cffi]"`
  * 現在、`yt-dlp`（Unix zipimportバイナリ）、`yt-dlp_x86`（Windows 32-bit）、`yt-dlp_musllinux_aarch64`を*除く*ほとんどのビルドに含まれています。


### メタデータ

* [**mutagen**](https://github.com/quodlibet/mutagen)\* - 特定のフォーマットで`--embed-thumbnail`を使用するために必要です。[GPLv2+](https://github.com/quodlibet/mutagen/blob/master/COPYING)ライセンスです。
* [**AtomicParsley**](https://github.com/wez/atomicparsley) - `mutagen`/`ffmpeg`が使用できない場合に`mp4`/`m4a`ファイルで`--embed-thumbnail`を使用するために必要です。[GPLv2+](https://github.com/wez/atomicparsley/blob/master/COPYING)ライセンスです。
* [**xattr**](https://github.com/xattr/xattr)、[**pyxattr**](https://github.com/iustin/pyxattr)、または[**setfattr**](http://savannah.nongnu.org/projects/attr) - **Mac**および**BSD**でxattrメタデータ（`--xattrs`）を書き込むために必要です。それぞれ[MIT](https://github.com/xattr/xattr/blob/master/LICENSE.txt)、[LGPL2.1](https://github.com/iustin/pyxattr/blob/master/COPYING)、[GPLv2+](http://git.savannah.nongnu.org/cgit/attr.git/tree/doc/COPYING)ライセンスです。

### その他

* [**pycryptodomex**](https://github.com/Legrandin/pycryptodome)\* - AES-128 HLSストリームやその他の様々なデータの復号化に必要です。[BSD-2-Clause](https://github.com/Legrandin/pycryptodome/blob/master/LICENSE.rst)ライセンスです。
* [**phantomjs**](https://github.com/ariya/phantomjs) - JavaScriptを実行する必要があるエクストラクタで使用されます。[BSD-3-Clause](https://github.com/ariya/phantomjs/blob/master/LICENSE.BSD)ライセンスです。
* [**secretstorage**](https://github.com/mitya57/secretstorage)\* - **Linux**で**Chromium**ベースのブラウザのクッキーを復号化する際に**Gnome**キーリングにアクセスするために`--cookies-from-browser`で使用されます。[BSD-3-Clause](https://github.com/mitya57/secretstorage/blob/master/LICENSE)ライセンスです。
* `--downloader`で使用したい任意の外部ダウンローダー

### 非推奨

* [**avconv** と **avprobe**](https://www.libav.org) - 現在は**非推奨**のffmpegの代替。ライセンスは[ビルドによります](https://libav.org/legal)。
* [**sponskrub**](https://github.com/faissaloo/SponSkrub) - 現在は**非推奨**の[sponskrubオプション](#sponskrub-options)を使用するために必要。[GPLv3+](https://github.com/faissaloo/SponSkrub/blob/master/LICENCE.md)ライセンスです。
* [**rtmpdump**](http://rtmpdump.mplayerhq.hu) - `rtmp`ストリームのダウンロード用。代わりに`--downloader ffmpeg`でffmpegを使用できます。[GPLv2+](http://rtmpdump.mplayerhq.hu)ライセンスです。
* [**mplayer**](http://mplayerhq.hu/design7/info.html) または [**mpv**](https://mpv.io) - `rstp`/`mms`ストリームのダウンロード用。代わりに`--downloader ffmpeg`でffmpegを使用できます。[GPLv2+](https://github.com/mpv-player/mpv/blob/master/Copyright)ライセンスです。

依存関係を使用または再配布するには、それぞれのライセンス条項に同意する必要があります。

スタンドアロンのリリースバイナリは、Pythonインタープリタと **\*** が付いたパッケージを含んでビルドされています。

試行しているタスクに必要な依存関係がない場合、yt-dlpは警告を表示します。現在利用可能なすべての依存関係は、`--verbose`出力の冒頭で確認できます。


## コンパイル

### スタンドアロンPyInstallerビルド
スタンドアロンの実行ファイルをビルドするには、Pythonと`pyinstaller`（および必要に応じてyt-dlpの[オプションの依存関係](#dependencies)）が必要です。実行ファイルは、使用されるPythonと同じCPUアーキテクチャ用にビルドされます。

以下のコマンドを実行できます：

```
python3 devscripts/install_deps.py --include pyinstaller
python3 devscripts/make_lazy_extractors.py
python3 -m bundle.pyinstaller
```

システムによっては、`python3`の代わりに`py`または`python`を使用する必要がある場合があります。

`python -m bundle.pyinstaller`は、`--onefile/-F`や`--onedir/-D`など、`pyinstaller`に渡すことができる任意の引数を受け付けます。これについては[こちら](https://pyinstaller.org/en/stable/usage.html#what-to-generate)で詳しく説明されています。

**注**: Pyinstallerバージョン4.4未満は、仮想環境を使用しない限り、WindowsストアからインストールされたPythonを[サポートしていません](https://github.com/pyinstaller/pyinstaller#requirements-and-tested-platforms)。

**重要**: `python -m bundle.pyinstaller`の代わりに`pyinstaller`を直接実行することは、公式にはサポートされて**いません**。これは正しく動作しない可能性があります。

### プラットフォーム非依存バイナリ (UNIX)
ビルドツールとして`python` (3.9+)、`zip`、`make` (GNU)、`pandoc`\*、`pytest`\*が必要です。

これらをインストールした後、単に`make`を実行してください。

また、`make yt-dlp`を実行して、追加ファイルを更新せずにバイナリのみをコンパイルすることもできます。（この場合、**\*** が付いたビルドツールは不要です）

### 関連スクリプト

* **`devscripts/install_deps.py`** - yt-dlpの依存関係をインストールします。
* **`devscripts/update-version.py`** - 現在の日付に基づいてバージョン番号を更新します。
* **`devscripts/set-variant.py`** - 実行ファイルのビルドバリアントを設定します。
* **`devscripts/make_changelog.py`** - 短いコミットメッセージを使用してマークダウンの変更履歴を作成し、`CONTRIBUTORS`ファイルを更新します。
* **`devscripts/make_lazy_extractors.py`** - 遅延エクストラクタを作成します。バイナリ（どのバリアントでも）をビルドする前にこれを実行すると、起動パフォーマンスが向上します。環境変数`YTDLP_NO_LAZY_EXTRACTORS`に空でない値を設定すると、遅延エクストラクタの読み込みを強制的に無効にします。

注：詳細は`--help`を参照してください。

### プロジェクトのフォーク
GitHubでプロジェクトをフォークした場合、フォークしたリポジトリの[ビルドワークフロー](.github/workflows/build.yml)を実行して、選択したバージョンをアーティファクトとして自動的にビルドできます。あるいは、[リリースワークフロー](.github/workflows/release.yml)を実行するか、[ナイトリーワークフロー](.github/workflows/release-nightly.yml)を有効にして、完全な（プレ）リリースを作成することもできます。

# 使い方とオプション

<!-- MANPAGE: BEGIN EXCLUDED SECTION -->
    yt-dlp [OPTIONS] [--] URL [URL...]

ヒント: `CTRL`+`F` (または `Command`+`F`) を使ってキーワードで検索できます。
<!-- MANPAGE: END EXCLUDED SECTION -->

<!-- Auto generated -->
## 一般オプション:
    -h, --help                      このヘルプテキストを表示して終了します。
    --version                       プログラムのバージョンを表示して終了します。
    -U, --update                    このプログラムを最新バージョンにアップデートします。
    --no-update                     アップデートをチェックしません (デフォルト)。
    --update-to [CHANNEL]@[TAG]     特定のバージョンにアップグレード/ダウングレードします。
                                    CHANNELはリポジトリでもかまいません。CHANNEL
                                    とTAGは省略した場合、それぞれ "stable" と "latest"
                                    がデフォルトになります。詳細は「アップデート」を参照してください。
                                    サポートされているチャンネル: stable, nightly, master
    -i, --ignore-errors             ダウンロードとポストプロセッシングのエラーを無視します。
                                    ポストプロセッシングが失敗しても、ダウンロードは成功したとみなされます。
    --no-abort-on-error             ダウンロードエラーが発生しても次の動画に進みます。
                                    例えば、プレイリスト内の利用不可能な動画をスキップします (デフォルト)。
    --abort-on-error                エラーが発生した場合、それ以降の動画のダウンロードを中止します
                                    (エイリアス: --no-ignore-errors)。
    --dump-user-agent               現在のユーザーエージェントを表示して終了します。
    --list-extractors               サポートされているすべてのエクストラクタを一覧表示して終了します。
    --extractor-descriptions        サポートされているすべてのエクストラクタの説明を出力して終了します。
    --use-extractors NAMES          使用するエクストラクタ名をカンマで区切って指定します。
                                    正規表現、"all"、"default"、"end"（URLマッチングの最後）も使用できます。
                                    例: --ies "holodex.*,end,youtube"。名前の前に "-" を付けると
                                    それを除外します。例: --ies default,-generic。エクストラクタ名の一覧は
                                    --list-extractors を使用してください (エイリアス: --ies)。
    --default-search PREFIX         修飾されていないURLにこのプレフィックスを使用します。例:
                                    "gvsearch2:python" は、検索語 "python" でGoogleビデオから2つの動画を
                                    ダウンロードします。"auto" を使用するとyt-dlpが推測します
                                    ("auto_warning" は推測時に警告を出します)。"error" はエラーを
                                    スローするだけです。デフォルト値 "fixup_error" は壊れたURLを修正しますが、
                                    修正できない場合は検索せずにエラーを出します。
    --ignore-config                 --config-locations で指定されたもの以外の設定ファイルを読み込みません。
                                    後方互換性のため、このオプションがシステム設定ファイル内で
                                    見つかった場合、ユーザー設定は読み込まれません (エイリアス: --no-config)。
    --no-config-locations           カスタム設定ファイルを一切読み込みません (デフォルト)。設定ファイル内で
                                    指定された場合、現在のファイルで定義された以前の --config-locations
                                    をすべて無視します。
    --config-locations PATH         メイン設定ファイルの場所。設定ファイルへのパスまたは
                                    それを含むディレクトリ ("-" は標準入力)。複数回使用でき、
                                    他の設定ファイル内でも使用できます。
    --plugin-dirs PATH              プラグインを検索する追加のディレクトリへのパス。このオプションは
                                    複数回使用して複数のディレクトリを追加できます。"default" を使用すると
                                    デフォルトのプラグインディレクトリを検索します (デフォルト)。
    --no-plugin-dirs                検索するプラグインディレクトリをクリアします。
                                    デフォルトや以前の --plugin-dirs で提供されたものも含まれます。
    --flat-playlist                 プレイリストのURL結果のエントリを抽出しません。一部のエントリの
                                    メタデータが欠落し、ダウンロードがバイパスされる可能性があります。
    --no-flat-playlist              プレイリストの動画を完全に抽出します (デフォルト)。
    --live-from-start               ライブストリームを最初からダウンロードします。
                                    現在実験的で、YouTubeとTwitchでのみサポートされています。
    --no-live-from-start            ライブストリームを現在の時間からダウンロードします (デフォルト)。
    --wait-for-video MIN[-MAX]      スケジュールされたストリームが利用可能になるまで待ちます。
                                    再試行の間に待つ最小秒数（または範囲）を渡します。
    --no-wait-for-video             スケジュールされたストリームを待ちません (デフォルト)。
    --mark-watched                  動画を視聴済みとしてマークします (--simulate でも有効)。
    --no-mark-watched               動画を視聴済みとしてマークしません (デフォルト)。
    --color [STREAM:]POLICY         出力にカラーコードを出すかどうか。オプションでSTREAM（stdoutまたは
                                    stderr）をプレフィックスとして設定を適用できます。
                                    "always"、"auto" (デフォルト)、"never"、または "no_color"
                                    （非カラーターミナルシーケンスを使用）のいずれかを指定できます。
                                    "auto-tty" または "no_color-tty" を使用すると、ターミナルの
                                    サポートのみに基づいて決定します。複数回使用できます。
    --compat-options OPTS           youtube-dlやyoutube-dlcの設定との互換性を保つのに役立つ
                                    オプション。yt-dlpで行われた変更の一部を元に戻します。
                                    詳細は「デフォルトの挙動の違い」を参照してください。
    --alias ALIASES OPTIONS         オプション文字列のエイリアスを作成します。エイリアスがダッシュ "-"
                                    で始まらない限り、"--" がプレフィックスされます。引数はPythonの
                                    文字列書式設定ミニ言語に従って解析されます。例: --alias
                                    get-audio,-X "-S aext:{0},abr -x --audio-format {0}" は、
                                    引数（ARG0）を取り、"-S aext:ARG0,abr -x --audio-format ARG0" に
                                    展開されるオプション "--get-audio" と "-X" を作成します。
                                    定義されたすべてのエイリアスは --help 出力に一覧表示されます。
                                    エイリアスオプションは他のエイリアスをトリガーする可能性があるため、
                                    再帰的なオプションを定義しないように注意してください。安全策として、
                                    各エイリアスは最大100回までトリガーされます。このオプションは
                                    複数回使用できます。
    -t, --preset-alias PRESET       定義済みのオプションセットを適用します。例: --preset-alias mp3。
                                    利用可能なプリセット: mp3, aac, mp4, mkv, sleep。
                                    詳細は最後の「プリセットエイリアス」セクションを参照してください。
                                    このオプションは複数回使用できます。

## ネットワークオプション:
    --proxy URL                     指定されたHTTP/HTTPS/SOCKSプロキシを使用します。SOCKSプロキシを
                                    有効にするには、適切なスキームを指定します。例:
                                    socks5://user:pass@127.0.0.1:1080/。
                                    直接接続するには、空の文字列 (--proxy "") を渡します。
    --socket-timeout SECONDS        タイムアウトするまでの待機時間（秒）。
    --source-address IP             バインドするクライアント側のIPアドレス。
    --impersonate CLIENT[:OS]       リクエストを偽装するクライアント。例: chrome, chrome-110,
                                    chrome:windows-10。--impersonate="" を渡すと任意のクライアントを
                                    偽装します。すべてのリクエストで偽装を強制すると、ダウンロード速度と
                                    安定性に悪影響を与える可能性があることに注意してください。
    --list-impersonate-targets      偽装可能なクライアントを一覧表示します。
    -4, --force-ipv4                すべての接続をIPv4経由で行います。
    -6, --force-ipv6                すべての接続をIPv6経由で行います。
    --enable-file-urls              file:// URLを有効にします。セキュリティ上の理由から
                                    デフォルトでは無効になっています。

## 地域制限:
    --geo-verification-proxy URL    一部の地域制限サイトでIPアドレスを検証するためにこのプロキシを使用します。
                                    実際のダウンロードには --proxy で指定されたデフォルトのプロキシ
                                    （オプションがない場合はなし）が使用されます。
    --xff VALUE                     地理的制限を回避するためにX-Forwarded-For HTTPヘッダーを
                                    どのように偽装するか。"default"（有用とわかっている場合のみ）、
                                    "never"、CIDR表記のIPブロック、または2文字のISO 3166-2
                                    国コードのいずれかを指定します。

## 動画の選択:
    -I, --playlist-items ITEM_SPEC  ダウンロードするアイテムのplaylist_indexをカンマで区切って指定します。
                                    "[START]:[STOP][:STEP]" を使用して範囲を指定できます。
                                    後方互換性のために START-STOP もサポートされています。
                                    負のインデックスを使用して右から数え、負のSTEPを使用して逆順に
                                    ダウンロードします。例: サイズ15のプレイリストで "-I 1:3,7,-5::2"
                                    を使用すると、インデックス1,2,3,7,11,13,15のアイテムが
                                    ダウンロードされます。
    --min-filesize SIZE             ファイルサイズがSIZEより小さい場合、ダウンロードを中止します。
                                    例: 50k または 44.6M
    --max-filesize SIZE             ファイルサイズがSIZEより大きい場合、ダウンロードを中止します。
                                    例: 50k または 44.6M
    --date DATE                     この日にアップロードされた動画のみをダウンロードします。
                                    日付は "YYYYMMDD" または [now|today|yesterday][-N[day|week|month|year]]
                                    の形式です。例: "--date today-2weeks" は2週間前の同じ日に
                                    アップロードされた動画のみをダウンロードします。
    --datebefore DATE               この日以前にアップロードされた動画のみをダウンロードします。
                                    受け入れられる日付形式は --date と同じです。
    --dateafter DATE                この日以降にアップロードされた動画のみをダウンロードします。
                                    受け入れられる日付形式は --date と同じです。
    --match-filters FILTER          汎用動画フィルター。「出力テンプレート」のフィールドを、
                                    「フォーマットのフィルタリング」で定義された演算子を使用して
                                    数値または文字列と比較できます。フィールドが存在するかどうかを
                                    確認するためにフィールドを指定するだけでもよく、"!field" で
                                    フィールドが存在しないことを確認し、"&" で複数の条件を確認できます。
                                    "&" や引用符をエスケープする必要がある場合は "\" を使用します。
                                    複数回使用した場合、いずれかの条件が満たされればフィルターは
                                    マッチします。例: --match-filters !is_live
                                    --match-filters "like_count>?100 & description~='(?i)\bcats \& dogs\b'" は、
                                    ライブではない動画、または「いいね」数が100より多い（または
                                    「いいね」フィールドが利用できない）かつ、説明に "cats & dogs"
                                    （大文字小文字を区別しない）というフレーズが含まれる動画に
                                    マッチします。"--match-filters -" を使用すると、各動画を
                                    ダウンロードするかどうかを対話形式で尋ねます。
    --no-match-filters              --match-filters を使用しません (デフォルト)。
    --break-match-filters FILTER    "--match-filters" と同じですが、動画が拒否されたときに
                                    ダウンロードプロセスを停止します。
    --no-break-match-filters        --break-match-filters を使用しません (デフォルト)。
    --no-playlist                   URLが動画とプレイリストの両方を参照している場合、動画のみを
                                    ダウンロードします。
    --yes-playlist                  URLが動画とプレイリストの両方を参照している場合、プレイリストを
                                    ダウンロードします。
    --age-limit YEARS               指定された年齢に適した動画のみをダウンロードします。
    --download-archive FILE         アーカイブファイルに記載されていない動画のみをダウンロードします。
                                    ダウンロードされたすべての動画のIDをそのファイルに記録します。
    --no-download-archive           アーカイブファイルを使用しません (デフォルト)。
    --max-downloads NUMBER          NUMBER個のファイルをダウンロードした後に中止します。
    --break-on-existing             --download-archive オプションで提供されたアーカイブに存在する
                                    ファイルに遭遇したときにダウンロードプロセスを停止します。
    --no-break-on-existing          アーカイブに存在するファイルに遭遇してもダウンロードプロセスを
                                    停止しません (デフォルト)。
    --break-per-input               --max-downloads、--break-on-existing、--break-match-filters、
                                    および自動番号付けを入力URLごとにリセットするように変更します。
    --no-break-per-input            --break-on-existing および同様のオプションは、
                                    ダウンロードキュー全体を終了させます。
    --skip-playlist-after-errors N  プレイリストの残りをスキップするまでに許容される失敗の数。

## ダウンロードオプション:
    -N, --concurrent-fragments N    dash/hlsnative動画のフラグメントを同時にダウンロードする数
                                    (デフォルトは1)。
    -r, --limit-rate RATE           最大ダウンロードレート（バイト/秒）。例: 50K または 4.2M
    --throttled-rate RATE           スロットリングが想定され、ビデオデータが再抽出される
                                    最小ダウンロードレート（バイト/秒）。例: 100K
    -R, --retries RETRIES           リトライ回数 (デフォルトは10)、または "infinite"。
    --file-access-retries RETRIES   ファイルアクセスエラーでのリトライ回数 (デフォルトは3)、
                                    または "infinite"。
    --fragment-retries RETRIES      フラグメントのリトライ回数 (デフォルトは10)、または "infinite"
                                    (DASH, hlsnative, ISM)。
    --retry-sleep [TYPE:]EXPR       リトライ間のスリープ時間（秒）。オプションでリトライのタイプ
                                    (http (デフォルト), fragment, file_access, extractor)
                                    をプレフィックスとしてスリープを適用できます。EXPRは数値、
                                    linear=START[:END[:STEP=1]]、または exp=START[:END[:BASE=2]]
                                    です。このオプションは、異なるリトライタイプにスリープを
                                    設定するために複数回使用できます。例: --retry-sleep linear=1::2
                                    --retry-sleep fragment:exp=1:20
    --skip-unavailable-fragments    DASH、hlsnative、ISMダウンロードで利用不可能なフラグメントを
                                    スキップします (デフォルト) (エイリアス:
                                    --no-abort-on-unavailable-fragments)。
    --abort-on-unavailable-fragments
                                    フラグメントが利用不可能な場合、ダウンロードを中止します
                                    (エイリアス: --no-skip-unavailable-fragments)。
    --keep-fragments                ダウンロードが終了した後も、ダウンロードしたフラグメントを
                                    ディスク上に保持します。
    --no-keep-fragments             ダウンロードが終了した後、ダウンロードしたフラグメントを
                                    削除します (デフォルト)。
    --buffer-size SIZE              ダウンロードバッファのサイズ。例: 1024 または 16K
                                    (デフォルトは1024)。
    --resize-buffer                 バッファサイズは --buffer-size の初期値から自動的に
                                    リサイズされます (デフォルト)。
    --no-resize-buffer              バッファサイズを自動的に調整しません。
    --http-chunk-size SIZE          チャンクベースのHTTPダウンロード用のチャンクサイズ。
                                    例: 10485760 または 10M (デフォルトは無効)。
                                    Webサーバーによる帯域幅スロットリングを回避するのに
                                    役立つ場合があります (実験的)。
    --playlist-random               プレイリストの動画をランダムな順序でダウンロードします。
    --lazy-playlist                 プレイリストのエントリを受信した順に処理します。
                                    これにより n_entries, --playlist-random, --playlist-reverse
                                    が無効になります。
    --no-lazy-playlist              プレイリスト全体が解析された後にのみ、プレイリストの動画を
                                    処理します (デフォルト)。
    --xattr-set-filesize            ファイルのxattr ytdl.filesizeに期待されるファイルサイズを設定します。
    --hls-use-mpegts                HLS動画にmpegtsコンテナを使用します。これにより、
                                    一部のプレーヤーはダウンロード中に動画を再生でき、
                                    ダウンロードが中断された場合のファイル破損の可能性を
                                    減らします。これはライブストリームではデフォルトで有効です。
    --no-hls-use-mpegts             HLS動画にmpegtsコンテナを使用しません。これは
                                    ライブストリームをダウンロードしていない場合のデフォルトです。
    --download-sections REGEX       正規表現に一致するチャプターのみをダウンロードします。
                                    "*" プレフィックスはチャプターではなく時間範囲を示します。
                                    負のタイムスタンプは末尾から計算されます。
                                    "*from-url" を使用すると、URLから抽出された "start_time" と
                                    "end_time" の間をダウンロードできます。ffmpegが必要です。
                                    このオプションは複数回使用して複数のセクションをダウンロードできます。
                                    例: --download-sections "*10:15-inf" --download-sections "intro"
    --downloader [PROTO:]NAME       使用する外部ダウンローダーの名前またはパス。オプションで
                                    それを使用するプロトコル（http, ftp, m3u8, dash, rstp, rtmp, mms）
                                    をプレフィックスとして指定できます。現在、native, aria2c,
                                    avconv, axel, curl, ffmpeg, httpie, wgetをサポートしています。
                                    このオプションを複数回使用して、異なるプロトコルに
                                    異なるダウンローダーを設定できます。例: --downloader aria2c
                                    --downloader "dash,m3u8:native" は、http/ftpダウンロードに
                                    aria2cを使用し、dash/m3u8ダウンロードにネイティブダウンローダーを
                                    使用します (エイリアス: --external-downloader)。
    --downloader-args NAME:ARGS     外部ダウンローダーにこれらの引数を渡します。ダウンローダー名と
                                    引数をコロン ":" で区切って指定します。ffmpegの場合、
                                    --postprocessor-args と同じ構文を使用して、異なる位置に
                                    引数を渡すことができます。このオプションを複数回使用して、
                                    異なるダウンローダーに異なる引数を渡すことができます
                                    (エイリアス: --external-downloader-args)。

## ファイルシステムオプション:
    -a, --batch-file FILE           ダウンロードするURLを含むファイル ("-" は標準入力)、
                                    1行に1つのURL。"#"、";"、"]"で始まる行はコメントと
                                    みなされ、無視されます。
    --no-batch-file                 バッチファイルからURLを読み込みません (デフォルト)。
    -P, --paths [TYPES:]PATH        ファイルをダウンロードするパス。ファイルの種類とパスを
                                    コロン ":" で区切って指定します。--output と同じTYPESが
                                    すべてサポートされています。さらに、"home" (デフォルト)
                                    および "temp" パスも提供できます。すべての中間ファイルは
                                    まずtempパスにダウンロードされ、ダウンロードが終了した後、
                                    最終的なファイルがhomeパスに移動されます。--output が
                                    絶対パスの場合、このオプションは無視されます。
    -o, --output [TYPES:]TEMPLATE   出力ファイル名のテンプレート。詳細は「出力テンプレート」を
                                    参照してください。
    --output-na-placeholder TEXT    --output で利用不可能なフィールドのプレースホルダー
                                    (デフォルト: "NA")。
    --restrict-filenames            ファイル名をASCII文字のみに制限し、ファイル名に "&" や
                                    スペースが含まれないようにします。
    --no-restrict-filenames         ファイル名にUnicode文字、"&"、スペースを許可します (デフォルト)。
    --windows-filenames             ファイル名を強制的にWindows互換にします。
    --no-windows-filenames          ファイル名を最小限にサニタイズします。
    --trim-filenames LENGTH         ファイル名の長さ（拡張子を除く）を指定された文字数に制限します。
    -w, --no-overwrites             どのファイルも上書きしません。
    --force-overwrites              すべての動画ファイルとメタデータファイルを上書きします。
                                    このオプションは --no-continue を含みます。
    --no-force-overwrites           動画は上書きしませんが、関連ファイルは上書きします (デフォルト)。
    -c, --continue                  部分的にダウンロードされたファイル/フラグメントを再開します (デフォルト)。
    --no-continue                   部分的にダウンロードされたフラグメントを再開しません。
                                    ファイルがフラグメント化されていない場合は、ファイル全体の
                                    ダウンロードを再開します。
    --part                          出力ファイルに直接書き込む代わりに .part ファイルを使用します (デフォルト)。
    --no-part                       .part ファイルを使用せず、出力ファイルに直接書き込みます。
    --mtime                         Last-modifiedヘッダーを使用してファイルの変更時刻を設定します。
    --no-mtime                      Last-modifiedヘッダーを使用してファイルの変更時刻を設定しません (デフォルト)。
    --write-description             動画の説明を .description ファイルに書き込みます。
    --no-write-description          動画の説明を書き込みません (デフォルト)。
    --write-info-json               動画のメタデータを .info.json ファイルに書き込みます
                                    （個人情報が含まれる場合があります）。
    --no-write-info-json            動画のメタデータを書き込みません (デフォルト)。
    --write-playlist-metafiles      --write-info-json、--write-description などを使用する際に、
                                    動画のメタデータに加えてプレイリストのメタデータを書き込みます (デフォルト)。
    --no-write-playlist-metafiles   --write-info-json、--write-description などを使用する際に、
                                    プレイリストのメタデータを書き込みません。
    --clean-info-json               ファイル名などの内部メタデータの一部をinfojsonから削除します (デフォルト)。
    --no-clean-info-json            すべてのフィールドをinfojsonに書き込みます。
    --write-comments                動画のコメントを取得してinfojsonに配置します。
                                    抽出が速いとわかっている場合、このオプションがなくても
                                    コメントは取得されます (エイリアス: --get-comments)。
    --no-write-comments             抽出が速いとわかっている場合を除き、動画のコメントを
                                    取得しません (エイリアス: --no-get-comments)。
    --load-info-json FILE           動画情報を含むJSONファイル（"--write-info-json"
                                    オプションで作成）。
    --cookies FILE                  クッキーを読み込み、クッキージャーをダンプするための
                                    Netscape形式のファイル。
    --no-cookies                    ファイルからクッキーを読み書きしません (デフォルト)。
    --cookies-from-browser BROWSER[+KEYRING][:PROFILE][::CONTAINER]
                                    クッキーを読み込むブラウザの名前。現在サポートされている
                                    ブラウザ: brave, chrome, chromium, edge, firefox, opera,
                                    safari, vivaldi, whale。オプションで、LinuxでChromiumの
                                    クッキーを復号化するためのKEYRING、クッキーを読み込む
                                    PROFILEの名前/パス、およびCONTAINER名（Firefoxの場合）
                                    （"none" はコンテナなし）をそれぞれの区切り文字で指定できます。
                                    デフォルトでは、最も最近アクセスされたプロファイルの
                                    すべてのコンテナが使用されます。現在サポートされている
                                    キーリング: basictext, gnomekeyring, kwallet, kwallet5, kwallet6
    --no-cookies-from-browser       ブラウザからクッキーを読み込みません (デフォルト)。
    --cache-dir DIR                 yt-dlpがダウンロードした情報（クライアントIDや署名など）を
                                    永続的に保存できるファイルシステムの場所。
                                    デフォルトは ${XDG_CACHE_HOME}/yt-dlp
    --no-cache-dir                  ファイルシステムキャッシングを無効にします。
    --rm-cache-dir                  すべてのファイルシステムキャッシュファイルを削除します。

## サムネイルオプション:
    --write-thumbnail               サムネイル画像をディスクに書き込みます。
    --no-write-thumbnail            サムネイル画像をディスクに書き込みません (デフォルト)。
    --write-all-thumbnails          すべてのサムネイル画像フォーマットをディスクに書き込みます。
    --list-thumbnails               各動画の利用可能なサムネイルを一覧表示します。
                                    --no-simulate が使用されない限りシミュレートします。

## インターネットショートカットオプション:
    --write-link                    現在のプラットフォームに応じてインターネットショートカットファイル
                                    (.url, .webloc, .desktop) を書き込みます。URLはOSによって
                                    キャッシュされる場合があります。
    --write-url-link                .url Windowsインターネットショートカットを書き込みます。
                                    OSはファイルパスに基づいてURLをキャッシュします。
    --write-webloc-link             .webloc macOSインターネットショートカットを書き込みます。
    --write-desktop-link            .desktop Linuxインターネットショートカットを書き込みます。

## 詳細表示とシミュレーションオプション:
    -q, --quiet                     静音モードを有効にします。--verbose と共に使用すると、
                                    ログをstderrに出力します。
    --no-quiet                      静音モードを無効にします (デフォルト)。
    --no-warnings                   警告を無視します。
    -s, --simulate                  動画をダウンロードせず、ディスクに何も書き込みません。
    --no-simulate                   印刷/リスト表示オプションが使用されていても動画をダウンロードします。
    --ignore-no-formats-error       「動画フォーマットがありません」エラーを無視します。動画が
                                    実際にダウンロードできなくてもメタデータを抽出するのに
                                    役立ちます (実験的)。
    --no-ignore-no-formats-error    ダウンロード可能な動画フォーマットが見つからない場合に
                                    エラーをスローします (デフォルト)。
    --skip-download                 動画はダウンロードしませんが、関連するすべてのファイルを
                                    書き込みます (エイリアス: --no-download)。
    -O, --print [WHEN:]TEMPLATE     画面に表示するフィールド名または出力テンプレート。オプションで
                                    それをいつ表示するかをコロン ":" で区切ってプレフィックス
                                    できます。サポートされている "WHEN" の値は --use-postprocessor
                                    と同じです (デフォルト: video)。--quiet を含意します。
                                    --no-simulate または後の段階のWHENが使用されない限り、
                                    --simulate を含意します。このオプションは複数回使用できます。
    --print-to-file [WHEN:]TEMPLATE FILE
                                    指定されたテンプレートをファイルに追加します。WHENとTEMPLATE
                                    の値は --print と同じです。FILEは出力テンプレートと同じ
                                    構文を使用します。このオプションは複数回使用できます。
    -j, --dump-json                 静音ですが、各動画のJSON情報を表示します。--no-simulate が
                                    使用されない限りシミュレートします。利用可能なキーの説明は
                                    「出力テンプレート」を参照してください。
    -J, --dump-single-json          静音ですが、渡された各URLまたはinfojsonのJSON情報を表示します。
                                    --no-simulate が使用されない限りシミュレートします。URLが
                                    プレイリストを参照している場合、プレイリスト全体の情報が
                                    1行でダンプされます。
    --force-write-archive           -s や他のシミュレーションオプションが使用されていても、
                                    エラーが発生しない限り、ダウンロードアーカイブエントリを
                                    強制的に書き込みます (エイリアス: --force-download-archive)。
    --newline                       プログレスバーを改行として出力します。
    --no-progress                   プログレスバーを表示しません。
    --progress                      静音モードでもプログレスバーを表示します。
    --console-title                 コンソールのタイトルバーに進捗を表示します。
    --progress-template [TYPES:]TEMPLATE
                                    進捗出力のテンプレート。オプションで "download:" (デフォルト),
                                    "download-title:" (コンソールタイトル), "postprocess:",
                                    または "postprocess-title:" のいずれかをプレフィックスできます。
                                    動画のフィールドは "info" キーの下で、進捗属性は "progress"
                                    キーの下でアクセスできます。例: --console-title
                                    --progress-template "download-title:%(info.id)s-%(progress.eta)s"
    --progress-delta SECONDS        進捗出力間の時間（デフォルト: 0）。
    -v, --verbose                   様々なデバッグ情報を表示します。
    --dump-pages                    問題をデバッグするために、ダウンロードしたページをbase64で
                                    エンコードして表示します (非常に冗長)。
    --write-pages                   問題をデバッグするために、ダウンロードした中間ページを
                                    現在のディレクトリのファイルに書き込みます。
    --print-traffic                 送受信されたHTTPトラフィックを表示します。

## 回避策:
    --encoding ENCODING             指定されたエンコーディングを強制します (実験的)。
    --legacy-server-connect         RFC 5746の安全な再ネゴシエーションをサポートしないサーバーへの
                                    HTTPS接続を明示的に許可します。
    --no-check-certificates         HTTPS証明書の検証を抑制します。
    --prefer-insecure               暗号化されていない接続を使用して動画の情報を取得します
                                    (現在、YouTubeでのみサポート)。
    --add-headers FIELD:VALUE       カスタムHTTPヘッダーとその値をコロン ":" で区切って指定します。
                                    このオプションは複数回使用できます。
    --bidi-workaround               双方向テキストをサポートしないターミナルのための回避策。
                                    PATHにbidivまたはfribidi実行ファイルが必要です。
    --sleep-requests SECONDS        データ抽出中のリクエスト間にスリープする秒数。
    --sleep-interval SECONDS        各ダウンロードの前にスリープする秒数。
                                    --max-sleep-interval と共に使用する場合、これは
                                    最小スリープ時間です (エイリアス: --min-sleep-interval)。
    --max-sleep-interval SECONDS    スリープする最大秒数。--min-sleep-interval と共にのみ
                                    使用できます。
    --sleep-subtitles SECONDS       各字幕ダウンロードの前にスリープする秒数。

## 動画フォーマットオプション:
    -f, --format FORMAT             動画フォーマットコード。詳細は「フォーマットの選択」を参照してください。
    -S, --format-sort SORTORDER     指定されたフィールドでフォーマットをソートします。詳細は
                                    「フォーマットのソート」を参照してください。
    --format-sort-force             ユーザー指定のソート順がすべてのフィールドよりも優先されるように
                                    強制します。詳細は「フォーマットのソート」を参照してください
                                    (エイリアス: --S-force)。
    --no-format-sort-force          一部のフィールドはユーザー指定のソート順よりも優先されます
                                    (デフォルト)。
    --video-multistreams            複数のビデオストリームを1つのファイルにマージすることを許可します。
    --no-video-multistreams         各出力ファイルに対して1つのビデオストリームのみがダウンロード
                                    されます (デフォルト)。
    --audio-multistreams            複数のオーディオストリームを1つのファイルにマージすることを許可します。
    --no-audio-multistreams         各出力ファイルに対して1つのオーディオストリームのみがダウンロード
                                    されます (デフォルト)。
    --prefer-free-formats           同じ品質の非フリーコンテナよりもフリーコンテナのビデオフォーマットを
                                    優先します。品質に関係なくフリーコンテナを厳密に優先するには
                                    "-S ext" と共に使用します。
    --no-prefer-free-formats        フリーコンテナに特別な優先順位を与えません (デフォルト)。
    --check-formats                 実際にダウンロード可能なフォーマットからのみ選択されることを
                                    確認します。
    --check-all-formats             すべてのフォーマットが実際にダウンロード可能かどうかをチェックします。
    --no-check-formats              フォーマットが実際にダウンロード可能であることをチェックしません。
    -F, --list-formats              各動画の利用可能なフォーマットを一覧表示します。
                                    --no-simulate が使用されない限りシミュレートします。
    --merge-output-format FORMAT    フォーマットをマージする際に使用できるコンテナを "/" で
                                    区切って指定します。例: "mp4/mkv"。マージが不要な場合は
                                    無視されます。(現在サポート: avi, flv, mkv, mov, mp4, webm)

## 字幕オプション:
    --write-subs                    字幕ファイルを書き込みます。
    --no-write-subs                 字幕ファイルを書き込みません (デフォルト)。
    --write-auto-subs               自動生成された字幕ファイルを書き込みます
                                    (エイリアス: --write-automatic-subs)。
    --no-write-auto-subs            自動生成された字幕を書き込みません (デフォルト)
                                    (エイリアス: --no-write-automatic-subs)。
    --list-subs                     各動画の利用可能な字幕を一覧表示します。
                                    --no-simulate が使用されない限りシミュレートします。
    --sub-format FORMAT             字幕フォーマット。"/" で区切られたフォーマットの優先順位を
                                    受け付けます。例: "srt" または "ass/srt/best"
    --sub-langs LANGS               ダウンロードする字幕の言語（正規表現可）または "all" を
                                    カンマで区切って指定します。例: --sub-langs "en.*,ja"
                                    ("en.*" は "en" の後に任意の文字が0個以上続く正規表現パターン)。
                                    言語コードの前に "-" を付けると、要求された言語からそれを
                                    除外できます。例: --sub-langs all,-live_chat。
                                    利用可能な言語タグの一覧は --list-subs を使用してください。

## 認証オプション:
    -u, --username USERNAME         このアカウントIDでログインします。
    -p, --password PASSWORD         アカウントのパスワード。このオプションを省略すると、
                                    yt-dlpが対話形式で尋ねます。
    -2, --twofactor TWOFACTOR       二要素認証コード。
    -n, --netrc                     .netrc認証データを使用します。
    --netrc-location PATH           .netrc認証データの場所。パスまたはそれを含むディレクトリ。
                                    デフォルトは ~/.netrc
    --netrc-cmd NETRC_CMD           エクストラクタの認証情報を取得するために実行するコマンド。
    --video-password PASSWORD       動画固有のパスワード。
    --ap-mso MSO                    Adobe PassのMSO（TVプロバイダー）識別子。
                                    利用可能なMSOの一覧は --ap-list-mso を使用してください。
    --ap-username USERNAME          MSOアカウントのログイン。
    --ap-password PASSWORD          MSOアカウントのパスワード。このオプションを省略すると、
                                    yt-dlpが対話形式で尋ねます。
    --ap-list-mso                   サポートされているすべてのMSOを一覧表示します。
    --client-certificate CERTFILE   PEM形式のクライアント証明書ファイルへのパス。
                                    秘密鍵を含む場合があります。
    --client-certificate-key KEYFILE
                                    クライアント証明書用の秘密鍵ファイルへのパス。
    --client-certificate-password PASSWORD
                                    暗号化されている場合、クライアント証明書の秘密鍵のパスワード。
                                    提供されない場合、鍵が暗号化されていればyt-dlpが
                                    対話形式で尋ねます。

## ポストプロセッシングオプション:
    -x, --extract-audio             動画ファイルを音声のみのファイルに変換します
                                    (ffmpegとffprobeが必要)。
    --audio-format FORMAT           -x が使用されたときに音声を変換するフォーマット。
                                    (現在サポート: best (デフォルト), aac, alac, flac,
                                    m4a, mp3, opus, vorbis, wav)。--remux-video と
                                    同様の構文を使用して複数のルールを指定できます。
    --audio-quality QUALITY         -x で音声を変換する際に使用するffmpegの音声品質を指定します。
                                    VBRの場合は0 (最高) から10 (最低) の値を、または128Kの
                                    ような特定のビットレートを挿入します (デフォルトは5)。
    --remux-video FORMAT            必要に応じてビデオを別のコンテナにリマックスします
                                    (現在サポート: avi, flv, gif, mkv, mov, mp4, webm,
                                    aac, aiff, alac, flac, m4a, mka, mp3, ogg, opus,
                                    vorbis, wav)。ターゲットコンテナがビデオ/オーディオ
                                    コーデックをサポートしていない場合、リマックスは失敗します。
                                    複数のルールを指定できます。例: "aac>m4a/mov>mp4/mkv" は
                                    aacをm4aに、movをmp4に、その他をmkvにリマックスします。
    --recode-video FORMAT           必要に応じてビデオを別のフォーマットに再エンコードします。
                                    構文とサポートされているフォーマットは --remux-video と同じです。
    --postprocessor-args NAME:ARGS  ポストプロセッサーにこれらの引数を渡します。
                                    ポストプロセッサー/実行可能ファイル名と引数をコロン ":" で
                                    区切って指定します。サポートされているPP: Merger,
                                    ModifyChapters, SplitChapters, ExtractAudio, VideoRemuxer,
                                    VideoConvertor, Metadata, EmbedSubtitle, EmbedThumbnail,
                                    SubtitlesConvertor, ThumbnailsConvertor, FixupStretched,
                                    FixupM4a, FixupM3u8, FixupTimestamp, FixupDuration。
                                    サポートされている実行可能ファイル: AtomicParsley, FFmpeg,
                                    FFprobe。"PP+EXE:ARGS" を指定して、特定のポストプロセッサーが
                                    使用する場合にのみ、指定された実行可能ファイルに引数を渡すことも
                                    できます。さらに、ffmpeg/ffprobeの場合、プレフィックスに
                                    "_i"/"_o" を付け、オプションで数値を続けることで、
                                    指定された入出力ファイルの前に引数を渡すことができます。
                                    例: --ppa "Merger+ffmpeg_i1:-v quiet"。
                                    このオプションを複数回使用して、異なるポストプロセッサーに
                                    異なる引数を渡すことができます (エイリアス: --ppa)。
    -k, --keep-video                ポストプロセッシング後も中間ビデオファイルをディスク上に
                                    保持します。
    --no-keep-video                 ポストプロセッシング後に中間ビデオファイルを削除します (デフォルト)。
    --post-overwrites               ポストプロセッシングされたファイルを上書きします (デフォルト)。
    --no-post-overwrites            ポストプロセッシングされたファイルを上書きしません。
    --embed-subs                    字幕をビデオに埋め込みます (mp4, webm, mkvビデオのみ)。
    --no-embed-subs                 字幕を埋め込みません (デフォルト)。
    --embed-thumbnail               サムネイルをカバーアートとしてビデオに埋め込みます。
    --no-embed-thumbnail            サムネイルを埋め込みません (デフォルト)。
    --embed-metadata                メタデータをビデオファイルに埋め込みます。
                                    --no-embed-chapters/--no-embed-info-json が
                                    使用されない限り、チャプター/infojsonも埋め込みます
                                    (エイリアス: --add-metadata)。
    --no-embed-metadata             ファイルにメタデータを追加しません (デフォルト)
                                    (エイリアス: --no-add-metadata)。
    --embed-chapters                チャプターマーカーをビデオファイルに追加します
                                    (エイリアス: --add-chapters)。
    --no-embed-chapters             チャプターマーカーを追加しません (デフォルト)
                                    (エイリアス: --no-add-chapters)。
    --embed-info-json               infojsonをmkv/mkaビデオファイルの添付ファイルとして
                                    埋め込みます。
    --no-embed-info-json            infojsonをビデオファイルの添付ファイルとして埋め込みません。
    --parse-metadata [WHEN:]FROM:TO
                                    他のフィールドからタイトル/アーティストなどの追加メタデータを
                                    解析します。詳細は「メタデータの変更」を参照してください。
                                    サポートされている "WHEN" の値は --use-postprocessor
                                    と同じです (デフォルト: pre_process)。
    --replace-in-metadata [WHEN:]FIELDS REGEX REPLACE
                                    指定された正規表現を使用してメタデータフィールドのテキストを
                                    置換します。このオプションは複数回使用できます。
                                    サポートされている "WHEN" の値は --use-postprocessor
                                    と同じです (デフォルト: pre_process)。
    --xattrs                        メタデータをビデオファイルのxattrsに書き込みます
                                    (Dublin CoreとXDG標準を使用)。
    --concat-playlist POLICY        プレイリスト内のビデオを連結します。"never", "always",
                                    または "multi_video" (デフォルト; ビデオが単一の
                                    番組を形成する場合のみ) のいずれか。連結可能であるためには、
                                    すべてのビデオファイルが同じコーデックとストリーム数を
                                    持っている必要があります。"pl_video:" プレフィックスを
                                    "--paths" と "--output" で使用して、連結ファイルの
                                    出力ファイル名を設定できます。詳細は「出力テンプレート」を
                                    参照してください。
    --fixup POLICY                  ファイルの既知の不具合を自動的に修正します。"never"
                                    (何もしない), "warn" (警告のみ出す), "detect_or_warn"
                                    (デフォルト; 可能であればファイルを修正し、そうでなければ
                                    警告する), "force" (ファイルが既に存在する場合でも
                                    修正を試みる) のいずれか。
    --ffmpeg-location PATH          ffmpegバイナリの場所。バイナリへのパスまたはそれを含む
                                    ディレクトリ。
    --exec [WHEN:]CMD               コマンドを実行します。オプションで、実行するタイミングを
                                    コロン ":" で区切ってプレフィックスします。
                                    サポートされている "WHEN" の値は --use-postprocessor
                                    と同じです (デフォルト: after_move)。出力テンプレートと
                                    同じ構文を使用して、任意のフィールドをコマンドの引数として
                                    渡すことができます。フィールドが渡されない場合、
                                    %(filepath,_filename|)q がコマンドの末尾に追加されます。
                                    このオプションは複数回使用できます。
    --no-exec                       以前に定義された --exec を削除します。
    --convert-subs FORMAT           字幕を別のフォーマットに変換します (現在サポート: ass,
                                    lrc, srt, vtt)。変換を無効にするには "--convert-subs none"
                                    を使用します (デフォルト) (エイリアス: --convert-subtitles)。
    --convert-thumbnails FORMAT     サムネイルを別のフォーマットに変換します (現在サポート:
                                    jpg, png, webp)。"--remux-video" と同様の構文を使用して
                                    複数のルールを指定できます。変換を無効にするには
                                    "--convert-thumbnails none" を使用します (デフォルト)。
    --split-chapters                内部チャプターに基づいてビデオを複数のファイルに分割します。
                                    "chapter:" プレフィックスを "--paths" と "--output" で
                                    使用して、分割ファイルの出力ファイル名を設定できます。
                                    詳細は「出力テンプレート」を参照してください。
    --no-split-chapters             チャプターに基づいてビデオを分割しません (デフォルト)。
    --remove-chapters REGEX         タイトルが指定された正規表現に一致するチャプターを削除します。
                                    構文は --download-sections と同じです。このオプションは
                                    複数回使用できます。
    --no-remove-chapters            ファイルからどのチャプターも削除しません (デフォルト)。
    --force-keyframes-at-cuts       セクションをダウンロード/分割/削除する際に、カット部分に
                                    キーフレームを強制します。再エンコードが必要なため遅くなりますが、
                                    結果のビデオはカット周辺のアーティファクトが少なくなる
                                    可能性があります。
    --no-force-keyframes-at-cuts    カット/分割時にチャプター周辺にキーフレームを強制しません
                                    (デフォルト)。
    --use-postprocessor NAME[:ARGS]
                                    有効にするプラグインポストプロセッサーの(大文字小文字を
                                    区別する)名前、および(オプションで)それに渡す引数を
                                    コロン ":" で区切って指定します。ARGSはセミコロン ";"
                                    区切りのNAME=VALUEのリストです。"when" 引数は、
                                    ポストプロセッサーがいつ呼び出されるかを決定します。
                                    "pre_process" (ビデオ抽出後), "after_filter" (ビデオが
                                    フィルターを通過した後), "video" (--formatの後;
                                    --print/--outputの前), "before_dl" (各ビデオダウンロードの前),
                                    "post_process" (各ビデオダウンロードの後; デフォルト),
                                    "after_move" (ビデオファイルを最終的な場所に移動した後),
                                    "after_video" (ビデオのすべてのフォーマットをダウンロード
                                    および処理した後), または "playlist" (プレイリストの最後)
                                    のいずれかです。このオプションは複数回使用して、異なる
                                    ポストプロセッサーを追加できます。

## SponsorBlockオプション:
[SponsorBlock API](https://sponsor.ajay.app)を使用して、ダウンロードした
    YouTubeビデオから様々なセグメント（スポンサー、イントロなど）を削除したり、
    チャプターエントリを作成したりします。

    --sponsorblock-mark CATS        チャプターを作成するSponsorBlockカテゴリをカンマで区切って
                                    指定します。利用可能なカテゴリ: sponsor, intro, outro,
                                    selfpromo, preview, filler, interaction,
                                    music_offtopic, poi_highlight, chapter, all,
                                    default (=all)。カテゴリの前に "-" を付けると除外できます。
                                    カテゴリの説明は を参照してください。例:
                                    --sponsorblock-mark all,-preview
                                    https://wiki.sponsor.ajay.app/w/Segment_Categories
    --sponsorblock-remove CATS      ビデオファイルから削除するSponsorBlockカテゴリをカンマで
                                    区切って指定します。カテゴリがmarkとremoveの両方に存在する場合、
                                    removeが優先されます。構文と利用可能なカテゴリは
                                    --sponsorblock-mark と同じですが、"default" は
                                    "all,-filler" を指し、poi_highlight, chapterは
                                    利用できません。
    --sponsorblock-chapter-title TEMPLATE
                                    --sponsorblock-mark で作成されたSponsorBlockチャプターの
                                    タイトルの出力テンプレート。利用可能なフィールドは
                                    start_time, end_time, category, categories, name,
                                    category_names のみです。デフォルトは
                                    "[SponsorBlock]: %(category_names)l"
    --no-sponsorblock               --sponsorblock-mark と --sponsorblock-remove の両方を
                                    無効にします。
    --sponsorblock-api URL          SponsorBlock APIの場所。デフォルトは
                                    https://sponsor.ajay.app

## エクストラクタオプション:
    --extractor-retries RETRIES     既知のエクストラクタエラーのリトライ回数 (デフォルトは3)、
                                    または "infinite"。
    --allow-dynamic-mpd             動的DASHマニフェストを処理します (デフォルト)
                                    (エイリアス: --no-ignore-dynamic-mpd)。
    --ignore-dynamic-mpd            動的DASHマニフェストを処理しません
                                    (エイリアス: --no-allow-dynamic-mpd)。
    --hls-split-discontinuity       HLSプレイリストを広告ブレークなどの不連続点で異なる
                                    フォーマットに分割します。
    --no-hls-split-discontinuity    HLSプレイリストを広告ブレークなどの不連続点で異なる
                                    フォーマットに分割しません (デフォルト)。
    --extractor-args IE_KEY:ARGS    IE_KEYエクストラクタにARGS引数を渡します。詳細は
                                    「エクストラクタ引数」を参照してください。このオプションを
                                    複数回使用して、異なるエクストラクタに引数を渡すことができます。

## プリセットエイリアス:
利便性と使いやすさのために定義済みのエイリアス。yt-dlpの将来の
    バージョンではプリセットが追加または調整される可能性がありますが、
    既存のプリセット名は変更または削除されません。

    -t mp3                          -f 'ba[acodec^=mp3]/ba/b' -x --audio-format
                                    mp3

    -t aac                          -f
                                    'ba[acodec^=aac]/ba[acodec^=mp4a.40.]/ba/b'
                                    -x --audio-format aac

    -t mp4                          --merge-output-format mp4 --remux-video mp4
                                    -S vcodec:h264,lang,quality,res,fps,hdr:12,a
                                    codec:aac

    -t mkv                          --merge-output-format mkv --remux-video mkv

    -t sleep                        --sleep-subtitles 5 --sleep-requests 0.75
                                    --sleep-interval 10 --max-sleep-interval 20

# 設定

yt-dlpは、サポートされているコマンドラインオプションを設定ファイルに記述することで設定できます。設定は以下の場所から読み込まれます：

1. **メイン設定**:
    * `--config-location`で指定されたファイル
1. **ポータブル設定**: (ポータブルインストールに推奨)
    * バイナリを使用している場合、バイナリと同じディレクトリにある`yt-dlp.conf`
    * ソースコードから実行している場合、`yt_dlp`の親ディレクトリにある`yt-dlp.conf`
1. **ホーム設定**:
    * `-P`で指定されたホームパスにある`yt-dlp.conf`
    * `-P`が指定されていない場合、現在のディレクトリが検索されます
1. **ユーザー設定**:
    * `${XDG_CONFIG_HOME}/yt-dlp.conf`
    * `${XDG_CONFIG_HOME}/yt-dlp/config` (Linux/macOSで推奨)
    * `${XDG_CONFIG_HOME}/yt-dlp/config.txt`
    * `${APPDATA}/yt-dlp.conf`
    * `${APPDATA}/yt-dlp/config` (Windowsで推奨)
    * `${APPDATA}/yt-dlp/config.txt`
    * `~/yt-dlp.conf`
    * `~/yt-dlp.conf.txt`
    * `~/.yt-dlp/config`
    * `~/.yt-dlp/config.txt`

    参照: [環境変数に関する注意](#notes-about-environment-variables)
1. **システム設定**:
    * `/etc/yt-dlp.conf`
    * `/etc/yt-dlp/config`
    * `/etc/yt-dlp/config.txt`

例：以下の設定ファイルを使用すると、yt-dlpは常に音声を抽出し、mtimeをコピーし、プロキシを使用し、すべての動画をホームディレクトリの`YouTube`ディレクトリに保存します：
```
# #で始まる行はコメントです

# 常に音声を抽出
-x

# mtimeをコピー
--mtime

# このプロキシを使用
--proxy 127.0.0.1:3128

# すべての動画をホームディレクトリのYouTubeディレクトリに保存
-o ~/YouTube/%(title)s.%(ext)s
```

**注**: 設定ファイル内のオプションは、通常のコマンドライン呼び出しで使用されるスイッチと同じです。したがって、`-`や`--`の後に**空白を入れてはいけません**。例：`-o`や`--proxy`はOKですが、`- o`や`-- proxy`はNGです。また、UNIXシェルのように、必要に応じて引用符で囲む必要があります。

特定のyt-dlpの実行ですべての設定ファイルを無効にしたい場合は、`--ignore-config`を使用できます。`--ignore-config`がいずれかの設定ファイル内で見つかった場合、それ以上の設定は読み込まれません。例えば、ポータブル設定ファイルにこのオプションがあると、ホーム、ユーザー、システムの設定が読み込まれなくなります。さらに、（後方互換性のために）`--ignore-config`がシステム設定ファイル内で見つかった場合、ユーザー設定は読み込まれません。

### 設定ファイルのエンコーディング

設定ファイルは、UTF BOMが存在する場合はそれに従ってデコードされ、それ以外の場合はシステムロケールのエンコーディングでデコードされます。

ファイルを異なるエンコーディングでデコードしたい場合は、ファイルの先頭に`# coding: ENCODING`を追加してください（例：`# coding: shift-jis`）。その前にスペースやBOMを含め、いかなる文字もあってはいけません。

### .netrcによる認証

認証をサポートするエクストラクタ（`--username`と`--password`でログインとパスワードを提供）のために、yt-dlpを実行するたびにコマンドライン引数として認証情報を渡したり、シェルコマンド履歴に平文のパスワードが残るのを防ぐために、自動的な認証情報ストレージを設定したい場合があるかもしれません。これは、エクストラクタごとに[`.netrc`ファイル](https://stackoverflow.com/tags/.netrc/info)を使用することで実現できます。そのためには、`--netrc-location`に`.netrc`ファイルを作成し、あなただけが読み書きできるように権限を制限する必要があります：
```
touch ${HOME}/.netrc
chmod a-rwx,u+rw ${HOME}/.netrc
```
その後、以下の形式でエクストラクタの認証情報を追加できます。ここで、*extractor*はエクストラクタの名前を小文字で指定します：```
machine <extractor> login <username> password <password>
```
例：
```
machine youtube login myaccount@gmail.com password my_youtube_password
machine twitch login my_twitch_account_name password my_twitch_password
```
`.netrc`ファイルによる認証を有効にするには、yt-dlpに`--netrc`を渡すか、[設定ファイル](#configuration)に記述する必要があります。

.netrcファイルのデフォルトの場所は`~`です（下記参照）。

平文ファイルにパスワードを保持するという欠点がある`.netrc`ファイルの代替として、エクストラクタの認証情報を提供するカスタムシェルコマンドを設定できます。これは`--netrc-cmd`パラメータを提供することで行われ、netrc形式で認証情報を出力し、成功時には`0`を返す必要があります。その他の値はエラーとして扱われます。コマンド内の`{}`はエクストラクタの名前に置き換えられ、正しいエクストラクタの認証情報を選択できるようになります。

例：`.authinfo.gpg`として保存された暗号化された`.netrc`ファイルを使用する場合
```
yt-dlp --netrc-cmd 'gpg --decrypt ~/.authinfo.gpg' 'https://www.youtube.com/watch?v=BaW_jenozKc'
```


### 環境変数に関する注意
* 環境変数は通常、UNIXでは`${VARIABLE}`/`$VARIABLE`、Windowsでは`%VARIABLE%`として指定されますが、このドキュメントでは常に`${VARIABLE}`と表記されます。
* yt-dlpは、Windowsでもパス関連のオプション（例：`--output`, `--config-location`）でUNIXスタイルの変数を使用できます。
* `${XDG_CONFIG_HOME}`が設定されていない場合、デフォルトは`~/.config`、`${XDG_CACHE_HOME}`は`~/.cache`になります。
* Windowsでは、`~`は`${HOME}`が存在すればそれを指し、そうでなければ`${USERPROFILE}`または`${HOMEDRIVE}${HOMEPATH}`を指します。
* Windowsでは、`${USERPROFILE}`は通常`C:\Users\<user name>`を、`${APPDATA}`は`${USERPROFILE}\AppData\Roaming`を指します。

# 出力テンプレート

`-o`オプションは出力ファイル名のテンプレートを指定するために使用され、`-P`オプションは各種類のファイルを保存するパスを指定するために使用されます。

<!-- MANPAGE: BEGIN EXCLUDED SECTION -->
**要約:** [例へ移動](#output-template-examples).
<!-- MANPAGE: END EXCLUDED SECTION -->

`-o`の最も簡単な使い方は、単一のファイルをダウンロードする際にテンプレート引数を設定しないことです。例：`yt-dlp -o funny_video.flv "https://some/video"`（このようにファイル拡張子をハードコーディングすることは推奨*されず*、一部のポストプロセッシングが壊れる可能性があります）。

しかし、各動画をダウンロードする際に置き換えられる特別なシーケンスを含めることもできます。特別なシーケンスは[Pythonの文字列フォーマット操作](https://docs.python.org/3/library/stdtypes.html#printf-style-string-formatting)に従ってフォーマットできます。例：`%(NAME)s`や`%(NAME)05d`。具体的には、パーセント記号の後に括弧で囲まれた名前が続き、その後にフォーマット操作が続きます。

フィールド名自体（括弧内の部分）も特別なフォーマットを持つことができます：

1. **オブジェクト走査**: メタデータで利用可能な辞書やリストは、ドット`.`区切りで走査できます。例：`%(tags.0)s`、`%(subtitles.en.-1.ext)s`。コロン`:`を使ってPythonのスライシングができます。例：`%(id.3:7)s`、`%(id.6:2:-1)s`、`%(formats.:.format_id)s`。中括弧`{}`を使って特定のキーのみを持つ辞書を構築できます。例：`%(formats.:.{format_id,height})#j`。空のフィールド名`%()s`はinfodict全体を指します。例：`%(.{id,title})s`。この方法で利用可能になるすべてのフィールドが以下にリストされているわけではないことに注意してください。そのようなフィールドを確認するには`-j`を使用してください。

1. **算術演算**: 数値フィールドでは`+`、`-`、`*`を使った簡単な算術演算ができます。例：`%(playlist_index+10)03d`、`%(n_entries+1-playlist_index)d`

1. **日付/時刻フォーマット**: 日付/時刻フィールドは、フィールド名と`>`で区切って指定することで[strftimeフォーマット](https://docs.python.org/3/library/datetime.html#strftime-and-strptime-format-codes)に従ってフォーマットできます。例：`%(duration>%H-%M-%S)s`、`%(upload_date>%Y-%m-%d)s`、`%(epoch-3600>%H-%M-%S)s`

1. **代替**: 代替フィールドは`,`で区切って指定できます。例：`%(release_date>%Y,upload_date>%Y|Unknown)s`

1. **置換**: フィールドが*空でない*場合に、実際のフィールド内容の代わりに使用される置換値を、[`str.format`ミニ言語](https://docs.python.org/3/library/string.html#format-specification-mini-language)に従って`&`区切りで指定できます。これは代替フィールドが考慮された後に行われるため、*いずれか*の代替フィールドが*空でない*場合に置換が使用されます。例：`%(chapters&has chapters|no chapters)s`、`%(title&TITLE={:>20}|NO TITLE)s`

1. **デフォルト**: フィールドが空の場合のデフォルト値を`|`区切りでリテラルとして指定できます。これは`--output-na-placeholder`を上書きします。例：`%(uploader|Unknown)s`

1. **追加の変換**: 通常のフォーマットタイプ`diouxXeEfFgGcrs`に加えて、yt-dlpは`B` = **B**ytes、`j` = **j**son（`#`フラグで整形印刷、`+`でUnicode）、`h` = HTMLエスケープ、`l` = カンマ区切りの**l**ist（`#`フラグで`\n`改行区切り）、`q` = ターミナル用に**q**uoteされた文字列（`#`フラグでリストを別々の引数に分割）、`D` = **D**ecimalサフィックスを追加（例：10M）（`#`フラグで1024を因数として使用）、`S` = ファイル名として**S**anitize（`#`フラグで制限付き）への変換をサポートします。

1. **Unicode正規化**: フォーマットタイプ`U`はNFC [Unicode正規化](https://docs.python.org/3/library/unicodedata.html#unicodedata.normalize)に使用できます。代替形式フラグ（`#`）は正規化をNFDに変更し、変換フラグ`+`はNFKC/NFKD互換等価正規化に使用できます。例：`%(title)+.100U`はNFKCです。

要約すると、フィールドの一般的な構文は次のようになります：
```
%(name[.keys][addition][>strf][,alternate][&replacement][|default])[flags][width][.precision][length]type
```

さらに、ファイルの種類に続けてテンプレートをコロン`:`で区切って指定することで、様々なメタデータファイルに対して、一般的な出力テンプレートとは別に異なる出力テンプレートを設定できます。サポートされているファイルの種類は`subtitle`, `thumbnail`, `description`, `annotation` (非推奨), `infojson`, `link`, `pl_thumbnail`, `pl_description`, `pl_infojson`, `chapter`, `pl_video`です。例：`-o "%(title)s.%(ext)s" -o "thumbnail:%(title)s\%(title)s.%(ext)s"`は、サムネイルを動画と同じ名前のフォルダに入れます。いずれかのテンプレートが空の場合、その種類のファイルは書き込まれません。例：`--write-thumbnail -o "thumbnail:"`は、動画ではなくプレイリストのサムネイルのみを書き込みます。

<a id="outtmpl-postprocess-note"></a>

**注**: ポストプロセッシング（マージなど）のため、実際の出力ファイル名は異なる場合があります。すべてのポストプロセッシングが完了した後の名前を取得するには、`--print after_move:filepath`を使用してください。

利用可能なフィールドは以下の通りです：

 - `id` (文字列): 動画のID
 - `title` (文字列): 動画のタイトル
 - `fulltitle` (文字列): ライブのタイムスタンプや一般的なタイトルを無視した動画タイトル
 - `ext` (文字列): 動画のファイル拡張子
 - `alt_title` (文字列): 動画のセカンダリタイトル
 - `description` (文字列): 動画の説明
 - `display_id` (文字列): 動画の代替ID
 - `uploader` (文字列): 動画アップローダーのフルネーム
 - `uploader_id` (文字列): 動画アップローダーのニックネームまたはID
 - `uploader_url` (文字列): 動画アップローダーのプロフィールURL
 - `license` (文字列): 動画がライセンスされているライセンス名
 - `creators` (リスト): 動画の作成者
 - `creator` (文字列): 動画の作成者（カンマ区切り）
 - `timestamp` (数値): 動画が利用可能になった瞬間のUNIXタイムスタンプ
 - `upload_date` (文字列): 動画のアップロード日（UTC）（YYYYMMDD）
 - `release_timestamp` (数値): 動画がリリースされた瞬間のUNIXタイムスタンプ
 - `release_date` (文字列): 動画がリリースされた日付（UTC）（YYYYMMDD）
 - `release_year` (数値): 動画またはアルバムがリリースされた年（YYYY）
 - `modified_timestamp` (数値): 動画が最後に変更された瞬間のUNIXタイムスタンプ
 - `modified_date` (文字列): 動画が最後に変更された日付（UTC）（YYYYMMDD）
 - `channel` (文字列): 動画がアップロードされたチャンネルのフルネーム
 - `channel_id` (文字列): チャンネルのID
 - `channel_url` (文字列): チャンネルのURL
 - `channel_follower_count` (数値): チャンネルのフォロワー数
 - `channel_is_verified` (ブール値): チャンネルがプラットフォームで認証されているかどうか
 - `location` (文字列): 動画が撮影された物理的な場所
 - `duration` (数値): 動画の長さ（秒）
 - `duration_string` (文字列): 動画の長さ（HH:mm:ss）
 - `view_count` (数値): プラットフォームで動画が視聴された回数
 - `concurrent_view_count` (数値): 現在プラットフォームで動画を視聴しているユーザー数
 - `like_count` (数値): 動画の高評価数
 - `dislike_count` (数値): 動画の低評価数
 - `repost_count` (数値): 動画のリポスト数
 - `average_rating` (数値): ユーザーによる平均評価（スケールはウェブページによる）
 - `comment_count` (数値): 動画のコメント数（一部のエクストラクタでは、コメントは最後にダウンロードされるため、このフィールドは使用できません）
 - `age_limit` (数値): 動画の年齢制限（年）
 - `live_status` (文字列): "not_live", "is_live", "is_upcoming", "was_live", "post_live" (ライブだったが、VODはまだ処理されていない) のいずれか
 - `is_live` (ブール値): この動画がライブストリームか固定長の動画か
 - `was_live` (ブール値): この動画が元々ライブストリームだったか
 - `playable_in_embed` (文字列): この動画が他のサイトの埋め込みプレーヤーで再生可能か
 - `availability` (文字列): 動画が "private", "premium_only", "subscriber_only", "needs_auth", "unlisted", "public" のいずれか
 - `media_type` (文字列): サイトによって分類されたメディアのタイプ（例："episode", "clip", "trailer"）
 - `start_time` (数値): URLで指定された再生開始時間（秒）
 - `end_time` (数値): URLで指定された再生終了時間（秒）
 - `extractor` (文字列): エクストラクタの名前
 - `extractor_key` (文字列): エクストラクタのキー名
 - `epoch` (数値): 情報抽出が完了した時点のUnixエポック
 - `autonumber` (数値): ダウンロードごとに増加する番号。`--autonumber-start`から始まり、5桁になるようにゼロでパディングされます
 - `video_autonumber` (数値): 動画ごとに増加する番号
 - `n_entries` (数値): プレイリストで抽出されたアイテムの総数
 - `playlist_id` (文字列): 動画が含まれるプレイリストのID
 - `playlist_title` (文字列): 動画が含まれるプレイリストの名前
 - `playlist` (文字列): `playlist_title`が利用可能な場合はそれ、そうでなければ`playlist_id`
 - `playlist_count` (数値): プレイリスト内のアイテムの総数。プレイリスト全体が抽出されていない場合は不明な場合があります
 - `playlist_index` (数値): プレイリスト内の動画のインデックス。最終インデックスに応じてゼロでパディングされます
 - `playlist_autonumber` (数値): プレイリストのダウンロードキュー内での動画の位置。プレイリストの全長に応じてゼロでパディングされます
 - `playlist_uploader` (文字列): プレイリストアップローダーのフルネーム
 - `playlist_uploader_id` (文字列): プレイリストアップローダーのニックネームまたはID
 - `playlist_channel` (文字列): プレイリストをアップロードしたチャンネルの表示名
 - `playlist_channel_id` (文字列): プレイリストをアップロードしたチャンネルのID
 - `playlist_webpage_url` (文字列): プレイリストのウェブページのURL
 - `webpage_url` (文字列): 動画のウェブページへのURL。yt-dlpに与えると、再び同じ結果が得られるはずです
 - `webpage_url_basename` (文字列): ウェブページURLのベース名
 - `webpage_url_domain` (文字列): ウェブページURLのドメイン
 - `original_url` (文字列): ユーザーが指定したURL（またはプレイリストエントリの場合は`webpage_url`と同じ）
 - `categories` (リスト): 動画が属するカテゴリのリスト
 - `tags` (リスト): 動画に割り当てられたタグのリスト
 - `cast` (リスト): キャストメンバーのリスト

[フォーマットのフィルタリング](#filtering-formats)のすべてのフィールドも使用できます。

何らかの論理的なチャプターやセクションに属する動画で利用可能：

 - `chapter` (文字列): 動画が属するチャプターの名前またはタイトル
 - `chapter_number` (数値): 動画が属するチャプターの番号
 - `chapter_id` (文字列): 動画が属するチャプターのID

何らかのシリーズや番組のエピソードである動画で利用可能：

 - `series` (文字列): 動画エピソードが属するシリーズまたは番組のタイトル
 - `series_id` (文字列): 動画エピソードが属するシリーズまたは番組のID
 - `season` (文字列): 動画エピソードが属するシーズンのタイトル
 - `season_number` (数値): 動画エピソードが属するシーズンの番号
 - `season_id` (文字列): 動画エピソードが属するシーズンのID
 - `episode` (文字列): 動画エピソードのタイトル
 - `episode_number` (数値): シーズン内の動画エピソードの番号
 - `episode_id` (文字列): 動画エピソードのID

音楽アルバムのトラックまたは一部であるメディアで利用可能：

 - `track` (文字列): トラックのタイトル
 - `track_number` (数値): アルバムまたはディスク内のトラック番号
 - `track_id` (文字列): トラックのID
 - `artists` (リスト): トラックのアーティスト
 - `artist` (文字列): トラックのアーティスト（カンマ区切り）
 - `genres` (リスト): トラックのジャンル
 - `genre` (文字列): トラックのジャンル（カンマ区切り）
 - `composers` (リスト): 曲の作曲者
 - `composer` (文字列): 曲の作曲者（カンマ区切り）
 - `album` (文字列): トラックが属するアルバムのタイトル
 - `album_type` (文字列): アルバムの種類
 - `album_artists` (リスト): アルバムに参加したすべてのアーティスト
 - `album_artist` (文字列): アルバムに参加したすべてのアーティスト（カンマ区切り）
 - `disc_number` (数値): トラックが属するディスクまたは他の物理メディアの番号

`--download-sections`を使用している場合、および内部チャプターを持つ動画で`--split-chapters`を使用している場合の`chapter:`プレフィックスでのみ利用可能：

 - `section_title` (文字列): チャプターのタイトル
 - `section_number` (数値): ファイル内のチャプター番号
 - `section_start` (数値): チャプターの開始時間（秒）
 - `section_end` (数値): チャプターの終了時間（秒）

`--print`でのみ利用可能：

 - `urls` (文字列): 要求されたすべてのフォーマットのURL、1行に1つずつ
 - `filename` (文字列): 動画ファイルの名前。注：[実際のファイル名は異なる場合があります](#outtmpl-postprocess-note)
 - `formats_table` (テーブル): `--list-formats`で表示される動画フォーマットテーブル
 - `thumbnails_table` (テーブル): `--list-thumbnails`で表示されるサムネイルフォーマットテーブル
 - `subtitles_table` (テーブル): `--list-subs`で表示される字幕フォーマットテーブル
 - `automatic_captions_table` (テーブル): `--list-subs`で表示される自動字幕フォーマットテーブル

 動画がダウンロードされた後でのみ利用可能 (`post_process`/`after_move`)：

 - `filepath`: ダウンロードされた動画ファイルの実際のパス

`--sponsorblock-chapter-title`でのみ利用可能：

 - `start_time` (数値): チャプターの開始時間（秒）
 - `end_time` (数値): チャプターの終了時間（秒）
 - `categories` (リスト): チャプターが属する[SponsorBlockカテゴリ](https://wiki.sponsor.ajay.app/w/Types#Category)
 - `category` (文字列): チャプターが属する最小のSponsorBlockカテゴリ
 - `category_names` (リスト): カテゴリの分かりやすい名前
 - `name` (文字列): 最小カテゴリの分かりやすい名前
 - `type` (文字列): チャプターの[SponsorBlockアクションタイプ](https://wiki.sponsor.ajay.app/w/Types#Action_Type)

前述の各シーケンスは、出力テンプレートで参照されると、シーケンス名に対応する実際の値に置き換えられます。例：`-o %(title)s-%(id)s.%(ext)s`で、タイトルが`yt-dlp test video`、IDが`BaW_jenozKc`のmp4動画の場合、カレントディレクトリに`yt-dlp test video-BaW_jenozKc.mp4`というファイルが作成されます。

**注**: 一部のシーケンスは、特定のエクストラクタによって取得されたメタデータに依存するため、存在が保証されていません。そのようなシーケンスは、`--output-na-placeholder`で提供されるプレースホルダー値（デフォルトでは`NA`）に置き換えられます。

**ヒント**: 特定のURLで利用可能なフィールドを特定するには、`-j`の出力を確認してください。

数値シーケンスについては、[数値関連のフォーマット](https://docs.python.org/3/library/stdtypes.html#printf-style-string-formatting)を使用できます。例：`%(view_count)05d`は、視聴回数を5文字になるようにゼロでパディングした文字列になります（例：`00042`）。

出力テンプレートには任意の階層パスを含めることもできます。例：`-o "%(playlist)s/%(playlist_index)s - %(title)s.%(ext)s"`は、各動画をこのパステンプレートに対応するディレクトリにダウンロードします。存在しないディレクトリは自動的に作成されます。

出力テンプレートでパーセントリテラルを使用するには`%%`を使用します。標準出力に出力するには`-o -`を使用します。

現在のデフォルトテンプレートは`%(title)s [%(id)s].%(ext)s`です。

場合によっては、ダウンロードしたファイル名をWindowsシステムに転送したり、8ビット非対応のチャネルを通じてファイル名を渡したりする際に、中、スペース、&などの特殊文字を使用したくないことがあります。このような場合は、`--restrict-filenames`フラグを追加して、より短いタイトルを取得してください。

#### 出力テンプレートの例

```bash
$ yt-dlp --print filename -o "test video.%(ext)s" BaW_jenozKc
test video.webm    # 正しい拡張子を持つリテラル名

$ yt-dlp --print filename -o "%(title)s.%(ext)s" BaW_jenozKc
youtube-dl test video ''_ä↭𝕐.webm    # あらゆる種類の奇妙な文字

$ yt-dlp --print filename -o "%(title)s.%(ext)s" BaW_jenozKc --restrict-filenames
youtube-dl_test_video_.webm    # 制限されたファイル名

# YouTubeプレイリストの動画を、プレイリスト内の動画順でインデックス付けされた別々のディレクトリにダウンロードする
$ yt-dlp -o "%(playlist)s/%(playlist_index)s - %(title)s.%(ext)s" "https://www.youtube.com/playlist?list=PLwiyx1dc3P2JR9N8gQaQN_BCvlSlap7re"

# YouTubeプレイリストの動画を、アップロードされた年に応じて別々のディレクトリにダウンロードする
$ yt-dlp -o "%(upload_date>%Y)s/%(title)s.%(ext)s" "https://www.youtube.com/playlist?list=PLwiyx1dc3P2JR9N8gQaQN_BCvlSlap7re"

# プレイリストインデックスに " - " 区切り文字を接頭辞として付けるが、利用可能な場合のみ
$ yt-dlp -o "%(playlist_index&{} - |)s%(title)s.%(ext)s" BaW_jenozKc "https://www.youtube.com/user/TheLinuxFoundation/playlists"

# YouTubeチャンネル/ユーザーのすべてのプレイリストをダウンロードし、各プレイリストを別々のディレクトリに保存する:
$ yt-dlp -o "%(uploader)s/%(playlist)s/%(playlist_index)s - %(title)s.%(ext)s" "https://www.youtube.com/user/TheLinuxFoundation/playlists"

# Udemyコースをダウンロードし、各チャプターをホームのMyVideosディレクトリ下の別々のディレクトリに保存する
$ yt-dlp -u user -p password -P "~/MyVideos" -o "%(playlist)s/%(chapter_number)s - %(chapter)s/%(title)s.%(ext)s" "https://www.udemy.com/java-tutorial"

# シリーズのシーズン全体をダウンロードし、各シリーズと各シーズンをC:/MyVideos下の別々のディレクトリに保存する
$ yt-dlp -P "C:/MyVideos" -o "%(series)s/%(season_number)s - %(season)s/%(episode_number)s - %(episode)s.%(ext)s" "https://videomore.ru/kino_v_detalayah/5_sezon/367617"

# 動画を "C:\MyVideos\uploader\title.ext" として、字幕を "C:\MyVideos\subs\uploader\title.ext" としてダウンロードし、
# すべての一時ファイルを "C:\MyVideos\tmp" に置く
$ yt-dlp -P "C:/MyVideos" -P "temp:tmp" -P "subtitle:subs" -o "%(uploader)s/%(title)s.%(ext)s" BaW_jenozKc --write-subs

# 動画を "C:\MyVideos\uploader\title.ext" として、字幕を "C:\MyVideos\uploader\subs\title.ext" としてダウンロードする
$ yt-dlp -P "C:/MyVideos" -o "%(uploader)s/%(title)s.%(ext)s" -o "subtitle:%(uploader)s/subs/%(title)s.%(ext)s" BaW_jenozKc --write-subs

# ダウンロード中の動画を標準出力にストリーミングする
$ yt-dlp -o - BaW_jenozKc```

# フォーマットの選択

デフォルトでは、オプションを**渡さない**場合、yt-dlpは利用可能な最高の品質をダウンロードしようとします。
これは一般的に`-f bestvideo*+bestaudio/best`を使用するのと同じです。しかし、複数のオーディオストリームが有効になっている場合（`--audio-multistreams`）、デフォルトのフォーマットは`-f bestvideo+bestaudio/best`に変わります。同様に、ffmpegが利用できない場合、またはyt-dlpを使用して標準出力にストリーミングする場合（`-o -`）、デフォルトは`-f best/bestvideo+bestaudio`になります。

**非推奨の警告**: yt-dlpの最新バージョンでは、ffmpegを使用して複数のフォーマットを同時に標準出力にストリーミングできます。そのため、将来のバージョンでは、このデフォルトは通常のダウンロードと同様に`-f bv*+ba/b`に設定されます。`-f b/bv+ba`の設定を維持したい場合は、設定オプションで明示的に指定することをお勧めします。

フォーマット選択の一般的な構文は`-f FORMAT`（または`--format FORMAT`）で、`FORMAT`はダウンロードしたいフォーマットを記述する*セレクタ式*です。

<!-- MANPAGE: BEGIN EXCLUDED SECTION -->
**要約:** [例へ移動](#format-selection-examples).
<!-- MANPAGE: END EXCLUDED SECTION -->

最も簡単なケースは、特定のフォーマットを要求することです。例えば、`-f 22`でフォーマットコードが22のフォーマットをダウンロードできます。特定の動画で利用可能なフォーマットコードのリストは、`--list-formats`または`-F`で取得できます。これらのフォーマットコードはエクストラクタ固有であることに注意してください。

また、ファイル拡張子（現在サポートされているのは`3gp`, `aac`, `flv`, `m4a`, `mp3`, `mp4`, `ogg`, `wav`, `webm`）を使用して、単一のファイルとして提供される特定のファイル拡張子の最高品質のフォーマットをダウンロードすることもできます。例えば、`-f webm`は、単一のファイルとして提供される`webm`拡張子の最高品質のフォーマットをダウンロードします。

`-f -`を使用すると、*各動画ごとに*対話形式でフォーマットセレクタを提供できます。

また、特殊な名前を使用して、特定のエッジケースのフォーマットを選択することもできます：

 - `all`: **すべてのフォーマットを**個別に選択
 - `mergeall`: **すべてのフォーマットをマージして**選択（`--audio-multistreams`、`--video-multistreams`、または両方と併用する必要があります）
 - `b*`, `best*`: ビデオ、オーディオ、またはその両方を**いずれか含む**最高品質のフォーマットを選択（つまり、`vcodec!=none or acodec!=none`）
 - `b`, `best`: ビデオとオーディオの**両方を含む**最高品質のフォーマットを選択。`best*[vcodec!=none][acodec!=none]`と同等
 - `bv`, `bestvideo`: 最高品質の**ビデオのみ**のフォーマットを選択。`best*[acodec=none]`と同等
 - `bv*`, `bestvideo*`: **ビデオを含む**最高品質のフォーマットを選択。オーディオを含む場合もあります。`best*[vcodec!=none]`と同等
 - `ba`, `bestaudio`: 最高品質の**オーディオのみ**のフォーマットを選択。`best*[vcodec=none]`と同等
 - `ba*`, `bestaudio*`: **オーディオを含む**最高品質のフォーマットを選択。ビデオを含む場合もあります。`best*[acodec!=none]`と同等（[使用しないでください！](https://github.com/yt-dlp/yt-dlp/issues/979#issuecomment-919629354)）
 - `w*`, `worst*`: ビデオまたはオーディオのいずれかを含む最低品質のフォーマットを選択
 - `w`, `worst`: ビデオとオーディオの両方を含む最低品質のフォーマットを選択。`worst*[vcodec!=none][acodec!=none]`と同等
 - `wv`, `worstvideo`: 最低品質のビデオのみのフォーマットを選択。`worst*[acodec=none]`と同等
 - `wv*`, `worstvideo*`: ビデオを含む最低品質のフォーマットを選択。オーディオを含む場合もあります。`worst*[vcodec!=none]`と同等
 - `wa`, `worstaudio`: 最低品質のオーディオのみのフォーマットを選択。`worst*[vcodec=none]`と同等
 - `wa*`, `worstaudio*`: オーディオを含む最低品質のフォーマットを選択。ビデオを含む場合もあります。`worst*[acodec!=none]`と同等

例えば、最低品質のビデオのみのフォーマットをダウンロードするには、`-f worstvideo`を使用できます。しかし、`worst`および関連オプションの使用は推奨されません。フォーマットセレクタが`worst`の場合、すべての点で最も悪いフォーマットが選択されます。ほとんどの場合、実際に欲しいのはファイルサイズが最も小さいビデオです。そのため、`-f worst`の代わりに`-S +size`またはより厳密に`-S +size,+br,+res,+fps`を使用する方が一般的に良いです。詳細は[フォーマットのソート](#sorting-formats)を参照してください。

`best<type>.<n>`を使用して、n番目に良いタイプのフォーマットを選択できます。例えば、`best.2`は2番目に良い結合フォーマットを選択します。同様に、`bv*.3`は3番目に良いビデオストリームを含むフォーマットを選択します。

複数の動画をダウンロードし、それらが同じフォーマットを利用できない場合、スラッシュを使用して優先順位を指定できます。左側のフォーマットが優先されることに注意してください。例えば、`-f 22/17/18`は、フォーマット22が利用可能であればそれをダウンロードし、そうでなければフォーマット17が利用可能であればそれをダウンロードし、そうでなければフォーマット18が利用可能であればそれをダウンロードし、そうでなければ適切なフォーマットがダウンロードできないと文句を言います。

同じビデオの複数のフォーマットをダウンロードしたい場合は、カンマを区切り文字として使用します。例：`-f 22,17,18`は、もちろん利用可能であれば、これら3つのフォーマットすべてをダウンロードします。または、優先順位機能と組み合わせたより洗練された例：`-f 136/137/mp4/bestvideo,140/m4a/bestaudio`。

`-f <format1>+<format2>+...`を使用して、複数のフォーマットのビデオとオーディオを1つのファイルにマージできます（ffmpegのインストールが必要です）。例：`-f bestvideo+bestaudio`は、最高のビデオのみのフォーマットと最高のオーディオのみのフォーマットをダウンロードし、ffmpegでそれらを結合します。

**非推奨の警告**: *以下の*説明されている動作は複雑で直感的でないため、これは削除され、将来的にはマルチストリームがデフォルトで有効になります。代わりに、フォーマットを単一のオーディオ/ビデオに制限する新しい演算子が追加されます。

`--video-multistreams`が使用されていない限り、最初のものを除くすべてのビデオストリームを持つフォーマットは無視されます。同様に、`--audio-multistreams`が使用されていない限り、最初のものを除くすべてのオーディオストリームを持つフォーマットは無視されます。例：`-f bestvideo+best+bestaudio --video-multistreams --audio-multistreams`は、指定された3つのフォーマットすべてをダウンロードしてマージします。結果のファイルには2つのビデオストリームと2つのオーディオストリームが含まれます。しかし、`-f bestvideo+best+bestaudio --no-video-multistreams`は、`bestvideo`と`bestaudio`のみをダウンロードしてマージします。ビデオストリームを含む別のフォーマット（`bestvideo`）がすでに選択されているため、`best`は無視されます。したがって、フォーマットの順序は重要です。`-f best+bestaudio --no-audio-multistreams`は`best`のみをダウンロードしますが、`-f bestaudio+best --no-audio-multistreams`は`best`を無視し、`bestaudio`のみをダウンロードします。

## フォーマットのフィルタリング

`-f "best[height=720]"`（またはセレクタなしのフィルタは`best`と解釈されるため`-f "[filesize>10M]"`）のように、角括弧内に条件を記述してビデオフォーマットをフィルタリングすることもできます。

以下の数値メタフィールドは、比較演算子`<`、`<=`、`>`、`>=`、`=`（等しい）、`!=`（等しくない）と共に使用できます：

 - `filesize`: 事前にわかっている場合のバイト数
 - `filesize_approx`: 推定バイト数
 - `width`: わかっている場合のビデオの幅
 - `height`: わかっている場合のビデオの高さ
 - `aspect_ratio`: わかっている場合のビデオのアスペクト比
 - `tbr`: オーディオとビデオの平均ビットレート（[kbps](## "1000 bits/sec")）
 - `abr`: 平均オーディオビットレート（[kbps](## "1000 bits/sec")）
 - `vbr`: 平均ビデオビットレート（[kbps](## "1000 bits/sec")）
 - `asr`: オーディオサンプリングレート（ヘルツ）
 - `fps`: フレームレート
 - `audio_channels`: オーディオチャンネル数
 - `stretched_ratio`: ビデオのピクセルが正方形でない場合の`幅:高さ`

また、フィルタリングは比較演算子`=`（等しい）、`^=`（で始まる）、`$=`（で終わる）、`*=`（を含む）、`~=`（正規表現に一致）および以下の文字列メタフィールドで機能します：

 - `url`: ビデオURL
 - `ext`: ファイル拡張子
 - `acodec`: 使用されているオーディオコーデックの名前
 - `vcodec`: 使用されているビデオコーデックの名前
 - `container`: コンテナフォーマットの名前
 - `protocol`: 実際のダウンロードに使用されるプロトコル、小文字（`http`, `https`, `rtsp`, `rtmp`, `rtmpe`, `mms`, `f4m`, `ism`, `http_dash_segments`, `m3u8`, or `m3u8_native`）
 - `language`: 言語コード
 - `dynamic_range`: ビデオのダイナミックレンジ
 - `format_id`: フォーマットの簡単な説明
 - `format`: 人間が読める形式のフォーマットの説明
 - `format_note`: フォーマットに関する追加情報
 - `resolution`: 幅と高さのテキスト説明

文字列比較は、反対の比較を生成するために否定`!`を前に付けることができます。例：`!*=`（を含まない）。文字列比較の比較対象は、スペースや`._-`以外の特殊文字を含む場合、二重引用符または単一引用符で囲む必要があります。

**注**: 前述のメタフィールドのいずれも、特定のエクストラクタによって取得されたメタデータ、つまりウェブサイトによって提供されるメタデータにのみ依存するため、存在が保証されているわけではありません。エクストラクタによって利用可能になった他のフィールドもフィルタリングに使用できます。

値が不明なフォーマットは、演算子の後に疑問符（`?`）を付けない限り除外されます。フォーマットフィルタを組み合わせることができます。例えば、`-f "bv[height<=?720][tbr>500]"`は、最大720pのビデオ（または高さが不明なビデオ）で、ビットレートが少なくとも500 kbpsのものを選択します。`all`とフィルタを組み合わせて、フィルタを満たすすべてのフォーマットをダウンロードすることもできます。例：`-f "all[vcodec=none]"`は、すべてのオーディオのみのフォーマットを選択します。

フォーマットセレクタは括弧でグループ化することもできます。例：`-f "(mp4,webm)[height<480]"`は、高さが480未満の最高品質の事前マージ済みmp4およびwebmフォーマットをダウンロードします。

## フォーマットのソート

`-S`（`--format-sort`）を使用して、`best`と見なされる基準を変更できます。これの一般的なフォーマットは`--format-sort field1,field2...`です。

利用可能なフィールドは以下の通りです：

 - `hasvid`: ビデオストリームを持つフォーマットを優先します
 - `hasaud`: オーディオストリームを持つフォーマットを優先します
 - `ie_pref`: フォーマットの優先度
 - `lang`: エクストラクタによって決定される言語の優先度（例：オリジナル言語が音声解説より優先）
 - `quality`: フォーマットの品質
 - `source`: ソースの優先度
 - `proto`: ダウンロードに使用されるプロトコル（`https`/`ftps` > `http`/`ftp` > `m3u8_native`/`m3u8` > `http_dash_segments`> `websocket_frag` > `mms`/`rtsp` > `f4f`/`f4m`）
 - `vcodec`: ビデオコーデック（`av01` > `vp9.2` > `vp9` > `h265` > `h264` > `vp8` > `h263` > `theora` > その他）
 - `acodec`: オーディオコーデック（`flac`/`alac` > `wav`/`aiff` > `opus` > `vorbis` > `aac` > `mp4a` > `mp3` > `ac4` > `eac3` > `ac3` > `dts` > その他）
 - `codec`: `vcodec,acodec`と同等
 - `vext`: ビデオ拡張子（`mp4` > `mov` > `webm` > `flv` > その他）。`--prefer-free-formats`を使用する場合、`webm`が優先されます。
 - `aext`: オーディオ拡張子（`m4a` > `aac` > `mp3` > `ogg` > `opus` > `webm` > その他）。`--prefer-free-formats`を使用する場合、順序は`ogg` > `opus` > `webm` > `mp3` > `m4a` > `aac`に変わります。
 - `ext`: `vext,aext`と同等
 - `filesize`: 事前にわかっている場合の正確なファイルサイズ
 - `fs_approx`: おおよそのファイルサイズ
 - `size`: 利用可能な場合は正確なファイルサイズ、そうでなければおおよそのファイルサイズ
 - `height`: ビデオの高さ
 - `width`: ビデオの幅
 - `res`: ビデオの解像度、最小の次元として計算されます。
 - `fps`: ビデオのフレームレート
 - `hdr`: ビデオのダイナミックレンジ（`DV` > `HDR12` > `HDR10+` > `HDR10` > `HLG` > `SDR`）
 - `channels`: オーディオチャンネル数
 - `tbr`: 総平均ビットレート（[kbps](## "1000 bits/sec")）
 - `vbr`: 平均ビデオビットレート（[kbps](## "1000 bits/sec")）
 - `abr`: 平均オーディオビットレート（[kbps](## "1000 bits/sec")）
 - `br`: 平均ビットレート（[kbps](## "1000 bits/sec")）、`tbr`/`vbr`/`abr`
 - `asr`: オーディオサンプルレート（Hz）

**非推奨の警告**: これらのフィールドの多くには（現在文書化されていない）エイリアスがあり、将来のバージョンで削除される可能性があります。文書化されたフィールド名のみを使用することをお勧めします。

特に指定がない限り、すべてのフィールドは降順でソートされます。これを逆にするには、フィールドの前に`+`を付けます。例：`+res`は最も解像度の小さいフォーマットを優先します。さらに、フィールドに優先値をコロン`:`で区切って接尾辞として付けることができます。例：`res:720`はより大きなビデオを優先しますが、720pより大きくなく、720p未満のビデオがない場合は最も小さいビデオを優先します。`codec`と`ext`については、2つの優先値を指定できます。1つ目はビデオ用、2つ目はオーディオ用です。例：`+codec:avc:m4a`（`+vcodec:avc,+acodec:m4a`と同等）は、ビデオコーデックの優先順位を`h264` > `h265` > `vp9` > `vp9.2` > `av01` > `vp8` > `h263` > `theora`に、オーディオコーデックの優先順位を`mp4a` > `aac` > `vorbis` > `opus` > `mp3` > `ac3` > `dts`に設定します。また、区切り文字として`~`を使用して、提供された値に最も近い値をソートで優先させることもできます。例：`filesize~1G`は、ファイルサイズが1GiBに最も近いフォーマットを優先します。

フィールド`hasvid`と`ie_pref`は、ユーザー定義の順序に関係なく、常にソートで最も高い優先度が与えられます。この動作は`--format-sort-force`を使用することで変更できます。これらを除き、使用されるデフォルトの順序は`lang,quality,res,fps,hdr:12,vcodec,channels,acodec,size,br,asr,proto,ext,hasaud,source,id`です。エクストラクタはこのデフォルトの順序を上書きすることがありますが、ユーザーが提供した順序を上書きすることはできません。

hdrのデフォルトは`hdr:12`であることに注意してください。つまり、Dolby Visionは優先されません。この選択は、DVフォーマットがまだほとんどのデバイスと完全に互換性がないために行われました。これは将来変更される可能性があります。

フォーマットセレクタが`worst`の場合、ソート後の最後のアイテムが選択されます。これは、すべての点で最も悪いフォーマットが選択されることを意味します。ほとんどの場合、実際に欲しいのはファイルサイズが最も小さいビデオです。そのため、`-f best -S +size,+br,+res,+fps`を使用する方が一般的に良いです。

**ヒント**: `-v -F`を使用して、フォーマットがどのようにソートされたか（悪いものから良いものへ）を確認できます。

## フォーマット選択の例

```bash
# 最高のビデオのみのフォーマットと最高のオーディオのみのフォーマットをダウンロードしてマージする、
# またはビデオのみのフォーマットが利用できない場合は最高の結合フォーマットをダウンロードする
$ yt-dlp -f "bv+ba/b"

# ビデオを含む最高のフォーマットをダウンロードし、
# まだオーディオストリームがない場合は、最高のオーディオのみのフォーマットとマージする
$ yt-dlp -f "bv*+ba/b"

# 上記と同じ
$ yt-dlp

# 最高のビデオのみのフォーマットと最高のオーディオのみのフォーマットをマージせずにダウンロードする
# この場合、デフォルトではbestvideoとbestaudioは同じファイル名になるため、
# 出力テンプレートを使用する必要があります。
$ yt-dlp -f "bv,ba" -o "%(title)s.f%(format_id)s.%(ext)s"

# ビデオストリームを持つ最高のフォーマットと、
# すべてのオーディオのみのフォーマットを1つのファイルにダウンロードしてマージする
$ yt-dlp -f "bv*+mergeall[vcodec=none]" --audio-multistreams

# ビデオストリームを持つ最高のフォーマットと、
# 上位2つのオーディオのみのフォーマットを1つのファイルにダウンロードしてマージする
$ yt-dlp -f "bv*+ba+ba.2" --audio-multistreams


# 以下の例は、フォーマット選択の古い方法（-Sなし）と、
# -Sを使用して同様の（しかし一般的にはより良い）結果を得る方法を示しています

# 利用可能な最低品質のビデオをダウンロードする（古い方法）
$ yt-dlp -f "wv*+wa/w"

# 利用可能な最高のビデオを、しかし解像度が最も小さいものをダウンロードする
$ yt-dlp -S "+res"

# 利用可能な最も小さいビデオをダウンロードする
$ yt-dlp -S "+size,+br"



# 利用可能な最高のmp4ビデオ、またはmp4が利用できない場合は最高のビデオをダウンロードする
$ yt-dlp -f "bv*[ext=mp4]+ba[ext=m4a]/b[ext=mp4] / bv*+ba/b"

# 最高の拡張子を持つ最高のビデオをダウンロードする
# （ビデオの場合、mp4 > mov > webm > flv。オーディオの場合、m4a > aac > mp3 ...）
$ yt-dlp -S "ext"



# 利用可能な最高のビデオを、しかし480pより良くないものをダウンロードする、
# または480p以下のビデオがない場合は最低品質のビデオをダウンロードする
$ yt-dlp -f "bv*[height<=480]+ba/b[height<=480] / wv*+ba/w"

# 利用可能な最高のビデオを、高さが最大で480pより良くないものをダウンロードする、
# または480p以下のビデオがない場合は解像度が最も小さい最高のビデオをダウンロードする
$ yt-dlp -S "height:480"

# 利用可能な最高のビデオを、解像度が最大で480pより良くないものをダウンロードする、
# または480p以下のビデオがない場合は解像度が最も小さい最高のビデオをダウンロードする
# 解像度は最小の次元を使用して決定されます。
# そのため、垂直ビデオでも正しく動作します。
$ yt-dlp -S "res:480"



# 最高のビデオ（オーディオも含む）を、しかし50MBより大きくないものをダウンロードする、
# または50MB以下のビデオがない場合は最低品質のビデオ（オーディオも含む）をダウンロードする
$ yt-dlp -f "b[filesize<50M] / w"

# 最大のビデオ（オーディオも含む）を、しかし50MBより大きくないものをダウンロードする、
# または50MB以下のビデオがない場合は最小のビデオ（オーディオも含む）をダウンロードする
$ yt-dlp -f "b" -S "filesize:50M"

# サイズが50MBに最も近い最高のビデオ（オーディオも含む）をダウンロードする
$ yt-dlp -f "b" -S "filesize~50M"



# HTTP/HTTPSプロトコル経由の直接リンクで利用可能な最高のビデオをダウンロードする、
# またはそのようなビデオがない場合は任意のプロトコルで利用可能な最高のビデオをダウンロードする
$ yt-dlp -f "(bv*+ba/b)[protocol^=http][protocol!*=dash] / (bv*+ba/b)"

# 最高のプロトコルで利用可能な最高のビデオをダウンロードする
# （https/ftps > http/ftp > m3u8_native > m3u8 > http_dash_segments ...）
$ yt-dlp -S "proto"



# h264またはh265コーデックの最高のビデオをダウンロードする、
# またはそのようなビデオがない場合は最高のビデオをダウンロードする
$ yt-dlp -f "(bv*[vcodec~='^((he|a)vc|h26[45])']+ba) / (bv*+ba/b)"

# 最高のコーデックを持つ最高のビデオを、しかしh264より良くないものをダウンロードする、
# またはそのようなビデオがない場合は最低のコーデックを持つ最高のビデオをダウンロードする
$ yt-dlp -S "codec:h264"

# 最低のコーデックを持つ最高のビデオを、しかしh264より悪くないものをダウンロードする、
# またはそのようなビデオがない場合は最高のコーデックを持つ最高のビデオをダウンロードする
$ yt-dlp -S "+codec:h264"



# より複雑な例

# 720pより良くなく、フレームレートが30より大きいものを優先する最高のビデオをダウンロードする、
# またはそのようなビデオがない場合は（それでもフレームレートが30より大きいものを優先する）最低品質のビデオをダウンロードする
$ yt-dlp -f "((bv*[fps>30]/bv*)[height<=720]/(wv*[fps>30]/wv*)) + ba / (b[fps>30]/b)[height<=720]/(w[fps>30]/w)"

# 解像度が最大で720pより良くないビデオをダウンロードする、
# またはそのようなビデオがない場合は利用可能な解像度が最も小さいビデオをダウンロードする、
# 同じ解像度のフォーマットではより大きなフレームレートを優先する
$ yt-dlp -S "res:720,fps"



# 解像度が最小で480pより悪くないビデオをダウンロードする、
# またはそのようなビデオがない場合は利用可能な解像度が最大のビデオをダウンロードする、
# 同じ解像度ではより良いコーデック、そしてより大きな総ビットレートを優先する
$ yt-dlp -S "+res:480,codec,br"
```

# メタデータの変更

エクストラクタによって取得されたメタデータは、`--parse-metadata`と`--replace-in-metadata`を使用して変更できます。

`--replace-in-metadata FIELDS REGEX REPLACE`は、任意のメタデータフィールドのテキストを[Pythonの正規表現](https://docs.python.org/3/library/re.html#regular-expression-syntax)を使用して置換するために使用されます。高度な使用法のために、置換文字列で[後方参照](https://docs.python.org/3/library/re.html?highlight=backreferences#re.sub)を使用できます。

`--parse-metadata FROM:TO`の一般的な構文は、データを抽出するフィールドの名前または[出力テンプレート](#output-template)と、それを解釈するフォーマットをコロン`:`で区切って指定します。`TO`には、名前付きキャプチャグループを持つ[Pythonの正規表現](https://docs.python.org/3/library/re.html#regular-expression-syntax)、単一のフィールド名、または[出力テンプレート](#output-template)と同様の構文（`%(field)s`フォーマットのみサポート）を使用できます。このオプションは、様々なフィールドを解析および変更するために複数回使用できます。

これらのオプションは相対的な順序を保持するため、解析されたフィールドで置換を行ったり、その逆を行ったりできることに注意してください。また、このようにして作成されたフィールドは、[出力テンプレート](#output-template)で使用でき、`--embed-metadata`を使用する際に追加されるメディアファイルのメタデータにも影響します。

このオプションには、いくつかの特別な用途もあります：

* 現在ダウンロード中の動画のメタデータに基づいて、追加のURLをダウンロードできます。これを行うには、フィールド`additional_urls`をダウンロードしたいURLに設定します。例：`--parse-metadata "description:(?P<additional_urls>https?://www\.vimeo\.com/\d+)"`は、説明内で最初に見つかったvimeo動画をダウンロードします。

* これを使用して、メディアファイルに埋め込まれるメタデータを変更できます。これを行うには、対応するフィールドの値を`meta_`プレフィックス付きで設定します。例えば、`meta_description`フィールドに設定した値は、ファイルの`description`フィールドに追加されます。これを使用して、異なる「description」と「synopsis」を設定できます。個々のストリームのメタデータを変更するには、`meta<n>_`プレフィックスを使用します（例：`meta1_language`）。`meta_`フィールドに設定された値は、すべてのデフォルト値を上書きします。

**注**: メタデータの変更は、フォーマット選択、抽出後、およびその他のポストプロセッシング操作の前に行われます。これらのステップ中に一部のフィールドが追加または変更され、あなたの変更が上書きされる可能性があります。

参考までに、これらはyt-dlpがデフォルトでファイルメタデータに追加するフィールドです：

メタデータフィールド         | 元のフィールド
:--------------------------|:------------------------------------------------
`title`                    | `track` または `title`
`date`                     | `upload_date`
`description`,  `synopsis` | `description`
`purl`, `comment`          | `webpage_url`
`track`                    | `track_number`
`artist`                   | `artist`, `artists`, `creator`, `creators`, `uploader` または `uploader_id`
`composer`                 | `composer` または `composers`
`genre`                    | `genre` または `genres`
`album`                    | `album`
`album_artist`             | `album_artist` または `album_artists`
`disc`                     | `disc_number`
`show`                     | `series`
`season_number`            | `season_number`
`episode_id`               | `episode` または `episode_id`
`episode_sort`             | `episode_number`
各ストリームの`language`   | フォーマットの`language`

**注**: ファイルフォーマットによっては、これらのフィールドの一部をサポートしていない場合があります。


## メタデータ変更の例

```bash
# タイトルを "アーティスト - タイトル" として解釈する
$ yt-dlp --parse-metadata "title:%(artist)s - %(title)s"

# 正規表現の例
$ yt-dlp --parse-metadata "description:Artist - (?P<artist>.+)"

# タイトルを "シリーズ名 S01E05" として設定する
$ yt-dlp --parse-metadata "%(series)s S%(season_number)02dE%(episode_number)02d:%(title)s"

# 動画メタデータの "artist" フィールドとしてアップローダーを優先する
$ yt-dlp --parse-metadata "%(uploader|)s:%(meta_artist)s" --embed-metadata

# webpage_urlの代わりにdescriptionを使用して動画メタデータの "comment" フィールドを設定し、
# 複数行を正しく処理する
$ yt-dlp --parse-metadata "description:(?s)(?P<meta_comment>.+)" --embed-metadata

# 動画メタデータに "synopsis" を設定しない
$ yt-dlp --parse-metadata ":(?P<meta_synopsis>)"

# infojsonから "formats" フィールドを空文字列に設定して削除する
$ yt-dlp --parse-metadata "video::(?P<formats>)" --write-info-json

# タイトルとアップローダーのすべてのスペースと "_" を `-` に置き換える
$ yt-dlp --replace-in-metadata "title,uploader" "[ _]" "-"

```

# エクストラクタ引数

一部のエクストラクタは、`--extractor-args KEY:ARGS`を使用して渡すことができる追加の引数を受け付けます。`ARGS`は`;`（セミコロン）で区切られた`ARG=VAL1,VAL2`の文字列です。例：`--extractor-args "youtube:player-client=tv,mweb;formats=incomplete" --extractor-args "twitter:api=syndication"`

注：CLIでは、`ARG`は`_`の代わりに`-`を使用できます。例：`youtube:player-client"`は`youtube:player_client"`になります。

以下のエクストラクタがこの機能を使用します：

#### youtube
* `lang`: この言語コード（大文字小文字を区別）の翻訳されたメタデータ（`title`, `description`など）を優先します。デフォルトでは、動画のプライマリ言語のメタデータが優先され、`en`の翻訳にフォールバックします。サポートされているコンテンツ言語コードのリストは、[youtube/_base.py](https://github.com/yt-dlp/yt-dlp/blob/415b4c9f955b1a0391204bd24a7132590e7b3bdb/yt_dlp/extractor/youtube/_base.py#L402-L409)を参照してください。
* `skip`: `hls`、`dash`、または`translated_subs`のいずれかまたは複数を指定して、m3u8マニフェスト、dashマニフェスト、および[自動翻訳字幕](https://github.com/yt-dlp/yt-dlp/issues/4090#issuecomment-1158102032)の抽出をそれぞれスキップします。
* `player_client`: 動画データを抽出するクライアント。現在利用可能なクライアントは`web`, `web_safari`, `web_embedded`, `web_music`, `web_creator`, `mweb`, `ios`, `android`, `android_vr`, `tv`, `tv_simply`, `tv_embedded`です。デフォルトでは`tv_simply,tv,web`が使用されますが、クッキーで認証する場合は`tv,web_safari,web`、プレミアムアカウントでは`tv,web_creator,web`が使用されます。ログインしたクッキーが使用される場合、`music.youtube.com`のURLには`web_music`クライアントが追加されます。年齢制限のある動画には`web_embedded`クライアントが追加されますが、動画が埋め込み可能な場合にのみ機能します。アカウントの年齢確認が必要な場合、年齢制限のある動画には`tv_embedded`と`web_creator`クライアントが追加されます。`web`や`web_music`のような一部のクライアントは、フォーマットをダウンロードするために`po_token`が必要です。`web_creator`のような一部のクライアントは認証でのみ機能します。すべてのクライアントがクッキーによる認証をサポートしているわけではありません。デフォルトのクライアントには`default`を、すべてのクライアントには`all`（非推奨）を使用できます。クライアントの前に`-`を付けると除外できます。例：`youtube:player_client=default,-ios`
* `player_skip`: 堅牢な抽出に通常必要な一部のネットワークリクエストをスキップします。`configs`（クライアント設定をスキップ）、`webpage`（最初のウェブページをスキップ）、`js`（jsプレーヤーをスキップ）、`initial_data`（初期データ/次のエピソードリクエストをスキップ）のいずれかまたは複数。これらのオプションは、必要なリクエストの数を減らしたり、一部のレート制限を回避したりするのに役立ちますが、フォーマットやメタデータが欠落するなどの問題を引き起こす可能性があります。詳細は[#860](https://github.com/yt-dlp/yt-dlp/pull/860)と[#12826](https://github.com/yt-dlp/yt-dlp/issues/12826)を参照してください。
* `webpage_skip`: 埋め込みウェブページデータの抽出をスキップします。`player_response`、`initial_data`のいずれかまたは両方。これらのオプションはテスト目的であり、ネットワークリクエストをスキップしません。
* `player_params`: プレーヤーリクエストに使用するYouTubeプレーヤーパラメータ。yt-dlpによって設定されたデフォルトのものを上書きします。
* `player_js_variant`: 署名とnsigの解読に使用するプレーヤージャバスクリプトのバリアント。既知のバリアントは`main`, `tce`, `tv`, `tv_es6`, `phone`, `tablet`です。デフォルトは`main`で、その他はデバッグ目的です。サイトによって規定されているものを使用するには`actual`を使用できます。
* `comment_sort`: `top`または`new`（デフォルト） - コメントのソートモード（YouTube側）を選択します。
* `max_comments`: 収集するコメントの量を制限します。`max-comments,max-parents,max-replies,max-replies-per-thread`を表す整数のカンマ区切りリスト。デフォルトは`all,all,all,all`です。
    * 例：`all,all,1000,10`は、合計で最大1000件の返信を取得し、スレッドごとに最大10件の返信を取得します。`1000,all,100`は、最大1000件のコメントを取得し、合計で最大100件の返信を取得します。
* `formats`: 返すフォーマットの種類を変更します。`dashy`（HTTPをDASHに変換）、`duplicate`（内容は同じだがURLやプロトコルが異なる。`dashy`を含む）、`incomplete`（完全にダウンロードできない - ライブdashとポストライブm3u8）、`missing_pot`（POトークンが必要だが欠落しているフォーマットを含む）
* `innertube_host`: すべてのAPIリクエストに使用するInnertube APIホスト。例：`studio.youtube.com`, `youtubei.googleapis.com`。あるサブドメインからエクスポートされたクッキーは他のサブドメインでは機能しないことに注意してください。
* `innertube_key`: すべてのAPIリクエストに使用するInnertube APIキー。デフォルトではAPIキーは使用されません。
* `raise_incomplete_data`: `Incomplete Data Received`は警告を報告する代わりにエラーを発生させます。
* `data_sync_id`: Innertube APIリクエストで使用されるアカウントのData Sync IDを上書きします。`youtube:player_skip=webpage,configs`または`youtubetab:skip=webpage`を持つアカウントを使用している場合に必要になることがあります。
* `visitor_data`: Innertube APIリクエストで使用されるVisitor Dataを上書きします。これは`player_skip=webpage,configs`でクッキーなしで使用する必要があります。注：不適切に使用すると悪影響を及ぼす可能性があります。ブラウザからのセッションが必要な場合は、代わりにクッキーを渡す必要があります（これにはVisitor IDが含まれています）。
* `po_token`:  使用するProof of Origin (PO) Token。`CLIENT.CONTEXT+PO_TOKEN`の形式のPOトークンのカンマ区切りリスト。例：`youtube:po_token=web.gvs+XXX,web.player=XXX,web_safari.gvs+YYY`。コンテキストは`gvs`（Google Video Server URL）、`player`（Innertubeプレーヤーリクエスト）、`subs`（字幕）のいずれかです。
* `pot_trace`: POトークン取得のためのデバッグロギングを有効にします。`true`または`false`（デフォルト）のいずれか。
* `fetch_pot`: プロバイダーからPOトークンを取得するためのポリシー。`always`（クライアントが特定のコンテキストでPOトークンを必要とするかどうかにかかわらず、常にPOトークンを取得しようとする）、`never`（POトークンを絶対に取得しない）、または`auto`（デフォルト；クライアントが特定のコンテキストでPOトークンを必要とする場合にのみPOトークンを取得する）のいずれか。
* `playback_wait`: フォーマットが利用可能になることを保証するために、抽出とダウンロードの段階の間に待機する時間（秒）。デフォルトは`6`秒です。

#### youtubepot-webpo
* `bind_to_visitor_id`: WebPOトークンをキャッシュするためにVisitor Dataの代わりにVisitor IDを使用するかどうか。`true`（デフォルト）または`false`のいずれか。

#### youtubetab (YouTubeプレイリスト、チャンネル、フィードなど)
* `skip`: `webpage`（最初のウェブページダウンロードをスキップ）、`authcheck`（最初のウェブページがダウンロードされない場合に認証が必要なプレイリストのダウンロードを許可する。これは望ましくない動作を引き起こす可能性があります。詳細は[#1122](https://github.com/yt-dlp/yt-dlp/pull/1122)を参照）のいずれかまたは複数。
* `approximate_date`: フラットプレイリストで、おおよその`upload_date`と`timestamp`を抽出します。これにより、日付ベースのフィルタが若干ずれる可能性があります。

#### generic
* `fragment_query`: 値が提供されない場合、mpd/m3u8マニフェストURLのクエリをそのフラグメントにパススルーするか、`fragment_query=VALUE`として与えられたクエリ文字列を適用します。ストリームにHLS AES-128キーがある場合、`key_query`エクストラクタ引数が渡されるか、`hls_key`エクストラクタ引数を介して外部キーURIが提供されない限り、クエリパラメータはキーURIにも渡されることに注意してください。ffmpegには適用されません。
* `variant_query`: 値が提供されない場合、マスターm3u8 URLのクエリをそのバリアントプレイリストURLにパススルーするか、`variant_query=VALUE`として与えられたクエリ文字列を適用します。
* `key_query`: 値が提供されない場合、マスターm3u8 URLのクエリをそのHLS AES-128復号化キーURIにパススルーするか、`key_query=VALUE`として与えられたクエリ文字列を適用します。`hls_key`エクストラクタ引数を介してキーURIが提供される場合、これは効果がないことに注意してください。ffmpegには適用されません。
* `hls_key`: HLS AES-128キーURI *または* キー（16進数）、およびオプションでIV（16進数）を`(URI|KEY)[,IV]`の形式で指定します。例：`generic:hls_key=ABCDEF1234567980,0xFEDCBA0987654321`。これらの値のいずれかを渡すと、ネイティブHLSダウンローダーの使用が強制され、m3u8プレイリストで見つかった対応する値が上書きされます。
* `is_live`: ライブHLS検出をバイパスし、手動で`live_status`を設定します - `false`の値は`not_live`を設定し、その他の値（または値なし）は`is_live`を設定します。
* `impersonate`: 最初のウェブページリクエストで偽装を試みるターゲット。例：`generic:impersonate=safari,chrome-110`。利用可能な任意のターゲットを偽装するには`generic:impersonate`を、偽装を無効にするには`generic:impersonate=false`（デフォルト）を使用します。

#### vikichannel
* `video_types`: ダウンロードする動画の種類 - `episodes`, `movies`, `clips`, `trailers`のいずれかまたは複数。

#### youtubewebarchive
* `check_all`: より多くのリクエストを犠牲にして、より多くをチェックしようとします。`thumbnails`, `captures`のいずれかまたは複数。

#### gamejolt
* `comment_sort`: `hot`（デフォルト）、`you`（クッキーが必要）、`top`、`new` - コメントのソートモード（GameJolt側）を選択します。

#### hotstar
* `res`: 無視する解像度 - `sd`, `hd`, `fhd`のいずれかまたは複数。
* `vcodec`: 無視するvcodec - `h264`, `h265`, `dvh265`のいずれかまたは複数。
* `dr`: 無視するダイナミックレンジ - `sdr`, `hdr10`, `dv`のいずれかまたは複数。

#### instagram
* `app_id`: APIリクエストに使用される`X-IG-App-ID`ヘッダーの値。デフォルトはウェブアプリIDの`936619743392459`です。

#### niconicochannelplus
* `max_comments`: 抽出するコメントの最大数 - デフォルトは`120`です。

#### tiktok
* `api_hostname`: モバイルAPI呼び出しに使用するホスト名。例：`api22-normal-c-alisg.tiktokv.com`
* `app_name`: モバイルAPI呼び出しで使用するデフォルトのアプリ名。例：`trill`
* `app_version`: モバイルAPI呼び出しで使用するデフォルトのアプリバージョン - `manifest_app_version`と共に設定する必要があります。例：`34.1.2`
* `manifest_app_version`: モバイルAPI呼び出しで使用するデフォルトの数値アプリバージョン。例：`2023401020`
* `aid`: モバイルAPI呼び出しで使用するデフォルトのアプリID。例：`1180`
* `app_info`: `<iid>/[app_name]/[app_version]/[manifest_app_version]/[aid]`の形式の1つ以上のアプリ情報文字列でモバイルAPI抽出を有効にします。ここで`iid`は一意のアプリインストールIDです。`iid`は必須の値であり、他のすべての値とその`/`区切り文字は省略できます。例：`tiktok:app_info=1234567890123456789`または`tiktok:app_info=123,456/trill///1180,789//34.0.1/340001`
* `device_id`: モバイルAPI呼び出しで使用する本物のデバイスIDでモバイルAPI抽出を有効にします。デフォルトはランダムな19桁の文字列です。

#### rokfinchannel
* `tab`: ダウンロードするタブ - `new`, `top`, `videos`, `podcasts`, `streams`, `stacks`のいずれか。

#### twitter
* `api`: ツイート抽出用のAPIとして`graphql`（デフォルト）、`legacy`、または`syndication`のいずれかを選択します。ログインしている場合は効果がありません。

#### stacommu, wrestleuniverse
* `device_id`: ウェブサイトによって割り当てられ、有料ライブストリームコンテンツのデバイス制限を強制するために使用されるUUID値。ブラウザのローカルストレージで見つけることができます。

#### twitch
* `client_id`: GraphQLリクエストと共に送信されるクライアントIDの値。例：`twitch:client_id=kimne78kx3ncx6brgo4mv6wki5h1ko`

#### nhkradirulive (NHK らじる★らじる LIVE)
* `area`: 抽出する地域バリエーション。有効なエリアは`sapporo`, `sendai`, `tokyo`, `nagoya`, `osaka`, `hiroshima`, `matsuyama`, `fukuoka`です。デフォルトは`tokyo`です。

#### nflplusreplay
* `type`: 抽出するゲームリプレイの種類。有効なタイプは`full_game`, `full_game_spanish`, `condensed_game`, `all_22`です。`all`を使用して利用可能なすべてのリプレイタイプを抽出できます。これがデフォルトです。

#### jiocinema
* `refresh_token`: ブラウザのローカルストレージからの`refreshToken` UUIDを渡して、`token`をユーザー名、ブラウザのローカルストレージからの`accessToken`をパスワードとしてログインする際のログインセッションの寿命を延ばすことができます。

#### jiosaavn
* `bitrate`: リクエストするオーディオビットレート。`16`, `32`, `64`, `128`, `320`のいずれかまたは複数。デフォルトは`128,320`です。

#### afreecatvlive
* `cdn`: ストリームURLのAPI呼び出しで使用する1つ以上のCDN ID。例：`gcp_cdn`, `gs_cdn_pc_app`, `gs_cdn_mobile_web`, `gs_cdn_pc_web`

#### soundcloud
* `formats`: APIからリクエストするフォーマット。リクエストする値は`{protocol}_{codec}`の形式である必要があります。例：`hls_opus,http_aac`。`*`文字はワイルドカードとして機能します。例：`*_mp3`、単独で渡してすべてのフォーマットをリクエストすることもできます。既知のプロトコルには`http`, `hls`, `hls-aes`があり、既知のコーデックには`aac`, `opus`, `mp3`があります。オリジナルの`download`フォーマットは常に抽出されます。デフォルトは`http_aac,hls_aac,http_opus,hls_opus,http_mp3,hls_mp3`です。

#### orfon (orf:on)
* `prefer_segments_playlist`: 利用可能な場合、単一の完全なビデオの代わりに番組セグメントのプレイリストを優先します。個々のセグメントが必要な場合は、`--concat-playlist never --extractor-args "orfon:prefer_segments_playlist"`を使用してください。

#### bilibili
* `prefer_multi_flv`: レガシーフォーマットをまだ提供している古い動画に対して、mp4よりもflvフォーマットの抽出を優先します。

#### sonylivseries
* `sort_order`: シリーズ抽出のエピソードのソート順 - `asc`（昇順、古いものが先）または`desc`（降順、新しいものが先）のいずれか。デフォルトは`asc`です。

#### tver
* `backend`: 抽出に使用するバックエンドAPI - `streaks`（デフォルト）または`brightcove`（非推奨）のいずれか。

#### vimeo
* `client`: 動画データを抽出するクライアント。現在利用可能なクライアントは`android`, `ios`, `web`です。1つのクライアントしか使用できません。デフォルトでは`web`クライアントが使用されます。`web`クライアントはアカウントのクッキーまたはログイン認証情報でのみ機能します。`android`および`ios`クライアントは、以前にキャッシュされたOAuthトークンでのみ機能します。
* `original_format_policy`: オリジナルフォーマットの抽出を試みる際のポリシー。`always`, `never`, `auto`のいずれか。デフォルトの`auto`ポリシーは、Vimeoが動画のダウンロード可能性を公表している場合にのみ追加のリクエストを行うことで、WebクライアントのAPIレート制限を超えないようにします。

**注**: これらのオプションは、後方互換性を考慮せずに将来変更/削除される可能性があります。

<!-- MANPAGE: MOVE "INSTALLATION" SECTION HERE -->


# プラグイン

**すべての**プラグインは、呼び出されなくてもインポートされること、およびプラグインコードに対して**チェックは行われない**ことに注意してください。**プラグインは自己責任で使用し、コードを信頼できる場合にのみ使用してください！**

プラグインは`<type>`が`extractor`または`postprocessor`のいずれかです。
- エクストラクタプラグインはCLIから有効にする必要がなく、入力URLがそれに適している場合に自動的に呼び出されます。
- エクストラクタプラグインは、組み込みのエクストラクタよりも優先されます。
- ポストプロセッサプラグインは、`--use-postprocessor NAME`を使用して呼び出すことができます。


プラグインは、名前空間パッケージ`yt_dlp_plugins.extractor`および`yt_dlp_plugins.postprocessor`からロードされます。

言い換えると、ディスク上のファイル構造は次のようになります：

        yt_dlp_plugins/
            extractor/
                myplugin.py
            postprocessor/
                myplugin.py

yt-dlpは、多くの場所（下記参照）でこれらの`yt_dlp_plugins`名前空間フォルダを探し、**すべて**の場所からプラグインをロードします。
プラグインのロードを完全に無効にするには、環境変数`YTDLP_NO_PLUGINS`に空でない値を設定してください。

[既知のプラグインについてはWikiを参照してください](https://github.com/yt-dlp/yt-dlp/wiki/Plugins)

## プラグインのインストール

プラグインは、さまざまな方法と場所を使用してインストールできます。

1. **設定ディレクトリ**:
   プラグインパッケージ（`yt_dlp_plugins`名前空間フォルダを含む）は、以下の標準的な[設定場所](#configuration)に配置できます：
    * **ユーザープラグイン**
      * `${XDG_CONFIG_HOME}/yt-dlp/plugins/<package name>/yt_dlp_plugins/` (Linux/macOSで推奨)
      * `${XDG_CONFIG_HOME}/yt-dlp-plugins/<package name>/yt_dlp_plugins/`
      * `${APPDATA}/yt-dlp/plugins/<package name>/yt_dlp_plugins/` (Windowsで推奨)
      * `${APPDATA}/yt-dlp-plugins/<package name>/yt_dlp_plugins/`
      * `~/.yt-dlp/plugins/<package name>/yt_dlp_plugins/`
      * `~/yt-dlp-plugins/<package name>/yt_dlp_plugins/`
    * **システムプラグイン**
      * `/etc/yt-dlp/plugins/<package name>/yt_dlp_plugins/`
      * `/etc/yt-dlp-plugins/<package name>/yt_dlp_plugins/`
2. **実行ファイルの場所**: プラグインパッケージは、実行ファイルの場所の下にある`yt-dlp-plugins`ディレクトリにも同様にインストールできます（ポータブルインストールに推奨）：
    * バイナリ: `<root-dir>/yt-dlp.exe`がある場合、`<root-dir>/yt-dlp-plugins/<package name>/yt_dlp_plugins/`
    * ソース: `<root-dir>/yt_dlp/__main__.py`がある場合、`<root-dir>/yt-dlp-plugins/<package name>/yt_dlp_plugins/`

3. **pipおよび`PYTHONPATH`内の他の場所**
    * プラグインパッケージは`pip`を使用してインストールおよび管理できます。例については[yt-dlp-sample-plugins](https://github.com/yt-dlp/yt-dlp-sample-plugins)を参照してください。
      * 注：pipでインストールされたプラグインパッケージ間のプラグインファイルは、一意のファイル名を持つ必要があります。
    * `PYTHONPATH`内の任意のパスは、`yt_dlp_plugins`名前空間フォルダについて検索されます。
      * 注：これはPyinstallerビルドには適用されません。


ルートに`yt_dlp_plugins`名前空間フォルダを含む`.zip`、`.egg`、`.whl`アーカイブもプラグインパッケージとしてサポートされています。

* 例：`${XDG_CONFIG_HOME}/yt-dlp/plugins/mypluginpkg.zip`、ここで`mypluginpkg.zip`には`yt_dlp_plugins/<type>/myplugin.py`が含まれています。

プラグインがロードされたかどうかを確認するには、`--verbose`を付けてyt-dlpを実行してください。

## プラグインの開発

テンプレートプラグインパッケージについては[yt-dlp-sample-plugins](https://github.com/yt-dlp/yt-dlp-sample-plugins)リポジトリを、プラグイン開発ガイドについてはWikiの[プラグイン開発](https://github.com/yt-dlp/yt-dlp/wiki/Plugin-Development)セクションを参照してください。

名前が`IE`/`PP`で終わるすべてのパブリッククラスは、それぞれエクストラクタとポストプロセッサのために各ファイルからインポートされます。これはアンダースコアプレフィックス（例：`_MyBasePluginIE`はプライベート）と`__all__`を尊重します。同様に、モジュール名の前にアンダースコアを付けることでモジュールを除外できます（例：`_myplugin.py`）。

既存のエクストラクタをそのサブクラスで置き換えるには、`plugin_name`クラスキーワード引数を設定します（例：`class MyPluginIE(ABuiltInIE, plugin_name='myplugin')`は`ABuiltInIE`を`MyPluginIE`に置き換えます）。エクストラクタは親を置き換えるため、上記の方法のいずれかを使用してサブクラスエクストラクタをプライベートにすることで、個別にインポートされないようにする必要があります。

プラグインの作成者である場合は、見つけやすくするためにリポジトリのトピックに[yt-dlp-plugins](https://github.com/topics/yt-dlp-plugins)を追加してください。

エクストラクタの作成とテストの方法については、[開発者向けの手順](https://github.com/yt-dlp/yt-dlp/blob/master/CONTRIBUTING.md#developer-instructions)を参照してください。

# YT-DLPの埋め込み

yt-dlpは優れたコマンドラインプログラムであることを目指しており、したがってどのプログラミング言語からでも呼び出せるはずです。

あなたのプログラムは、将来のバージョンで変更される可能性があるため、通常の標準出力を解析することを避けるべきです。代わりに、`-J`、`--print`、`--progress-template`、`--exec`などのオプションを使用して、確実に再現および解析できるコンソール出力を作成する必要があります。

Pythonプログラムからは、yt-dlpをより強力な方法で埋め込むことができます。このようになります：

```python
from yt_dlp import YoutubeDL

URLS = ['https://www.youtube.com/watch?v=BaW_jenozKc']
with YoutubeDL() as ydl:
    ydl.download(URLS)
```

おそらく、さまざまなオプションを使用したいと思うでしょう。利用可能なオプションのリストについては、[`yt_dlp/YoutubeDL.py`](yt_dlp/YoutubeDL.py#L183)を参照するか、Pythonシェルで`help(yt_dlp.YoutubeDL)`を実行してください。すでにCLIに精通している場合は、[`devscripts/cli_to_api.py`](https://github.com/yt-dlp/yt-dlp/blob/master/devscripts/cli_to_api.py)を使用して任意のCLIスイッチを`YoutubeDL`のパラメータに変換できます。

**ヒント**: youtube-dlからyt-dlpにコードを移植している場合、注意すべき重要な点は、`YoutubeDL.extract_info`の戻り値がjsonシリアライズ可能であること、あるいは辞書であることさえ保証しないことです。辞書に似ていますが、シリアライズ可能な辞書であることを保証したい場合は、[以下の例](#extracting-information)に示すように`YoutubeDL.sanitize_info`を介して渡してください。

## 埋め込みの例

#### 情報の抽出

```python
import json
import yt_dlp

URL = 'https://www.youtube.com/watch?v=BaW_jenozKc'

# ℹ️ 利用可能なオプションと公開関数のリストについては、help(yt_dlp.YoutubeDL)を参照してください
ydl_opts = {}
with yt_dlp.YoutubeDL(ydl_opts) as ydl:
    info = ydl.extract_info(URL, download=False)

    # ℹ️ ydl.sanitize_infoは情報をjsonシリアライズ可能にします
    print(json.dumps(ydl.sanitize_info(info)))
```
#### info-jsonを使用したダウンロード

```python
import yt_dlp

INFO_FILE = 'path/to/video.info.json'

with yt_dlp.YoutubeDL() as ydl:
    error_code = ydl.download_with_info_file(INFO_FILE)

print('一部の動画のダウンロードに失敗しました' if error_code
      else 'すべての動画が正常にダウンロードされました')
```

#### 音声の抽出

```python
import yt_dlp

URLS = ['https://www.youtube.com/watch?v=BaW_jenozKc']

ydl_opts = {
    'format': 'm4a/bestaudio/best',
    # ℹ️ 利用可能なポストプロセッサとその引数のリストについては、help(yt_dlp.postprocessor)を参照してください
    'postprocessors': [{  # ffmpegを使用して音声を抽出
        'key': 'FFmpegExtractAudio',
        'preferredcodec': 'm4a',
    }]
}

with yt_dlp.YoutubeDL(ydl_opts) as ydl:
    error_code = ydl.download(URLS)
```

#### 動画のフィルタリング

```python
import yt_dlp

URLS = ['https://www.youtube.com/watch?v=BaW_jenozKc']

def longer_than_a_minute(info, *, incomplete):
    """1分より長い動画のみをダウンロード（または長さが不明な場合）"""
    duration = info.get('duration')
    if duration and duration < 60:
        return '動画が短すぎます'

ydl_opts = {
    'match_filter': longer_than_a_minute,
}

with yt_dlp.YoutubeDL(ydl_opts) as ydl:
    error_code = ydl.download(URLS)
```

#### ロガーとプログレスフックの追加

```python
import yt_dlp

URLS = ['https://www.youtube.com/watch?v=BaW_jenozKc']

class MyLogger:
    def debug(self, msg):
        # youtube-dlとの互換性のため、debugとinfoの両方がdebugに渡されます
        # '[debug] 'プレフィックスで区別できます
        if msg.startswith('[debug] '):
            pass
        else:
            self.info(msg)

    def info(self, msg):
        pass

    def warning(self, msg):
        pass

    def error(self, msg):
        print(msg)


# ℹ️ help(yt_dlp.YoutubeDL)の "progress_hooks" を参照してください
def my_hook(d):
    if d['status'] == 'finished':
        print('ダウンロード完了、ポストプロセッシング中...')


ydl_opts = {
    'logger': MyLogger(),
    'progress_hooks': [my_hook],
}

with yt_dlp.YoutubeDL(ydl_opts) as ydl:
    ydl.download(URLS)
```

#### カスタムポストプロセッサの追加

```python
import yt_dlp

URLS = ['https://www.youtube.com/watch?v=BaW_jenozKc']

# ℹ️ help(yt_dlp.postprocessor.PostProcessor)を参照してください
class MyCustomPP(yt_dlp.postprocessor.PostProcessor):
    def run(self, info):
        self.to_screen('何か処理をしています')
        return [], info


with yt_dlp.YoutubeDL() as ydl:
    # ℹ️ "when"はyt_dlp.utils.POSTPROCESS_WHENの任意の値を取ることができます
    ydl.add_post_processor(MyCustomPP(), when='pre_process')
    ydl.download(URLS)
```


#### カスタムフォーマットセレクタの使用

```python
import yt_dlp

URLS = ['https://www.youtube.com/watch?v=BaW_jenozKc']

def format_selector(ctx):
    """ mkvにならない最高のビデオと最高のオーディオを選択します。
    注: これは単なる例であり、すべてのケースを処理するわけではありません """

    # フォーマットはすでに悪いものから良いものへソートされています
    formats = ctx.get('formats')[::-1]

    # acodec='none'はオーディオがないことを意味します
    best_video = next(f for f in formats
                      if f['vcodec'] != 'none' and f['acodec'] == 'none')

    # 互換性のあるオーディオ拡張子を見つけます
    audio_ext = {'mp4': 'm4a', 'webm': 'webm'}[best_video['ext']]
    # vcodec='none'はビデオがないことを意味します
    best_audio = next(f for f in formats if (
        f['acodec'] != 'none' and f['vcodec'] == 'none' and f['ext'] == audio_ext))

    # これらはマージされたフォーマットに必要な最小限のフィールドです
    yield {
        'format_id': f'{best_video["format_id"]}+{best_audio["format_id"]}',
        'ext': best_video['ext'],
        'requested_formats': [best_video, best_audio],
        # プロトコルの+区切りリストである必要があります
        'protocol': f'{best_video["protocol"]}+{best_audio["protocol"]}'
    }


ydl_opts = {
    'format': format_selector,
}

with yt_dlp.YoutubeDL(ydl_opts) as ydl:
    ydl.download(URLS)
```


# YOUTUBE-DLからの変更点

### 新機能

* [**yt-dlc@f9401f2**](https://github.com/blackjack4494/yt-dlc/commit/f9401f2a91987068139c5f757b12fc711d4c0cee)からフォークし、[**youtube-dl@a08f2b7**](https://github.com/ytdl-org/youtube-dl/commit/a08f2b7e4567cdc50c0614ee0a4ffdff49b8b6e6)とマージしました（[例外あり](https://github.com/yt-dlp/yt-dlp/issues/21)）

* **[SponsorBlock連携](#sponsorblock-options)**: [SponsorBlock](https://sponsor.ajay.app) APIを利用して、YouTube動画のスポンサーセクションをマーク/削除できます

* **[フォーマットのソート](#sorting-formats)**: デフォルトのフォーマットソートオプションが変更され、単にビットレートが大きいだけでなく、より高い解像度とより良いコーデックが優先されるようになりました。さらに、`-S`でソート順を指定できるようになりました。これにより、単に`--format`を使用するよりもはるかに簡単なフォーマット選択が可能になります（[例](#format-selection-examples)）

* **animelover1984/youtube-dlとのマージ**: `--write-comments`、`BiliBiliSearch`、`BilibiliChannel`、mp4/ogg/opusへのサムネイル埋め込み、プレイリストのinfojsonなど、[animelover1984/youtube-dl](https://github.com/animelover1984/youtube-dl)のほとんどの機能と改善点が得られます。詳細は[#31](https://github.com/yt-dlp/yt-dlp/pull/31)を参照してください。

* **YouTubeの改善**:
    * クリップ、ストーリー（`ytstories:<channel UCID>`）、検索（フィルタ含む）**\***、YouTube Music検索、チャンネル固有検索、検索プレフィックス（`ytsearch:`, `ytsearchdate:`）**\***、ミックス、フィード（`:ytfav`, `:ytwatchlater`, `:ytsubs`, `:ythistory`, `:ytrec`, `:ytnotif`）をサポート
    * [n-sigベースのスロットリング](https://github.com/ytdl-org/youtube-dl/issues/29326)の修正**\***
    * `--live-from-start`を使用してライブストリームを最初からダウンロード（*実験的*）
    * チャンネルURLは、ショート動画やライブを含む、チャンネルのすべてのアップロードをダウンロードします
    * [OAuthでのログイン](https://github.com/yt-dlp/yt-dlp/wiki/Extractors#logging-in-with-oauth)のサポート

* **ブラウザからのクッキー**: `--cookies-from-browser BROWSER[+KEYRING][:PROFILE][::CONTAINER]`を使用して、すべての主要なWebブラウザからクッキーを自動的に抽出できます

* **時間範囲指定ダウンロード**: `--download-sections`を使用して、タイムスタンプまたはチャプターに基づいて動画を部分的にダウンロードできます

* **チャプターによる動画分割**: `--split-chapters`を使用して、チャプターに基づいて動画を複数のファイルに分割できます

* **マルチスレッドでのフラグメントダウンロード**: m3u8/mpd動画の複数のフラグメントを並行してダウンロードします。使用するスレッド数を設定するには、`--concurrent-fragments`（`-N`）オプションを使用します

* **Aria2cとHLS/DASH**: DASH(mpd)およびHLS(m3u8)フォーマットの外部ダウンローダーとして`aria2c`を使用できます

* **新規および修正されたエクストラクタ**: 多くの新しいエクストラクタが追加され、既存のものの多くが修正されました。[変更履歴](Changelog.md)または[サポートされているサイトのリスト](supportedsites.md)を参照してください

* **新しいMSO**: Philo, Spectrum, SlingTV, Cablevision, RCNなど

* **マニフェストからの字幕抽出**: ストリーミングメディアマニフェストから字幕を抽出できます。詳細は[commit/be6202f](https://github.com/yt-dlp/yt-dlp/commit/be6202f12b97858b9d716e608394b51065d0419f)を参照してください

* **複数のパスと出力テンプレート**: 異なる種類のファイルに対して、異なる[出力テンプレート](#output-template)とダウンロードパスを指定できます。また、`--paths`（`-P`）を使用して、中間ファイルがダウンロードされる一時的なパスを設定できます

* **ポータブル設定**: 設定ファイルはホームディレクトリとルートディレクトリから自動的にロードされます。詳細は[設定](#configuration)を参照してください

* **出力テンプレートの改善**: 出力テンプレートは、日付時刻フォーマット、数値オフセット、オブジェクト走査などを持つことができるようになりました。詳細は[出力テンプレート](#output-template)を参照してください。`--parse-metadata`と`--replace-in-metadata`の助けを借りて、さらに高度な操作も可能です

* **その他の新オプション**: `--alias`, `--print`, `--concat-playlist`, `--wait-for-video`, `--retry-sleep`, `--sleep-requests`, `--convert-thumbnails`, `--force-download-archive`, `--force-overwrites`, `--break-match-filters`など、多くの新しいオプションが追加されました

* **改善**: `--format`/`--match-filters`での正規表現およびその他の演算子、複数の`--postprocessor-args`および`--downloader-args`、より高速なアーカイブチェック、より多くの[フォーマット選択オプション](#format-selection)、複数ビデオ/オーディオのマージ、複数の`--config-locations`、異なる段階での`--exec`など

* **プラグイン**: エクストラクタとポストプロセッサを外部ファイルからロードできます。詳細は[プラグイン](#plugins)を参照してください

* **自己アップデーター**: `yt-dlp -U`を使用してリリースを更新でき、必要に応じて`--update-to`を使用してダウングレードできます

* **自動ビルド**: [ナイトリー/マスタービルド](#update-channels)は`--update-to nightly`と`--update-to master`で使用できます

変更の完全なリストについては、[変更履歴](Changelog.md)または[コミット](https://github.com/yt-dlp/yt-dlp/commits)を参照してください

**\*** が付いた機能はyoutube-dlにバックポートされています

### デフォルトの挙動の違い

yt-dlpの一部のデフォルトオプションは、youtube-dlやyoutube-dlcとは異なります：

* yt-dlpは[Python 3.9+](## "Windows 8")のみをサポートし、[EOLになると](https://devguide.python.org/versions/#python-release-cycle)、さらに多くのバージョンのサポートを削除します。一方、[youtube-dlはまだPython 2.6+と3.2+をサポートしています](https://github.com/ytdl-org/youtube-dl/issues/30568#issue-1118238743)
* オプション`--auto-number`（`-A`）、`--title`（`-t`）、`--literal`（`-l`）は機能しなくなりました。詳細は[削除されたオプション](#Removed)を参照してください
* `avconv`は`ffmpeg`の代替としてサポートされていません
* yt-dlpは、youtube-dlとは少し異なる場所に設定ファイルを保存します。正しい場所のリストについては[設定](#configuration)を参照してください
* デフォルトの[出力テンプレート](#output-template)は`%(title)s [%(id)s].%(ext)s`です。この変更に特別な理由はありません。これはyt-dlpが公開される前に変更されたものであり、現在`%(title)s-%(id)s.%(ext)s`に戻す計画はありません。代わりに、`--compat-options filename`を使用できます
* デフォルトの[フォーマットソート](#sorting-formats)はyoutube-dlとは異なり、高いビットレートではなく、より高い解像度とより良いコーデックを優先します。`--format-sort`オプションを使用してこれを好みの順序に変更するか、`--compat-options format-sort`を使用してyoutube-dlのソート順を使用できます。古いバージョンのyt-dlpは、より広い互換性のためにVP9を優先していました。そのフォーマットソートの優先順位に戻すには、`--compat-options prefer-vp9-sort`を使用できます。これら2つの互換オプションは一緒に使用できません
* デフォルトのフォーマットセレクタは`bv*+ba/b`です。これは、最高のビデオのみのフォーマットよりも優れた結合ビデオ+オーディオフォーマットが見つかった場合、後者が優先されることを意味します。これを元に戻すには、`-f bv+ba/b`または`--compat-options format-spec`を使用します
* youtube-dlcとは異なり、yt-dlpはデフォルトで複数のオーディオ/ビデオストリームを1つのファイルにマージすることを許可しません（これは`-f bv*+ba`の使用と競合するため）。必要な場合は、この機能を`--audio-multistreams`と`--video-multistreams`を使用して有効にする必要があります。両方を有効にするには`--compat-options multistreams`も使用できます
* `--no-abort-on-error`がデフォルトで有効になっています。エラー時に中止するには、`--abort-on-error`または`--compat-options abort-on-error`を使用します
* サムネイル、説明、infojsonなどのメタデータファイルを書き込む際、同じ情報（利用可能な場合）がプレイリストにも書き込まれます。これらのファイルを書き込まないようにするには、`--no-write-playlist-metafiles`または`--compat-options no-playlist-metafiles`を使用します
* `--add-metadata`は、`--write-info-json`と共に使用すると、メタデータを書き込むのに加えて、`infojson`を`mkv`ファイルに添付します。これを元に戻すには、`--no-embed-info-json`または`--compat-options no-attach-info-json`を使用します
* `--add-metadata`を使用すると、一部のメタデータはyoutube-dlと比較して異なるフィールドに埋め込まれます。最も注目すべきは、`comment`フィールドに`webpage_url`が、`synopsis`フィールドに`description`が含まれることです。これを好みに合わせて変更するには[`--parse-metadata`を使用](#modifying-metadata)するか、`--compat-options embed-metadata`を使用して元に戻すことができます
* `playlist_index`は、`--playlist-reverse`や`--playlist-items`などのオプションと共に使用すると、動作が異なります。詳細は[#302](https://github.com/yt-dlp/yt-dlp/issues/302)を参照してください。以前の動作を維持したい場合は、`--compat-options playlist-index`を使用できます
* `-F`の出力は新しい形式でリストされます。これを元に戻すには、`--compat-options list-formats`を使用します
* ライブチャット（利用可能な場合）は字幕と見なされます。ライブチャットを除くすべての字幕をダウンロードするには、`--sub-langs all,-live_chat`を使用します。また、`--compat-options no-live-chat`を使用して、ライブチャット/弾幕のダウンロードを防ぐこともできます
* YouTubeのチャンネルURLは、チャンネルのすべてのアップロードをダウンロードします。特定のタブの動画のみをダウンロードするには、タブのURLを渡します。チャンネルが要求されたタブを表示しない場合、エラーが発生します。また、ライブ動画がない場合、`/live` URLはチャンネル全体をサイレントにダウンロードする代わりにエラーを発生させます。これらのリダイレクトをすべて元に戻すには、`--compat-options no-youtube-channel-redirect`を使用できます
* 利用できない動画もYouTubeプレイリストにリストされます。これを削除するには、`--compat-options no-youtube-unavailable-videos`を使用します
* YouTubeから抽出されたアップロード日はUTCです。
* ダウンローダーとして`ffmpeg`を使用する場合、可能な限りフォーマットのダウンロードとマージが1つのステップで行われます。これを元に戻すには、`--compat-options no-direct-merge`を使用します
* `mp4`へのサムネイル埋め込みは、可能であればmutagenで行われます。代わりにAtomicParsleyを強制的に使用するには、`--compat-options embed-thumbnail-atomicparsley`を使用します
* ファイル名などの一部の内部メタデータは、デフォルトでinfojsonから削除されます。これを元に戻すには、`--no-clean-infojson`または`--compat-options no-clean-infojson`を使用します
* `--embed-subs`と`--write-subs`を一緒に使用すると、字幕はディスクに書き込まれ、メディアファイルにも埋め込まれます。サブを埋め込んで別のファイルを自動的に削除するには、単に`--embed-subs`を使用できます。詳細は[#630 (comment)](https://github.com/yt-dlp/yt-dlp/issues/630#issuecomment-893659460)を参照してください。これを元に戻すには、`--compat-options no-keep-subs`を使用できます
* `certifi`がインストールされている場合、SSLルート証明書に使用されます。システム証明書（自己署名など）を使用したい場合は、`--compat-options no-certifi`を使用します
* yt-dlpのファイル名の無効な文字のサニタイズは、youtube-dlよりも異なり/賢くなっています。youtube-dlの動作に戻すには、`--compat-options filename-sanitization`を使用できます
* ~~yt-dlpは、可能であれば外部ダウンローダーの出力を標準の進捗出力に解析しようとします（現在実装されているもの：[aria2c](https://github.com/yt-dlp/yt-dlp/issues/5931)）。ダウンローダーの出力をそのまま取得するには、`--compat-options no-external-downloader-progress`を使用できます~~
* 2021.09.01から2023.01.02までのyt-dlpバージョンは、ネストされたプレイリストに`--match-filters`を適用していました。これは[8f18ac](https://github.com/yt-dlp/yt-dlp/commit/8f18aca8717bb0dd49054555af8d386e5eda3a88)の意図しない副作用であり、[d7b460](https://github.com/yt-dlp/yt-dlp/commit/d7b460d0e5fc710950582baed2e3fc616ed98a80)で修正されました。これを元に戻すには、`--compat-options playlist-match-filter`を使用します
* 2021.11.10から2023.06.21までのyt-dlpバージョンは、フラグメント化/マニフェストフォーマットの`filesize_approx`値を推定していました。これは[f2fe69](https://github.com/yt-dlp/yt-dlp/commit/f2fe69c7b0d208bdb1f6292b4ae92bc1e1a7444a)で利便性のために追加されましたが、推定値の潜在的な極端な不正確さのために[0dff8e](https://github.com/yt-dlp/yt-dlp/commit/0dff8e4d1e6e9fb938f4256ea9af7d81f42fd54f)で元に戻されました。推定値の抽出を続けるには、`--compat-options manifest-filesize-approx`を使用します
* yt-dlpは`requests`などの最新のhttpクライアントバックエンドを使用します。標準のhttpリクエストにレガシーhttpハンドラ（`urllib`）を優先して使用するには、`--compat-options prefer-legacy-http-handler`を使用します。
* サブモジュール`swfinterp`、`casefold`は削除されました。
* `--simulate`を渡すこと（または`download=False`で`extract_info`を呼び出すこと）は、デフォルトのフォーマット選択を変更しなくなりました。詳細は[#9843](https://github.com/yt-dlp/yt-dlp/issues/9843)を参照してください。
* yt-dlpは、デフォルトでサーバーの変更時刻をダウンロードしたファイルに適用しなくなりました。これを元に戻すには、`--mtime`または`--compat-options mtime-by-default`を使用します。

使いやすさのために、さらにいくつかの互換オプションが利用可能です：

* `--compat-options all`: すべての互換オプションを使用します（**使用しないでください！**）
* `--compat-options youtube-dl`: `--compat-options all,-multistreams,-playlist-match-filter,-manifest-filesize-approx,-allow-unsafe-ext,-prefer-vp9-sort`と同じです
* `--compat-options youtube-dlc`: `--compat-options all,-no-live-chat,-no-youtube-channel-redirect,-playlist-match-filter,-manifest-filesize-approx,-allow-unsafe-ext,-prefer-vp9-sort`と同じです
* `--compat-options 2021`: `--compat-options 2022,no-certifi,filename-sanitization`と同じです
* `--compat-options 2022`: `--compat-options 2023,playlist-match-filter,no-external-downloader-progress,prefer-legacy-http-handler,manifest-filesize-approx`と同じです
* `--compat-options 2023`: `--compat-options 2024,prefer-vp9-sort`と同じです
* `--compat-options 2024`: `--compat-options mtime-by-default`と同じです。これを使用して、将来のすべての互換オプションを有効にします

以下の互換オプションは、セキュリティパッチ以前の脆弱な動作を復元します：

* `--compat-options allow-unsafe-ext`: 任意の拡張子（安全でないものを含む）のファイルのダウンロードを許可します（[GHSA-79w7-vh3h-8g4j](<https://github.com/yt-dlp/yt-dlp/security/advisories/GHSA-79w7-vh3h-8g4j>))

    > :warning: 拡張子が一般的でないと検出されたために有効なファイルのダウンロードが拒否された場合にのみ使用してください
    >
    > **このオプションはリモートコード実行を可能にする可能性があります！代わりに[Issueを立てる](<https://github.com/yt-dlp/yt-dlp/issues/new/choose>)ことを検討してください！**

### 非推奨のオプション

これらはすべての非推奨のオプションと、同じ効果を達成するための現在の代替手段です

#### ほぼ冗長なオプション
これらのオプションは新しい counterparts とほぼ同じですが、冗長になるのを防ぐいくつかの違いがあります

    -j, --dump-json                  --print "%()j"
    -F, --list-formats               --print formats_table
    --list-thumbnails                --print thumbnails_table --print playlist:thumbnails_table
    --list-subs                      --print automatic_captions_table --print subtitles_table

#### 冗長なオプション
これらのオプションは冗長ですが、使いやすさからまだ使用されることが期待されています

    --get-description                --print description
    --get-duration                   --print duration_string
    --get-filename                   --print filename
    --get-format                     --print format
    --get-id                         --print id
    --get-thumbnail                  --print thumbnail
    -e, --get-title                  --print title
    -g, --get-url                    --print urls
    --match-title REGEX              --match-filters "title ~= (?i)REGEX"
    --reject-title REGEX             --match-filters "title !~= (?i)REGEX"
    --min-views COUNT                --match-filters "view_count >=? COUNT"
    --max-views COUNT                --match-filters "view_count <=? COUNT"
    --break-on-reject                --break-match-filtersを使用
    --user-agent UA                  --add-headers "User-Agent:UA"
    --referer URL                    --add-headers "Referer:URL"
    --playlist-start NUMBER          -I NUMBER:
    --playlist-end NUMBER            -I :NUMBER
    --playlist-reverse               -I ::-1
    --no-playlist-reverse            デフォルト
    --no-colors                      --color no_color

#### 非推奨
これらのオプションはまだ機能しますが、同じことを達成するための他の代替手段があるため、使用は推奨されません

    --force-generic-extractor        --ies generic,default
    --exec-before-download CMD       --exec "before_dl:CMD"
    --no-exec-before-download        --no-exec
    --all-formats                    -f all
    --all-subs                       --sub-langs all --write-subs
    --print-json                     -j --no-simulate
    --autonumber-size NUMBER         文字列フォーマットを使用、例：%(autonumber)03d
    --autonumber-start NUMBER        %(autonumber+NUMBER)sのような内部フィールドフォーマットを使用
    --id                             -o "%(id)s.%(ext)s"
    --metadata-from-title FORMAT     --parse-metadata "%(title)s:FORMAT"
    --hls-prefer-native              --downloader "m3u8:native"
    --hls-prefer-ffmpeg              --downloader "m3u8:ffmpeg"
    --list-formats-old               --compat-options list-formats (エイリアス: --no-list-formats-as-table)
    --list-formats-as-table          --compat-options -list-formats [デフォルト] (エイリアス: --no-list-formats-old)
    --youtube-skip-dash-manifest     --extractor-args "youtube:skip=dash" (エイリアス: --no-youtube-include-dash-manifest)
    --youtube-skip-hls-manifest      --extractor-args "youtube:skip=hls" (エイリアス: --no-youtube-include-hls-manifest)
    --youtube-include-dash-manifest  デフォルト (エイリアス: --no-youtube-skip-dash-manifest)
    --youtube-include-hls-manifest   デフォルト (エイリアス: --no-youtube-skip-hls-manifest)
    --geo-bypass                     --xff "default"
    --no-geo-bypass                  --xff "never"
    --geo-bypass-country CODE        --xff CODE
    --geo-bypass-ip-block IP_BLOCK   --xff IP_BLOCK

#### 開発者オプション
これらのオプションはエンドユーザーが使用することを意図していません

    --test                           エクストラクタのテストのためにビデオの一部のみをダウンロード
    --load-pages                     --write-pagesでダンプされたページをロード
    --youtube-print-sig-code         youtubeの署名のテスト用
    --allow-unplayable-formats       再生不可能なフォーマットもリストする
    --no-allow-unplayable-formats    デフォルト

#### 古いエイリアス
これらはさまざまな理由で文書化されなくなったエイリアスです

    --avconv-location                --ffmpeg-location
    --clean-infojson                 --clean-info-json
    --cn-verification-proxy URL      --geo-verification-proxy URL
    --dump-headers                   --print-traffic
    --dump-intermediate-pages        --dump-pages
    --force-write-download-archive   --force-write-archive
    --no-clean-infojson              --no-clean-info-json
    --no-split-tracks                --no-split-chapters
    --no-write-srt                   --no-write-subs
    --prefer-unsecure                --prefer-insecure
    --rate-limit RATE                --limit-rate RATE
    --split-tracks                   --split-chapters
    --srt-lang LANGS                 --sub-langs LANGS
    --trim-file-names LENGTH         --trim-filenames LENGTH
    --write-srt                      --write-subs
    --yes-overwrites                 --force-overwrites

#### Sponskrubオプション
[SponSkrub](https://github.com/faissaloo/SponSkrub)のサポートは、`--sponsorblock`オプションを優先して非推奨になりました

    --sponskrub                      --sponsorblock-mark all
    --no-sponskrub                   --no-sponsorblock
    --sponskrub-cut                  --sponsorblock-remove all
    --no-sponskrub-cut               --sponsorblock-remove -all
    --sponskrub-force                該当なし
    --no-sponskrub-force             該当なし
    --sponskrub-location             該当なし
    --sponskrub-args                 該当なし

#### サポート終了
これらのオプションは意図したとおりに機能しなくなる可能性があります

    --prefer-avconv                  avconvはyt-dlpによって公式にサポートされていません (エイリアス: --no-prefer-ffmpeg)
    --prefer-ffmpeg                  デフォルト (エイリアス: --no-prefer-avconv)
    -C, --call-home                  実装されていません
    --no-call-home                   デフォルト
    --include-ads                    サポート終了
    --no-include-ads                 デフォルト
    --write-annotations              現在アノテーションを持つサポートサイトはありません
    --no-write-annotations           デフォルト
    --compat-options seperate-video-versions  不要になりました
    --compat-options no-youtube-prefer-utc-upload-date  サポート終了

#### 削除済み
これらのオプションは2014年から非推奨となり、完全に削除されました

    -A, --auto-number                -o "%(autonumber)s-%(id)s.%(ext)s"
    -t, -l, --title, --literal       -o "%(title)s-%(id)s.%(ext)s"


# 貢献する
[Issueの作成](CONTRIBUTING.md#opening-an-issue)および[プロジェクトへのコードの貢献](CONTRIBUTING.md#developer-instructions)の手順については、[CONTRIBUTING.md](CONTRIBUTING.md#contributing-to-yt-dlp)を参照してください。

# WIKI
詳細については[Wiki](https://github.com/yt-dlp/yt-dlp/wiki)を参照してください。
