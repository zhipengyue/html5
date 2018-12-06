#html

##常用语义标签

###一、结构
**<header><header>**
适合放置在网站头部，用于展示网站概览信息，可以包含banner和导航信息
**<main><main>**
唯一性，整个页面只允许一个。放置主要内容
**<aside></aside>**
侧边栏，一般放置快捷导航，推荐内容等。
**<footer></footer>**
页脚
**<embed></embed>**
一般嵌入swf 嵌入内容


###二、导航
**<nav></nav>**
链接容器，可以装载一系列的链接标签

###三、标题
**<h></h>**
h1-h6 层级标题
**<hgroup></hgroup>**
标题组

###四、段落
**<section></section>**
**<article></article>**

###五、文本
####1.类型文本
**<time></time>**
**<address></address>**

####2.强调文本
**<mark></mark>**
类似马克笔画的标记，有底色

**<em></em>**
em会对文本含义有改变作用，类似读一句话时重读某一个字或词会表达不一样的意思一样。

**<strong></strong>**
strong会突出包含文本的重要性、严重性和紧急性等。

####3.辅助文本
**<del></del>**
删除线
**<u></u>**
下划线
**<ins></ins>**
插入元素 ，默认下划线
**<abbr></abbr>**
省略标签
例如：abbr的内容是经过省略的，完全的内容放在title中
```
<abbr title="这是一段来自eleven的内心独白：尽管我从业十年，但是面对面试官的基本问题，有时候还是举足无措，追根溯源，是自己知识不扎实导致的，这是我整理文档的根本原因。">
这是一段来自eleven的内心独白
</abbr>
```
**<ruby></ruby>**
音标标签
例如：<ruby>魑<rp>(</rp><rt>chī </rt><rp>)</rp></ruby>
**<bdo></bdo>**
控制文本输出方向
例如：
```
<p>
  <bdo dir="ltr">文字从左往右</bdo><br>
  <bdo dir="rtl">文字从右往左</bdo>
</p>
```
####4.上下标
**<sub></sub>**
下标
**<sup></sup>**
上标

####5.引用文本
**<blockquote></blockquote>**
引用，cite指定
<blockquote cite="引用作品的地址">
            这是一段引用文本
</blockquote>

**<q></q>**
引用的书名，一般在q:before q:after加上书名号

**<dfn></dfn>**
术语定义

####6.程序文本
**<kbd></kbd>**
用户输入文本
**<samp></samp>**
计算机输出内容
**<var></var>**
**<code></code>**
计算机变量

####六、组件
**<details><summery></summery></details>**
配套出现，展开功能，默认闭合，点击展开
例如：
```
<details>
  <summary>展开查看详情</summary>
  <p>
      这是一段详情描述<br>
      只有展开才能查看
  </p>
</details>
```
**<dialog></dialog>**
对话框,fireFox不支持
例如：
```
<section>
        <h2>dialog</h2>
        <p>
            <a onclick="showDialogModal()">打开对话框</a>
            </p><dialog id="myDialog">
                对话框
            </dialog>
        <p></p>
</section>
<script>
    var dialogStatus=false;
    function openDialog(){
        var dialog = document.getElementById("myDialog");
        dialogStatus=!dialogStatus;
        
        if(dialogStatus){
            dialog.show();
        }else{
            dialog.close();
        }
    }
    function showDialogModal(){
        var dialog = document.getElementById("myDialog");
        dialog.showModal();
    }
</script>
```
**<progress></progress>**
进度条

例如：
```
<progress max="100" value="60">
   <span>60</span>%
</progress>
```
**<meter></meter>**
度量
例如：
```
<meter value="3" min="0" max="10">3/10</meter>
```
**<hr></hr>**
分隔线

###七、表
**<ol></ol>**
有序表格
例如：
```
<ol start="50">
<li>咖啡</li>
<li>牛奶</li>
<li>茶</li>
</ol>
```
**<dl></dl>**
说明列表
例如：
```
<dl>
    <dt><img href="#"></dt>
    <dd>图片标题</dd>
</dl>
```
或：
```
<dl>
    <dt>计算机</dt>
    <dd>用来计算的仪器 ... ...</dd>
    <dt>显示器</dt>
    <dd>以视觉方式显示信息的装置 ... ...</dd>
</dl>
```
其中dt是标题，dd是说明描述.

