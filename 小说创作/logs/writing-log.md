# 写作日志

仅供审计，不作为叙事真值来源。连续性与真值以 `08-dynamic-state.md` 与各标准文件为准。

## 对话归属：代词只在同类候选人唯一时成立

- revised_at: 2026-09-18
- cause: 用户指出「王大爷问：'你奶走前，说过什么没有？' 他说：'我在省城，没赶上。'」是病句，并要求讲清底层逻辑，不能一句一句照改
- scope: 第 2 至 7 章对话归属句，`09-style-guide.md`，七张控制卡
- method:
  - 病因不在用词，在指派。归属句的职责是把说话人唯一地交给读者。「他」是代词，场上同类候选人不止一个时就不成立
  - 这一场有两个男的：先出场的王大爷，和答话的谭正阳。读者顺着上一句把「他」派给王大爷，读到「我在省城」才发现派错了，得回读一次。改「谭正阳说」，一步到位
  - 同类清洗按同一条规则走，覆盖第 2 章王大爷问答、第 4 章王大爷与谭正阳同场、第 5 章电工与谭正阳同场、第 6 章楼道邻居与深夜门外两场、第 7 章老李与老周两场。凡同类候选人为二，主角开口写「谭正阳说」「谭正阳问」
  - 留一处不点名的例外：第 7 章「他问：'周叔，你们要是有事，明儿白天走不行吗？'」。引语第一句就是呼语，读者顺着「周叔」认得出是谁在问，归属句让位给节奏
  - 反向克制：无歧义处仍写「他」，不把第三人称限知改成通篇点名
  - 顺带修同一人换称呼造成的假歧义。旁白「老头」一律并到「王大爷」，第 3 章「姓王的老头」与「他抱遗像」拆开重写
- checks:
  - rg 核对：第 2 至 7 章凡男性对男性同场的对话归属，不再出现「他说」「他问」起头的主角落款
  - 逐句遮上下文抽读：每个归属句第一反应指向的人与真说话人一致
- updated_files:
  - chapters/01 至 07: 对话归属句与「老头」称呼；第 1 章具名后旁白并到「王大爷」
  - 09-style-guide.md: 新增「对话归属」八条；自检动作补一条
  - control-cards/01 至 07: 各补一条 attribution_task
- open_question: 无

## 修掉旁白报告句与镜头跳接

- revised_at: 2026-09-18
- cause: 用户指出第 2 章「他心里动了一下。晚饭那会儿，姑姑跟他说的就是这一句」镜头不严谨，并说同类句子很多
- scope: 第 1 至 7 章的内心旁白句
- method:
  - 病灶有两处。一是「心里＋动词」这类旁白报告，把镜头从人物身上拉出来解说；二是把读者刚看过的对话复述一遍当解释
  - 第 2 章那句改成「他坐直了。饭桌上那句话，他当是姑姑自己的规矩。原来是从奶奶嘴里出来的」。动作顶替报告，复述换成他先前理解错了、现在改了口径
  - 同类清洗：「他忽然想起」改成直接切入回忆或让实物先出现；「他觉得」改成动作或直接写出想到的内容；「他在心里过了一遍」改成「又过了一遍」这类动作
  - 第 5 章删掉「他说不清自己为什么不想走」，改由「香炉空着，他没去添」把不肯走的理由落到动作上
  - 第 7 章删掉「他给自己想了几种解释」，让那几种解释直接排出来当他的念头
  - 第 6 章「说不清是蜡烛的光，还是眼睛慢了一步」按黑名单改写，给出并列的两个具体说法
- checks:
  - rg 核对：正文不再出现「心里动了一下」「忽然想起」「他意识到」「他感到」「不由自主」「莫名的」
  - 逐章通读：上一段刚出现的对话，下一段不再重讲
- updated_files:
  - chapters/01 至 07: 旁白报告句与镜头跳接
  - 09-style-guide.md: 叙事距离下新增「镜头纪律」八条；AI 腔黑名单补入报告句
  - control-cards/01 至 07: Human Writing Check 各补一条 camera_task
- open_question: 无

## 称谓按关系重排

