# /evt:words コマンド

引数: $ARGUMENTS

## 処理フロー

### 1. words/ ディレクトリから登録済み単語を取得

Grep ツールを使って登録済みの単語を効率的に取得してください:

```
pattern: ^[ \t]*- `[^`]+`
path: words/
glob: *.md
output_mode: content
```

これにより全ファイルを Read せずに、単語行のみを取得できます。

### 2. 引数に応じた処理

#### `$ARGUMENTS` が数字のみの場合

1. 指定された数だけ、以下のリスト (優先度順) から英単語をピックアップしてください。ただし、既に `words/` にリストされている単語は除外すること。
   - NGSL (New General Service List) - 約2,800語で一般英文の約92%をカバー
   - GSL (General Service List) - Michael Westが1953年に作成した古典的リスト約2,000語
   - AWL (Academic Word List) - 学術論文・教科書によく出る570語族
   - COCA頻度リスト - Corpus of Contemporary American Englishに基づく頻度順リスト
   - SVL 12000 (Standard Vocabulary List)

2. ピックアップした単語を適切なファイルに追加してください。

#### `$ARGUMENTS` が具体的な英単語の場合

1. その単語が既に `words/` に存在するか確認
2. 存在する場合: その行をコンソールに表示するのみ
3. 存在しない場合: 適切なファイルに追加

### 3. 書き込み

`word-format` スキルに従って、適切なファイルに追加してください。

### 4. YouGlish で実例動画を検索 (共通処理)

追加した単語/表現について、YouGlish のリンクをコンソールに出力してください:
- URL形式: `https://youglish.com/pronounce/{単語}/english`
- WebFetch で該当ページにアクセスし、動画IDとタイムスタンプを取得
- 取得した動画を YouTube URL 形式で出力

例:
```
YouTube Videos for "shout":
- YouGlish: https://youglish.com/pronounce/shout/english

1. https://youtube.com/watch?v=xxxxx&t=120 (2:00)
2. https://youtube.com/watch?v=yyyyy&t=45 (0:45)
...
```
