# isNaN()全局函数确定一个值是否为NaN

以下语句的结果是：  
> isNaN(NaN);  
> isNaN(undefined);  
> isNaN({}); 
>
> isNaN(true);    
> isNaN(false);   
> isNaN(null);  
> isNaN(37);  
>
> isNaN("37");  
> isNaN("37.37");  
> isNaN("");  
> isNaN(" "); 
>
> isNaN(new Date());  
> isNaN(new Date().toString());  
>
> isNaN("blabla");  

解析：isNaN的原理是先把里面的值强制进行Number()方法，然后对Number之后的结果进行isNaN判断  

isNaN(NaN); // true
isNaN(undefined); // true Number()之后为NaN  
isNaN({}); // true Number()之后为NaN  

isNaN(true); // false  
isNaN(false); // false  
isNaN(null); // false  
isNaN(37); // false  

isNaN("37"); // false  
isNaN("37.37"); // false  
isNaN(""); // false: 空字符串Number("")之后为0  
isNaN(" "); // false: 含空格的字符串Number(" ")为0  

isNaN(new Date()); // false  
isNaN(new Date().toString()); // true  

isNaN("blabla"); // true: Number ("blabla")为NaN  