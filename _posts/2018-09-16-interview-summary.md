最近面试了很多家互联网公司，包括阿里， 拼多多，七牛云（挂了），今日头条（止步一面，丢脸），平安
面试题分为几个方面的问题：
#### 1. JS方面（核心，频率最高）
  ##### a. bind函数怎么实现？
  ```javascript
  Function.prototype.myBind = function (context) {
    var args = Array.prototype.splice.call(arguments);
    var self = this;
    return function() {
      return self.apply(context, args.concat(Array.prototype.splice.call(arguments, 1)));
    }
  }
  ```
  ###### b. 说一说js闭包。
  ###### c. 将{a: 1, b: 2} 转为： [['a', 1], ['b', 2]]
  ###### d. 遍历对象属性有哪些方法？
  ###### e. Object.keys()能拿到对象的原型链的属性吗？
  ###### f. new操作符的原理，写一个自己的new方法实现js的new操作符。
  ###### g. 如何实现apply方法？
  ###### h. 以下输出是什么？
    ```javascript
      for(var i=0;i<5;i++){
          setTimeout(function(){
              console.log(i);
          });
      }
    ```
  ###### i. 如何实现以上代码的正确输出？（闭包，let）
  ###### j. 如果要0秒打印0，1秒打印1，2秒打印2，直到第100秒打印100，写出代码。
  ###### k. 使用promise实现上一题的需求。
  ###### l. 实现一个链式调用， a().b().c();
  ###### m. 实现a, b, c三者的任意调用， a().b().c(), b().a().c(), c().a().b()等
  ###### n. var year = 2017;
    var month = 7;
    var day = 12;
    实现 render(‘${year}-${month}-${day}’)
  ###### o. 现在render是任意模版，render(‘今天是${year}年${month}月${day}日’)，怎么实现？
  ###### p. 实现一个自己的Object.create()方法
  ###### q. 数组去重，O(n)的算法复杂度
  ###### r. Set怎么做到代码去重的？
  ###### s. Promise.all()的实现方法
  ###### t. js中的class和prototype有什么不一样？

#### 2. css方面
  ###### a. css的rem和em有什么不一样。
  ###### b. css中选择器的优先级
  ###### c. position的细节
  ###### d. 怎么实现元素的垂直居中
  ###### e. css的盒子模型
  ###### f. css中背景延伸问题

#### 3. BOM方面
  ###### a. js中操作dom的一些api（增删改查）

#### 4. React框架方面
  ###### a. createStore方法怎么实现？
  ###### b. store的结构是怎样的？
  ###### c. 多页面结构中，怎么combine多个reducer和state？
  ###### d. react的diff算法
  ###### e. react中怎么做性能优化？

#### 5. 算法和数据结构
  ###### a. 冒泡排序和快速排序的思路和时间复杂度？
  ###### b. 斜四十五度打印二维数组（z字型）
  ###### c. typeahead多级列表（树结构）

#### 6. 网络方面内容
  ###### a. 为什么会跨域？
  ###### b. 跨域的几种方法？
  ###### c. HTTP Request Header头的各种细节
  ###### d. JSONP
  ###### e. CORS
  ###### f. 为什么服务器端可以不跨域呢？
  ###### g. 什么是session
  ###### h. cookie是什么？