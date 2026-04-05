## 具体的なシステム開発で利用するシチュエーション

実務では以下のような場面で標準出力が頻繁に利用されます。

- **API通信のデバッグ**
    - リクエストパラメータ、レスポンスデータの内容確認
- **ユーザー操作に対するイベント確認**
    - クリック、入力、スクロールなどのイベント発火確認
- **状態管理の検証**
    - React / Vue などで state（状態）の変化を追跡
- **非同期処理（Promise・async/await）の挙動確認**
    - 処理順・成功失敗の確認
- **本番障害調査用のログ出力**
    - 例：異常値・例外発生時の記録

---

## 3. 具体例（基本〜実務想定）

### 3-1. 基本的な標準出力

```jsx
const userName = "Taro";
const age = 25;

console.log(userName);
console.log(age);

```

---

### 3-2. オブジェクト・配列の出力

```jsx
const user = {
  id: 1,
  name: "Taro",
  email: "taro@example.com"
};

console.log(user);

```

---

### 3-3. APIレスポンスの確認

```jsx
fetch("/api/users")
  .then(res => res.json())
  .then(data => {
    console.log("APIレスポンス:", data);
  });

```

---

### 3-4. 出力レベルの使い分け

console.info("処理開始");
console.warn("この値は想定外です");
console.error("致命的なエラーが発生しました");
console.debug("デバッグ用の詳細情報");

---