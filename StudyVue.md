# Vue.js 为 v-on 提供了 事件修饰符
阻止单击事件冒泡
```
<a v-on:click.stop="doThis"></a>
```
提交事件不再重载页面
```
<form v-on:submit.prevent="onSubmit"></form>
```
 修饰符可以串联
```
<a v-on:click.stop.prevent="doThat"></a>
```
只有修饰
```
<form v-on:submit.prevent></form>
```
添加事件侦听器时使用事件捕获模式
```
<div v-on:click.capture="doThis">...</div>
```
只当事件在该元素本身（比如不是子元素）触发时触发回调
```
<div v-on:click.self="doThat">...</div>
```
点击事件将只会触发一次
```
<a v-on:click.once="doThis"></a>
```
