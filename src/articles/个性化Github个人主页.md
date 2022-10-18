---
title: Github个人主页
tag: Github
date: 2020-11-14
category: Github
---

刚了解到Github可以通过创建和用户名相同的仓库，在个人主页上显示这个仓库的**README.md**

<!-- more -->

这是新建Repo的描述

> You found a secret! pinguo-zhouwei/pinguo-zhouwei is a ✨special ✨ repository that you can use to add a README.md to your GitHub profile. Make sure it’s public and initialize it with a README to get started.

---

# 于是

没事干的我在[知乎](https://www.zhihu.com/question/23498424?sort=created)上找有趣的项目,看到这位[大佬](https://github.com/tw93)的主页，经过无脑乱塞，于是就有了[Sanksu/Sanksu](https://github.com/Sanksu/Sanksu)

---

# build_readme.py

用Github Actions跑Python脚本
运行build_readme.py，执行
- 检索所有存储库中每个release的最新版本
- 通过博客的feed.xml获取最近5篇博文
- 通过豆瓣的feed: rss 2.0 获取我的收藏
- 获取显示在gist上的WakaTime每周语言使用统计
- 获取显示在gist上的steam游戏时长统计(后来加的)

在build_readme.py加了几行
```
def fetch_play_time():
    return httpx.get(
        "https://gist.githubusercontent.com/Sanksu/f47f02e2f4f067be39427ed9d76bc9cd/raw/"
    )
```

```
    play_time_text = "\n```text\n"+fetch_play_time().text+"\n```\n"

    rewritten = replace_chunk(rewritten, "play_time", play_time_text)
```

在README.md加了这

```
#### 🎮 <a href="https://gist.github.com/Sanksu/f47f02e2f4f067be39427ed9d76bc9cd" target="_blank">Steam playtime leaderboard</a>

<!-- play_time starts -->

```text
🔫 Counter-Strike: Global Offensive 🕘 378 hrs 41 mins
🍳 PLAYERUNKNOWN'S BATTLEGROUNDS    🕘 235 hrs 57 mins
🔫 Tom Clancy's Rainbow Six Siege   🕘 125 hrs 2 mins
🎮 Sea of Thieves                   🕘 41 hrs 27 mins
🎮 Counter-Strike                   🕘 17 hrs 48 mins
``` (删掉我)

<!-- play_time ends -->
```

就像这样![](https://cdn.jsdelivr.net/gh/sanksu/Blog-Old@master/image/github/github_2020-11-14_20-20-26.png)
