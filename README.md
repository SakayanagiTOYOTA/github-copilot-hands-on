# apf-github-copilot-hands-on
AI活用&amp;改善活動「GithubCopilotハンズオン会」用のリポジトリです
## 前提
CCoE提供のGithubおよびGithub Copilot環境を前提として説明します。他の環境の場合は適宜読み替えてください
## 事前準備
### 生成AI免許取得
社内ルールとして「生成AI免許」の取得が必要です。以下教育を受講してください。詳細は[Github Copilot 利用者向けガイド](https://tmc-ccoe.atlassian.net/servicedesk/customer/portal/3/article/230195221)を参照ください。
- [生成AI免許 for コーディング オンライン講座(要予約)](https://torotto-c.mx.toyota.co.jp/ai-education/course_list)
- [生成AI免許試験 for コーディング](https://zamas.dig.toyota/)
### Githubアカウント取得とGithub Copilotの有効化
所属するCCoEプロジェクトの管理者にお願いしてGithubアカウントの作成とGithub Copilotの有効化を依頼してください。
## Quick Start in GitHub Codespaces
[![Open in Github Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/SakayanagiTOYOTA/github-copilot-hands-on?quickstart=1)
* 上記ボタンより新しいCodespacesを作成して下さい。
* 右側の`チャット`ウインドウでGithub Copilotに指示ができます。「このリポジトリについて説明して」と入力してみてください
* [examples/gen_python.py](examples/gen_python.py)を開き、`チャット`ウインドウに「静岡県裾野市の天気を取得するコードを書いて」と入力してみてください
## Quick Start in Visual Studio Code
ソフトウェア開発における生成AI利用ガイドラインの規定により原則として閉環境(VM, devcontainer等)で利用せねばなりません。
### 閉環境としてCodespacesを利用する場合
[Quick start](#quick-start-in-github-codespaces)の手順でCodespaces画面表示後に左下のステータスバーの`><`マークか、左上のメニューの`≡`マークから`Open in VS Code Desktop`を選んでください。Codespacesへリモート接続した状態になります

Codespace上と異なり、Githubに自動ログインされていません。左下の下から3番目のアイコンがGithubの個人アイコンと異なる場合はクリックしてGithubにログインしてください。その後`チャット`ウインドウからGithub Copilotに指示ができます。

### 閉環境としてDevcontainerを利用する場合
ローカルにDevcontainer環境を構築します。社内のWin-PC環境の場合は以下の準備が必要です。
#### 事前準備
- WSL(Windows subsystem for Linux)のインストール
- WSL上にDocker Engineをインストール
#### サンプル実行手順
Win+Rからwslを起動
```cmd
wsl
```
リポジトリをクローン(必要に応じてGithubCLIをインストールし、`gh auth login`を先に実行してgithubにログインしておいてください)
```bash
gh repo clone SakayanagiTOYOTA/github-copilot-hands-on
```
vscode実行
```bash
code github-copilot-hands-on
```
本リポジトリには[devcontainer.json](./devcontainer/devcontainer.json)があるため、VSCode実行時に自動で読み込まれDevcontainerで開きなおすか選択肢が出ます。出ない場合は左下の`><`をクリックし、`コンテナで再度開く`を選択し、左下が`><開発コンテナー`と表示されればOKです。

Githubにログインされていない場合はログインし、`チャット`ウインドウからGithub Copilotに指示してください。