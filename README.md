# GASG Podcast

GitHub Pages で動くポッドキャスト / 音楽配信プレイヤーです。

## 仕組み

- `music/` フォルダに MP3 を置く
- `embed-player.html` が埋め込み用プレイヤー
- `index.html` でエピソード一覧と埋め込みコードを確認できる

## 使い方

### 1. GitHub Pages を有効化

リポジトリ → Settings → Pages → Source: `main` ブランチ `/root` を選択

### 2. MP3 を追加

`music/` フォルダに MP3 ファイルを追加してプッシュ。

### 3. index.html にエピソードを追加

```js
const episodes = [
  {
    title: 'エピソード1',
    date: '2026-01-01',
    track: 'music/episode1.mp3',
    subtitle: 'GASG Podcast'
  },
  // 追加していく...
];
```

### 4. 埋め込み

`index.html` を開くと各エピソードの埋め込みコードが表示されます。

```html
<iframe src="https://KunihiroS.github.io/gasg-podcast/embed-player.html?track=...&title=..." width="480" height="100" frameborder="0"></iframe>
```
