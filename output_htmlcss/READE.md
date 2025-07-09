# `<input>`要素の基本と使い方

`<input>`要素はHTMLのフォームで非常に重要な要素で、多彩な`type`属性を指定してさまざまな入力方法を実現できます。

## 1. `<input>`の記述の流れ

1. `<input>`タグを記述
2. `type`属性を選択し設定
3. `placeholder`属性で仮の文字列を設定
4. `class`属性や`id`属性を設定し、CSSやJavaScriptで制御

## 2. 例：基本的な`<input>`の記述
```html
<input type="text" placeholder="名前を入力" class="my-input" />
```

## 3. よく使われる`type`の値と用途

| 値           | 内容                         | 例・用途                              |
|--------------|------------------------------|-------------------------------------|
| `text`       | 単一行のテキスト入力          | 名前、住所など                        |
| `password`   | パスワード入力               | パスワード入力欄                     |
| `checkbox`   | チェックボックス             | 選択ON/OFF                          |
| `radio`      | ラジオボタン                 | 複数候補から一つ選択                |
| `submit`     | 送信ボタン                   | フォーム送信                        |
| `reset`      | リセットボタン               | 入力内容をリセット                  |
| `email`      | メールアドレス入力            | email専用バリデーションあり       |
| `number`     | 数値入力                     | 数値のみ入力                        |
| `date`       | 日付選択                     | カレンダー入力                     |

## 4. 複合例
```html
<form>
  <input type="text" placeholder="名前" class="name-input" />
  <input type="email" placeholder="メールアドレス" class="email-input" />
  <input type="checkbox" class="subscribe" /> 購読する
  <button type="submit" class="submit-btn">送信</button>
</form>
```

---

## 5. まとめ
- `<input>`タグでさまざまな入力を作成できる
- `type`属性で入力タイプを選ぶ
- `placeholder`で案内や入力例を表示
- `class`や`id`でスタイルや動作を制御

---