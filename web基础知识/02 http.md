# 02 http

## 历史

1997 html4

2014 html5

## html 和 XHTML

- html 复杂，对解析器的要求高
- XHTML 语法更严格，对解析器的要求低，可以用XML工具解析
- 都是标记语言

## html总体组成部分

- DOCTYPE

  - 在HTML4.01中，<!DOCTYPE>声明引用DTD，因为HTML4.01基于SGML。DTD规定了标记语言的规则，这样浏览器才能正确的呈现内容。在HTML4.01中有三种<!DOCTYPE>声明。

    严格模式：`<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"  "http://www.w3.org/TR/html4/strict.dtd">`

    过渡模式：`<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN"  "http://www.w3.org/TR/html4/loose.dtd">`

    框架模式：`<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Frameset//EN"  "http://www.w3.org/TR/html4/frameset.dtd">`

  - HTML5 不依赖SGML，只有一种    `<!DOCTYPE html>`

- HEAD

  ```html
  <head>
      <title>文档标题</title>
      <meta charset = 'utf-8'>
      <meta name = 'keywords' content = '搜索关键词'>
      <meta name = 'description' content = '描述网站，在搜索页面呈现'>
      <!-- name 还有 author generatorgenerator用于说明网站的采用的什么软件制作 -->
  </head>
  ```

- BODY

  要渲染的内容

## html元素：块元素和内联元素

1. 块元素
   - 一整块大的区域
   - 纵向排列，块与块之间有空隙
   - 例如：p list table
2. 内敛元素
   - 一小块内容
   - 横向排列
   - 在块元素中
   - 例如：bold text 、code fragment、images

## a 是内联元素，必须放在块元素中

## table

```html
<table>
    <tr><th>name</th><th>gender</th></tr>
    <tr><td>Bill</td><td>male</td></tr>
    <tr><td>Susan</td><td>female</td></tr>
</table>
```

<table>
    <tr><th>name</th><th>gender</th></tr>
    <tr><td>Bill</td><td>male</td></tr>
    <tr><td>Susan</td><td>female</td></tr>
</table>

## blockquote 引用（块元素）

```html
<blockquote>
    asdf
</blockquote>
```

<blockquote>
    asdf
</blockquote>

## q 引用（内联元素）

```html
<p>
    <q>asdf</q>
</p>
```

<p>
    <q>asdf</q>
</p>

## HTML character entities 在网页上表示任何文本的方式

```html
&lt;p&gt; &#1048;
```

&lt;p&gt; &#1048;

---

## form表单——创建GUI

1. 作用：获取客户信息，发给服务器处理来解决问题

2. 表单由==控件==组成，控件是内联元素

   ```html
   <form>
    <div class="form-group">
    <label for="inputEmail">Email</label>
    <input type="email" class="form-control" id="inputEmail" value="Email">
    </div>
    <div class="form-group">
    <label for="inputPassword">Password</label>
    <input type="password" class="form-control" id="inputPwd" placeholder="Password">
    </div>
    <div class="checkbox">
    <label><input type="checkbox"> Remember me</label>
    </div>
    <button type="submit" class="btn">Login</button>
    </form>
   ```

   <form><label for = "inputEmail">Email</label><input type = "email" placeholder = "Email"></input><br><label for="inputPassword">Password</label> <input type="password" class="form-control" id="inputPwd" placeholder="Password"><br><label><input type="checkbox"> Remember me</label><br><button type="submit" class="btn">Login</button></form>

## &在html中是&amp

## 