- revised_at: 2026-09-18
- cause: 用户指出旁白里一口一个「谭玉兰」，出戏；称谓要从现实里人与人的关系出发，什么关系叫什么。姑姑叫谭正阳可以叫小名「小阳」
- scope: 第 1 至 7 章旁白与对话里的称谓，`09-style-guide.md`、`08-dynamic-state.md`、七张控制卡
- method:
  - 旁白里的「谭玉兰」全部改回视角人物心里的称呼「姑姑」。全篇是贴近第三人称、以谭正阳为唯一视角中心，他叫姑姑「姑」，旁白就跟「姑姑」
  - 姑姑的全名改由二姨之口带出一次，第 4 章二姨开口叫「玉兰」。旁白不再报户口
  - 姑姑叫谭正阳用小名「小阳」，落在第 1 章使唤他放箱子、第 3 章叫他抱遗像、第 4 章把包交给他三处。当外人面介绍时仍说「我侄儿」
  - 旁白里的主角从满篇全名改回「他」。只在场景跳转、重新定位，或在场的「他」分不清时写回「谭正阳」。第 2 章由 48 处降到 1 处，第 5 章由 64 处降到 1 处，第 6 章由 76 处降到 2 处
  - 姑姑对谭正阳提死者说「你奶奶」「你奶」，对赵老太太、二姨说「我妈」。这条本来就对，重排时保留
  - 第 1 章表舅打听房本那处原是逗号引语，改成「姑姑说：“……”」的冒号加双引号，与全篇对话格式统一
- checks:
  - 脚本核对：正文七章不再出现「谭玉兰」
  - 脚本核对：无行首引号、无方头括号、无连写的「他他」
  - 逐章通读：同一段不出现两个指不同人的「他」或「她」
- updated_files:
  - chapters/01 至 07: 旁白称谓与代词
  - 09-style-guide.md: 新增「称谓」一组，八条
  - 08-dynamic-state.md: 新增「称谓与叙述口径」一节
  - control-cards/01 至 07: Human Writing Check 各补一条 addressing_task
- open_question: 无

## 大纲与控制卡对齐最新正文

- revised_at: 2026-09-18
- cause: 正文经过加钩子与对话重排后，控制卡、章纲与伏笔台账还停在前一版颗粒度上，章末钩子与新增桥段没有登记，后续章节会照着旧版写
- scope: 七张控制卡、`07-chapter-roadmap.md` 章末钩子栏、`06-foreshadow-ledger.md`、`08-dynamic-state.md`
- method:
  - 每张控制卡新增 `## Opening Hook` 段，记开局钩子原文与钩子类型
  - 每张控制卡补 `plausibility_task`，把常理要求写成该章的具体检查项；补 `dialogue_format_task`，把说话人加冒号加双引号写成硬要求
  - 各章 `structure_task` 改成冷开场再退时间线，`theme_landing_action` 与 `## Ending Hook` 按正文重写，并与控制卡前段的「章末钩子」指向对齐
  - 章纲第 1 至 7 章的收尾栏改成与正文一致的落点，并注明章纲只保留章末钩子一栏，开局钩子归控制卡
  - 台账新增 F026 表舅打听房本、F027 姑姑半夜动包、F028 姓常的；F002 补上「数鸡没数过人」这句
  - 动态真值补第 1、3、4、7 章新落的事实、张开的债与悬念区，确认老周家是借车连夜去闺女家避一避
- checks:
  - 脚本核对：七张控制卡的章节小节数量与 `Opening Hook`、`Ending Hook` 两段齐全
  - 脚本核对：控制卡 `Ending Hook` 与章纲收尾栏指向同一件事
  - 全库核对：不再有「老周家连夜搬走」这类与「借车去闺女家」冲突的说法
- updated_files:
  - control-cards/01 至 07: 补 `Opening Hook`、两项 task，重写结构任务与章末钩子
  - 07-chapter-roadmap.md: 第 1 至 7 章收尾栏与钩子说明
  - 06-foreshadow-ledger.md: 新增 F026、F027、F028，F002 补细节
  - 08-dynamic-state.md: 第 1、3、4、7 章事件、债与悬念
- open_question: 无

## 修掉生造词与假钩子

- revised_at: 2026-09-18
- cause: 用户指出第 1 章开头「听一耳朵这句是谁的」是生造的别扭说法，整段抽象玄乎，不构成钩子，属于瞎写
- scope: 第 1 章开局与第 7 章一处用词；全库同步替换「听一耳朵」这一说法
- method:
  - 第 1 章开局换成具体的电话悬念：姑姑只说「你奶奶走了」，问到哪天走、身边有没有人，两回都是「你回来就知道了」
  - 原先接的一句「姑姑办了半辈子红白喜事」按常理站不住，改成街坊谁家办白事都请她去张罗、她张口能报出几桌几双筷子，收在「这回是自家的事，她一个字都不肯先说」
  - 删掉「有些话从他嘴里出来的时候，不全是他的」这段抽象独白。身上有东西这一核心设定改成可观察的写法：开口之前总要停一下，认一认这句话是不是自己要说的，认得慢了话就接不上，别人当他走神
  - 第 7 章「听了一耳朵」改成「认了认」。08-dynamic-state、两张控制卡、试写稿、日志里的同类措辞一并替换，避免后续章节再用
