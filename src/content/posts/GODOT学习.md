---
title: GODOT学习之2D game
published: 2025-09-13
description: "Godot"
image: "/images/Godot2Dsample.png" #本地图片
tags: [Godot]
category: "学习"
draft: false 
---

<style>
.photo {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
}

.photo img {
    margin: 0;
    max-width: 100%;
}

.photo p {
    font-size: 10px;
}
</style>

# 教学视频

<iframe width="100%" height="468" src="//player.bilibili.com/player.html?isOutside=true&aid=113719677884016&bvid=BV1JuCrYcEvJ&cid=27543930756&p=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"></iframe>
<br>

# 1. 场景搭建

## 🌟游戏场景  
### >Root Node

根节点下方有多个子节点，每个子节点下面也可有对应多个子节点，以此类推……

点击 `2D场景` 创建2D节点作为根节点。

### >Sprite Node

点击场景树左上角的 `+` 或者快捷键 **Crtl + A** 打开节点面板以添加节点；
此处搜索Sprite，创建 `Sprite2D` node，用以显示图片。

将图片拖动至Node的Texture里面，观察窗即可显示图片。

PS: 左上角 `项目`->`项目设置`->`渲染`->`纹理`->`默认纹理过滤`->`Nearest`，这样像素背景便会变得清晰。

快捷键 **[W]** 进入移动模式即可拖动鼠标移动当前选中节点， **[Shift + W]** 可限制水平/垂直移动， **[Ctrl + D]** 可复制节点配合移动可以扩大背景图； **[Q]** 退回选择模式， **[Ctrl + S]** 保存场景，建议保存至分类好的Scenes场景文件夹；**[F5]** 可运行游戏。

### >Camera2D Node

若想将场景渲染在正中央，需要添加 `Camera2D` node，拉远视角即可发现渲染范围（粉色方框）；选中该节点，在 `zoom` 修改数值/LMB拖拽可渲染全图范围。

Don`t forget to SAVE **[Ctrl + S]** , then run the game **[F5]** .

And if u dont want to mess with so many nodes, use **[Ctrl + L]** to lock the node chosen.

## 🌟AnimatedSprite2D Node

一般玩家节点单独保存为一个独立场景，如此，当需要修改玩家数值时，修改玩家场景中数值即可。

在观察窗上方 `+` 创建新场景，添加 `CharacterBody2D` node，完成后再添加Sprite中 `AnimatedSprite2D` node，右侧栏属性 `Animation`->`SpriteFrames`->`新建SpriteFrames`

下方栏 `SpriteFrames`->`从精灵列表中添加帧`（网格状按钮），找到对应文件夹的玩家图，设置好对应水平/垂直数量来自动切割SpriteSheet，根据切割好的对应行选择一系列图片添加帧。

点击播放按钮即可播放预览动画，可增加帧率以提速，双击动画名称即可改名；待机动画（idle）：设置完成后，勾选自动播放按钮，玩家便可在游戏运行时自动播放待机动画。

添加玩家至主场景：场景树左上角点击链接按钮，找到玩家场景即可；在场景树中找到玩家节点，点击在编辑中打开即可快速跳转玩家场景编辑。

# 2. GD Script Coding


# 3.碰撞体



创建根节点[Node 2D]
use Ctrl+A 添加子节点
Find [Sprite2D]

