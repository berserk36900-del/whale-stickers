# whale-stickers

鲸鱼娘（DeepSeek娘 / 蓝色大肥鱼）表情包库，给聊天机器人用的。

形象是社区二创里的公开设定：蓝发、鲸尾、深蓝白女仆裙，圆滚滚爱摸鱼的那只。

## 里面有什么

```
stickers/whale-<编号>.jpg   56 张，统一 512×512 方形，JPEG q88
index.json                  编号 → 情绪标签 / 原始台词 / 来源
```

`index.json` 每条形如：

```json
"079": {
  "file": "stickers/whale-079.jpg",
  "emotion": "得意",
  "caption": "DeepSeek娘『最强』自信得意表情包",
  "source": "https://img.aigengtu.com/meme/079.webp"
}
```

## 怎么用

直链格式：

```
https://gcore.jsdelivr.net/gh/berserk36900-del/whale-stickers@main/stickers/whale-079.jpg
```

- **聊天机器人**：在回复里写 `![](上面这个链接)`，平台会自己去拉图。图片必须是公网可访问的直链。
- **手动斗图**：浏览器打开链接就能存。

### CDN 说明（重要）

不要用 `cdn.jsdelivr.net` 主域——它对新仓库/未缓存路径会 `301` 跳到 `raw.githubusercontent.com`，国内大概率拉不到。用这两个节点之一，直接返回图片：

```
https://gcore.jsdelivr.net/gh/...
https://testingcf.jsdelivr.net/gh/...
```

引用前先验一下：

```bash
curl -s -o /dev/null -w "%{http_code}\n" "https://gcore.jsdelivr.net/gh/berserk36900-del/whale-stickers@main/stickers/whale-079.jpg"
```

要 200，不是 200 就别用。

## 怎么加图

1. 图片裁成方形、缩到 512×512，存成 JPEG
2. 命名 `stickers/whale-<编号>.jpg`，编号不要和已有的重复
3. 在 `index.json` 里补一条：情绪标签写"这张图在表达什么"（得意 / 翻白眼 / 累死 / 糊弄…），不要写搜索关键词
4. 提交后等缓存刷新（约一刻钟），再验一次 200

## 素材来源与授权

图来自梗鲸（aigengtu.com）收录的社区二创，逐张人工筛过：去掉低分辨率、立绘/设定图、露骨内容。
鲸鱼娘原始设定由社区作者创作，公开约定为非商业二创使用。

**仅限非商业用途的群聊斗图。** 商用或再分发前请自行确认原作者授权。
