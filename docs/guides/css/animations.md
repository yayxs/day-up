---
title: CSS3 系列之动画 animations
---

# CSS3 系列之动画 animations

动画包括两部分：

- 其一 描述动画的样式规则
- 其二 指定动画开始、结束、中间点的关键帧（此处指的是帧动画|可以理解为一帧一帧的）

脚本也可以实现动画，那么纯正的`css` 实现动画有什么好处或者优点

>1. 能够非常容易地创建简单动画，你甚至不需要了解JavaScript就能创建动画。
>2. 动画运行效果良好，甚至在低性能的系统上。渲染引擎会使用跳帧或者其他技术以保证动画表现尽可能的流畅。而使用JavaScript实现的动画通常表现不佳（除非经过很好的设计）。
>3. 让浏览器控制动画序列，允许浏览器优化性能和效果，如降低位于隐藏选项卡中的动画更新频率。
>
>摘自《MDN》

先来看一段css3的动画

```html
  <style>
    * {
      margin: 0;
      padding: 0;
    }
    body {
      width: 100vw;
      height: 100vh;
      background-color: yellowgreen;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    main {
      width: 100px;
      height: 100px;
      background-color: #fff;
      animation-name: animationName;
      animation-duration: 4s;
    }

    @keyframes animationName {
      form {
        background-color: #fff;
      }
      to {
        background-color: black;
      }
    }
  </style>
  <body>
    <main></main>
  </body>
```

其中`animation-xxx` 描述的是动画的细节、这些细节指的是动画持续的时间、时长、等等

```css
 animation: name duration timing-function delay iteration-count direction fill-mode;
```

上述不明白暂时没有关系，接着看