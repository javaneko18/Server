# マインクラフトサーバーのセットアップ方法

## 必要なもの

* Java 17以上
  * ダウンロードは[ここから](https://adoptium.net/temurin/releases/?version=17)
  * Windowsの場合は「Windows x64 Installer (.msi)」をダウンロード

## サーバーの準備

### 1. PaperMCのダウンロード

1. [PaperMCのダウンロードページ](https://papermc.io/downloads)にアクセス
2. 最新バージョンの「Download」ボタンをクリック
3. ダウンロードしたファイルを「paper.jar」という名前に変更

### 2. サーバーの起動準備

1. ページ右上の[<>Code]をクリックしてDownload ZIPを押してZIPファイルをダウンロード
2. PCのエクスプローラーを開き左側のショートカットからダウンロード(Downloads)フォルダをクリック
3.  ダウンロードしたファイル(Server-main)をクリック
4. 選択すると右上に"すべて展開"と表示されるのでクリック
5. 展開(E)を押してファイルと展開すると自動で中身が開く
6. 開いたらServer-mainをダブルクリックして以下のファイルがあることを確認：
   * start.bat

## サーバーの起動方法

1. 「start.bat」をダブルクリック

### サーバーが起動しない場合

* Javaがインストールされているか確認
* 「paper.jar」の名前が正しいか確認
* すべてのファイルが同じフォルダにあるか確認

### それでも動かない場合

* 誠に質問してください

## 設定の変更方法

* server.properties - サーバーの基本設定
* plugins - プラグインフォルダ
* world - ワールドデータ

詳しい設定方法は各ファイルを開いて確認してください。

# プラグインの導入方法

### プラグインのダウンロード元

* [Spigot](https://www.spigotmc.org/resources/) - 最も一般的なプラグインサイト
* [Modrinth](https://modrinth.com/plugins) - 新しいプラグインサイト
* [Hangar](https://hangar.papermc.io/) - PaperMC公式のプラグインサイト

### インストール手順

1. 使いたいプラグインの.jarファイルをダウンロード
2. サーバーフォルダ内の「plugins」フォルダに入れる
3. サーバーを再起動
4. プラグインの設定は「plugins」フォルダ内に自動生成されます

### おすすめプラグイン

* WorldEdit - 建築支援
* CoreProtect - ログ管理、荒らし対策
* LuckPerms - 権限管理
* EssentialsX - 基本的なコマンド追加

## バックアップの取り方

1. サーバーを停止
2. 以下のフォルダ/ファイルをコピー：
   * world（ワールドデータ）
   * plugins（プラグイン設定）
   * server.properties
   * ops.json（管理者設定）

## よくある質問

### Q: メモリーエラーが出る
A: start.batの`-Xmx4G`の数字を調整してください（PCのメモリに応じて）

### Q: 外部から接続できない
A: 以下を確認：
* ポート開放（25565）の設定
* ファイアウォールの設定
* server.propertiesの`server-ip`設定
