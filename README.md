# textlint-rule-ja-official-documents

公用文校正のためのtextlintルール

- examples
    - 「わたし」→「私」
    - 「ご案内」→「御案内」

詳細は辞書の定義を参照

- [dict/prh.yml](dict/prh.yml)
- [src/dictionary.js](src/dictionary.js)

## Install

Install with [npm](https://www.npmjs.com/):

    npm install --save-dev textlint
    npm install --save-dev textlint-rule-prh
    npm install @textlint-ja/textlint-rule-morpheme-match
    npm install --save-dev yabuuchi-hiroaki/textlint-rule-ja-official-documents

## Usage

Via `.textlintrc`(Recommended)

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

## 参考
- [公用文における漢字使用等について（平成22年内閣訓令第1号）](http://www.bunka.go.jp/kokugo_nihongo/sisaku/joho/joho/kijun/sanko/koyobun/pdf/kunrei.pdf)
- [法令における漢字使用等について（平成22年内閣法制局通知）](https://www.clb.go.jp/info/other/houreiniokerukanji.pdf)


