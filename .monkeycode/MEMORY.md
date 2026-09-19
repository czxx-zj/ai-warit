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
- Date: 2026-09-19
- Context: 用户审阅《小说创作》换底后的设定与正文，指出旁白动不动就把世界运行硬套成「写本子、记账、算得明白、量的准、记忆好」这类核算式解释
- Instructions:
  - 正文与设定文档禁用账本式写法。不把世界规则与人物判断改写成一套核算动作：记账、对账、逐条记下、算得明白、量的准、记忆好、笔笔记着，一律不用。
  - 判断力要写成手上的活计、看人的眼力、身体反应与器物细节；世界规则要写成单位、价钱、凭证、称谓、衣物、饭量、炭火这类可触摸的东西。
  - 统一判据：这句话，屋里的人能不能用手、眼、耳在现场做出来。能做出来就留，否则换成能做的动作或物件。
  - 具体拆解与替代对照表见 `小说创作/docs/07-大奉打更人-世界搭建与用词手法.md` 第五节。
  - 用户要求世界观「有血有肉、接近真实」，凡遇抽象交代，先问能不能换成器物、价钱、称谓或身体感受。

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
  - 《大奉打更人》已按章切分为 `/tmp/opencode/dafeng/ch/0001.txt` 至 `0820.txt`，另有 `index.json`（每项为 [全局章序, 中文标目, 章名, 汉字数]）。原书正文标目为卷内编号，与全局章序从第 100 多章起开始错位，核对引文时以全局章序的文件名为准。
