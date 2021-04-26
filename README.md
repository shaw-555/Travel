# travel

> (Vue 2.x 项目实战 )
> 
# 2020年4月25日踩的坑

```
1.stylus-loader 版本 高于 stylus，所以需要删除 stylus-loader ，再安装指定版本的stylus-loader

2.引入组件时，发生了文件路径引入的错误

3.在npm run start时，时常发生错误，后来在查各种资料后，确认要在 build/webpack.dev.config 下 把 Host 值改为 ’localhost‘就好了
  但是后来不知道为什么Host又变回了原来的值···
```
## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
