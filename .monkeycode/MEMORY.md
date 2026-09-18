# User Instruction Memory

This file records user instructions, preferences, and teachings for reference in future interactions.

## Format

### User Instruction Entry

[User Instruction Summary]
- Date: [YYYY-MM-DD]
- Context: [Mentioned scenario or time]
- Instructions:
  - [Content of user teaching or instruction, described line by line]

### Project Knowledge Entry

[Project Knowledge Summary]
- Date: [YYYY-MM-DD]
- Context: Discovered by Agent while performing [specific task description]
- Category: [Operations & Deployment|Build Methods|Testing Methods|Troubleshooting & Debugging|Workflow & Collaboration|Environment Configuration]
- Instructions:
  - [Specific knowledge points, described line by line]

## Deduplication Strategy

- Before adding a new entry, check for similar or identical instructions.
- If a duplicate is found, skip the new entry or merge it with the existing one.
- When merging, update the context or date information.
- This helps avoid redundant entries and keeps the memory file tidy.

## Entries

[User Instruction Summary]
- Date: 2026-09-18
- Context: 用户连续逐句校阅《小说创作》正文后，要求把我每次教的东西记住、以后都用上
- Instructions:
  - 作者逐句指出正文毛病时，除了改当前这句，还要做三件事：把这条规则写进 `小说创作/09-style-guide.md`（可执行、带正反例），回头扫一遍已写各章（`chapters/`）找同类句，并同步受影响的控制卡、`06-foreshadow-ledger.md`、`08-dynamic-state.md`、`logs/writing-log.md`。
  - 每章开写前先读 `小说创作/09-style-guide.md` 的「用户已教规则总表」，交付前逐条过一遍；新规则当场补进该总表。
  - 规则要写成看得见、数得出的判据（例如「同一意思比两回，留一处」），不写成「注意文笔」这类无法自检的提醒。
  - 作者的判据高于既有文档：若总表或控制卡与作者当场指出的问题冲突，以作者为准，并回头改文档。

[Project Knowledge Summary]
- Date: 2026-09-18
- Context: Discovered by Agent while committing and pushing 小说创作 chapter revisions
- Category: Troubleshooting & Debugging
- Instructions:
  - 本仓库直接提交并推送到 `main`，不新建分支。推送前先 `git fetch origin main`，若远端有新提交则先 `git rebase origin/main`。
  - `git push` 偶发 `gnutls_handshake() failed: The TLS connection was non-properly terminated.`，属瞬时网络问题，原样重试一次即可成功，不需要改 remote 或改写历史。

[Project Knowledge Summary]
- Date: 2026-09-18
- Context: Discovered by Agent while self-checking 小说创作 chapter drafts
- Category: Testing Methods
- Instructions:
  - 正文硬性自查用一段 Python 统计即可，不需要额外工具：去标题行后统计汉字数（`[一-龥]`）、叹号、省略号、破折号数量，并扫黑名单词与「以“ 开头的裸对话行」。
  - 判断标准写在 `小说创作/09-style-guide.md`；每章开写前先生成 `小说创作/control-cards/` 下对应控制卡，改稿后同步 `06-foreshadow-ledger.md`、`08-dynamic-state.md` 与 `logs/writing-log.md`。
  - 每章交付前把「本章事件、人物状态、世界规则、悬念池」的变更回填 `08-dynamic-state.md`，它是叙事真值来源；`logs/writing-log.md` 只作审计。

[Project Knowledge Summary]
- Date: 2026-09-18
- Context: Discovered by Agent while analysing reference novels for 小说创作
- Category: Environment Configuration
- Instructions:
  - 四本参考小说的 UTF-8 文本放在 `/tmp/opencode/`：`dafeng/dafeng.txt`、`xin.txt`、`qs.txt`、`db.txt` 与清洗后的 `db_clean.txt`。该目录是临时空间，新会话若缺失需从工作区根目录的压缩包或 txt 重新转换。
  - 东北鬼医语料有污染：第 414、415、416、419、421、422、426 章章末混入异书文本，引文只取第 1 至 413 章与第 427 至 779 章；414 至 426 章只取前半章。
