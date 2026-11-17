> **状态**：trial｜**证据分层**：[官方]=官方技能原文 · [案例]=项目实证 · [实测]=全量统计｜**更新**：2026-11-06｜**复审到期**：2027-05-04｜**依据**：ANERNEQ（S02，HEX×#5E7D95/未校正钨丝片/价值阶梯/RGB 通道）+ VENGEANCE（S08，银盐黑白灰阶）+ hex-codes 官方博客（S12，原文已读）+ DST 235 条全读逐字（S41，E236-E307）

# 通用/01 色彩立法与 HEX 体系（通用轨）

色彩不是形容词，是**可执行的色彩科学**：讲清白平衡错误的因果、给十六进制锚点、立价值阶梯、锁通道优势。

## 1. 白平衡错误因果法 [案例 ANERNEQ 一镜到底 24K]
> `SHOT ON TUNGSTEN-BALANCED 3200K FILM STOCK IN DAYLIGHT, WITHOUT AN 85 CORRECTION FILTER, AND PRINTED UNCORRECTED. This is the entire reason the image is blue... only the white balance is wrong.`
把色彩结果的**成因**讲给模型——曝光正常，只有白平衡错。

## 2. HEX 锚点 [案例 ANERNEQ]
> `DEEP STEEL BLUE, approximately #5E7D95. Matte, cold, absolutely uniform edge to edge — no clouds, no gradient, no lighter band`
十六进制 + 质面 + 全域均匀 + 禁渐变，四件套一起给。

## 3. 价值阶梯 [案例 ANERNEQ]
> `THE VALUE LADDER, BRIGHTEST TO DARKEST, AND IT NEVER CHANGES: snow → her lit face → sky → fur → bone.`
画面亮度排序是锁——**THE SKY IS CLEARLY DARKER THAN THE SNOW**（天比地暗，反 AI 默认）。

## 4. 通道优势法则 [案例 ANERNEQ]
> `THE BLUE CHANNEL IS THE STRONGEST AND THE RED CHANNEL THE WEAKEST IN EVERY PART OF THE IMAGE WITHOUT EXCEPTION, INCLUDING HER SKIN.`
全域无例外的通道强弱，皮肤也不例外。

## 5. 黑白片灰阶管理 [案例 VENGEANCE]
> silver-gelatin contrast, deep blacks, controlled highlights, fine real grain / jacket dark grey×246 / skin light grey×193 / grey mid-tones×242（行首块头口径；文档数口径 521）——黑白片里每种材质给**指定灰阶**。

## 6. COLOUR AND LIGHT LOCK [案例 ANERNEQ 466×，count_blocks.js 口径]
色彩与光合成一个锁块，跨镜复用（ANERNEQ 块频 ×334）。姊妹证据：VENGEANCE 的 THE LIGHT, THE TONE AND THE COLOUR ARE LOCKED×1,239（同构锁块，黑白片版）。

## 待验证

- HEX 在 seedream/nano_banana 各模型的遵从度差异（Q14）
- 价值阶梯与曝光立法的组合在彩色/黑白两种流程的通用性


## 2026-11-04 增补（S12 hex-codes 官方博客原文蒸馏）

### 7. Soul HEX 参考取色工作流 [官方 S12]
官方对色彩控制的第三条路：**不用文字描述、不用手写 HEX——从参考照片直接提取色板**。在 Soul 2.0 的 Color signature 区上传最多 20 张参考照片（单张也可），生成时自动提取并施加色板。

> `Soul HEX handles the color extraction and application behind the scenes, so you can focus on the creative direction while the palette stays consistent with your reference.`

适用四类：氛围匹配（雨街冷蓝/黄金时刻暖琥珀）/ 品牌色板一致 / 系列视觉连贯 / 说不出口的颜色（dusty rose）。

### 8. HEX 模型遵从度警告 [官方 S12]

> `Some models interpret HEX codes natively. Others disregard them completely. A few fall somewhere in between, responding to HEX values as loose guidance rather than precise instructions.`

**HEX 不是通用语**——各模型遵从度不一，跨模型套用前必须实测（呼应待验证 Q14）。