- checks:
  - rg 核对：全库不再出现「一耳朵」
  - 第 1 章开局三行内给出死者与姑姑的隐瞒，钩子落在信息缺口上
- updated_files:
  - chapters/01-多摆一个.md: 开局重写，设定改具体写法
  - chapters/07-猫不进院.md: 用词替换
  - 08-dynamic-state.md、control-cards/01、control-cards/02、docs/试写-打斗与泪点.md: 同类措辞替换
- open_question: 无

## 每章加钩子与人性戏

- revised_at: 2026-09-18
- cause: 用户指出「数鸡」和「数这个」接不上，要求每章开局看几行就抓人，中段有意思或起高潮，结尾下套让读者非看下一章不可，并且要拿捏人性
- scope: 第 1 至 7 章，改开局、结尾与「数鸡」那处对话，中段补人性戏；情节、人物、伏笔与章末钩子走向不变
- method:
  - 开局改成冷开场：先把本章最反常的一下摆出来，再退回时间线叙述。原先「X 前几天，家里没什么事」这类起手全删
  - 章末加套：第 4 章加姑姑半夜把包按进纸灰却不点火，第 7 章把请的人落到红布上见过的「常」字
  - 「数鸡」那条改成「她教过你数鸡，没教过你数人。鸡少一只，你一眼能看见。人少一个，你看不见」，与单子上缺的半边对上
  - 人性戏：第 1 章补表舅打听房本名字，谭正阳把「你在外头跟谁过日子」列成最怕被问的一句
  - 原先并到开局的抽象独白，隔一轮后按用户意见撤掉，改成可观察的写法
- checks:
  - 逐章核对：开局三行内给出反常物件或怪话
  - 逐章核对：章末最后一行都落在未答的问题或刚发生的反常上
- updated_files:
  - chapters/01-多摆一个.md 至 chapters/07-猫不进院.md: 开局、结尾与中段人性戏
  - 09-style-guide.md: 新增「每章的钩子」一组，并修顺对话归属条目
- open_question: 无

## 对话改用冒号加双引号

- revised_at: 2026-09-18
- cause: 用户指出「他站着没动，又问，明天的事怎么安排。她说都写单子上了」这类句子，他他他混在一起分不清谁是谁，要求双引号与冒号都用上
- scope: 第 1 至 7 章全文重排对话格式，情节、人物、伏笔与章末钩子不变
- method:
  - 对话统一改成「说话人 + 说／问 + 冒号 + 双引号」起手，如「谭玉兰说：“都写单子上了，你不用管。”」
  - 原先以方头括号起手、引号句在前、说话人在后的写法全部调转
  - 旁白里分不清指谁的代词一律换回人名，同段不再出现两个指不同人的「他」
  - 引语里的问句收问号，陈述与命令收句号，一句里不混两种收尾
- checks:
  - 脚本核对：正文无一行以引号起手，也不再有方头括号
  - 脚本核对：全部引号句前都紧接说话人加冒号
- updated_files:
  - chapters/01-多摆一个.md 至 chapters/07-猫不进院.md: 对话格式全文重排
  - 09-style-guide.md: 人怎么说话一条补冒号加双引号与收尾标点规则
- open_question: 无

## 对话归属与标点重排

- revised_at: 2026-09-18
- cause: 用户要求谁问、谁说、谁答和旁白都写清楚，标点符号用明白，一眼看出话是谁说的
- scope: 第 1 至 7 章再次全文重排，情节、人物、伏笔与章末钩子不变
- method:
  - 每句对话补回说话人：以「某某说」「某某问」收尾，或在本句带一个交代说话人的动作
  - 消除连续裸对话。谁问、谁说、谁答全部落到字面上
  - 旁白里指代不清处的代词改回人名，避免「他」连着指两个人
  - 问句统一改问号，陈述与命令用句号；原先用句号收尾的问句全部纠正
  - 补上原先略去的对话归属，如电工的三句问答、二姨那句「您数什么」、老李的「为什么」
- checks:
  - 脚本核对：以「」开头的行全部带说话人或交代说话人的动作
  - 脚本核对：含疑问词的引号句不再以句号收尾
