# use-gulp

#### 为什么使用gulp?
首先看一篇文章 [Gulp的目标是取代Grunt](http://www.infoq.com/cn/news/2014/02/gulp)
>根据gulp的文档，它努力实现的主要特性是：
>   - 易于使用：采用代码优于配置策略，gulp让简单的事情继续简单，复杂的任务变得可管理。
>   - 高效：通过利用node.js强大的流，不需要往磁盘写中间文件，可以更快地完成构建。
>   - 高质量：gulp严格的插件指导方针，确保插件简单并且按你期望的方式工作。
>   - 易于学习：通过把API降到最少，你能在很短的时间内学会gulp。构建工作就像你设想的一样：是一系列流管道。

> Gulp通过**流和代码优于配置**策略来尽量简化任务编写的工作。

别的先不说，通过代码来比较两者（gulp VS grunt）
可以参照我的代码，也可以阅读[该文章] (http://www.techug.com/gulp)。

- [Gruntfile.js](https://github.com/hjzheng/angular-cuf-nav/blob/master/Gruntfile.js)
- [gulpfile.js](https://github.com/hjzheng/html2js-gulp-for-cuf/blob/master/gulpfile.js)

两者的功能基本类似，gulp是通过代码完成任务，体现了代码优于配置的原则，对程序员更加友好，另外它也可以将多个功能一次性串起来，不需要暂存在本地，体现了对流的使用，这个可以阅读[该文章](http://www.techug.com/gulp)里的例子。

另外，经常会有人问，为什么gulp比grunt快，这个可以参考这篇[文章](https://github.com/imsobear/blog/issues/40)

#### 常用资料
- Gulp官网 http://gulpjs.com/
- Gulp中文网 http://www.gulpjs.com.cn/
- Gulp插件网 http://gulpjs.com/plugins/
- Awesome Gulp https://github.com/alferov/awesome-gulp

#### gulp常用插件

- **流控制**
  - [event-stream](http://www.atticuswhite.com/blog/merging-gulpjs-streams/) 事件流，不是插件但很有用 
  - [gulp-if](https://github.com/robrich/gulp-if) 有条件的运行一个task
  - [gulp-clone](https://github.com/mariocasciaro/gulp-clone) Clone files in memory in a gulp stream 非常有用
  - [vinyl-source-stream](https://github.com/hughsk/vinyl-source-stream) Use conventional text streams at the start of your gulp or vinyl pipelines 

- **AngularJS**
  - [gulp-ng-annotate](https://github.com/Kagami/gulp-ng-annotate) 注明依赖 for angular
  - [gulp-ng-html2js](https://github.com/marklagendijk/gulp-ng-html2js) html2js for angular
  - [gulp-angular-extender](https://libraries.io/npm/gulp-angular-extender) 为angular module添加dependencies

- **文件操作**
  - [gulp-clean](https://github.com/peter-vilja/gulp-clean)  删除文件和目录
  - [gulp-concat](https://github.com/wearefractal/gulp-concat) 合并文件
  - [gulp-rename](https://github.com/hparra/gulp-rename) 重命名文件
  - [gulp-order](https://github.com/sirlantis/gulp-order) 对src中的文件按照指定顺序进行排序
  - [gulp-filter](https://github.com/sindresorhus/gulp-filter) 过滤文件 非常有用

- **压缩**
  - [gulp-minify-css](https://github.com/murphydanger/gulp-minify-css)压缩css
  - [gulp-uglify](https://github.com/terinjokes/gulp-uglify) 用uglify压缩js


- **工具**
  - [gulp-load-plugins](https://github.com/jackfranklin/gulp-load-plugins) 自动导入gulp plugin
  - [gulp-load-utils](https://www.npmjs.com/package/gulp-load-utils) 增强版gulp-utils
  - [gulp-task-listing](https://github.com/OverZealous/gulp-task-listing) 快速显示gulp task列表
  - [gulp-help](https://github.com/chmontgomery/gulp-help) 为task添加帮助描述
  - [gulp-jsdoc](https://github.com/jsBoot/gulp-jsdoc) 生成JS文档

- **JS/CSS自动注入**
  - [gulp-usemin](https://github.com/zont/gulp-usemin) Replaces references to non-optimized scripts or stylesheets into a set of HTML files
  - [gulp-inject](https://github.com/klei/gulp-inject) 在HTML中自动添加style和script标签 [Example](https://github.com/hjzheng/CUF_meeting_knowledge_share/tree/master/2015-8-17/bower-dependence-inject)
  - [wiredep](https://github.com/taptapship/wiredep) 将bower依赖自动写到index.html中 [Example](https://github.com/hjzheng/CUF_meeting_knowledge_share/tree/master/2015-8-17/bower-dependence-inject)
  - [gulp-useref](https://github.com/jonkemp/gulp-useref) 功能类似与usemin [Example](https://github.com/hjzheng/CUF_meeting_knowledge_share/tree/master/2015-8-17/bower-dependence-inject)

- **浏览器相关**
  - [browser-sync](https://github.com/BrowserSync/browser-sync) 自动同步浏览器，结合gulp.watch方法一起使用 [Example](https://github.com/hjzheng/CUF_meeting_knowledge_share/tree/master/2015-5-30/gulp-babel-test)

- **Transpilation**
  - [gulp-babel](https://github.com/babel/gulp-babel) 将ES6代码编译成ES5   [Example](https://github.com/hjzheng/CUF_meeting_knowledge_share/tree/master/2015-5-30/gulp-babel-test)
  - [babelify](https://github.com/babel/babelify)  Browserify transform for Babel
  - [gulp-traceur](https://github.com/sindresorhus/gulp-traceur)  Traceur is a JavaScript.next-to-JavaScript-of-today compiler 

- **打包**
  - [gulp-browserify](https://www.npmjs.com/package/gulp-browserify)  用它和 babelify 实现ES6 module [Example](https://github.com/hjzheng/CUF_meeting_knowledge_share/tree/master/2015-5-30/gulp-es6-module)

- **编译**
  - [gulp-less](https://github.com/plus3network/gulp-less)  处理less [Example](https://github.com/hjzheng/CUF_meeting_knowledge_share/tree/master/2015-7-23/gulp-less-bootstrap)
  - [gulp-sass](https://github.com/dlmanning/gulp-sass) 处理sass

- **其他**
  - [gulp-autoprefixer](https://github.com/sindresorhus/gulp-autoprefixer)  Prefix CSS
  - [gulp-sourcemaps](https://github.com/floridoo/gulp-sourcemaps) 生成source map文件
  - [gulp-rev](https://github.com/sindresorhus/gulp-rev) Static asset revisioning by appending content hash to filenames: unicorn.css → unicorn-d41d8cd98f.css 
  - [gulp-iconfont](https://github.com/nfroidure/gulp-iconfont) 制作iconfont [Example](https://github.com/hjzheng/CUF_meeting_knowledge_share/tree/master/2015-7-24/gulp-test-iconfont)
  - [gulp-svg-symbols](https://github.com/Hiswe/gulp-svg-symbols) 制作SVG Symbols, [关于使用SVG Symbol](http://isux.tencent.com/zh-hans/16292.html)
  - [gulp-template](https://github.com/sindresorhus/gulp-template) 模板替换
  - [gulp-dom-src](https://github.com/cgross/gulp-dom-src) 将html中的script，link等标签中的文件转成gulp stream。
  - [gulp-cheerio](https://github.com/KenPowers/gulp-cheerio) Manipulate HTML and XML files with Cheerio in Gulp. 

#### gulp入门视频 

- **Learning Gulp** (youtube)
  - [Learning Gulp #1 - Installing & Introducing Gulp ](https://www.youtube.com/watch?v=wNlEK8qrb0M)
  - [Learning Gulp #2 - Using Plugins & Minifying JavaScript](https://www.youtube.com/watch?v=Kh4eYdd8O4w)
  - [Learning Gulp #3 - Named Tasks ](https://www.youtube.com/watch?v=YBGeJnMrzzE)
  - [Learning Gulp #4 - Watching Files With Gulp ](https://www.youtube.com/watch?v=0luuGcoLnxM)
  - [Learning Gulp #5 - Compiling Sass With Gulp ](https://www.youtube.com/watch?v=cg7lwX0u-U0)
  - [Learning Gulp #6 - Keep Gulp Running With Plumber ](https://www.youtube.com/watch?v=rF6niaDKcxE)
  - [Learning Gulp #7 - Handling Errors Without Plumber ](https://www.youtube.com/watch?v=o24f4imRbxQ)
  - [Learning Gulp #8 - LiveReload With Gulp ](https://www.youtube.com/watch?v=r5fvdIa0ETk)
  - [Learning Gulp #9 - Easy Image Compression](https://www.youtube.com/watch?v=oXxMdT7T9qU)
  - [Learning Gulp #10 - Automatic Browser Prefixing ](https://www.youtube.com/watch?v=v259QplNDKk)
  - [Learning Gulp #11 - Gulp Resources & What's Next ](https://www.youtube.com/watch?v=vGCzovUFBIY)

- **Get started with gulp**(youtube)
  - [Get started with gulp Part 1: Workflow overview and jade templates](https://www.youtube.com/watch?v=DkRoa2LooNM&index=8&list=PLhIIfyPeWUjoySSdufaqfaSLeQDmCCY3Q)
  - [Get started with gulp Part 2: gulp & Browserify](https://www.youtube.com/watch?v=78_iyqT-qT8&index=9&list=PLhIIfyPeWUjoySSdufaqfaSLeQDmCCY3Q)
  - [Get started with gulp Part 3: Uglify & environment variables](https://www.youtube.com/watch?v=gRzCAyNrPV8&index=10&list=PLhIIfyPeWUjoySSdufaqfaSLeQDmCCY3Q)
  - [Get started with gulp Part 4: SASS & CSS minification](https://www.youtube.com/watch?v=O_0S6Z9FIKM&index=11&list=PLhIIfyPeWUjoySSdufaqfaSLeQDmCCY3Q)
  - [Get started with gulp Part 5: gulp.watch for true automation](https://www.youtube.com/watch?v=nsMsFyLGjSA&list=PLhIIfyPeWUjoySSdufaqfaSLeQDmCCY3Q&index=12)
  - [Get started with gulp Part 6: LiveReload and web server](https://www.youtube.com/watch?v=KURMrW-HsY4&list=PLhIIfyPeWUjoySSdufaqfaSLeQDmCCY3Q&index=13)

- **Gulp in Action** (慕课网)
  - [Gulp in Action(一)](http://www.imooc.com/video/5692)
  - [Gulp in Action(二)](http://www.imooc.com/video/5693)
  - [Gulp in Action(三)](http://www.imooc.com/video/5694)

- **BGTSD** (youtube)
  - [BGTSD - Part 20: Gulp and Babel Basics ](https://www.youtube.com/watch?v=Mo2xqBPbnlQ)
  - [BGTSD - Part 21: TypeScript and Gulp Basics ](https://www.youtube.com/watch?v=5Z82cpVP_qo)

- **John Papa**(付费)
  - [JavaScript Build Automation With Gulp.js](http://www.pluralsight.com/courses/javascript-build-automation-gulpjs)

#### gulp精彩文章
- [Using GulpJS to Generate Environment Configuration Modules](http://www.atticuswhite.com/blog/angularjs-configuration-with-gulpjs/)
- [Merging multiple GulpJS streams into one output file](http://www.atticuswhite.com/blog/merging-gulpjs-streams/)
- [Getting ES6 modules working thanks to Browserify, Babel, and Gulp](http://advantcomp.com/blog/ES6Modules/)
- Gulp学习指南系列：
  - [Gulp学习指南之入门](http://segmentfault.com/a/1190000002768534)
  - [Gulp学习指南之CSS合并、压缩与MD5命名及路径替换](http://segmentfault.com/a/1190000002932998)
- [6 Gulp Best Practices](http://blog.rangle.io/angular-gulp-bestpractices/?utm_source=javascriptweekly&utm_medium=email) :star:
  - Automate all Imports (gulp-inject, wiredep, useref and angular-file-sort)
  - Understand directory structure requirements 
  - Provide distinct development and production builds  (browser-sync)
  - Inject files with gulp-inject and wiredep ( gulp-inject and wiredep )
  - Create production builds with gulp-useref (gulp-useref)
  - Separate Gulp tasks into multiple files ```require('require-dir')('./gulp')```
- [Gulp 范儿 -- Gulp 高级技巧](http://csspod.com/advanced-tips-for-using-gulp-js/) :star:
- [Gulp 错误管理](http://csspod.com/error-management-in-gulp/) :star:
- [探究Gulp的Stream](http://segmentfault.com/a/1190000003770541)
- [Gulp安装及配合组件构建前端开发一体化](http://www.dbpoo.com/getting-started-with-gulp/)
- [Gulp入门指南](https://github.com/nimojs/gulp-book)
- [Gulp入门指南 - nimojs](https://github.com/nimojs/blog/issues/19)
- [Gulp入门教程](http://markpop.github.io/2014/09/17/Gulp%E5%85%A5%E9%97%A8%E6%95%99%E7%A8%8B/)
- [Gulp开发教程（翻译）](http://www.w3ctech.com/topic/134)
- [Gulp：任务自动管理工具 - ruanyifeng](http://javascript.ruanyifeng.com/tool/gulp.html)
- [BrowserSync — 你值得拥有的前端同步测试工具](http://segmentfault.com/a/1190000003787713)

#### gulp项目应用实例
- [gulp模式](https://github.com/johnpapa/gulp-patterns) 
- [gf-skeleton-angularjs](https://github.com/gf-rd/gf-skeleton-angularjs)
- [generator-hottowel](https://github.com/johnpapa/generator-hottowel)

#### [gulp常见问题](http://segmentfault.com/t/gulp?type=newest)

- [如何拷贝一个目录?](http://stackoverflow.com/questions/25038014/how-do-i-copy-directories-recursively-with-gulp)
```js
gulp.src([ files ], { "base" : "." })
```

不定期更新中 ... ...