## 常见错误

- [官方 S21 ai-video-prompt-mistakes] 质量填充词（4k/hyperrealistic/best quality）→ 替换为 HEX 色值+材质名+光源方向
- [官方 S21 ai-video-prompt-mistakes] 全局色罩（teal-and-orange shortcut）→ 替换为独立局部色+空间限制
- [官方 S21 ai-video-prompt-mistakes] 情绪标签（warm nostalgic mood）→ 替换为物理描述（fire burns like real wood, fast irregular tongues）

## 2026-11-04 色彩三比立法增补 [案例 S25 chandler-rollerblade-commercial]

### 9. 60:30:10 法则成文 [案例 规格头 Color 行]
> `Color: 60:30:10 — dominant / secondary / accent.`

主色/辅色/点缀色的**画面占比合同式立法**——一行完成全片色彩分配。与 HEX 锚点法互补：HEX 管"是什么色"，60:30:10 管"各占多少"；与价值阶梯互补：阶梯管明度排序，三比管色相配比。

### 10. 色彩作为全局规格维度 [案例 chandler 十一行规格头]
色彩行与 Style/Lighting/Camera/Skin/Physics/Composition/Continuity/Technical/Audio 并列，**每行一维度一句冒号立法**——广告/短片项目头部的色彩立法形态（区别于视频十块结构中的 LIGHTING 块）。

### 11. HEX VALUES JSON 数组色板 [案例 S32 life-meter]
```
HEX VALUES: ["#0a090a", "#493428", "#2c1f18", "#151110", "#211915", "#402c21", "#37251c",
"#523f2f", "#5f4c37", "#705a40", "#967957", "#83694b", "#252c2e", "#353c3c"]
```
色板立法的 **JSON 数组形态**——14 个 HEX 色值整体作为一块声明（与 Soul 色板提取、60:30:10 比例法并列的第三种色板交付形态）；冷灰主导+暖棕点缀的低饱和 earth-tone 板。

### 12. 色彩豁免立法（选择性色彩的否定清单形态）[案例 S33 and-still-life 10,436c 逐字]
```
NO FULL-COLOR WORLD. NO NATURAL SKIN COLOR. NO COLORED CHURCH. ...
ONLY BLUE/CORAL PAINT HAS COLOR.
NO GLOW. NO MAGIC. NO NEON. NO MUSIC.
```
```
CRITICAL: herself remains completely BLACK AND WHITE.
ONLY actual BLUE/CORAL paint physically adhering to: her shoes, the lower hem of her dress,
the flooded ground may appear in color.
```
黑白世界的**唯一色彩例外=真实附着的颜料**（辛德勒名单式选择性色彩）：否定大区（全彩世界/自然肤色/彩色教堂逐禁）+ 豁免物立法（ONLY PAINT HAS COLOR）+ CRITICAL 块豁免点逐处枚举（鞋/裙摆/积水地面三处）。NO FACE DRIFT.×66 脸部漂移专项否定块；NO MUSIC.×197/NO SCORE.×112 否定超密度。

## 2026-11-05 增补：五分比色彩锁 [案例 S36 THE_LAST_GARDEN 最长 13,565c 逐字]
- `Color: Locked Aurelia palette — 60% soft pink, 15% lush sage/muted emerald green, 10% turquoise/pale cyan water, 10% warm golden sunlight, 5% ivory/pearl/silver/lavender accents.`——60:30:10 三分比的**五段占比**扩展实证（主 60 / 次 15 / 辅 10 / 光 10 / 点缀 5），且命名整体色板（Locked Aurelia palette）+ 前缀 `no Earth architecture, no cyberpunk aesthetic` 世界观排除。

## 2026-11-05 增补：色彩主题跨镜反转 [案例 S36 S_KOU 全量 90 条逐字 · E198]
- 全片色彩立法 `The yellow scarf is the ONLY saturated warm object in any sea or underwater frame`（黄=唯一暖色，90 条逐条复写）在欧洲海滩段**故意反转**：`This beach has its own light: bright, clean, warm morning sun…slightly overexposed whites…the yellow of the scarf almost lost against the brightness instead of being the only warm thing — the reversal of every other frame in the film`——色彩规则本身作为叙事装置（规则建立→规则反转），配独立 grade 锚（`sets the bright, clean, slightly overexposed grade used only on the European beach`）。

