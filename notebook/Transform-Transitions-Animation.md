Transform + Transitions + Animation
======================

## Transform 转换

### 一些常用的属性：

- transform: none | transform-functions;【通过设置该属性的值，我们可以对元素使用转换，具体的属性值在下面会专门介绍。】

- transform-origin: x-axis y-axis z-axis;【设置元素转换的中心点，最直观的例子旋转图片，改变图片选择依赖的旋转中心。】

- transform-style: flat | preserve-3d;【定义里面转换的元素是在2D平面呈现还是在3D空间呈现，讲的直白些，就是这个元素里面的空间维度是二维还是三维。】

- perspective: number | none;【属性是定义3D元素距试图的距离，设置以后，其子元素会获得透视效果，需要注意的是该值只对3D转换有效，这也是很容易理解的。此外，还可以通过Transform的属性值的方式设置，二者是有一定区别的，你可以认为，前者是把整个看成一个舞台，后者是每一个都是一个舞台。】

- perspective-origin: x-axis y-axis;【必须和perspective一起使用，只对3D转换元素有效，简单的理解就是你的眼睛看的焦点。】

- backface-visibility:hidden | visible;【这个很简单，设置当元素背对着屏幕时候，是否是可见的。】

上面介绍的属性transform: none | transform-functions;其中有很多方法可以使用，具体的请查看文件API，这里没有列举出来的意义，其中perspective(n)方法是为3D转换元素定义透视视图，需要稍微留意一下，其中一些方法比较特殊，以后会单独去介绍。

## Transitions 过渡

```css
transition: property duration timing-function delay;
```

请始终设置 transition-duration 属性，否则时长为 0，就不会产生过渡效果。上面是统一设置，也可以分别设置各个属性。

### 一些常用的属性：

- transition-property：规定设置过渡效果的 CSS 属性的名称；
- transition-duration：规定完成过渡效果需要多少秒或毫秒；
- transition-timing-function：规定速度效果的速度曲线；
- transition-delay：定义过渡效果何时开始。

## Animation 动画

```css
animation: name duration timing-function delay iteration-count direction;
```

请始终规定 animation-duration 属性，否则时长为 0，就不会播放动画了。上面是统一设置，也可以分别设置各个属性。

### 一些常用的属性：

- animation-name：规定需要绑定到选择器的 keyframe 名称；
- animation-duration：规定完成动画所花费的时间，以秒或毫秒计；
- animation-timing-function： 规定动画的速度曲线；
- animation-delay：规定在动画开始之前的延迟；
- animation-iteration-count：规定动画应该播放的次数；
- animation-direction：规定是否应该轮流反向播放动画；
- animation-fill-mode (可以设置为none | forwards | backwards | both)：规定动画在播放之前或之后，其动画效果是否可见；
- animation-play-state（可以设置为paused|running）：规定动画正在运行还是暂停，可以在 JavaScript 中使用该属性，这样就能在播放过程中暂停动画；
- @keyframes animName{from {} to {}}：定义动画名称为animName的动画关键帧。

[<< 返回首页](../README.md)
