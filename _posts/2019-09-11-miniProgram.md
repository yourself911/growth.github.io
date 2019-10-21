1. performance optimization
https://juejin.im/post/5b496d5d5188251a90187635#heading-7
2. 深入解读-微信小程序SDK
https://juejin.im/post/593b52d4ac502e006b2d54bc#heading-13
3. ESlint 入门教程
https://juejin.im/post/5bab946cf265da0ae92a75ca#heading-0

微信小程序scroll-view scroll-x="true" 在ios下滚动条没有显示，在Android下有显示。   
::-webkit-scrollbar   <http://caibaojian.com/webkit-scrollbar.html>   
::-webkit-overflow-scroll: touch  
引用自定义组件时，`<m-cmp class="my"/>` 要改变自定义组件的display值，对组件的样式操作才会生效。   
注意是对整个自定义组件，而不是组件内部元素。只有少数几个样式自定义组件内部才能定义，除非使用样式隔离，自定义组件名的元素选择器，和外部样式类，具体看文档。     
评论系统功能设计：<https://learnku.com/articles/8075/the-review-function-is-completed-by-the-way-by-the-way-the-experience-of-developing-reviews>  二级评论功能   
微信小程序组件化的解决方案：<https://zhuanlan.zhihu.com/p/33274694>   
微信小程序swiper的高度固定问题： lin-ui   
微信小程序tabs滚动效果，主要是那个计算居中的公式。瀑布流组件化实现，学习lin-ui的源码，自己尝试写一下。   
微信小程序video常见的开发需求解决方案<https://juejin.im/post/5c4ee15cf265da61193c32f2#heading-7> video用的是hls协议，看看imweb
腾讯课堂小程序开发流程，讲解了直播协议，以及性能优化方法。    
微信小程序生成带参数的二维码: <https://www.ifanr.com/minapp/823595>   
微信小程序实现底部弹出框动画效果: <http://www.hehaibao.com/wxapp-show-footer-animation-popup/>   
微信wxs的作用，一般用作过滤器。比如 后端返回的数据是 123123这样的时间毫秒数， 如果你要用js处理，那么你就得对发回的数据进行选择时间字段，   
然后就其进行转换，如果 数据是 `[ {a: { time: 12312} } ...]` 或者更深层次的嵌套，那么这样用js处理就需要遍历出每个time字段才行，   
这样很消耗性能，如果用wxs我们就可以在wxml中使用过滤器函数，而这时的数据绑定已经处理好，就不需要进行遍历了。    
微信小程序，点击元素，绑定事件，使用wx.navigateTo() 进行页面跳转时，如果短时间内点击多次，那么事件处理程序就会执行多次，而wx.navigateTo   
跳转需要一定的时间，这就就会出现两次跳转，那么久需要使用函数节流。     







