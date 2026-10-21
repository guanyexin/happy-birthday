# 🎂 Happy Birthday

一个送给老婆的生日页面 · A single-file birthday page.

**在线地址：** https://guanyexin.github.io/happy-birthday/

## 怎么改

全部内容都在 `index.html` 里，零依赖、无外链，打开就能看。

### 1. 改名字 / 在一起的天数

文件底部 `<script>` 开头有个 `CONFIG`：

```js
const CONFIG = {
  name: "老婆",              // 改成她的名字或昵称
  togetherSince: "",        // 填 "2019-05-20" 会显示"一起走过第 N 天"
  wish: "愿你所求皆如愿……"   // 吹灭蜡烛后弹窗里的愿望
};
```

### 2. 改那封信

搜索 `<!-- ============ LETTER ============ -->`，下面的 `<p>` 段落直接改文字。

### 3. 换成真实照片

1. 新建 `images/` 文件夹，把照片放进去（建议宽 600px 左右，别超过 500KB，加载快）
2. 搜索 `我们的照片墙`，把那三个 `<div class="ph">📷</div>` 换成：

```html
<div class="ph"><img src="images/photo1.jpg" alt="" style="width:100%;height:100%;object-fit:cover;border-radius:2px"></div>
```

### 4. 想换音乐？

生日歌是用 Web Audio 实时合成的（`playMelody()` 函数里的 `seq` 音符表），不需要音频文件。
想换成自己录的一段话或真实的歌，就把 mp3 放进仓库、用 `<audio>` 标签，然后改 `#musicBtn` 的点击事件。

## 小玩法

- 🕯️ 点亮着 5 根蜡烛，点一下就吹灭一根，全吹灭 → 彩带 + 愿望弹窗 + 生日歌
- 🎵 首页按钮可以单独播放合成的生日歌（手机需先点一下，浏览器才允许放声音）
- ✨ 星空、飘浮的心、极简响应式，手机打开也好看

---

Made with ❤️
