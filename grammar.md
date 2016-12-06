## let

* 变量作用域

> 只在块级作用域内有效

    var arr=[];
    for(var i=0;i<10;i++){  
      console.log(i)
    }
    console.log(i)  // 10
    arr[3]()  // 10

*i是全局变量，会在循环执行完成后变成10，会同时修改每项的i值*

    var arr=[]
    for(let i=0;i<10;i++){
      console.log(i)
    }
    console.log(i)  // Error
    arr[3]()  // 3
    
*此时i只有在循环体内部才能获取，所以输出i会报错，每完成一次循环i值不会再变* 
