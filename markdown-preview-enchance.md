---
export_on_save:
  html: true
---
<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->
<!-- code_chunk_output -->

* [标准标题写法](#标准标题写法)
* [扩展标题写法](#扩展标题写法)
* [列表](#列表)
	* [无序列表](#无序列表)
	* [有序列表](#有序列表)
* [任务列表](#任务列表)
* [表格](#表格)
* [Emoji](#emoji)
* [上标](#上标)
* [下标](#下标)
* [脚注](#脚注)
* [缩略](#缩略)
* [标记](#标记)
* [数学](#数学)
	* [Accents](#accents)
* [流程图](#流程图)
	* [Flow Charts](#flow-charts)
	* [sequence](#sequence)
	* [mermaid](#mermaid)
	* [puml](#puml)
	* [wavedrom](#wavedrom)
	* [dot && viz](#dot-viz)
	* [Vega && Vega-lite](#vega-vega-lite)
	* [Ditaa](#ditaa)
	* [导入外部文件](#导入外部文件)

<!-- /code_chunk_output -->

## 标准标题写法
# 这是 `<h1>` 一级标题  {ignore=true}
## 这是 `<h2>` 二级标题  {ignore=true}
### 这是 `<h3>` 三级标题  {ignore=true}
#### 这是 `<h4>` 四级标题  {ignore=true}
##### 这是 `<h5>` 五级标题  {ignore=true}
###### 这是 `<h6>` 六级标题  {ignore=true}

## 扩展标题写法
# 这个标题拥有一个 id # {#my_id ignore = true}
# 这个标题拥有二个 classes # {.class1 .class2 ignore = true}

*这会是 斜体 的文字*
_这会是 粗体 的文字_

**这会是 粗体 的文字**
__这会是 粗体 的文字__

_你也可以 **组合** 这些符号

~~这个文字将会被横线删除~~

## 列表
### 无序列表
 * Item1
 * Item2
 * Item3
    * Item3_1
    * Item3_2
### 有序列表
1. Item1
2. Item2
3. Item3
    1. Item3a
    2. Item3b

![GitHub_log](https://ss2.baidu.com/6ONYsjip0QIZ8tyhnq/it/u=906931310,2403105860&fm=58&bpow=1334&bpoh=750)
Format: ![Alt Text](url)
[GitHub](http://github.com)

正如 Kanye West 所说
> We're living the future so
> the present is out past.
---
***
___

`<addr>`

```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```
```java
class Test implements Serializable {
  private static final long serialVersionUID = 42l;
  public static void main(String[] args) {
    System.out.println("Hello World!");
  }
}
```

```javascript {.line-numbers}
function add(x, y) {
  return x + y
}
```

## 任务列表
- [x] todo
- [ ] add ass,vtt
- [x] markdonw

## 表格
| First Header       | Second Header                |
| ------------------ | ---------------------------- |
| Content from ceil1 | Content in the second column |
|                    |                              |

colspan `>` or `empty ceil`:
| a   | b   |
| ---| --- |
| 1   | 2   |
| ^   | 4   |
## Emoji
:smile:
:fa-car:

## 上标
30^th^

## 下标
H~2~O

## 脚注
Content [^1]
[^1]: Hi! This is a footnote

## 缩略
*[HTML]: Hyper Text Markup Language
*[W3C]: World Wide Web Consortium
The HTML specification
is maintained by the W3C.

## 标记
==marked==

{==高亮==}
{--删除--}
{~~test~>back~~}
{>>注释<<}
## 数学

### Accents
| $a'$         | $\tilde{a}$      | $\mathring{g}$        |
| ------------ | ---------------- | --------------------- |
| $a''$        | $\widetilde{ac}$ | $\overgroup{AB}$      |
| $a^{\prime}$ | $\utilde{AB}$    | $ \undergroup{AB}$    |
| $\acute{a}$  | $\vec{F}$        | $\Overrightarrow{AB}$ |
$$
\begin{matrix}
   a & b \\
   c & d
\end{matrix}
$$
$f(x) = sin(x) + 12$
$$\sum_{n=1}*100$$

## 流程图
### Flow Charts
```flow {filename="flow.png"}
st=>start: 开始
op=>operation: My Operation
cond=>condition: Yes or No?
test=>condition: test flow
e=>end
st->op->cond
cond(yes)->test
test(yes)->e
cond(no)->op
```
### sequence
```sequence {theme="hand" filename="sequence.png"}
Andrew->China: Says Hello
Note right of China: China thinks\nabout it
Note left of Andrew: Andrew is test
China-->Andrew: How are you?
Andrew->>China: I am good thanks!
```
### mermaid
```mermaid {filename="mermaid.png"}
graph LR
A-->B
B-->C
C-->A
```
### puml {filename="puml.png"}
```puml
@startuml
Alice -> Bob: Authentication Request
Bob --> Alice: Authentication Response
Alice -> Bob: Another authentication Request
Alice <-- Bob: another authentication Response
@enduml
```
### wavedrom
```wavedrom {filename="wavedrom.png"}
{signal: [
  {name: 'clk', wave: 'p.....|...'},
  {name: 'dat', wave: 'x.345x|=.x', data: ['head', 'body', 'tail', 'data']},
  {name: 'req', wave: '0.1..0|1.0'},
  {},
  {name: 'ack', wave: '1.....|01.'}
]}
```
### dot && viz
```dot {filename="dot.png"}
digraph G {
  A -> B
  B -> C
  B -> D
}
```
```dot {engine="circo" filename="dotviz.png"}
digraph G {
  A -> B
  B -> C
  B -> D
}
```
### Vega && Vega-lite
```Vega
{
  "$schema": "https://vega.github.io/schema/vega/v4.json",
  "description": "A specification outline example.",
  "width": 500,
  "height": 200,
  "padding": 5,
  "autosize": "pad",

  "signals": [],
  "data": [],
  "scales": [],
  "projections": [],
  "axes": [],
  "legends": [],
  "marks": []
}
```
### Ditaa
```ditaa {cmd=true args=["-E"] filename="ditaa.png"}
+--------+   +-------+    +-------+
|        | --+ ditaa +--> |       |
|  Text  |   +-------+    |diagram|
|Document|   |!magic!|    |       |
|     {d}|   |       |    |       |
+---+----+   +-------+    +-------+
    :                         ^
    |       Lots of work      |
    +-------------------------+
```
### 导入外部文件
@import ""

code code_chunk
```bash {cmd=true}
ls .
```
```python {cmd="/usr/local/bin/python3"}
print("这个将会运行 python3 程序")
```
```gnuplot {cmd=true output="html"}
set terminal svg
set title "Simple Plots" font ",20"
set key left box
set samples 50
set style data points

plot [-10:10] sin(x),atan(x),cos(atan(x))
```
```python {cmd=true matplotlib=true}
import matplotlib.pyplot as plt
plt.plot([1,2,3, 4])
plt.show() # show figure
```
