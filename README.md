# 瞑想

チャイム3回で区切る瞑想タイマー。単一HTMLのPWAで、オフラインでも動きます。

https://nabe-chan-1973.github.io/meiso-timer/

## 流れ

スタート →（はじまりまで）→ 🔔 瞑想スタート →（瞑想）→ 🔔 瞑想終了 →（覚醒）→ 🔔 覚醒終了

「はじまりまで」「瞑想」「覚醒」の時間はアプリの中で設定できます。

## 記録

瞑想終了のチャイムで自動保存します。1日1件で、`v` にその日の瞑想の分数が並びます。

```js
{ t: 保存時刻(ms), d: "YYYY-MM-DD", v: [20, 7] }   // この日は2回実践
```

記録画面は [wimhof-breathing の examples/record-screen.html](https://github.com/nabe-chan-1973/wimhof-breathing/blob/main/examples/record-screen.html) をひな形にしています。
URL の末尾に `#demo` を付けると、記録画面に動作確認用のボタンが出ます。

## ファイル

- `index.html` — アプリ本体
- `tingshaLong.mp3` — チャイムの音
- `sw.js` — オフライン用。`index.html` を更新したら `VERSION` を上げる
- `manifest.webmanifest`, `icons/` — ホーム画面に追加したときの名前とアイコン