- updated_files:
  - chapters/01-多摆一个.md 至 chapters/07-猫不进院.md: 全文重排
  - 09-style-guide.md: 真人写作标准的对话条补归属与标点规则
- open_question: 无

## 正文重写（第一章起）

- revised_at: 2026-09-18
- cause: 用户要求从第一章开始，按真人写作标准重写正文
- scope: 第 1 至 7 章全文重写，情节、人物、伏笔与章末钩子不变，只重做叙述句法与节奏
- method:
  - 句长参差：长句后接短句，单字与短句段只在冲击处出现，杜绝等长段链
  - 比喻收敛：全库「仿佛」「像是」「似乎」由 18 处降至 10 处，且同段不叠用
  - 对话与口语原样保留，术语零解释，不新增解释性段落
  - 破折号与省略号零使用，连接词起句零使用，对照句零使用
  - 第 2 章修正次日安排在姑姑进屋前后的先后顺序
- checks:
  - 逐章过控制卡 Human Writing Check 六项
  - 重写后每章 2600 至 3000 字符，篇幅与前稿相当
- updated_files:
  - chapters/01-多摆一个.md 至 chapters/07-猫不进院.md: 全文重写
- open_question: 无

## 真人写作标准

- revised_at: 2026-09-18
- cause: 用户要求写作思维手法符合或者接近真人写作 99%
- canonical_change:
  - 09-style-guide.md 新增「真人写作标准」模块，分句子、用词、段落、对话、细节五组给可执行条目，定合格线为每一千字机器痕迹不超过一处
  - AI 腔黑名单补七个新条目，修订标准补一条
  - docs/01-手法拆解.md 新增真人写作要点，作为写法底稿
- updated_files:
  - 09-style-guide.md: 新增真人写作标准；AI 腔黑名单与修订标准扩充
  - docs/01-手法拆解.md: 新增第十节真人写作要点
- resolved: 已把真人写作标准写进七张控制卡的验收条件，新增 Human Writing Check 段，逐章给句长、用词、段落、对话与朗读关的检查项

## Chapter 7

- drafted_at: 2026-09-18
- mode: serialized
- benchmark_check_ran: yes
- failed_benchmark_items:
  - 初稿篇幅偏短，约 1617 汉字，已补老李讲奶奶看事、黄猫旧事、孙姨一句「总得有人接」、单位催回城与老周借车细节，补足至 2092 汉字，含标点 2528
- rewrite_pass: 1
- retrieval_slice_used: 是，兑现第 6 章「明儿头七，你站我旁边」，再守一次第 1 章不能点香的规矩，续上第 5 章的煤与墙根
- forgotten_element_action: 香炉在头七当天再露一次并说明为何仍空；黄猫与奶奶窗台接上第 1 至 6 章的窗意象
- authenticity_pass_level: medium
- post_authenticity_mini_recheck_ran: yes
- marathon_mode: no
- auto_advanced_to_next_chapter: no
- primary_fix_origin: length
- updated_files:
  - chapters/07-猫不进院.md: 新建正文
  - control-cards/07-猫不进院-control-card.md: 新建控制卡
  - 06-foreshadow-ledger.md: 新增 F024 猫不进院、F025 奶奶后来不应人
  - 08-dynamic-state.md: 更新最新章节、事件、人物状态、关系、伏笔与悬念池
- temporary_assumptions:
  - 孙姨娘家那个庙具体在哪、灵不灵，本章不展开
  - 老周家去闺女家住多久，本章不交代
- third_pass_cause_summary:
  - not needed

## Chapter 6

- drafted_at: 2026-09-18
- mode: serialized
- benchmark_check_ran: yes
- failed_benchmark_items:
  - 初稿篇幅偏短，约 1681 汉字，已补断电过日子的实写（冰箱化冻、北阳台、邻居问灯）与门外安全解释逐一失效两段，补足至 2066 汉字，含标点 2453
- rewrite_pass: 1
- retrieval_slice_used: 是，动用第 2 章守夜规矩里的叫门与叫名字两条，续上第 1 章空香炉与「等人齐了再点香」，续上第 5 章整屋断电与红布包
- forgotten_element_action: 空香炉在本章再露一次，并让它在门外叫门时变成一个念头，避免被读者忘掉
- authenticity_pass_level: medium
- post_authenticity_mini_recheck_ran: yes
- marathon_mode: no
- auto_advanced_to_next_chapter: no
- primary_fix_origin: length
- updated_files:
  - chapters/06-夜里有人叫门.md: 新建正文
  - control-cards/06-夜里有人叫门-control-card.md: 新建控制卡
  - 06-foreshadow-ledger.md: F004 改为第 6 章已埋，新增 F023 夜里的叫门声
  - 08-dynamic-state.md: 更新最新章节、事件、人物状态、关系、伏笔与悬念池
