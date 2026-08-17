# BrainBridge — Project Guide

## 品牌定位
BrainBridge 帮助人们通过可信的科学、有温度的写作和富有同理心的引导,
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
- index.html —— 首页(Hero 大图、三种帮助方式、关于 BrainBridge、精选文章、
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

## 视觉规范
配色 hex、字体规范、间距等所有 visual specs 一律参考 design-system.md,
不在本文件中重复。
