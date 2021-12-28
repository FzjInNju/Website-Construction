





[TOC]

# 04 CSS Basic

## CSS定义

cascading style sheet 层叠样式表。CSS是一种基于规则的语言，它为html元素定义样式，例如修改元素的颜色、背景、大小、边框厚度

## ☆ 为什么使用CSS

1. 灵活
2. 简洁
3. 清晰
4. 有基础的格式化工具
5. 方便复杂的文件管理
6. ==使用类选择器提高效率==
7. 可格式化代码

---

## CSS语法

![image-20211229013132682](C:\Users\junlines\AppData\Roaming\Typora\typora-user-images\image-20211229013132682.png)

### 选择器 Selector

id选择器、类、标签、属性选择器([title]{color:blue})、伪类选择器、伪元素选择器

```
a:link{color:#000000;}   /*未访问链接*/
a:visited{color:#00ff00;}  /*已访问链接*/
a:hover{color:#ff00ff;}   /*鼠标移动到链接上*/
a:active{color:#0000ff;}   /*鼠标点击时*/
```

```
p:first-line{
color:#ff0000;
font-variant:small-caps;
}
```

### CSS 组合选择符

后代选择器( )、子元素选择器( > )、相邻兄弟选择器( + )、普通兄弟选择器( - )

---

## Cascading的含义（为什么叫层叠样式表）

元素样式的层叠顺序按照以下：

- 浏览器默认样式
- 外部样式表
- 内部样式表
- 内联元素

## 样式继承

## 计算选择符的特殊性

（css的最终样式由特殊性最高的决定）

![image-20211229015128417](C:\Users\junlines\AppData\Roaming\Typora\typora-user-images\image-20211229015128417.png)

---

## CSS3概述

1. 模块化，以便于更容易的浏览器是哟共
2. 近50个模块
3. 使用特定浏览器的前缀
4. 性能提高了
   - 没有图像的边框半径（圆角）
   - 梯度
   - 多列布局
   - 转换
   - web字体
   - 媒体查询

![image-20211229015504162](C:\Users\junlines\AppData\Roaming\Typora\typora-user-images\image-20211229015504162.png)