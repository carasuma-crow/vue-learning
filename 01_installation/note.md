# 安装

[参考链接](https://cn.vuejs.org/v2/guide/installation.html)

## 传统的引用js文件的方式

> 方便做简单的demo演示，方便学习vue功能特性（不需要安装nodejs相关的内容）

与传统的jQuery的开发类似，可以直接在通过`<script>`标签将vue相关的内容引用进来，通过全局对象`Vue`就可以像jq使用`$`一样，使用vue框架的内容

```html
<script src="https://cdn.jsdelivr.net/npm/vue@2.5.13/dist/vue.js"></script>
...
<script>
    var vm = new Vue({
        // 选项
    })
</script>
```

上面的引入和实例化，需要注意的是：

1. 直接下载并用`<script>`标签引入，Vue会被注册为一个全局变量。后面可以直接通过实例化产生vue对象（如代码段中的第二个script块）
2. `vue.js`代表开发版本，包含完整的警告和调试模式。`vue.min.js`为生产版本，删除了警告并做了压缩混淆，占用空间变小，加载速度变快。在实际使用中注意切换
3. 不同的版本有区别，注意锁版本

## 将vue看作是一个包进行安装

> 需要npm安装，但不用遵循脚手架那一套目录结构，比较自由

```sh
# 对于中国大陆用户，建议将 NPM 源设置为国内的镜像
# 最新稳定版
npm install vue
```

## 使用vue-cli安装

> vue-cli是vue提供的命令行工具，该工具为现代化的前端开发工作流提供了开箱即用的构建配置。相当于按照vue官方推荐的目录、配置去构建一个成熟项目，类似于【框架】

```sh
# 全局安装 vue-cli
npm install --global vue-cli
# 创建一个基于 webpack 模板的新项目 my-project (名字可以自定)
vue init webpack my-project

# 安装依赖
cd my-project
# 这里可以对比一下 将vue看作是一个包进行安装 和 使用vue-cli安装 的区别
# cat package.json
npm install
npm run dev
```
