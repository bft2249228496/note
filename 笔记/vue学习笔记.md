## 注册组件必须在实例化对象之前
## MVVM框架的三要素：响应式，模板引擎，渲染
## v-if 和v-for不要放在同一个标签中
## 默认情况下的watch一开始不会执行，只有值变化了才执行。如果需要一开始就执行，需要使用带选项的watch
## watch的适用情况：一个值变化了，影响多个值的情形，合适执行异步操作或较大开销操作的情况；computed的适用情况：一个值由其他值得来，多个值影响一个值的情形，有缓存性，计算所得的值如果没有变化不会重复执行
## created 组件实例已创建，由于未挂载，dom还不存在；mounted 中dom已存在
## vue各个生命周期使用场景：beforeCreate执行时组件实例还未创建，通常用于插件开发中执行一些初始化任务；created组件初始化完毕，各种数据可以使用，常用于异步数据获取；beforeMounted未执行渲染、更新，dom未创建；mounted初始化结束，dom已创建，可用于获取访问数据和dom元素；beforeUpdate更新前，可用于获取更新前各种状态；updated更新后，所有状态已是最新；beforeDestroy销毁前，可用于一些定时器或订阅的取消；destroyed组件已销毁，作用同上
## Vue组件化的理解：组件是可复用的Vue实例，准确讲它们是VueComponent的实例，可增加代码的复用性、可维护性和可测试性
## sfc单文件组件
## v-ref
## Vue.set, this.$set
## vm.$emit
## 事件总线：Vue.prototype.$bus = new Vue();
## 过滤器：格式化和数据的过滤
## 自定义指令：v-directive,自定义指令钩子函数：bind,inserted,update,componentUpdated,unbind
## v-ref和v-directive都能实现dom操作
## 函数式组件：functional:true;无任何管理状态的组件
## scoped只能控制根元素，无法穿透，向下穿透可用深度作用选择器>>>,例如#app>>>a(注意：Sass之类的预处理器无法准确解析>>>,可用/deep/或者::v-deep代替)
## module
## 快速原型开发：使用npm install -g @vue/cli-service-global 安装扩展后，即可使用vue serve和Vue build 命令对单个*.vue文件进行快速原型开发
## 动态路由匹配：在vue-router的路由路径中使用动态路径参数
## 通配符用来做404页面的路径，写在最后面
## 路由跳转：router.push()
## :key前面不能有空格
## props:用于父组件给子组件传值，即子组件用来接收父组件的值
## this.$emit(eventName, [...args]):用于子组件给父组件传值,第一个参数为事件名，其他参数都是作为该事件对应的函数的参数
## v-if和v-else必须连在一起，中间不能用其他标签隔开
## v-key尽量绑定唯一主键id，不要绑定index
## template代替div包裹元素的好处是template不会被页面渲染上
## 当需要两次循环时，可将循环放在父元素上只循环一次
## 遍历对象时，不能直接给对象加属性，可用Vue.set()方法(数组也可以)
## 有些 HTML 元素，诸如 <ul>、<ol>、<table> 和 <select>，对于哪些元素可以出现在其内部是有严格限制的。而有些元素，诸如 <li>、<tr> 和 <option>，只能出现在其它某些特定的元素内部。这会导致我们使用这些有约束条件的元素时遇到一些问题。会被作为无效的内容提升到外部，并导致最终渲染结果出错。可通过is属性解决
## 非根组件的data一定写成一个函数返回一个对象的形式
## ref属性实际上就是一个引用，作用类似于添加id属性，然后进行dom操作
## 父子组件传值的深入理解：父组件通过属性的方式给子组件传值