## 2026-11-05 增补：5_MINUTES 244 条全量逐字通读（E215）

- **调性延续法**：内景作 TONE reference 反推外景调色（how this exterior must be graded and paced, so the cut into it feels seamless）——剪辑连续性驱动的调色立法；参考亮度显式覆盖（the mood matches the interior, not the reference exterior’s brightness）
- **色调反差声明**：主动弃用全片主色调（Avoid…golden-hour warmth——建立镜克制冷调对比正片暖调）
- **色温双档时间线**：3200K 记忆段／4300K 现实段+百分比光强时间轴（红蓝脉冲 5%→40%）

## 待验证（生长点）

- HEX 在偏色光源下的遵从度
- 55/30/15 配比是否被理解为面积比
- 脏污漂移方向锁（toward brown NEVER red）是否防住变红

## 短摘录·好在哪·迁移法（2026-11-05 范本对齐）

### 配比+HEX+隔离色三件套 [案例 DST #82/#96 逐字]

> COLOUR: DEEP TEAL #155263 dominant…BURNT ORANGE #FF6F3C and AMBER #FF9A3C…GOLDEN YELLOW #FFC93C only as the faintest caught highlight…Roughly 55% teal, 30% amber-orange, 15% neutral…BRIGHT SATURATED RED and PALE SILVER exist ONLY on the drawn figure, at any depth.

**好在哪**：三件同页——主色 HEX 族+面积配比+隔离色（饱和红/银只许画中人，any depth）；并点名反经典调色（NO teal-and-orange lighting grade）。
**迁移**：全片色板=HEX 族+配比+隔离清单+"点名禁调色"一句；状态变化另加方向锁（见下）。

### 脏污色漂移方向立法 [案例 DST #75 逐字]

> the sweatshirt stays clearly ORANGE — grime dulls and darkens it toward brown, NEVER toward red.

**好在哪**：状态变化（变脏/变旧）限定色相漂移方向——向棕变深而非向红漂移；配合三联时间面板（face THINNED）把时间流逝写进外观账目。
**迁移**：一切条件漂移写"向 X 漂移，NEVER 向 Y"；三联/多面板按面板逐项给状态账。

## DST 收官蒸馏（2026-11-06 · E260-E307 · S41 全读补全）

### 三分配比制度 [案例 DST #162/#163/#175 等逐字，全项目最高频色彩块]
> COLOUR: ~55% dark desaturated TEAL-CYAN across the ruined concrete, the fallen slab block, the respirator rubber, the man's jacket and trousers…and the dark sky vault; ~30% AMBER-ORANGE carried entirely by the two real people and their kit — the boy's orange hoodie, his yellow pack with its orange stripe, both pairs of orange bootlaces, the man's rust-orange pack and yellow bedroll; ~15% neutral — bare grey concrete, pale spilled rock, snapped rebar, silt and dust.
**好在哪**：全片色彩预算按百分比立法（55 环境/30 人物/15 中性）——人物=唯一的 AMBER 携带者，世界=TEAL，写色即写"谁携带什么比例"。
**迁移**：任何项目定三分配比并逐项列携带物；人物色值写入比例清单而非单独描述。

### HEX 色标法 [案例 DST #186/#228 逐字]
> Deep teal #155263 dominant in the chasm shadow and the upper sky, burnt orange #FF6F3C and amber #FF9A3C only in the thin horizon band and on vertical faces, #FFC93C used sparingly as the faintest highlight. Roughly 55% teal, 30% amber-orange, 15% neutral grey.
**好在哪**：四色 HEX+用途逐项分配（主色/地平带/立面洗/最淡高光）+sparing 用量词——HEX 与三分配比在同一块合体；道具板同法（#213：#155263 case/#FF9A3C buttons/#FF6F3C cap）。
**迁移**：四色系=teal 主+orange 带+amber 强调+gold 略给；每色接一个用途短语。

