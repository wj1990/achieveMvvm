## 简单实现vue原理
### 思路：
1. 创建 Vue构造函数 接收 {el,data}
2. 通过Object.defineProperty方法给data说有的属性劫持，即设置get 和 set方法 （代码中的obersver）;
3. 通过文档碎片 DocumentFragment，收集el中的dom节点，然后对{{a.a}}替换为真实的值，最后插入el中（方法compile）；
4. data属性值的改变，引起视图同步更新实现：通过发布订阅者模式，在get方法里面订阅数据更新处理函数，在set方法里面发布该处理函数，即让此函数执行，达到视图同步更新；




