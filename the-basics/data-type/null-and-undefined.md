# Null and Undefined

在 JavaScript 有兩種方法來表示 “nothing“ ， 那就是 null 及 undefined 。

## undefined

undefined 指的是已經宣告，但還沒賦予值時，他就會表示是 undefined。

```javascript
let dog;
console.log(dog);  //undefined
```

但如果沒宣告，也沒賦予值時，這就跟 undefined 是不一樣的， 錯誤訊息則顯示 `cat is not defined` 。

```javascript
console.log(cat);  //cat is not defined
```

## null

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

## **Difference between null and undefined**

除了上述說的不同， 他們的 type 是不同的。 

```javascript
typeof undefined // undefined
typeof null // object

null === undefined // false
null == undefined // true
```

## 資料參考

[https://wesbos.com/javascript/01-the-basics/types-null-and-undefined](https://wesbos.com/javascript/01-the-basics/types-null-and-undefined)

