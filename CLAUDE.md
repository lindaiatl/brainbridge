# MindCadence 脑韵 — Project Guide

网站名:英文 MindCadence(连写),中文"脑韵"。主域名 mindcadence.org
(另有 rhythmofmind.org / rhythmofmind.online / rhythmofbrain.com,均跳转到主域名)。
中文页标志显示"脑韵 MindCadence";中文正文里单独提到品牌时只写"脑韵"。
旧名 BrainBridge、旧网址 brainbridge-nine.vercel.app 已停用。

## 品牌定位
MindCadence 帮助人们通过可信的科学、有温度的写作和富有同理心的引导,
更好地理解大脑、疾病、看护与生活。让脑科学连接普通人的真实生活。

## 目标受众
希望更好理解生活的人 —— 尤其是患者、看护者、家属,以及对神经科学感兴趣的读者。

## 我们提供什么
- 脑健康科普:用平实语言解释大脑与神经疾病
- 研究解读:把前沿神经科学转化为可读、可信的内容
- 看护支持:给家属与看护者的实用、温柔的指引
- 科学生活方式:关于艺术、自然与疗愈的反思,传递希望与陪伴

## Tone
专业、简洁、有温度。平静、可信、温暖、充满希望 —— 绝不冷漠或过度技术化。
面向"你"说话;句子简短、令人安心;不用行话;不用 emoji。

## 页面列表
- index.html —— 首页(Hero 大图、三种帮助方式、关于 MindCadence、精选文章、
  newsletter + 联系方式、页脚)
- article.html —— 文章详情页示例
- resources.html —— 资源列表页(按话题筛选的文章卡片列表,含所有话题)
- stories-of-hope.html —— "Stories of Hope" 专题目录页,列出该栏目下的所有
  文章(目前九篇,按 story-toc 顺序:01 mom-cold-warm.html「Mom, Are You
  Cold? Mom, Don't Be Afraid」、02 hope.html「A Three-Minute Walk」、
  03 mom-flowers.html「Flowers for the Fifth Seventh Day」、
  04 mom-dreamed.html「I Dreamed of Mom」、
  05 mom-miss.html「Mom, Today Is a Day I Miss You」、
  06 mom-day.html「Happy Mother's Day, Mom」、
  07 mom-palm.html「The Warmth of Mom's Hand in My Palm」、
  08 mom-work.html「In My Dream, Mom Took Me to Work」、
  09 mom-sea.html「Mom Is on the Other Side of the Sea」)。首页
  "Stories of Hope" 卡片指向这里,而不是直接指向某一篇文章。新增 Hope 分类
  文章时,除了在 resources.html 加卡片外,也要在这里加一张。
- hope.html / mom-cold-warm.html / mom-flowers.html / mom-dreamed.html /
  mom-miss.html / mom-day.html / mom-palm.html / mom-work.html /
  mom-sea.html —— Stories of Hope 栏目下的单篇文章页,在 "Related
  resources" 里链接到下一篇故事和其他分类文章,返回链接指向
  stories-of-hope.html。mom-flowers 到 mom-sea 这 7 篇没有专门录制的朗读
  音频,"Listen to this article" 用浏览器内置的 speechSynthesis 朗读正文
  (与 hope.html 相同的实现),背景音乐则各自使用 Mom 文件夹里对应的 mp3。

## 双语(英文 / 中文)
- 中文版放在 zh/ 目录:zh/index.html、zh/resources.html、zh/stories-of-hope.html,
  与同名英文页一一对应,每页 <head> 里有 hreflang 互指。
- 每个页面导航最后都有 "EN / 中文" 切换(.lang-switch)。英文文章页目前没有中文版,
  它们的"中文"链接指向对应的中文目录页(Hope 故事 → zh/stories-of-hope.html,
  其他文章 → zh/resources.html)。
