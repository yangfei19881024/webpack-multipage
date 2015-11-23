#webpack多页开发
##开发环境
`npm run dev`
##上线打包
`npm run release`
##本项目参考
[source](https://github.com/chemdemo/webpack-bootstrap.git)
### 业务开发

##### 目录结构

``` js
- root/
  - src/                   # 开发目录
    + css/                 # css资源
    + img/                 # 图片资源
    + js/                  # js&jsx资源
    + scss/                # scss资源
    + tmpl/                # 前端模板
    a.html                 # 入口文件a
    b.html                 # 入口文件b
  + assets/                # 编译输出目录
  + mock/                  # 假数据文件
  app.js                   # 本地server入口
  routes.js                # 本地路由配置
  webpack.config.js        # webpack配置文件
  webpack-dev.config.js    # 开发环境webpack配置文件
  gulpfile.js              # gulp任务配置
  config.rb                # compass配置
  package.json             # 项目配置
  README.md                # 项目说明
```

##### 单/多页面支持

约定`/src/*.html`为应用的入口文件，在`/src/js/`一级目录下有一个同名的js文件作为该入口文件的逻辑入口（即entry）。

在编译时会扫描入口html文件并且根据webpack配置项解决entry的路径依赖，同时还会对html文件进行压缩、字符替换等处理。

这样可以做到同时支持SPA和多页面型的项目。