- temporary_assumptions:
  - 门外声音是谁、为什么用奶奶的调子，本章不交代
  - 姑姑早醒着等了多久，本章不交代
- third_pass_cause_summary:
  - not needed

### 报号设定纠偏

- revised_at: 2026-09-18
- cause: 用户指出出马是正经一门、有出处，报号成立，主角名正言顺是正规弟马。真问题是他体内那东西是志怪，没有名字。旧稿一路写「号没人认」「名册上没有他」，方向反了
- supersedes:
  - 六门框架纠偏 中的「出马给他报了个号，号没人认；道教翻名册，册上没有他」
  - 卷次顺序调整 中的「报出的名字没人认，他要找一个能认定名字的地方」
  - 关卡结构与苗疆情感线 中的主题加固句
- canonical_change:
  - 出马是正经一门，有堂口、有堂单、有出处。他接堂报号，这一门认他
  - 卡住的是堂安不成：末了一格该由他身上的东西报号，那东西报不出来，因为它本来就没有名字
  - 道教先认他的号，认他是个正经弟子，查不出的是他身上那东西。册子上登得上他这个人，登不上它
  - 全书引擎改为：修为涨一分，那东西往他心智里多进一分；他做过的事、说过的话，他自己分不清哪些是他的
  - 六名表（叫法）保留，含义改写：是各门自己给它的一个叫法，不是它的名字
- updated_files:
  - 00-project-overview.md: 核心承诺、结局余味（末幕改为他报上自己的名字，满堂都认，堂上另有一个声音替他应了一声）
  - 01-theme-and-proposition.md: 对立价值、「最狠的一刀在苗疆」、报号母题改写
  - 02-worldbuilding.md: 出马、道教两节与「他身上的东西」引擎节改写
  - 03-cast-bible.md: 白守义矛盾点改写
  - 05-main-plotlines.md: L1、L2、L3 下一转与收束条件改写，F007 由「户口无名」改为「多出来的名字」
  - 06-foreshadow-ledger.md: F001、F007、F008 改写
  - 07-chapter-roadmap.md: 总纲、中心思想、六名表、卷一至卷二概览、卷一第 34 至 35、43 至 47、53 至 56、112、122 至 123、130 章改写，卷一收束状态与卷末交接改写
  - 08-dynamic-state.md: 「已确认」列表与悬念池改写
  - 09-style-guide.md: 苗疆言情线设定句改写
  - docs/01-手法拆解.md: 开场范式第 4、5 步改写
  - docs/试写-打斗与泪点.md: 打斗段「字号」改名「报号」并重写报号逻辑，苗疆情感段一句改写

## Chapter 1

- drafted_at: 2026-09-18
- mode: serialized
- benchmark_check_ran: yes
- failed_benchmark_items:
  - 初稿前半段吊唁场面偏散，已压缩聊厂子与电视描写
- rewrite_pass: 1
- retrieval_slice_used: no
- forgotten_element_action: 无，开篇章
- authenticity_pass_level: medium
- post_authenticity_mini_recheck_ran: yes
- marathon_mode: no
- auto_advanced_to_next_chapter: no
- primary_fix_origin: pace
- updated_files:
  - 07-chapter-roadmap.md: 第 1 章标题由「回来的那天下了雪」锁定为「多摆一个」
  - 08-dynamic-state.md: 记录旧碗筷、空香炉、谭正阳与谭玉兰关系状态
- temporary_assumptions:
  - 奶奶去世的具体原因暂留白
- third_pass_cause_summary:
  - not needed

## Chapter 5

- drafted_at: 2026-09-18
- mode: serialized
- benchmark_check_ran: yes
- failed_benchmark_items:
  - 初稿篇幅偏短，约 1262 汉字，已按控制卡补足至 2126 汉字，含标点 2492
- rewrite_pass: 1
- retrieval_slice_used: 是，回收第 1、2 章空着的香炉，续上第 2 章奶奶数东西与第 4 章二姨数手
- forgotten_element_action: 空香炉在本章再露一次，用「手伸到一半又收回来」压住，避免被读者忘掉
- authenticity_pass_level: medium
- post_authenticity_mini_recheck_ran: yes
- marathon_mode: no
- auto_advanced_to_next_chapter: no
- primary_fix_origin: length
- updated_files:
  - chapters/05-灯泡炸了.md: 新建正文
  - control-cards/05-灯泡炸了-control-card.md: 新建控制卡
  - 06-foreshadow-ledger.md: 新增 F022 只有他家停电
  - 08-dynamic-state.md: 更新最新章节、人物状态、伏笔与悬念池
