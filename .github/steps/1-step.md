## Step 1: Copilot にこんにちは

_「このリポジトリは何をするもの？」と聞くところから始めましょう。_

### GitHub Copilot とは

GitHub Copilot は、GitHub が提供する AI 搭載のコーディング支援ツールです。この演習では、次の機能を使います。

| 機能 | できること |
| --- | --- |
| Copilot Chat | コードベースの説明、質問への回答、実装方針の相談 |
| インライン候補 | 入力中のコードやコメントから次のコードを提案 |
| インラインチャット | エディタ内で選択範囲やファイルに対して変更を依頼 |
| Agent Mode | 複数ファイルにまたがる変更を Copilot に実装させる |
| Plan Agent | 実装前に計画を作り、段階的に進める |
| Pull request 連携 | PR の説明作成やレビュー補助 |

> [!IMPORTANT]
> この演習を進めるには、GitHub Copilot が利用できるアカウントが必要です。

### 作業 1: Codespace を開く

1. このリポジトリ上部の **Code** ボタンを押します。
1. **Codespaces** タブを開きます。
1. **Create codespace on main** を選択します。
1. VS Code のブラウザ版が起動するまで待ちます。

### 作業 2: Copilot 拡張機能を確認する

1. 左側の **Extensions** ビューを開きます。
1. `GitHub Copilot` と `GitHub Copilot Chat` が有効になっていることを確認します。
1. `Python` 拡張機能も有効になっていることを確認します。

![GitHub Copilot extension](https://raw.githubusercontent.com/tsato-cnlab/skills-getting-started-with-github-copilot/main/.github/images/copilot-extension-vscode.png)

![Python extension](https://raw.githubusercontent.com/tsato-cnlab/skills-getting-started-with-github-copilot/main/.github/images/python-extension-vscode.png)

### 作業 3: Copilot Chat でプロジェクトを理解する

1. VS Code 左側の Copilot Chat アイコンを開きます。
1. モードが **Ask** になっていることを確認します。

![Ask mode selection](https://raw.githubusercontent.com/tsato-cnlab/skills-getting-started-with-github-copilot/main/.github/images/ask-mode-selection.png)

チャットに次のように入力して、プロジェクトの構造と実行方法を確認します。

```text
このプロジェクトの構成を簡潔に説明してください。
実行するには何をすればよいですか？
```

### 作業 4: アプリを起動する

Copilot の説明に従ってアプリを起動します。通常はターミナルで次を実行します。

```bash
python -m uvicorn src.app:app --reload --host 0.0.0.0 --port 8000
```

ポート `8000` の通知が出たら、ブラウザで開いてアプリを確認します。

![Open in browser icon](https://raw.githubusercontent.com/tsato-cnlab/skills-getting-started-with-github-copilot/main/.github/images/open-in-browser-icon.png)

![Mergington High School webapp](https://raw.githubusercontent.com/tsato-cnlab/skills-getting-started-with-github-copilot/main/.github/images/mergington-high-school-webapp.png)

### 作業 5: ブランチを作成する

次の作業からは `accelerate-with-copilot` ブランチで進めます。ターミナルのインラインチャットを開き、Copilot に次のように依頼してみましょう。

```text
Copilot、"accelerate-with-copilot" という新しい Git ブランチを作成して公開するにはどうすればよいですか？
```

Copilot の提案に従って、ブランチを作成してリモートへ push してください。ブランチ名は必ず `accelerate-with-copilot` にします。

### 完了条件

`accelerate-with-copilot` ブランチを作成して push すると、次のステップが自動で投稿されます。
