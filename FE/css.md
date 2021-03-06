## posation
- 定位元素（positioned element）是其计算后位置属性为 relative, absolute, fixed 或 sticky 的一个元素。
- 相对定位元素（relatively positioned element）是计算后位置属性为 relative 的元素。
- 绝对定位元素（absolutely positioned element）是计算后位置属性为 absolute 或 fixed 的元素。
- 粘性定位元素（stickily positioned element）是计算后位置属性为 sticky 的元素。

[布局和包含块](https://developer.mozilla.org/zh-CN/docs/Web/CSS/All_About_The_Containing_Block)

补充: [CSS魔法堂：不得不说的Containing Block](https://segmentfault.com/a/1190000004642650)

## [z-index](https://developer.mozilla.org/zh-CN/docs/Web/Guide/CSS/Understanding_z_index)

- [Stacking without z-index](https://developer.mozilla.org/zh-CN/docs/Web/Guide/CSS/Understanding_z_index/Stacking_without_z-index) : 默认的摆放规则，即不含有 z-index 属性时
- [Stacking and float](https://developer.mozilla.org/zh-CN/docs/Web/Guide/CSS/Understanding_z_index/Stacking_and_float) : 浮动元素的处理方式
- [Adding z-index](https://developer.mozilla.org/zh-CN/docs/Web/Guide/CSS/Understanding_z_index/Adding_z-index) : 使用 z-index 来改变堆放顺序
- [The stacking context](https://developer.mozilla.org/zh-CN/docs/Web/Guide/CSS/Understanding_z_index/The_stacking_context) : 内容堆放注意事项
- [Stacking context example 1](https://developer.mozilla.org/zh-TW/docs/Web/CSS/CSS_Positioning/Understanding_z_index/Stacking_context_example_1) : 在两层元素的第二层上使用 z-index
- [Stacking context example 2](https://developer.mozilla.org/zh-CN/docs/Web/Guide/CSS/Understanding_z_index/Stacking_context_example_2) : 在两层元素的所有层上使用 z-index
- [Stacking context example 3](https://developer.mozilla.org/zh-CN/docs/Web/Guide/CSS/Understanding_z_index/Stacking_context_example_3) : 在三层元素的第二层上使用 z-index

层叠上下文由满足以下任意条件的元素形成
- 根元素 (HTML),
- z-index 值不为 "auto"的 绝对/相对定位，
- 一个 z-index 值不为 "auto"的 flex 项目 (flex item)，即：父元素 display: flex|inline-flex，
- opacity 属性值小于 1 的元素（参考 the specification for opacity），
- transform 属性值不为 "none"的元素，
- filter值不为“none”的元素，
- position: fixed
- mix-blend-mode 属性值不为 "normal"的元素，
- perspective值不为“none”的元素，
- isolation 属性被设置为 "isolate"的元素，
- 在 will-change 中指定了任意 CSS 属性，即便你没有直接指定这些属性的值（参考 [这篇文章](https://dev.opera.com/articles/css-will-change-property/)）
- -webkit-overflow-scrolling 属性被设置 "touch"的元素