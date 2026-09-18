# User Instruction Memory

This file records user instructions, preferences, and teachings for reference in future interactions.

## Format

### User Instruction Entry
User instruction entries should follow this format:

[User Instruction Summary]
- Date: [YYYY-MM-DD]
- Context: [Mentioned scenario or time]
- Instructions:
  - [Content of user teaching or instruction, described line by line]

### Project Knowledge Entry
Entries discovered by the Agent during task execution should follow this format:

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

[Project Knowledge Summary]
- Date: 2026-09-18
- Context: Discovered by Agent while producing the novel cover set under `小说创作/covers/`
- Category: Build Methods
- Instructions:
  - 环境内 LLM 出图工具只返回图片 URL，不做本地合成；封面文字压版走本地 Python + Pillow。
  - 依赖安装：`pip3 install --break-system-packages pillow`。
  - 中文字体从 jsDelivr 拉 Google Fonts 仓库的 TTF：`https://cdn.jsdelivr.net/gh/google/fonts@main/ofl/{mashanzheng/MaShanZheng-Regular.ttf,zcoolxiaowei/ZCOOLXiaoWei-Regular.ttf,longcang/LongCang-Regular.ttf}`。NotoSerifSC 的可变字体在该路径返回 403，不要再用。
  - 压版脚本：`/tmp/opencode/covers-build/make_covers.py`，底图放在同目录 `art2/`，成品写到 `小说创作/covers/`。改书名、副标题、压暗强度只改脚本参数。
  - `apt` 源里 tuna 镜像 TLS 握手失败，已改用 `mirrors.aliyun.com`；Playwright 浏览器下载需设 `PLAYWRIGHT_DOWNLOAD_HOST=https://registry.npmmirror.com/-/binary/playwright`。
  - 番茄小说封面规范：3:4，JPG 或 PNG，不超过 2MB，主色不超三种，书名最大、作者名次之，主体居中且缩略图可辨。
