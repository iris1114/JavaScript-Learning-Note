---
description: 函式本身是一個物件 object，不支援overloading， overloading是指
---

# Functions - Custom

## Defining a Function

有幾種方式可以定義函式， 先用最基礎的方法，可以自訂是否需要參數帶入函式，先從最簡單的不需加參數來定義函數。函式名稱可以取比較有意義的名稱，看了就明白這個函式在做什麼。

```javascript
// function definition
function calculateBill() {
  // this is the function body
  console.log("Running Calculate Bill!!");
}
// function call or function invocation
calculateBill();
```

## Returning Values

可以看函式的功能來決定是否需要回傳值。回傳值很簡單，就加入 return 回傳想要回傳的資料即可。

```javascript
// function definition
function calculateBill() {
  // this is the function body
  console.log("Running Calculate Bill!!");
  const total = 100 * 1.13;
  return total;
}
// function call or function invocation
calculateBill();
```

## Storing a Value Returned from A Function

```javascript
function calculateBill() {
  const total = 100 * 1.13;
  return total;
}
const myTotal = calculateBill();
console.log(myTotal);
console.log(`Your total is $${calculateBill()}`); 

```

## 參考資料

[https://wesbos.com/javascript/02-functions/functions-custom](https://wesbos.com/javascript/02-functions/functions-custom)

