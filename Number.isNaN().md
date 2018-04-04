# Number.isNaN()
> Number.isNaN()方法确定传递的值是否为 NaN和其类型是 Number。  
>
> 和全局函数 isNaN() 相比，该方法不会强制将参数转换成数字，只有在参数是真正的数字类型，且值为 NaN 的时候才会返回 true.  

我们继续看，下面的结果都会是什么呢？：  
Number.isNaN(NaN);   
Number.isNaN(Number.NaN);   
Number.isNaN(0 / 0)  

Number.isNaN("NaN");   
Number.isNaN(undefined);   
Number.isNaN({});   
Number.isNaN("blabla");   

Number.isNaN(true);   
Number.isNaN(null);   
Number.isNaN(37);   
Number.isNaN("37");   
Number.isNaN("37.37");  
Number.isNaN("");   
Number.isNaN(" ");   


直接公布答案咯：  
Number.isNaN(NaN); // true  
Number.isNaN(Number.NaN); // true  
Number.isNaN(0 / 0) // true  
 
// 下面这几个如果使用全局的 isNaN() 时，会返回 true。  
Number.isNaN("NaN"); // false，字符串 "NaN" 不会被隐式转换成数字 NaN。  
Number.isNaN(undefined); // false  
Number.isNaN({}); // false  
Number.isNaN("blabla"); // false  

Number.isNaN(true); // false  
Number.isNaN(null); // false  
Number.isNaN(37); // false  
Number.isNaN("37"); // false  
Number.isNaN("37.37"); // false  
Number.isNaN(""); // false  
Number.isNaN(" "); // false  