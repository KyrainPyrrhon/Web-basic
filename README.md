# Web-basic

## HTML Section

## CSS Section

### Reflow & Repaint

重排：浏览器从新计算网页中的某一个部分或整体的位置或几何结构；
重绘：根据重拍的结果去进行绘制网页内容；

重绘发生在重排之后；

哪些操作会触发重拍？简单来说就是改变了DOM结构。具体有以下等情况：
- 添加、删除、更新DOM结点
- 使用`display: none`隐藏DOM元素会触发重排和重绘
- 使用`visibility: hidden`只会触发重绘
- 将一个DOM结点进行移动或者动画处理会触发重排和重绘
- 调整window尺寸会触发重排
- 改变font-style会改变元素的集合结构，也会触发重排
- 添加样式也会触发重排或者重绘
- JS操作DOM也会触发重排和重绘

如何减少或者避免重排和重绘呢？
- 尽量不要修改单独的样式，选择修改其类名，也就是说在样式中替换样式
- 整体DOM变化（可以选择documentFragment）
- 不要重复计算样式，可以将他们cache起来

## JavaScript Section
