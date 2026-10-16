# MindCadence 脑韵 — Project Guide

网站名:英文 MindCadence(连写),中文"脑韵"。主域名 mindcadence.org
(另有 rhythmofmind.org / rhythmofmind.online / rhythmofbrain.com,均跳转到主域名)。
中文页标志显示"脑韵 MindCadence";中文正文里单独提到品牌时只写"脑韵"。
旧名 BrainBridge、旧网址 brainbridge-nine.vercel.app 已停用。

## 品牌定位
MindCadence 帮助人们通过可信的科学、有温度的写作和富有同理心的引导,
更好地理解大脑、疾病、照护与生活。让脑科学连接普通人的真实生活。

## 目标受众
希望更好理解生活的人 —— 尤其是患者、照护者、家属,以及对神经科学感兴趣的读者。

## 我们提供什么
- 脑健康科普:用平实语言解释大脑与神经疾病
- 研究解读:把前沿神经科学转化为可读、可信的内容
- 照护支持:给家属与照护者的实用、温柔的指引
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

## 视觉规范
配色 hex、字体规范、间距等所有 visual specs 一律参考 design-system.md,
不在本文件中重复。