- "希望的故事"九篇文章已有中文版:zh/<同名>.html,正文来自作者的中文原稿(桌面"hope双语版文章"文件夹),
  标题用作者原稿标题，中文页不显示作者署名。配图、背景音乐与英文版相同(引用 ../ 下同一文件)。
  中文版"朗读这篇文章"播放 zh/<同名>-narration.mp3(Mac 系统语音 Tingting 用 say 生成，朗读文本在桌面
  "hope双语版文章/朗读文本"),朗读时背景音乐自动调低。英文文章页的"中文"链接直接指向对应中文文章。
- 其他栏目(认识疾病等)只翻译了网站框架(导航、首页、栏目页、卡片标题与简介);文章正文仍是英文,
  中文页上的"阅读(英文)→"链接到 ../ 下的英文文章。
- 改动英文首页/资源页/Hope 目录页的文字或新增卡片时,要同步修改 zh/ 下对应页面。
- 以后翻译某篇文章时:新建 zh/<同名>.html,并把中文目录页里的链接改指向它,
  英文文章页的"中文"链接也改指向它。

## 2026-10-20 更新
- 五个栏目的首篇文章已有中文版:zh/article.html(认识阿尔茨海默病)、zh/caregivers.html、zh/brain-health.html、
  zh/neuroscience.html、zh/healing.html。正文来自桌面"双语版文章"文件夹的中文稿，配图与背景音乐与英文版相同。
  中文页署名"脑韵团队";"朗读这篇文章"暂用浏览器 speechSynthesis(zh-CN),还没有录制的朗读音频。
  英文页"中文"链接已指向对应中文页;中文目录/首页/相关文章里的"阅读（英文）"都已改为中文页。
- 神经科学栏目新增第二篇:beam-of-light.html / zh/beam-of-light.html
  (A Beam of Light Into the Depths of Memory / 一束光，照进记忆深处，2026 诺贝尔奖光遗传学与阿尔茨海默病),
  配图 beam-of-light.png,背景音乐 beam-of-light.mp3(原 leberch-inspirational-calm)。
- 新建神经科学目录页 neuroscience-articles.html / zh/neuroscience-articles.html(照 Stories of Hope 模式),
  首页"Neuroscience Made Simple / 轻松读懂神经科学"卡片指向它;两篇神经科学文章的返回链接也指向它。
- 修正：九篇中文希望故事页的语言切换原来把 EN 标成当前页，已改为 EN 链接 + 中文为当前。

## 2026-10-21 更新
- 看护者栏目新增第二篇：give-my-time.html / zh/give-my-time.html(I Give You My Time / 我把时间献给你，Lindai 的随笔),
  配图 give-my-time.jpg,背景音乐 give-my-time.mp3(原 velariomusic-relaxing-music),来源桌面 GiveMyTime 文件夹。
  英文页署名 Lindai,中文页不署名(同希望的故事)。朗读用浏览器 speechSynthesis。副标题由 Claude 撰写。
- 新建看护者目录页 caregivers-articles.html / zh/caregivers-articles.html,首页"A Guide for Caregivers / 看护者指南"卡片指向它;
  caregivers.html 两个语言版本的返回链接也指向它。

## 视觉规范
配色 hex、字体规范、间距等所有 visual specs 一律参考 design-system.md,
不在本文件中重复。

## 2026-10-22 更新：导航调整
- Articles 与 Resources 合并为 **Articles / 文章**:全部文章列表页改名 articles.html / zh/articles.html(原 resources.html 内容)。
  resources.html / zh/resources.html 现在只是跳转页(自动转到 articles.html),保留是为了旧链接不失效。
  以后新增文章卡片加在 articles.html(及 zh/articles.html),不要再改 resources.html。上文提到 resources.html 的地方都按 articles.html 理解。
- 全站导航统一为：How we help · About · Articles · Newsletter(中文：我们如何帮助 · 关于我们 · 文章 · 资讯简报)。
  文章页 "Related resources" 改为 "Related articles"。
