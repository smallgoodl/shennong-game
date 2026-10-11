# 神农 · 百草绘卷 / Shennong · Herbal Scroll

[中文](#中文) | [English](#english)

---

## 中文

### 简介
这是一个以中药材为主题的“抽卡 + 养成 + 自动战斗”网页小游戏原型（页面标题：《神农 · 百草绘卷 (完整原型)》）。玩家用“灵石”祈愿抽取药材角色，用重复卡产生的碎片给角色升星，再组队自动讨伐“瘟疫邪气 / 病魔”。整个游戏是单个 HTML 文件，无需安装、无需联网后端。

### 功能
- **祈愿（抽卡）**：单抽 10 灵石、十连 100 灵石；SSR 概率 1.2%，SR 约 13.8%，其余为 R；累计 40 抽必出 SSR（保底，页面显示保底进度）；抽到重复角色会转为 10 碎片。
- **养成（升星）**：在“我的百草园”点击卡牌打开培养面板，消耗碎片升星（当前星级 × 10 碎片，最高 5 星）；每升一星，面板中的生命/攻击属性提高 20%；3 星起天赋显示“(强化)”。
- **讨伐（战斗）**：从已拥有角色中最多选择 5 名出战；点击“开始讨伐”后每秒自动进行一个回合，右侧战斗日志实时显示；胜利获得 100 灵石。
  - 职业“岐黄”：每回合治疗（回复生命 = 攻击 × 0.5）；“破军”：造成攻击 × 1.5 的伤害；其他职业（龙盾、增益、解控）：普通攻击。
  - 敌方（病魔）固定 1000 生命，每回合对我方全队造成 50 伤害。
  - 羁绊：当出战角色恰为 3 名且同属一个阵营（木族 / 妖族 / 人族）时，激活“全属性 +15%”。
- **角色**：共 10 名药材角色（灵芝、茯苓、金银花、当归、鹿茸、地龙、蜈蚣、红枣、枸杞、生姜），分属木族 / 妖族 / 人族，稀有度为 SSR / SR / R。开局赠送红枣、茯苓，初始灵石 2000。
- **充值按钮**：页面顶部的“+”仅为演示，点击后确认即可免费获得 6480 灵石，不会产生任何真实扣费。
- 游戏进度只保存在页面内存中，刷新页面会重置。

### 玩法 / 使用方法
1. 底部导航有三个页面：**🏮 祈愿**、**🎒 养成**、**⚔️ 讨伐**，点击切换。
2. 在“祈愿”页单抽或十连获得角色。
3. 在“养成”页点击角色，碎片足够时点“⭐ 升星”。
4. 在“讨伐”页点选出战角色，点“⚔️ 开始讨伐 (病魔)”，观察战斗日志。
5. 操作方式为鼠标点击 / 触屏点按，没有键盘操作。

### 本地运行
无需安装任何依赖：直接用浏览器打开仓库中的 `shennong_game.html` 即可（双击文件，或在浏览器中选择“打开文件”）。

> 注意：代码中的角色图片路径写为 `立绘图片/<角色名>.png`，而本仓库的 PNG 图片目前直接放在仓库根目录，没有 `立绘图片/` 文件夹。因此直接打开时卡牌图片可能无法显示。若要显示图片，可将这些 PNG 放进名为 `立绘图片` 的文件夹中（与 `shennong_game.html` 同级）。

### 文件结构
```
shennong_game.html    游戏主文件（HTML + CSS + JavaScript 全部在内）
灵芝.png / 茯苓.png / 金银花.png / 当归.png / 鹿茸.png
地龙.png / 蜈蚣.png / 红枣.png / 枸杞.png / 生姜.png   药材角色立绘
```

### 技术栈
纯 HTML + CSS + 原生 JavaScript，单文件，无框架、无构建工具、无后端。

---

## English

### Introduction
A herbal-medicine-themed gacha / collection / auto-battle web game prototype (page title: "神农 · 百草绘卷 (完整原型)", i.e. "Shennong · Herbal Scroll (full prototype)"). Players spend "Spirit Stones" to summon herb characters, use fragments from duplicates to upgrade their stars, then send a team to automatically fight the "Plague / Disease Demon". The whole game is a single HTML file with no install step and no backend.

### Features
- **Summon (gacha)**: 1 pull = 10 stones, 10 pulls = 100 stones; SSR rate 1.2%, SR about 13.8%, otherwise R; a guaranteed SSR after 40 pulls (pity counter shown on screen); duplicates convert to 10 fragments.
- **Upgrade**: click a card in "My Herb Garden" to open the upgrade panel; spend fragments to raise stars (cost = current stars × 10, max 5 stars); each star adds 20% to the displayed HP/ATK; from 3 stars the skill is labelled "(enhanced)".
- **Battle**: pick up to 5 owned characters; press the start button and the battle auto-plays one round per second with a live log; a win rewards 100 stones.
  - Job "岐黄" (healer) heals ATK × 0.5 per round; "破军" (striker) deals ATK × 1.5 damage; other jobs (tank, buffer, controller) make a basic attack.
  - The enemy has a fixed 1000 HP and deals 50 damage to the whole team each round.
  - Bond: when exactly 3 characters are selected and all belong to the same faction (Wood / Beast / Human), "all stats +15%" is activated.
- **Characters**: 10 herb characters (Ganoderma, Poria, Honeysuckle, Angelica, Deer Antler, Earthworm, Centipede, Red Date, Goji, Ginger) across three factions and three rarities (SSR / SR / R). You start with Red Date and Poria and 2000 stones.
- **Recharge button**: the "+" in the header is a demo only; confirming simply grants 6480 free stones, no real payment is involved.
- Progress is kept in memory only; refreshing the page resets everything.

### How to play
1. Use the bottom navigation to switch between **Summon**, **Garden (upgrade)** and **Battle**.
2. Summon characters with single or 10-pulls.
3. In the Garden, click a character and press the star-up button when you have enough fragments.
4. In Battle, select your team and press the start button to watch the log.
5. Controls are mouse clicks / touch taps; there are no keyboard controls.

### Run locally
No dependencies. Just open `shennong_game.html` in a web browser (double-click it, or use "Open File").

> Note: the code loads character images from `立绘图片/<name>.png`, but in this repository the PNG files currently sit in the repo root and there is no `立绘图片/` folder, so card images may not show when opened directly. To display them, place the PNGs in a folder named `立绘图片` next to `shennong_game.html`.

### File structure
```
shennong_game.html    Main game file (HTML + CSS + JavaScript in one file)
*.png (10 files)      Herb character artwork
```

### Tech stack
Plain HTML + CSS + vanilla JavaScript in a single file. No frameworks, build tools or backend.