- temporary_assumptions:
  - 姑姑睡东屋、谭正阳睡里屋的住法沿用第 2 至 4 章，暂不细写房间归属
- third_pass_cause_summary:
  - not needed

## Chapter 4

- drafted_at: 2026-09-18
- mode: serialized
- benchmark_check_ran: yes
- failed_benchmark_items:
  - 初稿篇幅偏短，约 1672 汉字，已按控制卡补足至 2041 汉字，含标点 2501
- rewrite_pass: 1
- retrieval_slice_used: 是，回收第 3 章姑姑收走红布包留下的那句「你别碰它」，并对上第 2 章奶奶数东西
- forgotten_element_action: 二姨复现奶奶数东西的手势，把第 2 章的悬留接到第 4 章的人身上
- authenticity_pass_level: medium
- post_authenticity_mini_recheck_ran: yes
- marathon_mode: no
- auto_advanced_to_next_chapter: no
- primary_fix_origin: length
- updated_files:
  - chapters/04-不能烧.md: 新建正文
  - control-cards/04-不能烧-control-card.md: 新建控制卡
  - 06-foreshadow-ledger.md: 新增 F020 红布包不认火、F021 奶奶托王大爷带的话
  - 08-dynamic-state.md: 更新最新章节、人物状态、关系、伏笔与悬念池
- temporary_assumptions:
  - 赵老太太与二姨的身份只做老辈人处理，暂不扩写背景
- third_pass_cause_summary:
  - not needed

## Chapter 3

- drafted_at: 2026-09-18
- mode: serialized
- benchmark_check_ran: yes
- failed_benchmark_items:
  - 初稿篇幅偏短，约 2109 汉字，已按控制卡补足至 2409 汉字，含标点 2839
- rewrite_pass: 1
- retrieval_slice_used: 是，回收第 1 章柜子最上层的旧碗筷，并对上第 2 章奶奶「屋里有一处对不上」
- forgotten_element_action: 姓王老头重新露面，只在散场时远远看着，不给他台词，留给第 8 至 10 章
- authenticity_pass_level: medium
- post_authenticity_mini_recheck_ran: yes
- marathon_mode: no
- auto_advanced_to_next_chapter: no
- primary_fix_origin: length
- updated_files:
  - chapters/03-红布包.md: 新建正文
  - control-cards/03-红布包-control-card.md: 新建控制卡
  - 06-foreshadow-ledger.md: F002 堂单缺位标为已埋，隐藏含义改为成对名号缺半边
  - 07-chapter-roadmap.md: 第 3 章章末钩子由「堂单上有一处空白」改写为「名号成对，缺了半边」
  - 08-dynamic-state.md: 更新最新章节、人物状态、伏笔与悬念池
- temporary_assumptions:
  - 堂单上名号的完整内容，暂不交代
  - 姑姑叠布手法很熟，出处留待后文
- third_pass_cause_summary:
  - not needed

## 设定扩充：打斗与情感

- at: 2026-09-18
- cause: 用户要求全书要有打斗戏、情感戏、热血爽感与泪点
- decision: 打斗与情感纳入风格层，同时保留微恐底线。核心约束是一条：法器在人与人之间完全生效，对着他身上的东西一律无效
- files_updated:
  - 02-worldbuilding.md: 新增斗法三层、法器谱、斗法三条铁律、爽与怕同源；不可发生清单加入「没有一件法器能碰到他身上的东西」
  - 09-style-guide.md: 辅助风格加入热血与情感；新增打斗模块执行、情感模块执行
  - 07-chapter-roadmap.md: 新增卷一打斗与泪点配额，九场打斗与四个泪点落章
  - 05-main-plotlines.md: 新增 L6 斗法与地盘，L3 标注为泪点主场
  - docs/试写-打斗与泪点.md: 斗法与泪点各一段写法样本
- open_question: 法器是否引入等级与升级体系

### 六门框架纠偏

