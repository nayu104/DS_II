## 🧩 Flutter ⇔ React 対応表（基本）

| Flutter                         | React（JSX）                                                                          | 備考           |
| ------------------------------- | ----------------------------------------------------------------------------------- | ------------ |
| `Scaffold`                      | `<div>`＋CSS layout                                                                  | ページ土台、body扱い |
| `AppBar`                        | `<header>` or `<div>`                                                               | ヘッダーとして自作    |
| `Text()`                        | `<p>`, `<span>`, `<h1>`など                                                           | テキスト要素       |
| `TextField()`                   | `<input type="text" />`                                                             | 入力欄          |
| `ElevatedButton()`              | `<button>`                                                                          | 押すボタン        |
| `Icon()`                        | `<span class="material-icons">home</span>` または `<HomeIcon />`                       | MUI使用も可      |
| `ListView.builder()`            | `array.map(item => <div>{item}</div>)`                                              | リスト表示        |
| `Column()`                      | `<div style={{ display: 'flex', flexDirection: 'column' }}>`                        | 縦並び          |
| `Row()`                         | `<div style={{ display: 'flex' }}>`                                                 | 横並び          |
| `Container()`                   | `<div style={...}>`                                                                 | レイアウト用の箱     |
| `Padding()`                     | `<div style={{ padding: 16 }}>`                                                     | 余白           |
| `Center()`                      | `<div style={{ display: 'flex', justifyContent: 'center', alignItems: 'center' }}>` | 中央寄せ         |
| `GestureDetector(onTap: ...)`   | `<div onClick={...}>...</div>`                                                      | タップ・クリック     |
| `Image.asset()`                 | `<img src="./path/to/image.png" />`                                                 | 画像表示         |
| `Expanded()`                    | `flexGrow: 1` をstyleに追加                                                             | 柔軟な拡大        |
| `SizedBox(height: 10)`          | `<div style={{ height: 10 }}></div>`                                                | 空白スペース       |
| `StatefulWidget` + `setState()` | `useState()` フック                                                                    | 状態管理         |
| `StatelessWidget`               | 普通の関数コンポーネント                                                                        | 状態を持たない      |

---

## 🎨 スタイリング対応

| Flutter                          | React                             |
| -------------------------------- | --------------------------------- |
| `color: Colors.red`              | `style={{ color: 'red' }}`        |
| `padding: EdgeInsets.all(16)`    | `style={{ padding: 16 }}`         |
| `alignment: Alignment.center`    | `display: flex` + `justify/align` |
| `decoration: BoxDecoration(...)` | CSSの `border`, `background`など     |

---

## ⚙ イベント・ロジック対応

| Flutter               | React                                             |
| --------------------- | ------------------------------------------------- |
| `onPressed: () => {}` | `onClick={() => {}}`                              |
| `controller.text`     | `useRef().current.value`（非制御） or `useState()`（制御） |

---

### 🚀 特別編：状態管理（上級者向け）

| Flutter                | React                                     |
| ---------------------- | ----------------------------------------- |
| `Provider`, `Riverpod` | `Context`, `Redux`, `Zustand`, `Recoil`など |

---

### ✍ まとめ：

ReactはFlutterと似てる構造が多く、**レイアウトはCSSで細かく調整**するのがポイント。
Flutterの感覚をそのまま活かせるけど、**装飾・位置調整はJSX+CSSでやる**という意識を持つとすごくスムーズ。
