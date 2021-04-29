# travel

# 2021年4月29日 梳理兄弟组件间数据如何联动、实现点击字母弹出对应列表
  前提，List、Alphabet组件都是City组件的子组件，有公共父组件，所以不需用bus实现
  数据共享，使用$emit与prop即可

  步骤：
  1. 使用watch属性监听List中属性的变化，当letter变化时，通过this.$refs[字母][0]
     来拿到相应的dom，并使用该dom作为参数传入this.scroll.scrollToMove()来实现
     跳转到对应的列表模块
  2. 在Alphabet中，要实现滑动到对应字母，就弹出相应的字母开头的列表块。首先通过计算
     被滑动字母的位置与A字母之差，再除以字母块的高，得出对应的距离，再将该距离作为inedx
     传入this.letters，从而得到相应的字母。之后，使用this.$emmit，将之派发到父组
     件上，父组件再调用handleLetterChange把更新后的字母传给List组件，List组件监听
     到letter变化后，触发监听属性letter()调用 this.scroll.scrollToMove()来实现
     滚动跳转

# 2021年4月26日踩的坑
  1.更加注意函数名后面要加括号了

  2.要注意对象数组的逗号后面需要换行

  3.在Eslint中，行内不可以有空位···no trailing-space

# 2021年4月24日踩的坑
  stylus 的 outdent 问题，这是tab和空格混用了
  解决方法： 赋值没问题的stylus过来，再修改···
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
