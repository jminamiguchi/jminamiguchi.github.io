# jminamiguchi.github.io

南口誠介の個人ホームページ（https://jminamiguchi.github.io ）のソース．[Academic Pages](https://github.com/academicpages/academicpages.github.io) のテンプレートから作った．`main` に push すると GitHub Pages が Jekyll でビルドして公開する．

## 更新のしかた

| 更新する内容 | 編集するファイル |
|---|---|
| 氏名・所属・サイドバーのリンク | `_config.yml` の `author:` |
| トップページ（自己紹介・研究内容） | `_pages/about.md` |
| CV（学歴・受賞など） | `_pages/cv.md` |
| 論文 | `_publications/` に1本1ファイル |
| 講演 | `_talks/` に1件1ファイル |
| 上部のメニュー | `_data/navigation.yml` |

論文を足すときは，`_publications/` の既存ファイルを複製して書き換える．`category` は査読付きなら `refereed`，プレプリントなら `preprints`．プレプリントが出版されたら `category` を `refereed` に，`venue` を雑誌名・巻・論文番号に変え，`doiurl` に DOI の URL を足す．

講演を足すときは，`_talks/` の既存ファイルを複製して書き換える．日付が月までしか分からないときは，`date` に月の1日を入れ，`date_label` に表示する文字列（例: `"February 2026"`）を書く．

数式は `$$...$$` で書く（行内でも `$$` を使う）．

顔写真を載せるときは，画像を `images/` に置き，`_config.yml` の `author: avatar:` にファイル名を書く．

## 手元での確認

```bash
bundle install
bundle exec jekyll serve
```

http://localhost:4000 で確認できる．
