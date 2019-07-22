# textlint-rule-ja-official-documents

公用文校正のためのtextlintルール

- 例
    - 「わたし」→「私」
    - 「ご案内」→「御案内」

詳細は、辞書の定義を参照

- [dict/prh.yml](dict/prh.yml)
- [src/dictionary.js](src/dictionary.js)

## インストール
[node.js](https://nodejs.org/ja/download/) の事前インストール。その後、

    npm install --save-dev textlint
    npm install --save-dev textlint-rule-prh
    npm install @textlint-ja/textlint-rule-morpheme-match
    npm install --save-dev yabuuchi-hiroaki/textlint-rule-ja-official-documents

- `.textlintrc`に以下を書きこみ

```json
{
    "rules": {
        "@textlint-ja/morpheme-match": {
            "dictionaryPathList": ["node_modules/textlint-rule-ja-official-documents/src/dictionary.js"]
        },
        "prh": {
          "rulePaths": [
             "node_modules/textlint-rule-ja-official-documents/dict/prh.yml"
          ]
      }
   }
}

```

## 使い方

    npx textlint [Markdownファイルへのpath]

## 参考
- [公用文における漢字使用等について（平成22年内閣訓令第1号）](http://www.bunka.go.jp/kokugo_nihongo/sisaku/joho/joho/kijun/sanko/koyobun/pdf/kunrei.pdf)
- [法令における漢字使用等について（平成22年内閣法制局通知）](https://www.clb.go.jp/info/other/houreiniokerukanji.pdf)
- [公用文作成の要領（昭和27年内閣閣甲第16号）](http://www.bunka.go.jp/kokugo_nihongo/sisaku/joho/joho/kijun/sanko/koyobun/pdf/yoryo_ver02.pdf)
- 文部省用字用語例
- 常用漢字表
- [よくある日本語の誤用をチェックするtextlintルール（Github）](https://github.com/textlint-ja/textlint-rule-ja-no-abusage)

