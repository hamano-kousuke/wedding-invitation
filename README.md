# 結婚式招待状サイト — 画像の差し替え方法

## 画像URLの変更方法（これだけ覚えてください）

index.html の **冒頭付近** にある `IMAGES` という箇所に、すべての画像URLがまとまっています。

```
const IMAGES = {
  hero: "images/hero.jpg",       ← FVの写真
  groom: "images/groom.jpg",     ← 新郎の写真
  bride: "images/bride.jpg",     ← 新婦の写真
  ...
};
```

### やることは2つだけ：

1. **画像ファイルを `images/` フォルダに入れる**
2. **index.html の IMAGES にファイル名を書く**

例えば、ギャラリーの1枚目に写真を追加したい場合：
- `images/` フォルダに `gallery-01.jpg` を置く
- index.html の `gallery01: "",` を `gallery01: "images/gallery-01.jpg",` に変える

### 現在の画像一覧

| IMAGES内の名前 | 説明 | 状態 |
|---------------|------|------|
| `hero` | FVメインビジュアル | ✅ 設定済み |
| `groom` | 新郎プロフィール写真 | ✅ 設定済み |
| `bride` | 新婦プロフィール写真 | ✅ 設定済み |
| `okayamaHeader` | 岡山ヘッダー風景写真 | ⬜ 未設定 |
| `okayama01` | 岡山01：育った場所 | ✅ 設定済み |
| `okayama02` | 岡山02：地元らしさ | ✅ 設定済み |
| `okayama03` | 岡山03：お気に入り | ✅ 設定済み |
| `shizuokaHeader` | 静岡ヘッダー風景写真 | ⬜ 未設定 |
| `shizuoka01` | 静岡01：育った場所 | ⬜ 未設定 |
| `shizuoka02` | 静岡02：地元らしさ | ⬜ 未設定 |
| `shizuoka03` | 静岡03：お気に入り | ⬜ 未設定 |
| `shrineMain` | 八坂神社メイン画像 | ✅ 設定済み |
| `shrine01` | 八坂01：素戔嗚尊 | ✅ 設定済み |
| `shrine02` | 八坂02：青龍と龍穴 | ✅ 設定済み |
| `shrine03` | 八坂03：祈りと物語 | ✅ 設定済み |
| `gallery01`〜`04` | 二人のギャラリーサムネイル | ⬜ 未設定 |
| `coco01`〜`04` | ここちゃんギャラリーサムネイル | ⬜ 未設定 |

## Vercelデプロイ手順

1. GitHubで `wedding-invitation` リポジトリを作成
2. このフォルダの中身をすべてアップロード
3. Vercel（vercel.com）でGitHub連携 → Import → Deploy
4. 以降はGitHubでファイルを更新するだけで自動デプロイ
