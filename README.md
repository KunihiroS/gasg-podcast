# GASG Podcast

GASG の音声コンテンツを GitHub Pages でホスティング・公開するリポジトリです。

- 公開URL: https://KunihiroS.github.io/gasg-podcast/
- 各エピソードのプレイヤーを外部サイト（アーカイブサイト等）に `<iframe>` で埋め込んで使います。

---

## エピソードを追加する手順

### 1. MP3 を配置する

`music/` フォルダに MP3 ファイルを追加する。

- ファイル名は連番: `ep01.mp3`, `ep02.mp3`, `ep03.mp3` …
- ファイル名はユーザーに表示されないため、内容を問わず連番で管理する。

### 2. index.html にエピソード情報を追記する

`index.html` の `episodes` 配列に1エントリ追加する：

```js
const episodes = [
  {
    title: 'AI時代の優位性をつくる小さいコミュニティ',  // プレイヤーに表示されるタイトル
    date: '2026-04-16',                                  // 開催日
    track: 'music/ep01.mp3',                             // 配置したファイル名
    subtitle: 'GASG 2025年度活動振り返りと2026年度の展望' // プレイヤーに表示されるサブタイトル
  },
  // 新しいエピソードはここに追加していく
];
```

### 3. git push する

```bash
git add .
git commit -m "Add epNN: （タイトル）"
git push
```

GitHub Pages に自動で反映されます。

### 4. 埋め込みコードを取得する

https://KunihiroS.github.io/gasg-podcast/ を開き、該当エピソードの「埋め込みコードを表示」をクリックしてコードをコピーする。

---

## ファイル構成

| パス | 説明 |
| :--- | :--- |
| `music/epNN.mp3` | 音声ファイル（連番管理） |
| `index.html` | エピソード一覧・埋め込みコード生成ページ |
| `embed-player.html` | `<iframe>` で埋め込むプレイヤー本体 |
