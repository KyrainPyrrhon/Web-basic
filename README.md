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

### Event Loop

This is image is from Lydia Hallie
<img src=".\js-eventloop.png" />


### HTTP

#### A typical HTTP session

HTTP会话包括三个阶段
1. Client端建立一个TCP连接（或者其他连接）
2. Client发送请求，等待回应
3. Server端处理请求，将回应发送回去并且提供状态码和相应的数据

HTTP/1.1协议在第三个阶段后不在关闭连接，保证Client可以继续发送请求，这意味着第二、第三个阶段可以进行多次操作

Response status codes
- 200: OK.
- 301: Moved Permanently.
- 404: Not Found.



## Redux Section

### Redux Fundamentals: Part 1

#### Background Concepts

- State Management
  - state
  - view
  - actions
- Immutability
  - In order to update values immutably, your code must make copies of existing objects/arrays, and then modify the copies.

#### Redux Terminology

- Actions
- Reducers
  - Pitfall: They must not do any asynchronous logic, calculate random values, or cause other "side effects"
- Store
- Dispatch
- Selectors

#### Core Concepts and Principles

- Single Source of Truth
- State is Read-Only
- Changes are Made with Pure Reducer Functions
    
### Redux Fundamentals: Part 2













