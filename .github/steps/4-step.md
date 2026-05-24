## Step 4: Plan Agent でテストを追加する

_実装だけでなく、テストも Copilot と一緒に整えます。_

このステップでは Copilot の **Plan Agent** を使い、FastAPI のバックエンドテストを追加します。

### 作業 1: Plan Agent を選ぶ

Copilot Chat のモード選択から **Plan** を選びます。

![Plan mode dropdown](https://raw.githubusercontent.com/tsato-cnlab/skills-getting-started-with-github-copilot/main/.github/images/plan-mode-dropdown.png)

### 作業 2: テスト追加の計画を作る

Plan Agent に次のように依頼します。

```text
別の tests ディレクトリに、バックエンドの FastAPI テストを追加したいです。
```

計画が表示されたら内容を読み、必要なら次の条件も伝えます。

```text
テストは AAA（Arrange-Act-Assert）パターンで構成しましょう。
```

```text
`pytest` を使い、`requirements.txt` にも追加してください。
```

### 作業 3: 実装を開始する

計画に問題がなければ、実装を開始します。

![Plan mode start implementation](https://raw.githubusercontent.com/tsato-cnlab/skills-getting-started-with-github-copilot/main/.github/images/plan-mode-start-implementation.png)

Copilot が追加する `tests` ディレクトリ、テストファイル、`requirements.txt` の変更を確認します。

### 作業 4: テストを実行する

ターミナルで依存関係を入れ直し、テストを実行します。

```bash
pip install -r requirements.txt
pytest
```

失敗した場合は、エラー内容を Copilot Chat に貼り付けて修正を相談します。

### 作業 5: commit して push する

`tests` ディレクトリと `requirements.txt` の変更を commit し、`accelerate-with-copilot` ブランチへ push してください。

### 完了条件

`requirements.txt` に `pytest` があり、`tests` ディレクトリが追加されていると、次のステップが投稿されます。