### 红银专属画中人 [案例 DST #166/#192 等逐字]
> BRIGHT SATURATED RED and PALE SILVER exist ONLY on the drawn figure and appear NOWHERE else in the frame, at any depth…no red vehicle, no red signage, no red paint, no red plastic, no red light.
**好在哪**：角色识别色=全局排除色——红银只许一人，其余一切载体（车/牌/漆/塑/光）逐项禁；负清单与角色板同源。
**迁移**：主角识别色写"ONLY on X and NOWHERE else"+载体五连禁；防场景道具抢色。

### 冷光下唯一暖物 [案例 DST #179 逐字]
> under this cold light it is heavily desaturated and reads as a dull brick-brown, the only warm-hued object anywhere in frame and still far from bright.
**好在哪**：冷光场里的暖色会计——连主角卫衣都被降为 brick-brown 且仍是唯一暖物；暖色稀缺性=构图焦点。
**迁移**：冷调场景写"主角暖物被冷光压成 X 色+the only warm-hued object"双重声明。

### 色彩随光态折算 [案例 DST #206 逐字]
> COLOUR: ~80% near-black and deep desaturated teal-blue-grey…~12% burnt orange and amber, confined almost entirely to the thin sliver at the far end…the boy's sweatshirt is ORANGE, never red. ／ NEGATIVE: …a bright orange hoodie.
**好在哪**：同一卫衣在五种光态下的五套数值（55/30/15→80/12/8）——比例随光源重算；残照态下 bright orange 转入 NEGATIVE（负清单随光态更新）。
**迁移**：多光态项目逐态重算三分配比；NEGATIVE 里的色彩禁项跟随当前光态。

### 色彩 drain（场景自耗）[案例 DST #201 逐字]
> the scene drains across its own length. It opens at roughly 50% teal…35% amber…By the closing shot it has fallen to roughly 75% desaturated teal-grey with only ~10% dull amber left, sourced from the dim featureless glow beyond the glass.
**好在哪**：时间维度的色彩立法——开头/结尾两套配比+drain 动词+"amber 的最后来源"逐项追踪（dull glow+boy's sweatshirt）。
**迁移**：光衰/末日段写"opens at X% → fallen to Y%"双账+残余暖色的来源清单。

### 暖色专属于人 [案例 DST #165 逐字]
> THE TWO OF THEM CARRY THE ONLY WARM COLOUR IN THE FRAME, and in the final wide they are two small warm marks in a dead teal canyon.
**好在哪**：色彩叙事句——暖色=人的签名；远景里"两个小暖点"成为视觉诗（two small warm marks in a dead teal canyon）。
**迁移**：冷世界+暖人物的项目把此句式入 COLOUR 块收尾；远景写 two small warm marks。

### 道具板中性底 [案例 DST #205/#213/#215 逐字]
> 18% neutral gray seamless backdrop, one flat value corner to corner every panel, no gradient, no vignette. Flat shadowless studio light: one enormous soft frontal source, equal fill every side, no rim, no hotspot, no background or contact shadow.
**好在哪**：参考板布光/背景合同——18% 中性灰+单值无渐变+无晕影；平光五件（单源/等填/无 rim/无 hotspot/无接触影）。
**迁移**：一切 prop sheet 开头写 18% backdrop+flat shadowless studio light 五件；只许"镜片/金属/屏"三类带 sheen。

来源见[来源登记](../../../维护/来源登记.md)。沉淀样式对齐 imagegen/seedance25 两范本：短摘录逐字→好在哪→迁移法；整节编年版史保留于本页下方各增补节。


## 2026-11-07 增补：博客池 B2 批次（E404 · HEX 数组化）