- 新建 **Newsletter / 资讯简报** 页:newsletter.html / zh/newsletter.html。每月两期。页面有：简介、订阅表单、"每期内容"、往期列表(#issues)。
  目前往期列表是"第一期即将推出"的占位卡片;出第一期时，新建 newsletter/issue-01.html(及 zh/newsletter/issue-01.html),
  在 .issue-list 里按 HTML 注释中的模板加一张 .issue-card(最新的放最前),并删掉 .issue-empty。
- 订阅表单(首页和简报页)现在真正提交到 Formspree(https://formspree.io/f/xojggagy,与联系表单同一个),
  主题为 "New newsletter subscriber" / "资讯简报订阅",订阅邮箱会发到网站邮箱。之前的订阅表单只显示"谢谢"、并没有保存邮箱。

## 资讯简报（Newsletter）编辑方针 — 2026-10-22
- 每月两期：1 日「研究与发现 Research & Discovery」（阿尔茨海默病机制、早期诊断、生物标志物、治疗、临床试验）；
  15 日「心灵与人文 Mind & Humanity」（患者、家属、看护者的生活体验，结合脑科学、心理学、音乐、艺术、文学）。
- 三分钟读完，三个栏目：① The Discovery｜科学新发现（英文 120–150 词，一项研究，回答发现了什么/为什么值得关注/对普通人意味着什么，附原始研究链接，标证据类型）
  ② The Human Side｜人文视角（80–100 词） ③ Worth Exploring｜延伸阅读（40–60 词，推荐一篇网站文章或一项研究）。
- 配图：优先根据内容自制插图（放 newsletter/img/），或免费的公版原作；外部图片必须免费可用。
- 每期页面：newsletter/issue-NN.html、zh/newsletter/issue-NN.html；模板、选题记录(log.md)、每日科研跟踪(research-watch.md)、草稿都在 "Claude outputs/newsletter/"（不上传）。
- 每期须经站长确认后才发布；目前不群发邮件。
- 2026-10-22 补充：每期同时出 PDF 小册页（5.5×8.5 英寸，两页，中英文各一份，可打印收藏），发布在 newsletter/pdf/mindcadence-newsletter-NN-en.pdf / -zh.pdf，
  期刊网页上有"下载本期（PDF）"链接。每期内容写在一个 content.json 里，用 "Claude outputs/newsletter/kit/" 里的 make_issue.py + render_pdf.js
  一次生成网页和 PDF（见 kit/README.md）。旧的 template-*.html 已移到 old-templates/，不再使用。Word 版仅在有需要时另做。
- 2026-10-22：顶部导航去掉 "Come In / 进来看看" 按钮（与 Articles 重复）；首页大图里的 "Come In / 进来看看" 改为滚动到 #three（我们如何帮助），从头介绍网站。
  联系表单的输入框改为占满卡片宽度。
- 2026-10-22：资讯简报创刊号（第 1 卷第 1 期，2026-11-01）已定稿放入网站：newsletter/issue-01.html、zh/newsletter/issue-01.html，
  PDF 在 newsletter/pdf/，音乐与朗读在 newsletter/audio/（音乐 AudioCoffee《Peaceful Light Morning》，Pixabay；朗读 Ava/Tingting 录制），插图 newsletter/img/issue-01.svg。
  newsletter.html / zh 的往期列表已换成创刊号卡片。站长计划 11 月 1 日 push 上线。
  站长以后想用自己的声音朗读：她录好 mp3 放进当期草稿文件夹，在 content.json 的 "narration" 里填文件名即可。

## 音乐清单（2026-10-22 建立）
- "Claude outputs/MindCadence 音乐清单.xlsx"：每篇文章 / 每期简报一行（发布日期、类型、栏目、中英文标题、页面、音乐文件、音乐原名、作者、来源、时长、朗读文件、备注）。
- **每次新增文章或发布一期简报，都要在“音乐清单”表最后加一行**（中英文共用一首音乐只写一行）。不知道的信息填“（待补充）”并标黄。
- 该文件在 Claude outputs/ 里，不上传 GitHub；用 openpyxl 追加行，保持 Arial 字体和表格（Table "MusicList"）范围同步扩展。

## 2026-10-23 更新
- 网站联系邮箱改为 contact@mindcadence.org（全站 mailto 和显示文字）。Calendly 预约链接仍是 calendly.com/lindai-atl/30min。
  Formspree 表单（联系 + 订阅，同一个表单 "A New Form"）收件邮箱已于 10/23 改为 contact@mindcadence.org（Workflow → Email）。免费版：每月 50 次提交、最多 2 个关联邮箱。
- 中文用词：**所有"照护者"改为"看护者"**（全站已替换；以后新内容一律用"看护者"）。"照护"一词也已全部改为"看护"（10/23 站长要求），以后中文一律用"看护"。
- 首页"用可信的科学认识疾病"卡片：中文"清晰、准确地讲解大脑与神经系统疾病——用通俗的语言，讲清复杂的科学。"，英文 "…— complex science, in plain language."
- 资讯简报每月 1 日「研究与发现」扩展为：阿尔茨海默病 **及其他神经系统疾病** 的重要进展（简报页文字已改）。
- 资讯简报创刊号已从网站文件夹移出，暂存在 "Claude outputs/newsletter/drafts/issue-01/publish/"（和 out/），以便今天的其他改动可以先 push。
  11 月 1 日由提醒任务运行 kit/publish_issue.py 放回网站（期刊页、PDF、音频、往期卡片、首页"最新一期"）。
- 首页 Newsletter 区块有 `<!-- LATEST-ISSUE --><!-- /LATEST-ISSUE -->` 占位，publish_issue.py 会填入"最新一期"预览（样式 .latest-issue）。
- PDF 第二页左侧竖线改为浅绿色（print.css .p2::before），与第一页区分；第二页底部的图是第一页插图的下半部分（有意的呼应）。
- 2026-10-23：**Book a Call / 预约通话暂停**（站长很珍惜这个渠道，但目前先取消，以后需要时再加）。首页大图和联系卡片里的按钮已改成 HTML 注释保留，
  恢复时去掉注释即可。恢复时同时加上免责说明（草稿见对话：通话为非正式交流，不提供医疗/心理/法律建议，紧急情况拨 911，心理危机 988），并更新 Calendly 页面说明。
- 2026-10-23：资讯简报刊头语（站长定）：英文 "Where Brain Science Meets Human Life" / 中文"脑科学与人生相遇的地方"；
  副题 "Exploring the science of the mind and the beauty of being human" / "探索心智的科学，感受生命的人文之美"。
  用在：简报介绍页大标题+副题（.nl-tagline-sub）、每期网页期号上方（.nl-tagline）、PDF 第一页标志下（.p-motto）、PDF 第二页页脚。网站首页仍用原标语。
- 2026-10-26：创刊号中文版按站长修改定稿（科学新发现三段、人文视角）；参考文献统一为 "van Dyck CH, et al. (2023). Lecanemab in Early Alzheimer’s Disease. NEJM, 388(1), 9–21. https://doi.org/…"；中文朗读重录。
  英文人文视角保持原样（"Sing badly. Sing together." 在英文里自然，站长同意由 Claude 把关英文的语言与文化表达）。
  新增**横版 PDF**：第 1、2 页并排成一张 11×8.5 英寸横页（mindcadence-newsletter-NN-xx-spread.pdf，中英文都有），竖版照常保留；期刊网页有"横版（两页并排）"下载链接。render_pdf.js 自动生成。
  创刊号发布时间：11 月 1 日（周日）美东 8:30–9:00。
- 2026-10-27 中文文字微调（站长逐条定稿）：首页"关于脑韵"段落、"轻松读懂神经科学"卡片（"目前收录两篇文章"）、首页简报区块介绍、订阅说明
  （"你的邮箱地址只用于接收脑韵资讯简报，不会与第三方分享。你可以随时退订。"，首页和简报页都用）、联系卡片文字、
  导航/页脚"我们如何帮助"→"我们如何提供帮助"、简报页"每月两期"和"每期内容"各段、中文页脚标语改为"理解大脑，关怀生命"。
  中文全站称呼读者一律用"你"（不用"您"；文章里教读者对医生说的话除外）。
- 2026-10-28：首页栏目卡片**不再写篇数**（中英文的 "Two articles, so far" / "Nine stories, so far" / "目前共两篇"等都已取消；以后加文章也不要再写）。
  英文页脚标语 "Understanding, together." → "**Understanding the brain, caring for life**"（与中文"理解大脑，关怀生命"对应；22 页 + 简报工具）。
  中文简报介绍页顶部段落改为新说法（"写给患者、看护者……每月两期，每期只需三分钟阅读……可以一期一期收集成册。"）。
- 2026-10-28：疗愈栏目第二篇 **bachelor-three-graces.html / zh/bachelor-three-graces.html**（A Bachelor, Three Beauties, and a Song from Long Ago / 优胜美地的桃花运，Lindai 随笔，桌面"优胜美地"文件夹）。
  配图 bachelor-three-graces.jpg（友人照片，已获授权，文末注明）；背景音乐 bachelor-three-graces.mp3（Pixabay welc0mei0 "Piano Nostalgic Waltz"）；朗读用浏览器。
  中文稿小改：空格、"得来全不费工夫"、"不想不知道，记忆真奇妙"；原稿引用的两句歌词改为转述（歌词有版权；英文原稿本来就是转述）。
  新建疗愈目录页 healing-articles.html / zh/healing-articles.html；首页疗愈卡片和 healing.html 返回链接指向它；articles.html 加卡片；音乐清单已加一行。
- 背景音乐音量标准（2026-10-28）：新加的背景音乐一律用 ffmpeg loudnorm 统一到约 **-20 LUFS**（多数文章的音乐在 -20 ~ -22 LUFS）。
  例：ffmpeg -i 原文件.mp3 -af "loudnorm=I=-20:TP=-2:LRA=11" -ar 44100 -codec:a libmp3lame -b:a 128k -map_metadata -1 输出.mp3
  10/28 已把全站偏响的背景音乐统一调到约 -20 LUFS（首页 music、各文章、希望故事、创刊号音乐）；较轻的（-20 ~ -23.5）未动。
- 2026-11-01：创刊号（第 1 卷第 1 期）已用 publish_issue.py 放回网站（期刊页、PDF 竖版/横版、音频、往期卡片、首页最新一期），站长 push 上线。

## MindCadence 定位宣言（站长 2026-11-01 定，作为写文章、简报、改首页的指导原则；暂不全面改网站文字）
- 中文：**以关注阿尔茨海默病为起点，以脑科学为基础，以人文关怀为灵魂。**
- 英文：**Rooted in Alzheimer’s, grounded in neuroscience, guided by humanity.**
- 补充：科学给它深度，文学给它温度，音乐给它韵律。
- 将来若放到网站上，首选首页"关于脑韵 / About"那一段（标题"科学，应当准确、易懂，而且温柔"的上方或下方）。
- 2026-11-02：已放上首页"关于脑韵 / About"标题正下方（p.about-mission，styles.css 有对应样式；英文斜体衬线，中文正体）。原引言"每一个大脑都属于一个人……"保留。
- 音乐/图片致谢：先补全音乐清单（曲名、作者、来源），再建"致谢与鸣谢 / Credits"页面逐项列出，页脚放链接；不要写笼统的"主要来自 Pixabay"，除非已核实。
- 首页大标题上方小字（2026-11-01）：中文"初心 · 科学 · 人文"（站长选）；英文 "Purpose · Science · Humanity"（Claude 把关：与中文同为意译，单独出现也能看懂；"Rooted · Grounded · Guided" 留给完整宣言句使用）。

- 2026-11-01 首页“关于脑韵”段落定稿：创始人表述为“一位热爱写作的神经科学家” / "a neuroscientist who also loves to write"（创始人做过阿尔茨海默病、脊髓再生、脆性 X 综合征研究，论文发表于 PNAS）；前半句介绍创始人，后半句以“脑韵 / MindCadence”为主语；不用“我们”，英文不用 she（避免过于个人化，也适合以后多人参与）。其他页面提到创始人时保持同一说法。
- 2026-11-01 首页加"最近更新 / What's New"(大图正下方，大图上下留白略减):只放最新 3 条(类型 · 标题 · 日期)，"查看全部 →" 链到 articles.html。内容在 index.html / zh/index.html 的 `<!-- WHATS-NEW -->` 标记之间。发布简报时 kit/publish_issue.py 自动加入;发布新文章后运行 `python3 "Claude outputs/newsletter/kit/whats_new.py" . <文件名.html> <YYYY-MM-DD> "<EN 类型>" "<EN 标题>" "<中文类型>" "<中文标题>"`。

- 2026-11-03：看护者栏目第三篇 **feelings-memory.html / zh/feelings-memory.html**（She May Forget the Visit, but Not the Feeling / 忘了你说过的话，却记得你给的感觉），计划 11 月 10 日发布。
  研究解读：Feinstein 2010 PNAS、Guzmán-Vélez 2014 Cogn Behav Neurol、Klein-Koerkamp 2012 综述；署名"脑韵团队"/"The MindCadence Team"，朗读用浏览器。
  配图 feelings-memory.jpg（站长用 ChatGPT 生成，原文件 ChatGPT Image Nov 3, 2026, 07_17_59 PM.png）；背景音乐 feelings-memory.mp3（原 billy_ziogas-slow-jamming-master-track-240885，Pixabay；这首节奏感强、几乎没有轻重起伏，按 -20 LUFS 听着偏响，站长反馈后调到约 -24 LUFS）。
  已加入 articles.html、caregivers-articles.html（目录第 03 篇）及中文版，首页"最近更新"已加（日期 11/10）；音乐清单已加一行。
- 2026-11-03：音乐清单补全——站长"下载"文件夹里的原始文件经声音比对，确认首页、healing、hope、MomColdWarm、MomWork、MomPalm、MomSea 的原曲（来源标"Pixabay（待核实）"）；补上漏记的 bachelor-three-graces 一行。随后合并了站长自己补充的记录（来源均为 Pixabay；作者名 Ieberch 统一为 leberch）。仍不明：MomMiss 曲名、caregivers 曲名与作者；brain-health 待确认（见清单备注）。

- 2026-11-13 排期调整（站长定）：新栏目「脑韵随笔 · 心灵小憩」/ MindCadence Notes — A Moment's Rest，11/20 以《漫漫的秋日》开篇上线。
  「专家来函」（名称待定）先做好但不放导航、首页和文章列表，有一两篇稿子后再上线。
  12/1 简报；12/10 看护者文章（照顾好自己）；12/15 简报「节日聚会，怎样让失智的家人也自在参与」；12/20 健忘文章。
  feelings-memory 两个语言版本里"下一篇文章"的预告已改为"之后会专门写一篇"。

## 2026-11-13 新栏目「脑韵随笔 · 心灵小憩」（在 autumn-day 分支上，11/20 合并上线）
- 栏目目录页 notes-articles.html / zh/notes-articles.html（英文 MindCadence Notes — A Moment's Rest），文章总页筛选新增 "MindCadence Notes / 脑韵随笔"（data-topic="MindCadence Notes"），首页精选文章加第 7 张卡片。
- 首篇 autumn-day.html / zh/autumn-day.html（The Long Autumn Day / 漫漫的秋日，Lindai 随笔，来源桌面 AutumnDay 文件夹；英文署名 Lindai，中文不署名）。
  首页栏目卡片用 notes-cover.png（Claude 用代码绘制，与其他栏目封面同色调）；文章配图 autumn-day.jpg（AI 生成，头图下注明 "Illustration created with AI / 插图由 AI 生成"，styles.css 新增 .hero-caption）；音乐 autumn-day.mp3（alex-morgan《Autumn Leaves Falling》，Pixabay，约 -20 LUFS）；朗读用浏览器。
  中文稿小改三处（顿号、"传统门诺派"、"近在咫尺的现代生活"），英文标题加冒号。首页"最近更新"日期 2026-11-20。
- **上线方法**：这些改动都提交在 git 分支 autumn-day，main 上没有。11/20 在 main 上运行 `git merge autumn-day`（若 15 号简报改过 index.html，"最近更新"一段可能冲突，按日期顺序合并即可），再由站长 push。
