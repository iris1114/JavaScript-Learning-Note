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





  
[https://developer.mozilla.org/zh-TW/docs/Glossary/Number](https://developer.mozilla.org/zh-TW/docs/Glossary/Number)

