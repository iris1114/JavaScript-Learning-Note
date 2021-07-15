# Null and Undefined

在 JavaScript 有兩種方法來表示 "nothing"， 那就是 null 及 undefined 。

## 1. undefined

undefined 指的是已經宣告，但還沒賦予值時，他就會表示是 undefined。

```javascript
let dog;
console.log(dog);  //undefined
```

但如果沒宣告，也沒賦予值時，這就跟 undefined 是不一樣的， 錯誤訊息則顯示 `cat is not defined` 。

```javascript
console.log(cat);  //cat is not defined
```

## 2. null

null 則是已經賦予值， 而值為空值。 undefined 則是宣告了未被賦值。

```javascript
const cher = {
  first: "Cher",
};
const teller = {
  first: "Raymond",
  last: null,
};

console.log(cher.last) //undefined
console.log(teller.last) //null
```

## **3. Difference between null and undefined**

這兩個類型的共通點是，`null` 型別只有一種值，就是 `null` ，而 `undefined` 類型也只有一種值，就是 `undefined`。

但他們並不完全相等！null 的 type 是 object 。

```javascript
typeof undefined // undefined
typeof null // object

null === undefined // false
null == undefined // true
```

透過 `Number()` 強制為兩者轉型的時候多少可以看出點什麼：

```javascript
Number( null );         // 0

Number( undefined );    // NaN
```



剛好看到這張圖，覺得形容得很貼切，分享～

![](../../.gitbook/assets/t9m2j.png)

## 4. undefined 討人厭的地方

在非全域作用範圍下， `undefined` 允許被當成變數名稱，而且變數的值是可以被修改的：

```javascript
(function() {
  var undefined = 'foo';
  console.log(undefined, typeof undefined);    // 'foo', 'string'
})()
```

甚至是作為參數使用：

```javascript
(function(undefined) {
  console.log(undefined, typeof undefined);    // 'foo', 'string'
})('foo');
```

之前都不知道原來還可以這樣，這真的不能亂用 XDDD 

## 資料參考

[https://ithelp.ithome.com.tw/articles/10190873](https://ithelp.ithome.com.tw/articles/10190873)  
[https://wesbos.com/javascript/01-the-basics/types-null-and-undefined](https://wesbos.com/javascript/01-the-basics/types-null-and-undefined)  
[https://stackoverflow.com/questions/5076944/what-is-the-difference-between-null-and-undefined-in-javascript](https://stackoverflow.com/questions/5076944/what-is-the-difference-between-null-and-undefined-in-javascript)  