### HEX VALUES JSON 数组形态 [案例 sadiesfaction SCOTT PILGRIM/kaye]
> HEX VALUES: [#fefefe, #91a44b, #a9ad61, #c7b97c, #63605d, #585451, #736e6b, #798a39, #878380, #b49a6e, #49453d, #262221, #aca8a4, #e2cebc]
**好在哪**：色板数组化首见——14 色 JSON 数组直接嵌入生图 prompt（ANERNEQ HEX VALUES 块的数组演进形态）；数组隐含明暗排序（亮→暗）。
**迁移**：风格定调后抽 12-16 色 hex 数组附 prompt；数组顺序按明度排；配合 SBS 配色呼应立法（避开色+呼应物）使用。


## 2026-11-13 增补：博客池收官批次 [官博 E435-E796 · 277 件全逐字蒸馏]

### 三态理解论 [案例 官博 hex-codes-ai-image-generation-color-control-soul · E759]
> **Some models interpret HEX codes natively. Others disregard them completely. A few respond as loose guidance rather than precise instructions**（原生/无视/松散指引三态论）
**好在哪**：HEX 支持度三态定性——写 HEX 前先测该模型属哪态。
**迁移**：新模型先发一张纯 HEX 测试图验证色彩响应。

### 让参考图自己说话金句 [案例 官博 hex-codes · E759]
> **What words can't explain, eyes can see — and Moodboards are here to help** ｜ **let the reference image speak for itself** ｜ **carry that mood into your generation through color alone**（单凭色彩传 mood 论）｜ **even if you upload 1 photo — will still pull the needed color scheme**（1 图也行论）
**好在哪**：词穷解法三连——图代言/色传 mood/单图即可提取色板。
**迁移**：形容不出的色直接丢参考图；mood 转调用纯色板参考。

### 暖金出芥末论 [案例 官博 hex-codes · E759]
> **"Warm gold" might come out as mustard. "Soft teal" might read as aquamarine — without design expertise, precise color description is surprisingly hard**
**好在哪**：色彩词转译失真例证——描述词不可靠，HEX/参考图才精确。
**迁移**：色词描述一律降级为参考方案。

### Colorgrade 六参数+流派配比论 [案例 官博 cinema-studio-2-5 · E746]
> **Color temperature (warm/cool)/Contrast+saturation/Sharpness+effects/Highlights/Film grain/Exposure** ｜ **bloom and warmth for pop and R&B, hard contrast and cool temperature for electronic and hip-hop**
**好在哪**：调色面板六参数全列+流派-调色配对表（流行=泛光暖调，电音嘻哈=硬对比冷调）。
**迁移**：MV/品牌片按流派查配对表起步。

### 全集统一调色论 [案例 官博 cinema-studio-2-5 · E746]
> **apply a unified color grade across all clips for visual cohesion** ｜ 夏 campaign=暖高对比略过曝；高端 editorial=冷调去饱和胶粒
**好在哪**：系列一致性收尾工序=全集统一 grade；两类风格 preset 例。
**迁移**：多 clip 项目最后一道工序跑统一调色。

### Relight 七光 preset 全名单 [案例 官博 video-relight-color-palette · E763]
> **Auto, Silhouette, Practicals, Window, Overhead fall, Contre jour, Soft cross** ｜ **Soft Cross — closer to a studio key-and-fill setup**（影棚主补光论）｜ **setting every slider by hand would take longer than just describing it**（手设滑杆比描述慢论）｜ 主补光例：**"Window left, cool blue, medium brightness, soft diffused. Fill: camera right, neutral white, low"**
**好在哪**：七光 preset 全名单+双自定义光源+描述法快于手调。
**迁移**：换光先试七 preset；不合再写主/补光描述句。

### 可辨识色彩身份优先论 [案例 官博 video-relight-color-palette · E763]
> **Candy Pink and Lime Jam — built for content that wants a distinct, immediately recognizable color identity over a naturalistic look** ｜ 50+ preset 库：Film Colors/Black Gloss/Nostalgic Blue/Soft Palette/Overtime/Crimson Vigi
**好在哪**：调色两条路线——自然感 vs 可辨识身份；50+ preset 名单。
**迁移**：品牌内容选风格化 preset，纪实选自然档。

### 色彩叙事法 [案例 官博 santiago-breakdown · Santiago 足球短片]
> **cold tones for the painful memory, warm ones for the good one**
**好在哪**：双色温双时间线叙事法。
**迁移**：回忆/现实分色调；冷暖=情感坐标。
