# Array

## 检测数组

* value instanceof Array
* Array.isArray(value)

## push()、pop()、shift()、unshift()

![数组队栈方法](../images/数组队栈方法.png)

## 排序

### reverse()

``` javascript
var arr = [1,2,3,4,5];
arr.reverse();
console.log(arr); //[5,4,3,2,1]
```

### sort()

**sort()** 方法按升序排列数组项。为了实现排序，**sort()** 方法会调用每个数组项的 **toString()** 方法，然后比较得到的字符串，以确定如何排序。即使数组中的每一项都是数字值，**sort()** 比较的也是字符串。

``` javascript
var arr = [0,1,5,10,15];
arr.sort();
console.log(arr); //[0,1,10,15,5]
```

**sort()** 方法可以接收一个比较函数作为参数，以便指定比较的规则。

``` javascript
function compare(value1, value2){
    if(value1 < value2){
        return -1;
    }else if(value1 > value2){
        return 1;
    }else{
        return 0;
    }
}

var arr = [0,1,5,10,15];
arr.sort(compare);
console.log(arr); //[0,1,5,10,15]
```

## 操作方法

### concat()

``` javascript
var colors = ['red','green','blue'];
var colors2 = colors.concat("yellow",["black","brown"]);
console.log(colors); //["red", "green", "blue"]
console.log(colors2); //["red", "green", "blue", "yellow", "black", "brown"]
```

### slice()

``` javascript
var colors = ["red","green","blue","yellow","purple"];
var colors2 = colors.slice(1);
var colors3 = colors.slice(1,4);
console.log(colors); //["red", "green", "blue", "yellow", "purple"]
console.log(colors2); //["green", "blue", "yellow", "purple"]
console.log(colors3); //["green", "blue", "yellow"]
```

