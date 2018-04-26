## JavaScript在你的页面做什么
HTML和CSS已经被集合组装成一个网页后，浏览器的JavaScript引擎执行JavaScript。这保证了当JavaScript开始执行时，网页的结构和样式已经在该出现的地方了。
这是一件好事，正如JavaScript的普遍用处是使用DOM API动态的修改HTML和CSS来更新用户交互页面。如果JavaScript在HTML和CSS加载之前运行，那么会发生错误。

## 解释代码 vs 编译代码
JavaScript是解释语言--代码从上而下运行，而运行的结果会立马返回。在浏览器运行代码前，不必把它转化为其他的形式。
编译语言--需要在运行前转化为另一种语言。比如C/C++则要先被编译成汇编语言，然后再由电脑运行。

## 基本数据类型
Undefined Null Number Boolean String Object

## 算数运算符
+ - * /

## 比较运算符

* ===（严格等号运算符）<br>
 ==代表相同，===代表严格相同<br>
 当双等号比较的时候：先检查两个操作数的数据类型，如果相同，则进行===比较；如果不同，则先进行一次类型转换，转换成相同的类型后在进行比较。<br>
 ===比较时，如果类型不同，直接false<br>
 #### 比较过程
 ```
 ==：
 (1)如果两个值类型相同，再进行‘===’比较
 (2)如果两个值类型不同，也有可能相等，需根据以下规则进行类型转换再比较：
   1）如果是一个null，一个是undefined，那么相等。
   2) 如果一个是字符串，一个事数值，把字符串转换成数值后再进行比较。
 ===：
 (1)如果类型不同，就一定不相等。
 (2)如果两个都是Number，并且是同一个值，那么相等；如果其中至少一个NaN，那么不想等。（判断一个值是否是NaN，只能用isNaN()来判断）。
 (3)如果两个都是字符串，每个位置的字符都一样，那么相等，否则不等。
 (4)如果两个值都是true，或false，那么相等。
 (5)如果两个值都引用同一个对象或函数，那么相等，否则不等。
 (6)如果两个都是null，或undefined，那么相等。
 ```
* !==（严格不等于运算符）< >

#### 声明
```
var 声明拘捕变量和全局变量
let 声明块级作用域的局部变量
const 声明块级作用域的只读的命名常量
(注：x=42 直接赋值, 这样会声明一个全局变量并会在严格模式下产生一个ReferenceError,声明变量时不应该用这种方式)
#### ReferenceError(引用错误)对象表明一个不存在的变量被引用
当你尝试引用一个未被定一个变量时，将会抛出一个ReferenceError
```

var 1;let x;用var或let声明的变量，如果没有赋初值，其值为undefined <br>
1.使用undefined来判断变量是否已经赋值
```
var input;
if(input === undefined){
  doThis();
}else {
  doThat();
}
```
2.undefined值在Boolean环境中会被当作false。
```
var myArray = [];
if(!myArray[0]) {
//数组中的元素未被赋值，是undefined，当作了false
  myFunction();
}
```
3.数值环境中的undefined值会被转换为NaN
```
var a;
//计算为NaN
a+2;
```

4.当你对一个null变量求值的时候空值 null 在数值类型环境中会被当作0来对待，而布尔类型环境中会被当作 false。
```
var n = null;
typeof(n);
//object
console.log(n*32);//0
```