- revised_at: 2026-09-18
- cause: 用户指出「六家都想给他定名分」与「苗寨连名分都不给」前后矛盾，并明确只有出马和道教是给他定名分的体系，其余四门只是剧情需要
- canonical_change:
  - 撤掉「六家都想给他定名分」的说法。全库改为：只有出马和道教两套规矩跟他的名字较劲
  - 名字这条线收成三站：出马给他报了个号，号没人认；道教翻名册，册上没有他；苗寨真肯收他，代价是改姓
  - 后四门重新定位为关卡。不给名分，只管他是什么东西，并各拿走他一样：出神换掉一段自己、蛊认主、脸摘不下来、换星献东西
  - 师承账拆为两段：有师承的两家（出马、道教），与无门无分硬学来的四手（萨满、苗疆、傩戏、占星）
  - L2 由主线降为暗线，更名「那东西被叫过的名字」，改为一路上捡起来的痕迹
  - L4 由「六派互疑」改为「两家的旧账」，跨度收在卷一至卷二，卷三后转余账
- updated_files:
  - 00-project-overview.md: 核心承诺、主要钩子、结尾余味改写
  - 01-theme-and-proposition.md: 对立价值重写，「最狠的一刀在苗疆」改写为三站结构
  - 02-worldbuilding.md: 制度分布、底层规则、他怎么赢、师承账、人物认知改写
  - 03-cast-bible.md: 打架靠什么、关系压力，章节标题改为「各卷对手」
  - 05-main-plotlines.md: L1 因果链、L2 降级并更名、L4 更名改写、L5 L6 改写
  - 06-foreshadow-ledger.md: F001 隐藏含义改写
  - 07-chapter-roadmap.md: 总纲、名字表、师承顺序、卷四刀口、卷一终点、第 112 章改写
  - 09-style-guide.md: 苗疆言情线设定说明改写
  - README.md, docs/01-手法拆解.md: 同步

### 情感试写补充

- revised_at: 2026-09-18
- cause: 苗疆情感副线落定后，追加一段写法样本，验证「不通婚」这道题的泪点是否成立
- added: docs/试写-打斗与泪点.md 新增第三节《阿朵》，写分别场面。她把祖蛊的崽过到他身上，他从此不饿；代价是认主只认一次，她换不了主。收在她第一次把本名说出口
- check: 900 汉字，禁用词零，无破折号省略号，未写外貌夸奖与哭泣

### 打斗写法修订

- revised_at: 2026-09-18
- cause: 用户否掉原设计。主角靠测量、记录、复盘赢架，样章里掏纸念条目，用户判为不可用
- canonical_change:
  - 主角赢法改为五样：师承、感应、秘法、名头、偶尔动脑
  - 斗法铁律增补第三条：名头即战力，开打先报名号，用谁的名头就欠谁
  - 新增师承账，逐卷列明师承、所得与欠账
  - 明确禁止：测量、记录、翻本子、念条目不得作为赢架手段。测绘只用于察觉屋里不对
  - 卷一打斗配额由九场改为十场，首场口舌提前至第 21 至 22 章
- updated_files:
  - 02-worldbuilding.md: 斗法铁律增补名头条，重写「他怎么赢」，新增师承账与「赢了也算不上赢」
  - 09-style-guide.md: 打斗模块新增名头、赢法五样、感应代价与禁写条目
  - 03-cast-bible.md: 谭正阳新增打架靠什么、名头短处、感应三条
  - 07-chapter-roadmap.md: 打斗配额表首行新增第 21 至 22 章，第 39 与 41 至 43 章爽点改写为报号
  - docs/试写-打斗与泪点.md: 打斗段整体重写为《字号》，泪点段补足第 82 章「上一任是我」的揭示

### 卷次顺序调整

- revised_at: 2026-09-18
- cause: 用户指定家传出马之后学道法
- canonical_change:
  - 卷次改为：一卷出马、二卷道教、三卷萨满、四卷巫蛊、五卷傩戏、六卷占星
  - 卷二道教的动机改为「报出的名字没人认，他要找一个能认定名字的地方」
  - 卷三萨满的动机改为「道教把他退回民间，他只能顺着马长海那条线索北上找更古老的原型」
  - 骨与经络改为两段结构：前两卷往上找编制，后四卷往下摸骨头、容器、面具、命盘
  - 那东西被人叫过的六个名字随卷次调整：卷一空碑、卷二削名、卷三不回头的、卷四饿、卷五空相、卷六错宿
- updated_files:
  - 07-chapter-roadmap.md: 六卷表与六卷概览重排，新增「师承为什么是这个顺序」，卷末交接改写
  - 02-worldbuilding.md: 地理框改写，骨与经络补两段结构，师承账表重排
  - 05-main-plotlines.md: L2 因果链改写
  - 06-foreshadow-ledger.md: F009 F010 名字与卷次互换（改名不换设定，只挪卷）
  - 00-project-overview.md: 目标定位与风格配置同步

