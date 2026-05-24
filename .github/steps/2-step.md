## Step 2: Copilot でバグを直す

_同じ生徒が同じアクティビティに重複登録できる問題を直します。_

このステップでは、Copilot Chat とインライン候補を使って `src/app.py` を改善します。

### 作業 1: バグを説明してもらう

`src/app.py` を開き、Copilot Chat に次のように入力します。

```text
#codebase 生徒が同じアクティビティに 2 回登録できてしまいます。このバグがどこにありそうか探すのを手伝ってください。
```

Copilot の説明を読み、登録処理がどこにあるか確認します。

### 作業 2: 重複登録を防ぐ

`src/app.py` の登録処理付近に、次のコメントを追加します。

```python
# Validate student is not already signed up
```

Copilot のインライン候補が表示されたら、内容を確認して受け入れます。候補が出ない場合は、インラインチャットで「同じ生徒が同じ activity に登録済みならエラーにして」と依頼してください。

### 作業 3: アクティビティを増やす

`activities` の定義を探します。

![Activities dictionary](https://raw.githubusercontent.com/tsato-cnlab/skills-getting-started-with-github-copilot/main/.github/images/activities-dict-highlighted.png)

インラインチャットを開き、次のように依頼します。

```text
この辞書に、スポーツ系のアクティビティを 2 件、芸術系を 2 件、知的活動系を 2 件追加してください。
既存の項目と同じ構造を保ってください。
```

提案された変更を確認し、必要に応じて調整して受け入れます。

### 作業 4: 動作確認して commit する

1. アプリを起動し、同じ生徒が同じアクティビティに二重登録できないことを確認します。
1. 新しいアクティビティが画面に表示されることを確認します。
1. Source Control ビューで変更をステージします。
1. Copilot の **Generate Commit Message** を使うか、自分で commit message を書いて commit します。
1. `accelerate-with-copilot` ブランチへ push します。

### 完了条件

`src/app.py` にアクティビティが追加され、`accelerate-with-copilot` ブランチへ push されると、次のステップが投稿されます。
