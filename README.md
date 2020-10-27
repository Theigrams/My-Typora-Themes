# My-Typora-Themes

这是我写的一个Typora主题，基本上是由 `pie` 和 `ursine-polar` 修改而来，使用方法请参看Typora的帮助手册。

![shadow-MD_CSS](https://i.loli.net/2020/04/21/BrbJq6mpT58WHof.png)

首先因为我个人偏爱 `TimesNew` 字体，所以文中的英文字体全换成了 `TimesNew` 字体，然后感觉字体有点小，就把正文换成了17号字体。

其实主要修改的就是标题的样式，我写完4级标题的样式后，一直苦恼5级和6级标题的样式该怎么写，后来我想了一下，我一般用LaTeX也顶多是用到`\subsubsection`，也就是刚好4级，所以就基本上不需要考虑后面的情况了。可以看到我把4级标题设成了一个框，也就是希望把它作为最小的标题。

![shadow-f14](https://gitee.com//theigrams/FigureUpload/raw/master/https://gitee.com/theigrams/FigureUpload/f1.png)



这就是标题样式的CSS代码，其中`--main-6`是 `pie主题` 设置的主颜色，因为我是在它的基础上修改的，就干脆直接拿过来用了。

```css
h1 {
    text-align: center;
    padding-bottom: 0.3em;
    font-size: 2.2em;
    line-height: 1.2;
    margin: 2.4em auto 1.2em;
    color: var(--main-10);
  }

h1:after {
  content: '';
  display: block;
  margin: 0.2em auto 0;
  width: 100px;
  height: 2px;
  border-bottom: 2px solid var(--main-6);
}

h2 {
    margin: 2em auto 1.4em;
    padding-left: 10px;
    line-height: 1.4;
    font-size: 2em;
    border-left: 9px solid var(--main-6);
    border-bottom: 1px solid var(--main-6);
  }

h3 {
    font-size: 1.6rem;
    line-height: 1.43;
    margin: 1.6em auto 1.2em;
    padding-left: 9px;
    border-left: 5px solid var(--main-6);
}
```

然后是稍微修改了一下引用和行间代码，因为中文的`斜体`作用几乎为0，因此我把它改成了「显示红色」的效果，然后就是代码块的显示，稍微修改了一点点，就显得很清爽。


![shadow-f2](https://gitee.com//theigrams/FigureUpload/raw/master/https://gitee.com/theigrams/FigureUpload/f2.png)



看到下面这个红红的 `列表` 了么？没错，就是我从 `ursine-polar` 偷过来的😆。

![shadow-f3](https://gitee.com//theigrams/FigureUpload/raw/master/https://gitee.com/theigrams/FigureUpload/f3.png)

而图片的阴影效果是从`pie` 那偷来的，我只是稍微加强了一下阴影效果。

只需要在图片的名称前带上`shadow` 就能开启阴影效果，例如：
```markdown
![shadow-f3](https://github.com/Theigrams/My-Typora-Themes/blob/master/figure/f3.png)
```

然后稍微修改了一下表格的样式，既然追求又红又专，那就贯彻到底喽。

最后，里面应该还有很多可改进的地方，欢迎大家来使用或修改。

----

图中列表环境缩进过大、图片与表格没对齐的原因找到了，是因为我设置了首行缩进。。。

---

### 2020年10月27日更新

- 微调了列表排版
- 微调表格颜色
- 修改二级标题样式
- 修复5级标题和6级标题没对齐的bug
- 修改行内公式颜色为蓝色（为了醒目，导出PDF时仍为黑色）
- 修改超链接为蓝色样式
- 优化了导出PDF的样式效果
  - 设置导出的中文字体为`思源宋体`，英文字体为`Georgia`
  - 可以通过取消第766行的注释，设置导出字体为`宋体`+`Times New`
- 也可以取消第51行的注释，将书写样式和导出样式调整一致
  （个人认为思源宋体在书写时，阅读效果不是很好）、

> 注意：更新时，因为新添了思源宋体，所以请将`zj`文件夹一并更新
>
> 思源宋体压缩包为 `SiYuanSongTi.zip`

可以通过以下设置修改行内公式颜色和大小：

```css
[md-inline='inline_math'] {
    color: blue;
    font-size: 100%;
}
```

> 注意：在极少数情况下，会出现PDF导出失败的问题，等我吃完饭就来改这个bug

