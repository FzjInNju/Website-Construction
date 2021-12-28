# 03 html5

## html5历史和特性

- html4.01诞生于1999年，html5 2014年
- html5是==W3C==(万维网联盟)和==WHATWG==（Web Hypertext Application Technology Working Group）网络超文本应用技术工作组 合作的结果
- ==IETF==互联网工程任务组也参与了html5
- 优化了html4的语法
- html5 是专门为承载丰富的web内容而设计的，无需额外插件
- 有新的语义、图形和多媒体元素
- 新元素和新API简化web应用程序的搭建
- 跨平台，被设计在不同类型的硬件（pc、平板、手机、电视机）上运行
- 安全性强

## 旧路新铺——优化 input 语法

html4

```html
<form>
    <input name = "email" type = "text">
</form>
```

html5

```html
<input type = email required>
```

## 简单之上——<!DOCTYPE html>

## 简化字符集——<meta charset = utf-8>

## 简化Markup——去掉html head body 标签

```html
 <!DOCTYPE html>
 <meta charset=utf-8>
 <title>HTML5</title>
 <h1>HTML5!</h1>
```

## 无插件范式

## 默认是安全的

- 定义安全的跨起源共享
- html使用基于起源的安全
- html5中的问题可以得到快速修复

## html5具体改进

**新元素**

![image-20211228212801408](C:\Users\junlines\AppData\Roaming\Typora\typora-user-images\image-20211228212801408.png)

**新属性**

**完全⽀持 CSS3**

**Video 和 Audio**

**2D/3D 制图**

**本地存储**

**本地 SQL 数据**

**Web 应⽤**

## Microdata 微观数据

1. 概念和作用微观数据是以自定义词汇为核心，让我们回过头去看过去的工作。将所有html5的元素看作是一个词汇表，这个词汇表包含着的元素可以用来代表一个段落或者一篇文章的，但是他不包含能代表一个人或者一个事件的。如果你想要在网页上表现一个人，那么你需要自定义一个词汇。微观数据可以让你做到这一点。任何人都可以在自己的网页上自定义微观数据然后嵌入通用的属性。

   当正确的使用HTML但是HTML的语义表现力不够强时，微观数据能够发挥最大的效果。微观数据最显著作用就是对DOM中已经存在的数据在语义上微调补充。如果你想要语意化的数据并不在DOM中，你最好应该重新评估一下微观数据是否为正确的解决方案。

2. 使用

   具体参照http://simpleframework.net/news/view?newsId=6e749fcc84474471a1f3d975feb80a84

   - 通过在自己控制的域上选择一个 URL 就能很容易地创建一个全世界唯一的标识符。例如：http://data-vocabulary.org/Person
   - 在这个词汇表（vocabulary）中，要定义一些命名的属性，这里从三个基本的属性开始：
     - name (your full name)
     - photo (a link to a picture of you)
     - url (a link to a site associate to you, like a weblog or Gooogle profile)

   ```html
   <section itemscope itemtype = "http://data-vocabulary.org/Person">
       <h1 itemprop="name">
           Mark Pilgrim
       </h1>
       <!--这里是 http://data-vocabulary.org/Person 词汇表的一个 name 属性，它的属性值是 Mark Pilgrim。-->
       <p>
           <img itemprop = "photo" src = "http://www.example.com/photo.jpg" alt = "[me smiling]">
       </p>
       <!--这里是 http://data-vocabulary.org/Person 词汇表的一个 photo 属性，它的属性值为 http://www.example.com/photo.jpg。-->
   </section>
   ```

## 词汇表

- 谷歌和其他主要搜索引擎依靠schema.org词汇表来改进搜索结果
- 微数据词汇表提供了项目的语义或含义
- 词汇表定义了一组标准类型名称或属性名称

## HTML5表单

1. 新表单的功能
   - 不需要 js
   - 原生的输入类型：color data email number tel etc.
   - 新的输入属性：autocomplete autofocus min max
2. 旧浏览器（不支持HTML5表单）中新的表单控件会平滑降级（将表单控件识别为文本）

## HTML5 媒体

新的媒体元素 audio video

```html
<video controls src = "goldrush.mp4">
    A movie about HTML5
</video>
```

## HTML5 图形

- Canvas 和 SVG
- 原生画图功能，不需要插件
- 完全整合于HTML5 DOM
  - 由CSS提供样式
  - 有JS来绘制
- 用于动画、图表、图像、像素操作等

## SVG

1. Scalable Vector Graphics 可伸缩矢量模型

2. 基于==XML==格式定义图像

3. 改变尺寸时图形质量不会有损失

4. SVG是W3C万维网联盟的标准

   ```html
   <svg xmlns="http://www.w3.org/2000/svg" version="1.3">
      <circle cx="100" cy="100" r="30" stroke="yellow" stroke-width="3" fill="red"/>
   </svg> 
   <!--cx cy表示位置  r半径   stroke边框颜色   fill填充颜色-->
   ```

### SVG优势

- 可通过文本编辑器创建和修改
- 可被搜索、索引、脚本化压缩
- 可伸缩
- 可在任何分辨率下被高质量打印
- 可在图像质量不下降的情况下被放大

## Canvas

1. 基本原理：使用==js==在网页上绘制图像

   画布是矩形区域，可以控制每一像素

   有多种绘制路径、矩形、字符、添加图像的方法

## SVG 和 Canvas

![image-20211228234701433](C:\Users\junlines\AppData\Roaming\Typora\typora-user-images\image-20211228234701433.png)

---

## HTML5 Web存储——客户端存储数据的两个对象

1. localStorage：用于长久保存整个网站的数据，保存的数据没有过期时间，直到手动去除
2. sessionStorage：用于临时保存同一窗口（或标签页）的数据，在关闭窗口或标签页之后将会删除数据

## HTML5 应用程序缓存

1. 应用程序缓存的实现：通过创建cache manifest文件，可以轻松创建web应用的离线版本
2. 应用程序的作用：
   - 离线浏览：用户可在应用离线时使用它们
   - 速度：已缓存资源加载得更快
   - 减少服务器负载：浏览器将只从服务器下载==更新过==或更改过的资源
3. manifest文件：告知浏览器被缓存的内容（以及不缓存的内容），manifest明显的、海关验关单
   - CACHE MANIFEST ： 在次标题下列出的文件 在首次下载后进行缓存
   - NETWORK：在此标题下列出的文件 需要与服务器连接才能获得，不会被缓存
   - FALLBACK：    当页面无法访问时的回退页面（比如404页面）
4. 更新缓存
   - 用户清空浏览器缓存
   - manifest文件被修改
   - 有程序来更新应用缓存

### HTML5 Web Workers

1. 背景：当HTML页面执行脚本时，页面的状态是不可响应的，直到脚本已完成
2. 概念：web worker是==运行在后台==的js，独立于其他脚本，==不会影响页面的性能==。可以继续做任何愿意做的事情：点击、选取内容等

## HTML5 WebSocket

有点复杂，详见https://www.zhihu.com/question/20215561

## HTML5 Geolocation API 

获得用户地理位置

## HTML5 拖放Drag Drop 

任何元素都可拖放

