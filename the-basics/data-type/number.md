# Number

在 JavaScript, **Number** 是[雙精度64位浮點格式\(IEEE 754\)](http://en.wikipedia.org/wiki/Double_precision_floating-point_format)中的數字數據類型。在其他編程語言中可以存在不同的數字類型，如：整型\(Integers\)、浮點型\(Floats\)、雙精度型\(Doubles\)、 或 大數型\(Bignums\).

```javascript
const x = 180;
const y = 0.25;
```

也可以用科學記號表示法 \(scientific \(exponent\) notation\)：

```javascript
const x = 101e5;  // 10100000
const y = 101e-5; // 0.00101
```

## Infinity and Negative Infinity

`Infinity` 或 `-Infinity` 是 JavaScript 一個 global 的屬性，表示無限大或無限小。 可以使用\*\* 來乘以雙倍， 如 `10 ** 2` 會回傳100 ， `1000**2`  則回傳 1000000 。 不管是是無限大或無限小，資料型態都屬於  。

```javascript

console.log(100000000000 > Infinity); //false
console.log(-99999 > -Infinity); //true

const x =  2 / 0;  // x = Infinity
const y = -2 / 0;  // y = -Infinity
const z = 1000 ** 200 // z = Infinity

console.log(typeof Infinity); //number
console.log(typeof -Infinity); //number
```

## NaN \(Not a Number\)

NaN 是 JavaScript 一個 global 的屬性，表示一個值是非數值。

```javascript
const x = 10 / "dog";
console.log(x) //NaN

console.log(typeof NaN); //number
```

JavaScript 還有一個 global function `isNaN` 來讓看可以判段一個值是不是 NaN。例如：

```javascript
isNaN(NaN);       // true
isNaN(undefined); // true
isNaN({});        // true

isNaN(true);      // false
isNaN(null);      // false
isNaN(20);        // false
```



###  <a id="things-to-know-about-math-in-javascript"></a>

## Number\(\) 函數 - 型別轉換

Number\(\) 可以用來將其他的資料型態轉型 \(type conversion\) 成數值型態。

#### 字串轉數字 <a id="&#x5B57;&#x4E32;&#x8F49;&#x6578;&#x5B57;"></a>

```text
Number('3.14') // 3.14
Number('100')  // 100
Number(' ')    // 0
Number('')     // 0
Number('a123') // NaN
```

#### 布林值轉數字 <a id="&#x5E03;&#x6797;&#x503C;&#x8F49;&#x6578;&#x5B57;"></a>

```text
Number(false) // 0
Number(true)  // 1
```







  
[https://developer.mozilla.org/zh-TW/docs/Glossary/Number](https://developer.mozilla.org/zh-TW/docs/Glossary/Number)  
[https://www.fooish.com/javascript/number/](https://www.fooish.com/javascript/number/)  
[https://wesbos.com/javascript/01-the-basics/types-numbers](https://wesbos.com/javascript/01-the-basics/types-numbers)

