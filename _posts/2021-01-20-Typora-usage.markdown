---
layout: post
title: "Typora usage"
date:  2021-01-20 17:34:52 +0800
categories: tool
tags: typora
---
Typora是一个很好的markdown编辑器，windows、Mac和Linux都可以安装。个人认为Typora最大的好处就是支持及时渲染，语句输完，回车，解释器就立马给你呈现出来渲染结果，非常的方便。接下来就列举Typora中的一些常用的使用语法。

* 插入目录

  ~~~
  Typora是可以插入目录的，它会将你所有的标题都呈现出来，使得读者对你的文章结构了解的更加清晰，语法：
  [toc]
  ~~~

* 标题

  ~~~
  用 # 来标识标题，建议在标题标识符"#"后面加一个空格，这是标准的markdown语法，一共有六级标题，如下所示：
  # 一级标题
  ## 二级标题
  ...
  ###### 六级标题
  ~~~

* **加粗**

  ~~~
  加粗用左右两边各两颗*来描述：
  **加粗**
  ~~~

* *斜体*

  ~~~
  斜体用左右两边各一颗*来描述：
  *斜体*
  ~~~

* ***斜体加粗***

  ~~~
  用左右两边各三颗*来描述：
  ***斜体加粗***
  ~~~

* `monospace`

  ~~~
  `monospace`
  ~~~

* bullet list

  ~~~
  语法：
  - apple
  - orange
  - pear
  ~~~

  效果：

  - apple
  - orange
  - pear

* block quote

  ~~~
  语法：
  > First sentence
  > Second sentence
  ~~~

  效果：

  > First sentence
  >
  > Second sentence

* 行内公式

  ~~~
  有些环境默认没有打开行内公式，需要修改一下设置，我的win10就没有打开这个设置。设置方法：
  打开Typora --> 文件 --> 偏好设置 --> Markdown --> Markdown扩展语法 --> 勾选上内联公式、下标、上标等你需要的选项 --> 重启Typora
  本行有一个公式$x^2+y^2=z^2$
  ~~~

  本行有一个公式$x^2+y^2=z^2$

* 行间公式

  ~~~
  $$
  t=\frac{-b\pm\sqrt{b^2-4ac}}{2a}
  $$
  ~~~

  $$
  t=\frac{-b\pm\sqrt{b^2-4ac}}{2a}
  $$

* 插入图片

  ~~~
  ![figure](/img/freedom.jpg)
  ~~~

  ![figure](https://raw.githubusercontent.com/memory118/memory118.github.io/master/_posts/TyporaUsage/freedom.jpg)

* 插入链接

  ~~~
  [memorywu](www.memorywu.com)
  ~~~

  [memorywu](www.memorywu.com)

* 代码块

  ~~~
  ​~~~
  apha = 5
  if alpha > 0:
  	print("alpha is a positive number")
  ​~~~
  ~~~

  ~~~
  apha = 5
  if alpha > 0:
  	print("alpha is a positive number")
  ~~~

* 横向流程图

  ~~~
  ​~~~mermaid
  graph LR
  A[first step] --> B[Second step]
  	B --> C{condition i}
  	C --> |i>0| D{return True}
  	C --> |i<=0| E{return False}
  F[横向流程图]
  ​~~~
  ~~~

  ~~~mermaid
  graph LR
  A[first step] --> B[Second step]
  	B --> C{condition i}
  	C --> |i>0| D{return True}
  	C --> |i<=0| E{return False}
  F[横向流程图]
  ~~~

* 竖向流程图

  ~~~
  ​~~~mermaid
  graph TD
  A[first step] --> B[Second step]
  	B --> C{condition i}
  	C --> |i>0| D{return True}
  	C --> |i<=0| E{return False}
  F[横向流程图]
  ​~~~
  ~~~

  ~~~mermaid
  graph TD
  A[first step] --> B[Second step]
  	B --> C{condition i}
  	C --> |i>0| D{return True}
  	C --> |i<=0| E{return False}
  F[竖向流程图]
  	D --> G[end]
  	E --> G
  ~~~

* 折叠显示

  ~~~
  <details>
      <summary>folder</summary>
      <pre>
      first line
      second line
      third line
      ...
      </pre>
  </details>
  ~~~

  <details>
      <summary>folder</summary>
      <pre>
      first line
      second line
      third line
      ...
      </pre>
  </details>

* 标准横向流程图

  ~~~
  ```flow
  st=>start: 开始
  op=>operation: 处理
  cond=>condition: 判断
  sub1=>subroutine: 子流程
  io=>inputoutput: 输入输出
  e=>end: 结束
  st(right)->op(right)->cond
  cond(yes)->io(bottom)->e
  cond(no)->sub1(right)->op
  ```
  ~~~

  ```flow
  st=>start: 开始
  op=>operation: 处理
  cond=>condition: 判断
  sub1=>subroutine: 子流程
  io=>inputoutput: 输入输出
  e=>end: 结束
  st(right)->op(right)->cond
  cond(yes)->io(bottom)->e
  cond(no)->sub1(right)->op
  ```

* 标准竖向流程图

  ~~~
  ```flow
  st=>start: 开始
  op=>operation: 处理
  cond=>condition: 判断
  sub1=>subroutine: 子流程
  io=>inputoutput: 输入输出
  e=>end: 结束
  st->op->cond
  cond(yes)->io->e
  cond(no)->sub1(right)->op
  ```
  ~~~

  ```flow
  st=>start: 开始
  op=>operation: 处理
  cond=>condition: 判断
  sub1=>subroutine: 子流程
  io=>inputoutput: 输入输出
  e=>end: 结束
  st->op->cond
  cond(yes)->io->e
  cond(no)->sub1(right)->op
  ```

  

* 表格

  ~~~
  |  ID  | 姓名 | 性别 | 分数 |
  | :--: | :--: | :--: | :--: |
  |   12345   |   张三   |   男   |   120   |
  |   12346   |   李四   |   男   |   115   |
  |   12347   |   王五   |   男   |   136   |
  |   12348   |   刘六   |   女   |   128   |
  ~~~

  |  ID  | 姓名 | 性别 | 分数 |
  | :--: | :--: | :--: | :--: |
  |   12345   |   张三   |   男   |   120   |
  |   12346   |   李四   |   男   |   115   |
  |   12347   |   王五   |   男   |   136   |
  |   12348   |   刘六   |   女   |   128   |

* 本地视频

  ~~~
  <video id="video" controls="" preload="none">     
      <source id="mp4" src="../videos/typora_usage.mp4" type="video/mp4"> 
  </video>
  ~~~

  <video id="video" controls="" preload="none">     
      <source id="mp4" src="https://raw.githubusercontent.com/memory118/memory118.github.io/master/_posts/TyporaUsage/typora_usage.mp4" type="video/mp4"> 
  </video>

* 网络视频

  ~~~
  <iframe height=450 width=800 src="https://www.bilibili.com/video/BV1uK41137Kb"> 
  ~~~

  <iframe height=450 width=800 src="https://www.bilibili.com/video/BV1uK41137Kb"> 

