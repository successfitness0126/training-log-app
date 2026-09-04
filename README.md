# トレーニング記録ツール

筋トレのセッション記録・進捗・1RM推定に加え、VBT(挙上速度)の記録・進捗も管理できるツール。
顧客・種目名・セッション記録はすべて後から編集/削除できる。

- **公開URL**: https://successfitness0126.github.io/training-log-app/
- **リポジトリ**: https://github.com/successfitness0126/training-log-app

## iPhoneでアプリとして使う

1. iPhoneの **Safari** で公開URLを開く(Chrome等は不可)
2. 共有ボタン → 「ホーム画面に追加」

Mac/Windowsのブラウザでも同様に「インストール」してアプリのように使える(PWA対応)。

## データについて

記録データはブラウザの localStorage に保存される(このリポジトリにデータファイルは含まない)。
そのため **端末・ブラウザごとに記録は別々** で、他の端末とは同期されない。

## ファイル構成

```
index.html          アプリ本体(顧客管理・セッション記録・進捗グラフ・VBT機能をすべて含む単一ファイル)
manifest.json        PWA設定(アプリ名・アイコン・テーマカラー)
sw.js                 Service Worker(オフラインキャッシュ)
icons/                アプリアイコン(ダンベルマーク、複数サイズ)
```

## 編集・公開の手順

`index.html` を直接編集し、コミット・pushするだけで GitHub Pages に自動反映される。

```bash
git add -A
git commit -m "変更内容"
git push origin main
```

反映までは通常1分程度(GitHub Pagesのビルド完了を待つ)。
