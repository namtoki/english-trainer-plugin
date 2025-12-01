# 単語・表現の書き込みフォーマット

このスキルは、words/ ディレクトリへの単語・表現の追加時に使用するフォーマットを定義します。

---

## フォーマット

```
- `word` /pronunciation/            ([register] 訳)                 例文
```

### 各要素の詳細

#### word
- **format**: 英単語を ` で挟む
- **position**: `-` から 1 つスペースを空けて続けて置く

#### pronunciation
- **format**: IPA 方式の発音記号を `/` で挟む
- **position**: word から 1 つスペースを空けて続けて置く

#### ()
- **format**: register と訳を `()` で挟む
- **position**: 行左端から数えて **37 文字目** に `(` を置く。pronunciation から `(` までの間はスペースで埋める

##### register
- **format**: 以下のいずれかを `[]` で挟む
  - `Casual` - 友人などと口語でよく用いられる
  - `Formal` - 会社の上司、取引先、初めて会う人と口語で用いられる
  - `Neutral` - Casual にも Formal にも口語で用いられる
  - `Polite` - 礼儀正しい口語で用いられる
  - `Writing` - 口語ではあまり用いられず、文章で主に用いられる
- **position**: `(` の直後、スペースを入れずに続けて置く

##### 訳
- **format**: word の訳を日本語で **10文字以内** で書く
- **position**: register から 1 つスペースを空けて続けて置く

#### 例文
- **format**: 口語でよく用いられる例文を一つ書く（register が Writing の場合は文章でよく用いられる例文）
- **position**: 行左端から数えて **60 文字目** に例文を開始。`)` から例文までの間はスペースで埋める

### 例

```
- `hard` /hɑːd/                     ([Neutral] 努力を要する難しさ)  The test was hard.
```

### 類義語のインデント

類義語は 2 スペースでインデントして記載:

```
- `shout` /ʃaʊt/                    ([Neutral] 叫ぶ)                He shouted across the street.
  - `yell` /jel/                    ([Casual] 怒鳴る)               The coach yelled at the players.
  - `scream` /skriːm/               ([Neutral] 悲鳴を上げる)        He screamed for help.
```

---

## 書き込み先ファイル一覧

### フレームワーク (words/01_framework/)
- `cliche.md` - 定型表現
- `that_clause.md` - 構文パターン

### 動詞 (words/02_verb/)
- `0_AUX.md` - 助動詞のような働きの動詞
- `1_SVC.md` - SVC 文型の動詞
- `2_SVOC.md` - SVOC 文型の動詞
- `3_SVOO.md` - SVOO 文型の動詞
- `4_Opinion.md` - 考えを述べる際に使用する表現
- `5_Cognitive.md` - 認識を説明する時に使用する表現
- `6_Task.md` - タスク管理関連の表現
- `7_Description.md` - 何かを説明する時に使える表現
- `8_Common.md` - その他の表現

### 形容詞・名詞 (words/03_adjective_noun/)
- `0_Hedge.md` - ぼやけさせる名詞、形容詞
- `1_Business.md` - 仕事でよく使う名詞、形容詞
- `2_Politics_Religion.md` - 政治、宗教関連
- `3_Law_Crime.md` - 法律、犯罪関連
- `4_Education.md` - 教育、学術関連
- `5_Science.md` - 科学関連
- `6_Community.md` - 金融、不動産などの公共関連
- `7_Health.md` - 病院、健康、医療関連
- `8_Life.md` - 日常関連
- `9_Assessment.md` - 客観的な評価を表現する名詞、形容詞

### 副詞 (words/04_adverb/)
- `0_Conjunction.md` - 接続副詞
- `1_Reason.md` - 理由、目的の副詞
- `2_How.md` - 「どのように」を説明する副詞
- `3_Condition.md` - 条件を表す副詞
- `4_Concession.md` - 譲歩を表す副詞
- `5_Feeling.md` - 主観による情報を補足する副詞
- `6_When_Where.md` - 時間、場所を補足する副詞
