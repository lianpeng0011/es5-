# `JS`内容复习

### `JS`两种引入方式

- 内嵌式

  ```js
  <script> 
      console.log('我是内嵌式')
  </script>
  ```

- 外链式

```js
<script src="filePath.js"></script>
```

> 注意： <script src=""  /> 这种写法是错误的
>
> script标签的type 属性可以省略，但是值不能修改

### `JS`的注释方式

- 单行注释

  ```js
   // 单行注释
  ```

- 多行注释

  ```js
  /**
    多行注释
  */
  ```

### `JS`类型

- 简单类型

  - string   字符串

    ```js
     var  str = '124';
     var str = "23465";
     //错误演示
     var str = 'dshjda";
    ```

  - number  数字

    ```js
     var num = 123;
    ```

  - boolean   布尔类型

    ```js
    var bool = true;
    var bool = false;
    ```

  - undefined  未定义

    ```js
    var und;
    ```

  - null   空 

    ```js
    //定义一个null 的对象
    var name = null;
    ```

- 复杂类型

  - date  日期
  - 正则
  - 错误
  - 数组
  - 函数

### `JS`字符串类型

- 转换

  - new

    ```js
    var str = 123;
    str = new String(str);
    ```

  - `toString()`

    ```js
     var str = 123;
    str.toString();
    ```

  - 加号

    ```js
    var str = 12;
    str + "";
    str + "aaa";
    ```

- 拼接

  ```js
   //使用 + 对字符串进行拼接
  "Hello" + "" + "Word";
  ```

### `JS`运算符

- 算数运算符    +   -   *   /  % 

- 逻辑运算符  

  - || 或    左右两边有一个真即为真
  - && 且    左右两边必须同时为真
  - ! 非    取反

- 比较运算符     >    ==   <   >=   <=   !=

- 赋值运算符 

  -  = 

  - +=  

    ```js
     var num = 1;
     num += 2;
    // 等价于
    num = num + 2；
    ```

  - -=

  - *=

  - /=

  - %=

- 逗号运算符   从左到右依次进行计算  计算时，要根基符号优先级进行计算

  ```js
   x=2, x*2;
  ```

### 符号优先级

- 看下文档中符号的优先级

### 三元表达式

  三元表达式，也叫三目运算符

```js
// 表达式1 ？ 表达式2 ： 表达式3；
//当表达式结果为true 返回 表达式2 
//当结果为false时 返回表达式3
var  sex = '男';
var age = 18;
var result ;
result = sex == '男' ？ '是男的' : '未知';
result = sex == '女' && age == 18 ? '成年' ： '未成年';
```

### `JS`已学习过的关键字

- `typeof`  查询变量的类型 ， 返回的结果类型为字符串(string)

  ```js
  var name = '张三';
  typeof name;
  ```

- `var`  定义一个变量

  ```js
  //定义一个变量 方式有3定义变量的方式
  var value = 1;  //显示的定义一个固定值，这个值称之为字面量
  var name;
  name = "张三";
  var result = 1 + 2； //通过js语句给变量赋值 需要执行的后进行赋值的都称作语句
  ```

- `function` 定义一个函数

  ```js
  //function 关键字 + 函数名称 + () + {}
  //() 中用来方式函数接收的参数 如果是多个参数时，用逗号分隔
  //{} 中是这个函数具体执行语句
  function change(){
      //函数执行语句
  }
  //通过js调用函数
  change();
  ```

- `this`  当前元素或者作用域的对象

- `break`  跳出或者结束当前执行语句

- `if else`  选择语句

  ```js
  //第一种if语句
  //()中传入的是需要判断变量或对象的 js语句
  //() 中用来进行判断的值 只有两种结果 true false
  var res = '判断语句';
  //获取true 或者false 的方式 
  res == '语句'; //使用 == 或者 === 等于
  res || true；  //使用逻辑运算 || && ！
  // 直接使用boolean类型的变量
  if(res){
     
  }
  // 第二种方式
  if(res){
      //当（）中结果为true时执行
  }else{
      //当（）中结果false时执行
  }
  // 第三种方式
  if(res == 1){
     //当（）中结果为true时执行
  }else if(res == 2){
      //当（）中结果为true时执行   
  }else{
      //上面的全部不匹配，就执行这里
  }
  //第四种 嵌套方式
  if(){
    if(){
      
     } 
  }
  ```

- `switch case default` 第二种选择语句

  ```js
  // () 中传入需要判断的变量
  //可传入变量的类型  boolean、number、string
  // 在case 进行比较时，不只比较结果，而且还比较类型 使用的是绝对相等
  switch('变量'){
         case 1:
            //执行结果
         		break;
         case 2 :
            //执行结果
            break;
         default :
            //如果上面都不符合那么执行default中的代码
  }
  ```

- `new`   定义一个对象

  ```js
  var date = new Date();
  var str = new String();
  ```

### `js` 使用的一些函数

- 3种提示方式--- 弹窗

  - alert    直接弹出框   没有返回值，只是一个提示

    ```js
     alert('需要提示的内容');
    ```

  - prompt  输入弹出框   是带返回值的弹出框。 点击确定返回输入值，点击取消返回null

    ```js
    // 用法
    /**
     第一个参数 ： 弹框上显示的内容
     第二个参数 ： 输入框的默认值 
     返回值 ： 类型 是 string
    */
    //将表达式中返回的结果赋予变量
    var value = prompt( '内容','值' );
    ```

  - confirm  确认提示框   有返回值，类型为 boolean。点击确定时返回true

    ```js
    /**
    	参数: 提示内容
    	返回值：  boolean类型
    */
    var result = confirm('提示内容');
    ```

- `document` 对象， `dom`对象是`html`中显示的内容的一种抽象的命名。

  ```js
  //根据id获取元素对象， id 是html中 标签的id
  document.getElementById( 'id' )；
  //动态给html中的body 写入内容，但是会覆盖body中原有的内容
  document.write('内容');
  ```

- `console`对象， 用来做浏览器的控制台输出语句。绝大多数用法是在开发中进行js调试使用

  ```js
  console.log('控制台输出的内容')；
  ```

- `isNaN`方法， 判断对象是否是数值

  ```js
  var num = 1;
  /**
     参数 ： 需要判断的变量
     返回值： boolean类型， 当传入的变量的非数值时返回true
     is not number
  */
  var is = isNaN( num );
  ```

- `parseInt` 将变量转换为number 类型 正数

  ```js
   parseInt( "123" );
   //当字符串起始位置包含数字是，会将连续的数字取出，转换为number
   parseInt( "11ssss" );
   //如果传入变量为非数字，则转化为NaN
   parseInt('shdjadhaj');
  ```

- `parseFloat` 将变量转化为number 类型 用法和`parseInt`相等  浮点数

- `Number.MAX_VALUE` 获取数字的最大值
- `Number.MIN_VALUE`  获取数字的最小值

