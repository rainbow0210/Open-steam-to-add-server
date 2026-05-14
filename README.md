# Website_Open-steam-to-add-server

# Japanese
## 概要
Steam のカスタムプロトコルを利用して、指定したゲームサーバーへ接続を試みるための静的 HTML ページです。ブラウザでこのページを開くと、`steam://connect/<server_address>` へ遷移し、Steam クライアント側でサーバー接続を開始します。

## 使用技術
- 言語: HTML, CSS, JavaScript
- ライブラリ/フレームワーク: なし
- データベース: なし
- その他: Steam クライアント, カスタム URI スキーム

## 使い方
### 前提条件
- Steam クライアントがインストールされていること
- カスタムプロトコルの呼び出しをブラウザが許可していること
- 接続先のサーバーアドレスを把握していること

### インストール方法
```bash
git clone https://github.com/username/project.git
cd project
```

### 基本的な使い方
1. `index.html` をブラウザで開きます。
2. `steam://connect/your_server_address` の `your_server_address` を実際の接続先に置き換えます。
3. ページ読み込み時に Steam が起動しない場合は、画面内の「再読み込み」を実行します。

```bash
start index.html
```

## 主な機能
- Steam の接続プロトコルを使ってサーバー接続を起動します。
- 接続に失敗した場合の再読み込みリンクを表示します。
- 最小構成の静的ページとして、そのまま配布できます。

## 設定
接続先は [index.html](index.html) の以下の行で変更します。

```javascript
document.location.href = "steam://connect/your_server_address";
```

`your_server_address` を、実際のサーバーアドレスに置き換えてください。必要に応じて、ポート番号を含めた形式で指定します。

## ライセンス
Unlicense license

# English
## Overview
This is a static HTML page that uses Steam's custom protocol to attempt a connection to a specified game server. When the page is opened in a browser, it redirects to `steam://connect/<server_address>` and starts the server connection through the Steam client.

## Technologies Used
- Language: HTML, CSS, JavaScript
- Library / Framework: None
- Database: None
- Other: Steam client, custom URI scheme

## Usage
### Prerequisites
- Steam client is installed
- The browser allows custom protocol handling
- You know the target server address

### Installation
```bash
git clone https://github.com/username/project.git
cd project
```

### Basic Usage
1. Open `index.html` in a browser.
2. Replace `your_server_address` in `steam://connect/your_server_address` with the actual server address.
3. If Steam does not launch automatically, use the reload link shown on the page.

```bash
start index.html
```

## Main Features
- Starts a Steam server connection through the connection protocol.
- Shows a reload link when the connection fails.
- Can be distributed as a minimal static page.

## Configuration
The connection target is configured in the following line in [index.html](index.html):

```javascript
document.location.href = "steam://connect/your_server_address";
```

Replace `your_server_address` with the actual server address. Include a port number if required.

## License
Unlicense license
