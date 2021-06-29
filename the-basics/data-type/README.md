# JavaScript 資料型別

當我們在宣告變數賦值時，都有可能賦予不同類型的值，比如是數字、字串、true 等等，這些就是屬於不同的資料型別。  
  
在最新的 ECMAScript 標準定義了七種資料型別，主要可以分成基本型別 \(Primitives\) 與物件型別 \(Object\) 兩大類。 而基本型別又分成 `string`、`number`、`boolean`、`null`、`undefined` ，除了上述幾種之外，都可以歸類至物件型別 \(Object\)。  


## 1. String

字串會用 `' '` \(單引號\) 或 `" "` \(雙引號\) 包夾住，兩者不可混用。單引號和雙引號在 JavaScript 使用上是沒有差異的。

```text
let carName1 = "Volvo XC60";   // Using double quotes
let carName2 = 'Volvo XC60';   // Using single quotes
```

## **2. Number**

數值， 可用整數、帶有小數點的浮點數，極大或極小值也可以用指數來表示。

```text
var x1 = 34.0 // Written with decimals
var x2 = 34 // Written without decimals
var y = 123e5 // 12300000
var z = 123e-5 // 0.00123
```

## **3. Object**

由大括弧`{}`包住 key: value ，value 可以是任何資料型態，可以是string, number, 也可以是 function。除了object 外， 其他型別都屬於基本型別 \(Primitives\) 。

```text
var person = { firstName: 'John', lastName: 'Doe', age: 50, eyeColor: 'blue' }
```

## **4. Boolean** 

布林， 就只有兩個值， true 與 false。

```text
let x = 5;
let y = 5;
let z = 6;
(x == y)       // Returns true
(x == z)       // Returns false
```

## **5. null**

空值，`null` 型別只有一種值，就是 `null` 。 因為 JavaScript 有區分大小寫， null 與  `Null`, `NULL`  都是不同的。有趣的是， null 的 data type 是 object。

```text
var person = { firstName: 'John', lastName: 'Doe', age: 50, eyeColor: 'blue' }
person = null // Now value is null, but type is still an object
```

## **6. undefined**

`undefined` 類型也只有一種值，就是 `undefined`。當變數 `x`被宣告時，在沒有給變數任何數值的情況下，變數的預設值會是 `undefined`。

```text
var x; //create a variable but assign it no value

console.log("x's value is", x) //logs "x's value is undefined"
```

## **7. Symbol**

**是 ES6 的新型別， 是用來**表示獨一無二 \(unique\) 的值。在 ES5 中，object 的屬性 \(property\) 只能是字串，如果你要幫一個 object 添加新的屬性，很容易會造成名稱衝突，Symbol 就是用來解決這件事情的。也就是說，object property name 現在可以有兩種型態 - 字串和 Symbol。

```text
let s1 = Symbol();

// "symbol"
typeof s1;

let s2 = Symbol();

// false
s1 === s2;
```

##  \* **Difference between null and undefined**

undefined and null are equal in value but different in type**.**

```text
typeof undefined // undefined
typeof null // object

null === undefined // false
null == undefined // true
```



## 

是說，看了 wesbos 文章，他用了 SNOB'N'US 來記憶這 7 種資料型態， 想說什麼意思， 查了才知道原來 snob 意思。  
  
snob =&gt;  A snob is someone that is really arrogant. They think highly of themselves and talk down to other people.

大概勢力的人，就是狗眼看人低的人，哈哈，我是覺得好像突然有好記一點，面試的時候也許能排上用場 SNOB'N'US  \(勢力的人與我們\)。 

> SNOB'N'US   
> string number object boolean null symbol

##  參考資料

  
[https://www.fooish.com/javascript/data-types.html](https://www.fooish.com/javascript/data-types.html)  
[https://wesbos.com/javascript/01-the-basics/types-introduction](https://wesbos.com/javascript/01-the-basics/types-introduction)  
[https://ithelp.ithome.com.tw/articles/10190873](https://ithelp.ithome.com.tw/articles/10190873)  
[https://developer.mozilla.org/zh-TW/docs/Web/JavaScript/Guide/Grammar\_and\_types](https://developer.mozilla.org/zh-TW/docs/Web/JavaScript/Guide/Grammar_and_types)  
[https://www.fooish.com/javascript/ES6/Symbol.html](https://www.fooish.com/javascript/ES6/Symbol.html)



