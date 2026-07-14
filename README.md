# poke-langmap

ポケモンWiki（https://wiki.pokemonwiki.com/）の外国語名一覧ページから、ポケモン・とくせい・わざ・アイテムの多言語名対応表をCSVとして抽出するツール。

## 収録データ

| CSV | 内容 | 件数 |
| --- | --- | --- |
| `csv/foreign_names.csv` | ポケモン名 | 1,028件 |
| `csv/ability_foreign_names.csv` | とくせい名 | 306件 |
| `csv/move_foreign_names.csv` | わざ名 | 935件 |
| `csv/item_foreign_names.csv` | アイテム名 | 880件 |

各CSVは日本語・英語・フランス語・ドイツ語・イタリア語・スペイン語・韓国語・中国語(簡体/繁体)の列を持つ（列構成は元ページの表に準拠するため、ファイルによって多少異なる）。

## セットアップ

```bash
pip install -r requirements.txt
```

## 使い方

`html/` 配下に保存済みのポケモンWikiのHTML（4ページ分）を読み込み、`csv/` 配下にCSVを出力する。

```bash
python convert_html_to_csv.py
```

対象ページを更新したい場合は、`html/` 内の該当HTMLファイルを最新のものに差し替えてから再実行する。

## ライセンス

本リポジトリのスクリプトおよび生成されたCSVは [CC BY-NC-SA 4.0](LICENSE) の下で提供される。`html/`・`csv/` 配下のデータはポケモンWikiのコンテンツに由来し、引用元サイトの利用条件にも従うことに注意。
