<div align="center">

<img src="assets/rashnova-banner.png" alt="Rashnova：あなたのノートPCのブラックボックス（Alcyone Secure）" width="100%">

# Rashnova

### 改ざんが分かる、Windows 用アクティビティレコーダー

**PC を預けても、何が行われたかを封印された記録で確かめられます。**

[![Latest release](https://img.shields.io/github/v/release/sathvik-zoldyck/rashnova?style=flat-square&label=release&labelColor=111111&color=F25C05)](https://github.com/sathvik-zoldyck/rashnova/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/sathvik-zoldyck/rashnova/total?style=flat-square&labelColor=111111&color=F25C05)](https://github.com/sathvik-zoldyck/rashnova/releases)
[![Platform](https://img.shields.io/badge/Windows-10%20%7C%2011%20%28x64%29-F25C05?style=flat-square&labelColor=111111)](#requirements)
[![Price](https://img.shields.io/badge/price-free-F25C05?style=flat-square&labelColor=111111)](#download)
[![Licence](https://img.shields.io/badge/licence-proprietary-555555?style=flat-square&labelColor=111111)](LICENSE)

[**ダウンロード**](https://github.com/sathvik-zoldyck/rashnova/releases/latest) ·
[**ウェブサイト**](https://www.alcyonesecure.com) ·
[**既知の制限**](KNOWN_LIMITS.md) ·
[**プライバシー**](#privacy) ·
[**セキュリティ**](SECURITY.md)

</div>

> **言語** &nbsp;·&nbsp; [English](README.md) · [हिन्दी](README.hi.md) · [ಕನ್ನಡ](README.kn.md) · [മലയാളം](README.ml.md) · [Español](README.es.md) · [Français](README.fr.md) · [Deutsch](README.de.md) · [Português](README.pt.md) · **日本語** · [Bahasa Indonesia](README.id.md) · [עברית](README.he.md)

---
> [!NOTE]
> このページは英語からの翻訳です。Rashnova アプリ自体は英語のため、ボタンや画面の名前は英語のまま記載しています。
> このページと[英語版](README.md)の内容が異なる場合は、英語版が優先されます。


Rashnova は、Windows PC が他人の手にある間に何が起きたかを記録します。修理店、IT 部門、あるいは PC を預けたどんな
相手のもとでもです。預ける前に **Repair session** を開始し、PC が戻ってきたら終了します。すると Rashnova が判定（verdict）と
レポートを出します。何が開かれ、コピーされ、名前を変えられ、削除されたか、どのプログラムが実行されたか、どの USB
ドライブが接続されたかが分かります。

各エントリーは直前のエントリーと封印でつながっているため、記録の一部が変更・削除されればそれが分かり、何も記録
できなかった期間もすべて示されます。データはすべてお使いのコンピューター内に保存されます。アカウント不要、クラウドなし、
テレメトリーなし。


> [!NOTE]
> このリポジトリは Rashnova の**リリース**の場です：インストーラー、リリースノート、既知の制限、セキュリティポリシー。
> Rashnova は [Alcyone Secure](https://www.alcyonesecure.com) のプロプライエタリ（独自）ソフトウェアであり、ソースコードは
> ここでは公開していません。


## 目次

- [Rashnova が生まれた理由](#why)
- [できること](#what-it-does)
- [決して記録しないもの](#never)
- [仕組み](#how)
- [ダウンロードとインストール](#download)
- [システム要件](#requirements)
- [プライバシー](#privacy)
- [既知の制限](#limits)
- [アップデート](#updates)
- [サポートとセキュリティ](#support)
- [ライセンス](#licence)

<a name="why"></a>
## Rashnova が生まれた理由

航空機、列車、船にはブラックボックスがあります。しかし手元を離れたコンピューターには何もなく、それを持つ人は中の
すべてにアクセスできます。

そしてそのアクセスは実際に使われています。[University of Guelph の研究者による 2022 年の研究](https://arxiv.org/abs/2211.05824)
（IEEE Symposium on Security and Privacy 2023 で発表）では、ログを有効にしたノート PC を 12 の修理店に一晩預けました。
そのうち 6 店の技術者が中の個人データにアクセスし、2 店はノート PC からデータをコピーしていました。ウイルス対策や
エンドポイントのツールは、これに気づくようには作られていません。その人には鍵そのものが渡されていたのです。

Rashnova は防止策ではありません。証拠です。起きたことを、言い争いではなく確認によって明らかにするためのものです。

> *信頼は大切。証拠はもっと確か。*

<a name="what-it-does"></a>
## できること

<table>
<tr>
<td width="50%" valign="top">

**Repair Mode（修理モード）。** 見守られたセッションです。預ける前に PIN で開始し、PC が戻ったら PIN で終了します。
開かれた・作成された・名前を変えられた・コピーされた・削除されたファイル、起動されたプログラム、実行された PowerShell
コマンド、サインイン、接続された USB ストレージ（書き込まれた各ファイルを含む）を記録します。再起動、シャットダウン、
スリープでセッションが終わることはなく、レポートには各中断とその長さが示されます。

</td>
<td width="50%" valign="top">

<img src="assets/screenshots/session-summary.png" alt="セッションの概要：判定、特に注目すべきイベント、チェーンの検証">

</td>
</tr>
<tr>
<td width="50%" valign="top">

<img src="assets/screenshots/session-explorer.png" alt="セッションエクスプローラー：時間に沿ったすべてのイベント（プログラム別・フォルダー別）">

</td>
<td width="50%" valign="top">

**確かめられる記録。** 各セッションは判定とレポートで終わり、PDF、ウェブページ、スプレッドシートとして保存できます。
セッションエクスプローラーはすべてのイベントを時間に沿って、プログラム別・フォルダー別に表示し、チェーンの検証で記録が
損なわれていないかが分かります。保存するのはコピーで、元の記録は Rashnova の保管場所に残ります。

</td>
</tr>
<tr>
<td width="50%" valign="top">

**週次の Readout。** 1 週間を 1 つの判定に。確認する価値のある事柄は多くても数件だけです。それぞれに
"that was me"（自分だった）または "that wasn't me"（自分ではない）と印を付けます。Rashnova に何が見えて何が見えないかも、
平易な言葉で示します。

</td>
<td width="50%" valign="top">

<img src="assets/screenshots/weekly-readout.png" alt="週次の Readout：その週の判定、確認すべき事柄、日ごとのアクティビティ">

</td>
</tr>
<tr>
<td width="50%" valign="top">

<img src="assets/screenshots/always-on-choice.png" alt="セッション中のみの記録か、常時記録かの選択">

</td>
<td width="50%" valign="top">

**常時記録（always-on）は、選んだ場合のみ。** オンにするまではオフです。取り返しのつかないことや警戒すべきこと
（完全削除、機密に見えるファイル、リムーバブルドライブへの出し入れ）を残し、ご自身のファイルの日常的な利用は残しません。
オフにするのはトレイまたは Settings からワンクリックで、PIN は一切不要です。

</td>
</tr>
<tr>
<td width="50%" valign="top">

**トレイから。** セッションが記録中であることの確認、セッションの終了、ファイル操作を 30 秒間リアルタイムで
確認する（Monitor Now）、最後のレポートを開く、といった操作ができます。

</td>
<td width="50%" valign="top" align="center">

<img src="assets/screenshots/quick-panel.png" alt="Windows のトレイにあるクイックパネル" width="70%">

</td>
</tr>
</table>

<sub>スクリーンショットはサンプルのセッション（架空のユーザー "Riya"）で Rashnova を表示したものです。</sub>

**1.2.0 の新機能：** 家族、友人、同僚に PC を貸すときの Handover Mode（同じ封印済みレポート付き）、USB ストレージのブロック、
Start with Windows。[変更履歴](CHANGELOG.md)をご覧ください。

<a name="never"></a>
## 決して記録しないもの

Rashnova が記録するのは、何かが起きた**という事実**であり、画面に何が映っていたかではありません。次のものは記録しません：

- キー入力
- クリップボードの内容
- 画面（画像としても動画としても）
- カメラやマイク
- 文書、写真、メール、メッセージの中身
- 閲覧したウェブページやその内容

記録するものの中で、知っておいてほしい点が 2 つあります。Repair session 中は PowerShell コマンドが実行時に
記録され、人が起動した各プログラムの完全な起動コマンドラインも記録されます。そのため、リンクから開かれたブラウザーは
そのリンクを示します。

たとえばレポートには、`Bank_Statement_Aug2026.pdf` が `Documents\Finance` から Microsoft Edge によって
15:01:16 に開かれた、と記されます。明細に何が書かれていたかは記されません。

<a name="how"></a>
## 仕組み

1. **インストール。** インストーラーが Rashnova とバックグラウンドのレコーダーをインストールします。
2. **PIN を設定。** PIN はアプリのウィンドウではなく、レコーダーが検証します。
3. **預ける前に：** **Repair Mode > Activate**、続けて PIN を入力。
4. **預ける。** 「できること」に挙げたすべてが、封印された記録に書き込まれます。
5. **戻ってきたら：** **Deactivate**、続けて PIN を入力。判定、レポート、チェーンの検証結果が得られます。

レコーダーは Windows サービスとして動作するため、誰かが Rashnova のウィンドウを開いても開かなくても記録を続け、
再起動後は自動的に再開します。

**各セッションは 4 つの判定のいずれかで終わります：**

| 判定 | 意味 |
| --- | --- |
| **Quiet** | 記録は検証済みで完全であり、重要度の高い出来事はありませんでした。 |
| **Notable** | 重要度が高い（high）または重大（critical）なイベントが少なくとも 1 件あります：読む価値があります。 |
| **Compromised** | Windows が動作している間に Rashnova のレコーダーが停止された、または記録に干渉の形跡があるため、セッション全体を保証できません。再起動、シャットダウン、スリープはその長さとともに表示され、セッションの評価には影響しません。 |
| **Chain broken** | 記録が検証できません。すべてはそのまま表示されますが、未検証として示されます。 |

<a name="download"></a>
## ダウンロードとインストール

| ファイル | 用途 |
| --- | --- |
| **`Rashnova-1.2.1.msi`** | すべての方向け。.NET 10 の専用コピーと一緒に Rashnova をインストールするため、事前に他のものをインストールする必要はありません。 |
| `SHA256SUMS.txt` | 各ファイルの SHA-256。ダウンロードの確認用です。 |

1. [最新リリース](https://github.com/sathvik-zoldyck/rashnova/releases/latest)から `Rashnova-1.2.1.msi` をダウンロードします。ブラウザーが「一般的にダウンロードされていない」ファイルだと表示した場合は **Keep** を選びます（ブラウザーごとの手順は[既知の制限](KNOWN_LIMITS.md)にあります）。
2. **ファイルを確認します**（推奨）。PowerShell で：
   ```powershell
   Get-FileHash "$env:USERPROFILE\Downloads\Rashnova-1.2.1.msi"
   ```
   ハッシュが `SHA256SUMS.txt` およびリリースノートのものと完全に一致する必要があります。
3. 実行します。インストーラーはまだコード署名されていないため、Windows SmartScreen が発行元不明として
   **"Windows protected your PC"** を表示します（[既知の制限](KNOWN_LIMITS.md)を参照）。**More info**、続けて
   **Run anyway** を選びます。
4. [ライセンス条項](https://www.alcyonesecure.com/terms)に同意してインストールし、Rashnova を開きます。
5. PIN を設定し、セッション中のみの記録（既定）のままにするか、常時記録をオンにするかを選びます。


> [!IMPORTANT]
> 忘れた PIN は、私たちを含め誰にも復元できません。安全な場所に書き留めておいてください。
> 常時記録をオフにするのに PIN は一切不要です。


**1.1.0 をお使いですか？** その上に 1.2.1 をインストールしてください。記録、PIN、設定はそのまま残ります。**BlackBox 1.0.1 をお使いでしたか？** Rashnova は BlackBox の新しい名前です。1.2.1 をダウンロードしてインストールしてください。

<a name="requirements"></a>
## システム要件

- Windows 10 または Windows 11、64 ビット（Windows 10 で検証済み）
- ほかには何も不要：Rashnova は Microsoft .NET 10 の専用コピーを同梱しています
- インストールには管理者の承認が必要です（レコーダーが Windows サービスとして動作するため）

<a name="privacy"></a>
## プライバシー

- **ローカルのみ。** 記録はお使いのコンピューターに書き込まれ、保存されます。このバージョンにはアカウントもクラウドもなく、
  Rashnova は利用データを一切送信しません。
- **小さな通信が 2 つだけ。** どちらにも記録の内容は含まれません：新しいバージョンがないかを alcyonesecure.com に
  1 日 1 回確認する通信と、Repair session 中に Microsoft のタイムサーバーで時刻を確認する通信です。
- **記録を読めるのは誰か。** PIN を設定した Windows アカウントと、コンピューターの管理者です。2 つ目のコピーは
  暗号化されており、Rashnova は PIN が確認された後にのみそれを開きます。コンピューターの管理者は、それでも読むことができます。
- **PC を使う人に伝えてください。** 常時記録はコンピューター全体が対象で、Rashnova を一度も開かない人も含まれます。
- **Windows の設定について、はっきりと。** Repair または Handover のセッション中、Rashnova は Windows の PowerShell
  スクリプトログ記録をオンにし、セッション終了時に元の状態に戻します。他の人がオンにした設定をオフにすることはありません。

<a name="limits"></a>
## 既知の制限

事実に基づいて判断していただけるよう、Rashnova にできないことを公開しています。特に重要なもの：

- **コンピューターがオフ、スリープ、再起動中の間は何も記録できません。** セッションは続き、レポートには各中断と
  その長さが示されます。
- **管理者は記録を読めます。** どんなプログラムも、自分のファイルを Windows の管理者から隠すことはできません。
- **インストーラーはまだコード署名されていません。** そのため実行前にブラウザーや Windows SmartScreen が警告することがあります。
- **USB ストレージのブロックは USB ドライブを止めますが、ファイルを移すすべての手段を止めるわけではありません。** スマートフォン、
  コンピューター内蔵の SD カードスロット、ネットワークドライブはブロックされず、すでに接続されているドライブは取り外すまで使えます。

理由と今後の予定を含む完全な一覧（英語）：**[KNOWN_LIMITS.md](KNOWN_LIMITS.md)**

<a name="updates"></a>
## アップデート

Rashnova は 1 日に 1 回 alcyonesecure.com で新しいバージョンを確認し、あればお知らせします。ダウンロードと
インストールはご自身で行います。記録、PIN、設定は保持されます。各バージョンはリリースノートと SHA-256 とともにここで
公開されます。[変更履歴](CHANGELOG.md)をご覧ください。

<a name="support"></a>
## サポートとセキュリティ

- **ヘルプ：** [SUPPORT.md](SUPPORT.md) を参照するか、**support@alcyonesecure.com** までご連絡ください。
- **バグ：** [issue を作成](https://github.com/sathvik-zoldyck/rashnova/issues/new/choose)してください。issue には記録、
  ファイル名、個人的な情報を決して投稿しないでください。
- **セキュリティ上の脆弱性：** 公開の issue は作成しないでください。[SECURITY.md](SECURITY.md) に従ってください。

<a name="licence"></a>
## ライセンス

Rashnova はプロプライエタリソフトウェアで、ご自身が所有する、または監視を許可されたデバイスで無料で使用できます。
[LICENSE](LICENSE) と[利用条件](https://www.alcyonesecure.com/terms)（英語。こちらが正式なものです）をご覧ください。
このリポジトリの文書と画像は © Alcyone Secure です。

---

<div align="center">

<img src="assets/rashnova-icon.png" alt="Rashnova" width="72">

**Alcyone Secure** · インド・ベンガルールで開発 · [alcyonesecure.com](https://www.alcyonesecure.com)

*セキュリティは防止だけではありません。セキュリティとは説明責任です。*

</div>
