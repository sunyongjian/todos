## TODO
三种 TODO 事项，高优先级即一两周之内必须完成的，普通优先级是一个月之内要完成，低优先级是两个月之内完成的。

### high
- [x] [mock-koa](https://github.com/sunyongjian/mock-koa)
2017-12-12 done

简单版的已经实现，对 koa 也大概了解，不过还有几个功能没实现，很多细节还待深入挖掘，继续看源码，然后写个源码解析


- [x]  做一次 React 状态管理的分享。redux，mobx 实践，优化点，对比

2018-01-12

### general
- [ ] blog [issue-34](https://github.com/sunyongjian/blog/issues/34) 

### low 
- [ ] 依赖收集（vue，mobx）
- [ ] 依赖注入
- [ ] 结合以上，实现一个小的 mobx，react-mobx 的 library
- [x] 研究一下如何去写一个 webpack-plugin, 并优雅的解决 dll 的一个问题

写了半天，去寻找思路的时候，突然发现有一个 `html-webpack-include-assets-plugin` 插件，算是跟自己想要的结果差不多，就没有必要重复造了。读取 dll 生成的 manifest.json 里 chunkname 即提取的 js 文件名，并插入 html 里。

使用：
```js
new HtmlIncludeAssetsPlugin({
  assets: [`dll/${require('../dll/vendor-manifest.json').name}.js`],
  append: false //append vendor.js to html
})
```
