# My-Typora-Themes



---

> [Update on 2021-07-24]
>
> 新增主题：`G2`

`G2` 就是 `Github2` 的意思，原主题看久了有点审美疲劳，所以在默认主题 github 的基础上捣鼓了一款新的主题，力求简洁，并且加上了标题自动编号（关闭代码行号效果最佳），字体文件夹则是沿用原来的 `zj` 文件夹。

![QQ图片20210724140414](http://pic.theigrams.cn/20210724140505.jpg?imagslim)


___



> 如果GitHub图片加载不出来，可以去知乎看 https://zhuanlan.zhihu.com/p/133863913.

这是我写的一个Typora主题，基本上是由 `pie` 和 `ursine-polar` 修改而来，使用方法请参看Typora的帮助手册。

## 前言

Typora可谓是我最喜欢的Markdown编辑器了，可惜其自带的样式实在过于简陋，我到官网上把所有主题都下了一遍，其中**[少数派](https://link.zhihu.com/?target=https%3A//sspai.com/post/43873)**的主题应该是最好康的了，可在我的电脑上显示出来有些怪怪的，最后还是忍不住动手修改了一遍，终于心满意足了。


以下是实际笔记效果：

![img](https://pic1.zhimg.com/v2-173163ac793fbcda62af0f6f3d895a08_r.jpg)

![img](https://pic2.zhimg.com/v2-99f8f27984d0e1d1f1662a27cadbda41_r.jpg)

![img](https://pic2.zhimg.com/v2-7459caa13776f9a83f138ead20031361_r.jpg)

## 字体

首先因为我感觉字体有点小，就把正文换成了17号字体。

```css
html {
    font-size: 17px;
}
```

然后修改了一下字体（如果是Mac用户的话，可以把下面第二行注释掉，因为自带的苹方字体就很好看）。

```css
body {
    font-family: "Vollkorn", Palatino, Times;
    /* font-family: 'Source Han SerifCN', Georgia, Times, 'SimSun', serif!important; */
    color: var(--mid-13);
}
```



## 标题

我认为标题可以说是整个样式中最重要的一部分，因为正文基本上都差不多。

![img](https://pic2.zhimg.com/v2-6172c76a27bde96e4c2342796352c921_r.jpg)

一级标题一般对应一本书中的Chapter，故局中表示。一般来说一个md文档中最好只有一个一级标题，如果有内容包含多个章节的话，则应该拆成多个md文档。

二级标题对应section，因此带着一条长长的横线用来分隔。

三级标题是最常用的小标题subsection，微信中只支持到三级标题，在实际的短篇写作中一般也到此为止了。因此不宜花里胡哨，要做到又显目又低调，又精致又普通（～～以及五彩斑斓的红与黑～～这段删去）。

四五六级标题一般用不到，随便糊弄一下就好了。



## 文本样式

![img](https://pic2.zhimg.com/v2-3b263b633366f0dec168b44877c6880d_r.jpg)

对于行内公式，为了醒目和易于查找修改，我特意调成了蓝色（导出时依然是黑色）。

行间代码块则以简约的线条为主，用一条深红的竖线分隔行号与代码，显得很清爽。

因为中文的`斜体`作用几乎为0，因此我把它改成了「显示红色」的效果。

引用块则是大块的淡红色。



## 列表与表格

![img](https://pic2.zhimg.com/v2-aef79f96d7a55254258f7f39970e2001_r.jpg)

把列表和表格都改成了符合主题的红色（不知道为什么，大部分笔记软件默认主题都是红色，例如Notion）。



## 导出PDF优化

其实我很喜欢在写完笔记之后，导出成PDF欣赏或分享给别人，但typora导成PDF的样式和编辑时的样式区别很大，因此我特意设置了一番。

人在看电子屏幕时，更喜欢无衬线体，能给人一种休闲轻松的感觉。

但在阅读严肃正经的内容时，衬线字体更合适，因此我将导出PDF的字体改成了宋体+TimesNew，看起来更有感觉。

![img](https://pic2.zhimg.com/v2-15e30641f95416a64934a53d41293df9_r.jpg)

## 更新记录

### 2020年10月27日更新

- 微调了列表排版

- 微调表格颜色

- 修改二级标题样式

- 修复5级标题和6级标题没对齐的bug

- 修改行内公式颜色为蓝色（为了醒目，导出PDF时仍为黑色）

- 修改超链接为蓝色样式

- 优化了导出PDF的样式效果
  - 设置导出的中文字体为`思源宋体`，英文字体为`Georgia`
  
  

可以通过以下设置修改行内公式颜色和大小：

```css
[md-inline='inline_math'] {
    color: blue;
    font-size: 100%;
}
```

> 注意：在极少数情况下，会出现PDF导出失败的问题，等我吃完饭就来改这个bug


---

### 2020年10月28日更新

- 调小了2,3级标题样式的大小
- 默认导出PDF为`宋体`+`Times New`

> 导出PDF失败似乎是思源宋体的原因，因此将默认输出样式修改之后就OK了。



如果导出字体过大，可以搜索如下代码，将下面第6行中的字体调小（大概在原CSS的755行）。

> 在设置中把字体大小改成自动，否则打印字体大小就无法调节了

```css
@media print {
    .typora-export * {
        -webkit-print-color-adjust: exact;
    }
    html {
        font-size: 15px!important;
    }
}
```

