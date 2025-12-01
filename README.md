# English Vocabulary Trainer

Claude Code Plugin for English vocabulary learning. Manage words, practice with flashcard-style quizzes, and improve speaking skills through roleplay conversations.

## Installation

```bash
/plugin install https://github.com/namtoki/english-vocabulary-trainer
```

## Commands

| Command | Description |
|---------|-------------|
| `/words [n\|word]` | Add vocabulary words (by count or specific word) |
| `/cliche [n\|phrase]` | Add cliche/fixed expressions |
| `/framework [n\|pattern]` | Add sentence framework patterns |
| `/anki [n]` | Start a flashcard quiz with n questions |
| `/rollplay start` | Start an English conversation roleplay |
| `/rollplay end` | End roleplay and save conversation log |

## Directory Structure

```
english-vocabulary-trainer/
├── .claude-plugin/
│   └── plugin.json
├── commands/
│   ├── words.md
│   ├── cliche.md
│   ├── framework.md
│   ├── anki.md
│   └── rollplay.md
├── words/
│   ├── 02_verb/
│   ├── 03_adjective_noun/
│   ├── 04_adverb/
│   ├── cliche.md
│   └── framework.md
├── rollplay/
├── CLAUDE.md
└── README.md
```

## Word Format

Words are stored in markdown files with the following format:

```markdown
## Category Name
- `word` /pronunciation/ ([Register] Japanese meaning) Example sentence.
  - `synonym1` /pronunciation/ ([Register] meaning) Example.
  - `synonym2` /pronunciation/ ([Register] meaning) Example.
```

**Registers:**
- `[Formal]` - Formal/business contexts
- `[Neutral]` - General use
- `[Casual]` - Informal/spoken contexts

## Features

### Vocabulary Management (`/words`, `/cliche`, `/framework`)
- Add words from major word lists (NGSL, GSL, AWL, COCA, SVL 12000)
- Categorize by part of speech and semantic field
- Include pronunciation, register, meaning, and example sentences
- Search YouGlish for real-world usage videos

### Flashcard Quiz (`/anki`)
- Random selection from your vocabulary
- Interactive quiz format with reveal
- Track which file each word came from

### Conversation Roleplay (`/rollplay`)
- Practice speaking with current news topics
- Get feedback on your expressions
- Learn more natural ways to say things
- Save conversation logs for review

## License

MIT
