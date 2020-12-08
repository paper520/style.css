margin 外边距
======================

## 第一步：基础说明。

margin的意思很容易明白，就是外边距，用更通俗的话说，就是二个盒子之间间距的设置。

margin有许多需要注意的地方，比如块级元素垂直相邻外边距会合并，行内元素实际上不占上下外边距，左右外边距也不会合并，浮动元素的外边距也不会合并。

普通元素的margin百分百是按照父级元素（正确的说应该是包含块，具体可以看这篇文章[关于CSS中设置overflow属性的值为hidden的相关理解](./overflow-hidden.md)）的宽来计算的，而绝对定位的元素的margin百分比是按照第一个定位元素（relative，absolute和fixed）的宽来计算的。

## 第二步：block元素重叠。

block元素（不考虑float和absolute）在垂直方向发生margin重叠（不考虑writing-mode改变书写方式）；margin三种重叠：1.相邻兄弟元素；2.父亲元素和第一个或最后一个孩子元素；3.空的block元素。

## 第三步：重叠条件。

### 父子元素重叠条件（margin-top）

- 父元素非块状格式上下文元素；
- 父元素和第一个子元素之间没有inline元素分割；
- 父元素没有border-top或padding-top设置。

### 父子元素重叠条件（margin-bottom）

- 父元素非块状格式上下文元素；
- 父元素没有border-bottom或padding-bottom设置；
- 父元素和最后一个子元素之间没有inline元素分割；
- 父元素没有height,min-height和max-height的限制。

### 空的block元素重叠

- 元素没有border或padding或inline设置；
- 没有height或者min-height设置。

## 第四步：有价值的细节。

重叠计算方法：正正取最大、负负取最小和正负相加。

在书写方向的垂直方向，margin:auto会自动分配剩余空间（剩余空间的意思简单的可以理解为：在没有设置宽之前的长度去掉你设置的宽余下的那段距离）。

绝对定位元素的非定位方向margin无效（貌似是的，不过描述不准确，其实一直有效，只不过现在只可以影响自己，无法改变兄弟了，因此看起来失效了）。

最后一个题外话，margin-collapse可以设置重叠方式（collapse默认，重叠、discard取消margin,等于margin:0和separate分隔，就是不发生重叠）。

[<< 返回首页](../README.md)
