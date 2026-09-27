# 贪吃蛇 · 小游戏

一个用 HTML5 Canvas 写的极简贪吃蛇。**只有一个 HTML 文件**，不需要联网、不需要安装任何东西。

## 玩法

- `↑` `↓` `←` `→` 或 `W` `A` `S` `D` 控制方向
- 也可以点画面下方的方向按钮（触屏、手机可用）
- 吃到红球：变长、得分 +1
- 撞墙：从对面穿出去
- 咬到自己：游戏结束
- `R` 键或「重新开始」按钮：重来

> 打开后先用鼠标点一下游戏画面，键盘才会有反应（浏览器需要页面获得焦点）。

## 文件

| 文件 | 说明 |
| --- | --- |
| `index.html` | 整个游戏。样式、逻辑、图标全部在这一个文件里 |
| `README.md` | 这份说明 |

## 想改点什么

用记事本或 VS Code 打开 `index.html`，代码里有中文注释。

常用参数在 `<script>` 开头：

```js
const CELL = 20;    // 每格 20 像素，改它要同时改 canvas 的 width / height
const SPEED = 5;    // 蛇每秒走几格，数字越大越快
```

想换颜色，就在 `draw()` 函数里改这几个色值：

| 色值 | 用在哪 |
| --- | --- |
| `#1f6b45` | 蛇头 |
| `#48a868` | 蛇身 |
| `#e0574c` | 小球 |
| `#fafaf7` | 背景 |

改完保存，刷新浏览器就能看到效果。

## 放到网上（GitHub Pages，免费）

1. 注册并登录 [github.com](https://github.com)
2. 右上角 `+` → `New repository`
3. 仓库名填 `snake-game`，选 **Public**，点 `Create repository`
4. 在新仓库页面点 `uploading an existing file`，把 `index.html` 和 `README.md` 拖进去，点 `Commit changes`
5. 进入仓库的 `Settings` → 左侧 `Pages`
6. `Source` 选 `Deploy from a branch`，`Branch` 选 `main` 和 `/ (root)`，点 `Save`
7. 等 1 分钟左右刷新，页面顶部会出现网址，形如
   `https://你的用户名.github.io/snake-game/`

这个网址任何人都能打开，手机也能玩，而且长期有效。

## 更新网站内容

以后想改内容，回到仓库，点开 `index.html`，点铅笔图标编辑，改完提交，网站会在 1 分钟内自动更新。
