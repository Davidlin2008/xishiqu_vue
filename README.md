### xishiqu

##项目架构

##项目总结0316
#1. vue的swipe插件 mini ui的引入问题 
需要注意顺序，再就是设置外框以及引入别忘记加css 

#2. json跨域问题 以及json写在哪里

#3. vue.config.js的配置
runtimeCompiler 与  Compiler（淘汰） 
网上的一些方法 有过时的情况：
module.exports = {
  // 基本路径
  baseUrl: '/',
  // 输出文件目录
  outputDir: 'dist',
  // eslint-loader 是否在保存的时候检查
  lintOnSave: true,
  // use the full build with in-browser compiler?
  // https://vuejs.org/v2/guide/installation.html#Runtime-Compiler-vs-Runtime-only
  runtimeCompiler: true, //关键点在这 
  // webpack配置
  // see https://github.com/vuejs/vue-cli/blob/dev/docs/webpack.md
  chainWebpack: () => {},
  configureWebpack: () => {},

  devServer: {
    open: process.platform === 'darwin',
    host: '0.0.0.0',
    port: 5001,
    https: false,
    hotOnly: false,
    // See https://github.com/vuejs/vue-cli/blob/dev/docs/cli-service.md#configuring-proxy
    proxy: null, // string | Object
    before: app => {}
  },
  // 第三方插件配置
  pluginOptions: {
    // ...
  }
}
##项目总结0322
#1. 二级路由的设置，路由路径的注意事项

#2. 接口请求的时间把握，以及后期要注意引入打包的图片压缩工具

#3. 项目文件的分类 能清楚明了