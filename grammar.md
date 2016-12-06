## let

* 变量作用域

> 只在块级作用域内有效

    var arr=[];
    for(var i=0;i<10;i++){  
      console.log(i)
    }
    console.log(i)  // 10
    arr[3]()  // 10

**i是全局变量，会在循环执行完成后变成10，会同时修改每项的i值**

    var arr=[]
    for(let i=0;i<10;i++){
      console.log(i)
    }
    console.log(i)  // Error
    arr[3]()  // 3
    
**此时i只有在循环体内部才能获取，所以输出i会报错，每完成一次循环i值不会再变** 

* 块级作用域{}

> 可以用来取代(function(){})()形式
    
    let a=1
    {
      let a=5
    }
    console.log(a)  //1
    
    var a=1;
    (function(){
      var a=5
    })()
    console.log(a)  //1
    
**效果一样**

## const

> `const` 只能用来声明常量，声明过后不能改变
  用来声明引用类型常量时，地址不能改变，但是属性可以改变
  和`let`一样不能重复声明，同时`const`声明时必须要赋值否则会报错