### 关卡结构与苗疆情感线

- revised_at: 2026-09-18
- cause: 用户提出后四门改为关卡，并指定巫蛊拆白苗黑苗、主角救苗疆圣女、寨规不和外族通婚构成情感线与泪点
- canonical_change:
  - 卷三至卷六改为关卡，四段式：撞上、摩擦、一起办事、认还是不认。四卷结果依次为认、情、毁、价
  - 巫蛊拆为白苗（养蛊，守寨）与黑苗（放蛊，害人）。分界线是养与放，不是血统。黑苗里也有跑出来住在坡上的人
  - 新增圣女设定：蛊王选出来的，选上即收起本名，不能出寨、不能定亲、不能再用自己的名字。理由是祖蛊认她，换主时寨门会空
  - 新增 L7 苗疆情感副线。障碍是寨规不和外族通婚，规矩有实在理由，不是误会
  - 新增人物：阿朵（圣女）、龙阿公（白苗头人）、石岩（白苗青年）、麻老五（黑苗头人）、坡上的人
  - 主题加固：出马给了他一个号，那个号没人认；道教的名册上没有他；苗寨头一回真肯收他，代价是改姓
- updated_files:
  - 02-worldbuilding.md: 巫蛊扩写为白苗黑苗与圣女两节，新增关卡四段式，师承账卷四改写
  - 01-theme-and-proposition.md: 新增「最狠的一刀在苗疆」
  - 09-style-guide.md: 情感模块改写为双线，新增苗疆言情线执行
  - 03-cast-bible.md: 新增阿朵、龙阿公、石岩、麻老五、坡上的人五张人物卡
  - 04-relationship-map.md: 新增五条关系边
  - 05-main-plotlines.md: 新增 L7 苗疆，L6 补关卡斗法配额，新增关卡结构说明
  - 06-foreshadow-ledger.md: 新增 F015 至 F019
  - 07-chapter-roadmap.md: 卷四概览重写，卷三至卷六补关卡结果，新增关卡四段式表与卷四情感条目
  - 08-dynamic-state.md: 待确认项扩充
- open_question: 法器是否引入等级与升级体系

### Chapter 1 修订记录

- revised_at: 2026-09-18
- revision_cause: 用户确立人物核心事实，谭正阳从头就知道身上有东西
- canonical_change:
  - 新增：他知道有东西在，有些年了，没人知道他知道
  - 新增：开口之前先停一下，认一认这句话是不是自己要说的，这个习惯从第一章起就存在
  - 确立：全书不做「到底是灵异还是精神病」的悬念，动摇的只有他自己
- updated_files:
  - chapters/01-多摆一个.md: 插入一段内心事实，篇幅 2334 汉字
  - control-cards/01-多摆一个-control-card.md: 人物触发点与弧线进度点重写
  - 08-dynamic-state.md: 谭正阳内部状态与 L1 进度改写
  - 00-project-overview.md, 01-theme-and-proposition.md, 02-worldbuilding.md, 09-style-guide.md: 核心承诺、中心问题、不可发生、叙事距离同步
- wording_purge: 全库清除抽象概念词与设计文档腔，涉及 00 至 09、README

## Chapter 2

- drafted_at: 2026-09-18
- mode: serialized
- benchmark_check_ran: yes
- failed_benchmark_items:
  - 初稿篇幅偏短，仅约 950 汉字，已按控制卡补足至 2142 汉字
- rewrite_pass: 2
- retrieval_slice_used: 是，回收第 1 章空香炉与旧碗筷
- forgotten_element_action: 姓王老头在第 1 章欲言又止，本章给出一句台词，避免成废棋
- authenticity_pass_level: medium
- post_authenticity_mini_recheck_ran: yes
- marathon_mode: no
- auto_advanced_to_next_chapter: no
- primary_fix_origin: length
- updated_files:
  - chapters/02-灵前的规矩.md: 新建正文
  - control-cards/02-灵前的规矩-control-card.md: 新建控制卡
  - 08-dynamic-state.md: 更新最新章节、人物状态、伏笔与悬念池
  - 07-chapter-roadmap.md: 第 23 章标题与使命改写为「那段空白被人看见了」，以适配人物从头知道有东西的设定
- temporary_assumptions:
  - 奶奶临终时屋里还有谁，暂不交代
- third_pass_cause_summary:
  - not needed
