# chimee-helper-utils

[![Build Status](https://img.shields.io/travis/Chimeejs/chimee-helper-utils/master.svg?style=flat-square)](https://travis-ci.org/Chimeejs/chimee-helper-utils.svg?branch=master)
[![Coverage Status](https://img.shields.io/coveralls/Chimeejs/chimee-helper-utils/master.svg?style=flat-square)](https://coveralls.io/github/Chimeejs/chimee-helper-utils?branch=master)
[![npm](https://img.shields.io/npm/v/chimee-helper-utils.svg?colorB=brightgreen&style=flat-square)](https://www.npmjs.com/package/chimee-helper-utils)
[![dependency Status](https://david-dm.org/Chimeejs/chimee-helper-utils.svg)](https://david-dm.org/Chimeejs/chimee-helper-utils)
[![devDependency Status](https://david-dm.org/Chimeejs/chimee-helper-utils/dev-status.svg)](https://david-dm.org/Chimeejs/chimee-helper-utils?type=dev)

utils of chimee

## get started

```shell
npm install chimee-helper-utils --save
```

if you are using `flow`, you should import our flow defination, by adding this to your `.flowconfig`.

```ya
[ignore]

[include]

[libs]
./node_modules/chimee-helper-utils/lib/index.flow.js
[options]

[lints]
```

## doc

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

### inBrowser

[src/index.js:8-10](https://github.com/Chimeejs/chimee-helper-utils/blob/7eff79e4cede1bda28a36e60ae0893583a493ba3/src/index.js#L8-L10 "Source code on GitHub")

check if the code running in browser environment (not include worker env)

Returns **[Boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** 

### makeArray

[src/index.js:16-18](https://github.com/Chimeejs/chimee-helper-utils/blob/7eff79e4cede1bda28a36e60ae0893583a493ba3/src/index.js#L16-L18 "Source code on GitHub")

转变一个类数组对象为数组

**Parameters**

-   `obj` **any** 

Returns **[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;any>** 

### transObjectAttrIntoArray

[src/index.js:27-33](https://github.com/Chimeejs/chimee-helper-utils/blob/7eff79e4cede1bda28a36e60ae0893583a493ba3/src/index.js#L27-L33 "Source code on GitHub")

sort Object attributes by function
and transfer them into array

**Parameters**

-   `obj` **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** Object form from numric
-   `fn` **[Function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function)** sort function (optional, default `(a,b)=>+a-+b`)

Returns **[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)** the sorted attirbutes array

### runRejectableQueue

[src/index.js:39-56](https://github.com/Chimeejs/chimee-helper-utils/blob/7eff79e4cede1bda28a36e60ae0893583a493ba3/src/index.js#L39-L56 "Source code on GitHub")

run a queue one by one.If include function reject or return false it will stop

**Parameters**

-   `queue` **[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)** the queue which we want to run one by one
-   `args` **...any** 

Returns **[Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)** tell us whether a queue run finished

### runStoppableQueue

[src/index.js:62-74](https://github.com/Chimeejs/chimee-helper-utils/blob/7eff79e4cede1bda28a36e60ae0893583a493ba3/src/index.js#L62-L74 "Source code on GitHub")

run a queue one by one.If include function return false it will stop

**Parameters**

-   `queue` **[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)** the queue which we want to run one by one
-   `args` **...any** 

Returns **[boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** tell the user if the queue run finished

### setFrozenAttr

[src/index.js:82-91](https://github.com/Chimeejs/chimee-helper-utils/blob/7eff79e4cede1bda28a36e60ae0893583a493ba3/src/index.js#L82-L91 "Source code on GitHub")

set an attribute to an object which is frozen.
Means you can't remove it, iterate it or rewrite it.

**Parameters**

-   `obj` **!primitive** 
-   `key` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** 
-   `value` **Anything** 

### setAttrGetterAndSetter

[src/index.js:100-120](https://github.com/Chimeejs/chimee-helper-utils/blob/7eff79e4cede1bda28a36e60ae0893583a493ba3/src/index.js#L100-L120 "Source code on GitHub")

set attr on an Object. We will bind getter and setter on it if you provide to us

**Parameters**

-   `obj` **!primitive** 
-   `key` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** 
-   `$2` **any**  (optional, default `{}`)
    -   `$2.get`  
    -   `$2.set`  
-   `prefix` **[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** the origin data's prefix. We do not plan to save it by closure. (optional, default `'__'`)
-   `get` **[Function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function)** 
-   `set` **[Function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function)** 

### throttle

[src/index.js:232-280](https://github.com/Chimeejs/chimee-helper-utils/blob/7eff79e4cede1bda28a36e60ae0893583a493ba3/src/index.js#L232-L280 "Source code on GitHub")

函数节流（控制函数执行频率）

**Parameters**

-   `func` **[Function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function)** 要节流控制的函数，必填
-   `wait` **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** 
-   `options` **any** 
-   `cxt` **any** 

Returns **[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** wait 等待时长

Returns **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** options {
                     leading&lt;是否首次调用立即执行，否：则按wait设定等待到期后调用才执行>:false,
                     trailing&lt;是否在调用并未到期时启用定时器，以保证一定执行>:true
                   }

Returns **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** cxt 上下文对象

Returns **[Function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function)** 

### addTransMethod

[src/index.js:323-336](https://github.com/Chimeejs/chimee-helper-utils/blob/7eff79e4cede1bda28a36e60ae0893583a493ba3/src/index.js#L323-L336 "Source code on GitHub")

给obj对象扩展上trans方法，用以实现methodName对应的属性方法包装为静态函数且保持上下文的功能

**Parameters**

-   `obj` **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** 目标对象

### appendCSS

[src/index.js:343-353](https://github.com/Chimeejs/chimee-helper-utils/blob/7eff79e4cede1bda28a36e60ae0893583a493ba3/src/index.js#L343-L353 "Source code on GitHub")

追加样式代码到head的style标签，不存在则创建

**Parameters**

-   `cssText` **[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** 样式文本

Returns **[HTMLElement](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)** 

### formatDate

[src/index.js:361-379](https://github.com/Chimeejs/chimee-helper-utils/blob/7eff79e4cede1bda28a36e60ae0893583a493ba3/src/index.js#L361-L379 "Source code on GitHub")

格式化日期对象为：年-月-日 时:分:秒.毫秒

**Parameters**

-   `date` **[Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)** Date日期对象 (optional, default `new Date()`)
-   `pattern` **[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** 要输出的日期格式，默认：`yyyy-MM-dd hh:mm:ss.i` (optional, default `'yyyy-MM-dd hh:mm:ss.i'`)

Returns **[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** 

### getLocalStorage

[src/index.js:386-397](https://github.com/Chimeejs/chimee-helper-utils/blob/7eff79e4cede1bda28a36e60ae0893583a493ba3/src/index.js#L386-L397 "Source code on GitHub")

读取本地存储的值（不支持localStorage则降级到cookie）

**Parameters**

-   `key` **[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** 目标数据key

Returns **[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** 

### setLocalStorage

[src/index.js:404-415](https://github.com/Chimeejs/chimee-helper-utils/blob/7eff79e4cede1bda28a36e60ae0893583a493ba3/src/index.js#L404-L415 "Source code on GitHub")

将指定key对应值写入本地存储（不支持localStorage则降级到cookie）

**Parameters**

-   `key` **[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** 
-   `val` **[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** 

Returns **[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** 
