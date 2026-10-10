# 解説資料

marumie の仕組みを説明するための資料置き場。
ルールや仕様を定める正本ではなく、作成時点のコード（main @ 830f7b57、2026-10-06）を説明した資料である。
コードとの食い違いが見つかったら、実装が正しい。

| ファイル | 内容 | 主な読者 |
|---------|------|---------|
| [code-map.html](code-map.html) | コード逆引き。システム構成図・コンテキストマップ・レイヤー構成・リクエストの流れ・データモデルと、画面ごとに関係ファイルを検索できる機能逆引き | コードを読む人・コントリビューター |
| [code-map-images/](code-map-images/) | code-map.html の構成図と逆引き表を画像にしたもの（10枚） | 同上 |
| [marumie-guide-for-students.html](marumie-guide-for-students.html) | 中学生向けの仕組み解説。アーキテクチャ・データの流れ・調研費の領収書AI・使用ライブラリ | 開発経験のない人 |
| [x-images/](x-images/) | X（旧Twitter）投稿用の紹介画像（1600×900、7枚）。元データは `x-images/source/slides.html` | SNS での紹介 |

HTML はブラウザで直接開ける。外部への依存は Google Fonts の読み込みだけ。

## X 用画像の作り直し方

`x-images/source/slides.html` を編集し、ヘッドレス Chrome で `#1`〜`#7` を 1600×900 で撮影する。

```bash
chrome --headless --hide-scrollbars --window-size=1600,900 --virtual-time-budget=8000 \
  --screenshot=marumie-x-01.png "file://$PWD/docs/materials/x-images/source/slides.html#1"
```

5枚目の「みらい書店」や2枚目の金額など、画像内のデータは架空のもの（画像内にも注記あり）。
