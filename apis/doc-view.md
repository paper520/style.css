文档样式
======================

由于开发软件需要经常编辑文档，不过文档的主体是内容，而内容的排版其实都差不多，为了复用，就把内容设计的样式整合成一个独立的css文件。

使用方法
----------------------
```html
<div class="doc-view">
    <!-- 然后里面是具体的一些项目的样式，下面分别列出 -->
</div>
```

- 标题

h2、h3、h4分别表示文章标题、一级标题和二级标题。

- 段落

p标签表示一个段落

- 表格

```html
<table>
    <thead>
        <tr>
            <!-- 使用th或td -->
        </tr>
    </thead>
    <tbody>
        <tr>
            <!-- 使用th或td -->
        </tr>
        ......
    </tbody>
</table>
```

- 有序列表

```html
<ol>
    <li></li>
    ......
</ol>
```

- 无序列表

```html
<ul>
    <li></li>
    ......
</ul>
```

- 重要内容

```html
<div class='important'>
    // todo
</div>
```

- 可点击链接

```html
<div class='link'>
    // todo
</div>
```

- 过时标记

```html
<div class='outdated'>
    // todo
</div>
```

[<< 返回首页](../README.md)
