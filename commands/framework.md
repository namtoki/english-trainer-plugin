# /evt:framework コマンド

引数: $ARGUMENTS

## 処理フロー

### 1. 既存データの読み込み

Grep ツールを使って登録済みの表現を取得してください:

```
pattern: ^[ \t]*- `[^`]+`
path: words/framework.md
output_mode: content
```

### 2. 引数に応じた処理

#### `$ARGUMENTS` が数字のみの場合

1. 指定された数だけ、重要なフレームワーク表現をピックアップしてください。ただし、既に `words/framework.md` にリストされている表現は除外すること。
2. ピックアップするフレームワーク表現の例:
   - 理由・説明: S V in the sense that S V, The reason why S V is that S V
   - 対比: On the one hand S V, on the other hand S V
   - 条件: As long as S V, Provided that S V
   - 結果: As a result, S V, Consequently, S V
   - 追加: In addition to N, S V, Not only S V but also S V
   - 譲歩: Even though S V, S V, Despite N, S V
   - 強調: What I mean is that S V, The point is that S V
   - 例示: For example, S V, Such as N
   - 比較: Compared to N, S V, In comparison with N
   - 目的: In order to V, So that S V
   - その他構文パターン

3. `words/framework.md` に追加

#### `$ARGUMENTS` が具体的なフレームワーク表現の場合

1. その表現が既に `words/framework.md` に存在するか確認
2. 存在する場合: その行をコンソールに表示するのみ
3. 存在しない場合: `words/framework.md` に追加

### 3. 書き込み

`word-format` スキルに従って、`words/framework.md` に追加してください。

### 4. YouTube動画検索 (共通処理)

MCP サーバー `youtube` を使用して、追加した表現が使用されている動画を検索してください:
- 再生回数が多い動画を10件ピックアップ
- 各動画について、その表現が使われている再生時間も特定
- URL とタイムスタンプをコンソールに出力

例:
```
YouTube Videos for "in the sense that":
1. [Title] - https://youtube.com/watch?v=xxx&t=120 (2:00)
2. [Title] - https://youtube.com/watch?v=yyy&t=45 (0:45)
...
```
