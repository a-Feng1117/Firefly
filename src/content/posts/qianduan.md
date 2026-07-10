---
title: HTML & CSS 核心语法速览
published: 2026-07-07
description: "一份适合复习与参考的 HTML / CSS 语法要点"
image: api
tags: [Markdown, 学习]
category: "学习"
draft: false
---

# HTML + CSS 核心语法速查笔记
适用场景：前端基础复习、新手入门查阅、日常开发速查
AI时代，前端代码我们可以不熟练，但我们要有 review 的能力

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>页面标题</title>
</head>
<body>
    
</body>
</html>
常用基础标签示例
<h1>一级标题</h1>
<h2>二级标题</h2>

<p>这是正文段落文本，用于展示常规内容</p>

<div class="box">模块内容</div>

<p>普通文本 <span style="color:red">局部变色文本</span></p>

<a href="https://xxx.com" target="_blank">跳转链接</a>

<img src="img.png" alt="图片描述">

<ul>
    <li>列表项1</li>
    <li>列表项2</li>
</ul>

<ol>
    <li>第一步</li>
    <li>第二步</li>
</ol>
 表单常用标签
 <form action="" method="get">
    <input type="text" placeholder="请输入用户名">
    <input type="password" placeholder="请输入密码">

    <input type="radio" name="sex" id="man"><label for="man">男</label>
    <input type="radio" name="sex" id="woman"><label for="woman">女</label>

    <input type="checkbox" id="check"><label for="check">同意协议</label>

    <button type="submit">提交</button>
</form>
二、CSS 核心语法
CSS 三种引入方式
 外部样式
 <link rel="stylesheet" href="style.css">
 内部样式
 <style>
body {
    margin: 0;
}
</style>
行内样式
<div style="color: red; font-size: 14px;">文本内容</div>
四大基础选择器
* {
    margin: 0;
    padding: 0;
}

p {
    color: #333;
}

.box {
    width: 100px;
}

#header {
    height: 60px;
}
常用文本样式
.text {
    color: #333;
    font-size: 16px;
    font-weight: bold;
    text-align: center;
    line-height: 1.5;
    text-decoration: none;
}
盒子模型
.box {
    width: 200px;
    height: 200px;
    padding: 10px;
    margin: 20px auto;
    border: 1px solid #eee;
    box-sizing: border-box;
}
 Flex 弹性布局
 .flex-wrap {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    gap: 10px;
}
Position 定位布局
.pos-box {
    position: relative;
    position: absolute;
    position: fixed;
    top: 0;
    left: 0;
}
背景样式
.bg-box {
    background-color: #f5f5f5;
    background-image: url(./bg.png);
    background-repeat: no-repeat;
    background-size: cover;
}
通用 CSS 初始化模板
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-size: 16px;
    color: #333;
    background-color: #fff;
    font-family: "Microsoft Yahei", sans-serif;
}

a {
    text-decoration: none;
    color: #333;
}

ul, li {
    list-style: none;
}

img {
    border: none;
    max-width: 100%;
}
高频易错总结
行内元素：span、a、img 默认无法设置宽高、上下 margin，需添加 display: inline-block
盒模型踩坑点：不写 box-sizing: border-box，padding、border 会额外撑大盒子整体宽度
Flex 布局特性：子元素默认不会自动换行，多列布局必须添加 flex-wrap: wrap
绝对定位前提：子元素使用 absolute，父容器必须设置 position: relative
选择器优先级：行内样式 > ID 选择器 > 类选择器 > 标签选择器