table
表格
caption 表格说明
例如：
```
<table style="border:1px solid #ccc;">
  <caption>这是一个说明表格</caption>
  <thead>
    <tr><th>姓名</th><th>性别</th><th>联系方式</th></tr>
  </thead>
  <tbody>
    <tr><td>张珊珊</td><td>女</td><td>13414****</td></tr>
  </tbody>
</table>
```
colgroup 表格分组
例如：
```
<table border="1">
    <colgroup>
      <col style="background-color:red" span="2"><!--span 横跨若干列，-->
      <col style="background-color:yellow"><!--剩下的用这个颜色-->
    </colgroup>
    <tbody><tr>
      <th>ISBN</th>
      <th>Title</th>
      <th>Price</th>
    </tr>
    <tr>
      <td>3476896</td>
      <td>My first HTML</td>
      <td>$53</td>
    </tr>
    <tr>
      <td>5869207</td>
      <td>My first CSS</td>
      <td>$49</td>
    </tr>
  </tbody>
 </table>
```
###八、媒体
<figure></figure>
例如：
```
<figure>
    <img src="#">
    <figcaption>
        这是一张来自百度的图片
    </figcaption>
</figure>
```
可以理解为，figcaption是img的描述，如果是多图，可以考虑放在dl中

**<map></map>**
图片热区
例如：
```
<img src="http://www.w3school.com.cn/i/eg_planets.jpg" usemap="#planetmap" alt="Planets" border="0">
<map name="planetmap" id="planetmap">
<area shape="circle" coords="180,139,14" href="http://www.w3school.com.cn/example/html/venus.html" target="_blank" alt="Venus">

<area shape="circle" coords="129,161,10" href="http://www.w3school.com.cn/example/html/mercur.html" target="_blank" alt="Mercury">

<area shape="rect" coords="0,0,110,260" href="http://www.w3school.com.cn/example/html/sun.html" target="_blank" alt="Sun">

</map>
```

###九、script
**defer**
将script标签放到文档最后执行 只用于外部脚本
async
默认情况下，浏览器一遇到script元素，就会暂停解析html文档。执行完脚本之后才继续解析html文档。

###十、style

**media**

all 将样式应用于所有设备
aural 将样式应用于语音合成器
braille 将样式应用于盲文设备
handled 将样式应用于手持设备
projection 将样式应用于投影机
print 将样式应用于打印预览和打印页面时
screen 将样式应用于计算机显示屏幕
tty 将样式用于电传打字机之类的等宽设备
tv 将样式应用于电视机

可以通过 AND OR 和 NOT组合条件
供style元素的media属性使用的特性

width/height 指定浏览器窗口宽度和高度
device-width 指定整个设备
resolution 指定设备的像素密度。单位dpi(点/英寸) 或dpcm(点/厘米)
orietation 指定设备的较长边朝向 portrait 和 landscape
aspect-radio/device-aspect-radio 指定浏览器窗口或设备的宽高比 min-aspect-ratio:16/9
clolor monochrome 指定彩色或黑白设备上每个像素占用的二级制位数 min-monochrome:2
color-index 指定设备所显示的颜色数据 max-color-index:256
scan 指定电视的扫描模式 progressive/interlace scan:interlace
grid 指定设备的类型



##标签属性

###一、input
**accesskey**
指定快捷键，按下某键时，光标定位到该输入框
<input type="text" accesskey="n"/>

**tabindex**
按下tab键，文本输入框的获取焦点顺序

###二、文本
**dir**
方向控制
<span dir="ltr">左到右</span>

**lang**
语言
<div lang="fr"> Bonjour</div>

**spellcheck**
拼写错误检查，firfox下不好用
<span spellcheck="true" lang="en">Hollo haw ar you</span>

**abbr**
缩写
<abbr title="America">USA</abbr>





