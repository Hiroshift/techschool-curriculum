## 今日の学び・気づき（2025/7/7）

- contact-formのborder色がwhiteになっており、デザインが視認しづらかった。
- カリキュラム通りに進めるだけだと“自分が何を作っているのか”が曖昧になりやすいと感じた。細かい部分も「なぜこうするか」を意識して作る重要性を実感。
- contact-form内でname-formやmessage-form、将来的にはmail-form（※Railsならフレームワーク側で管理可能）など複数のユーザー情報を一括管理できる構造になっている。
- display: flexを親要素（contact-form）に指定することで、子要素（name-formやmessage-form）が横並びや中央配置など自由にレイアウトできると理解。
- name-formやmessage-formが左寄せになるのは、親であるcontact-formへのプロパティ設定が足りていないことが原因だった。
- marginは「左右auto」にすると親要素基準で中央に配置でき、上下は任意に調整可能。
