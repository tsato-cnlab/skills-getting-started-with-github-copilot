## Step 3: Agent Mode で UI を改善する

_アクティビティカードに参加者一覧と登録解除ボタンを追加します。_

このステップでは Copilot の **Agent Mode** を使い、`src/static/app.js` と `src/static/styles.css` を変更します。

### 作業 1: Agent Mode を選ぶ

Copilot Chat のモード選択から **Agent** を選びます。

![Agent mode dropdown](https://raw.githubusercontent.com/tsato-cnlab/skills-getting-started-with-github-copilot/main/.github/images/agent-mode-dropdown.png)

必要に応じて、対象ファイルをコンテキストへ追加します。

![Files added to context](https://raw.githubusercontent.com/tsato-cnlab/skills-getting-started-with-github-copilot/main/.github/images/files-added-to-context.png)

### 作業 2: 参加者一覧を追加する

Agent Mode に次のように依頼します。

```text
Copilot、アクティビティカードを編集して参加者セクションを追加してください。
そのアクティビティにすでに登録している参加者を箇条書きで表示してください。
見た目もきれいにしてください。
```

Copilot が提案した変更を確認し、`app.js` と `styles.css` の変更を受け入れます。

![Activity card with participants](https://raw.githubusercontent.com/tsato-cnlab/skills-getting-started-with-github-copilot/main/.github/images/activity-card-with-participants.png)

### 作業 3: 登録解除ボタンを追加する

続けて、次のように依頼します。

```text
#codebase 各参加者の横に削除アイコンを追加し、箇条書きの点は非表示にしてください。
クリックされたら、その参加者をアクティビティから登録解除するようにしてください。
```

提案された差分を確認し、必要に応じて修正して受け入れます。

### 作業 4: 画面更新のバグを直す

参加登録や登録解除の直後に画面が更新されない場合は、Copilot に次のように伝えます。

```text
バグらしき挙動に気づきました。
参加者を登録したあと、アクティビティ上の変更を見るにはページを更新しなければなりません。
```

アプリを再起動し、参加者一覧と登録解除ボタンが期待どおりに動くことを確認します。

### 作業 5: commit して push する

`src/static/app.js` と `src/static/styles.css` の変更を commit し、`accelerate-with-copilot` ブランチへ push してください。

### 完了条件

`src/static/app.js` と `src/static/styles.css` の変更が push されると、次のステップが投稿されます。
