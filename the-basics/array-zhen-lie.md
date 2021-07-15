# Array 陣列

陣列 \(array\) 是一個有序的序列，陣列中可以儲存不定數量的任何值，陣列在 JavaScript 中屬於複合資料型態 \(composite data type\)。

## 1. 宣告陣列 \(Create an Array\)

建立陣列同樣也可以透過 `new` 關鍵字來建立：

```javascript
var a = new Array();

a[0] = "apple";
a[1] = "boy";
a[2] = "cat";
```

也可以用 array literal `[]` 來宣告一個新陣列。

```javascript
var a = ["apple", "boy", "cat"];
```

## 2. 存取陣列 \(Access the Elements of an Array\)

陣列中的每一個值我們稱做一個元素，每一個元素儲存在陣列中固定的位置，我們稱做索引 \(index\)，索引值從 0 開始，表示陣列中的第一個元素，第二個之後的元素索引值則依序加 1 \(0, 1, 2, 3, ...\)。

我們可以用 `[]` 運算子來存取陣列中的元素。

```javascript
var a = ["apple", "boy", "cat"];
console.log( a[0] );  //索引值從 0 的值為 apple
console.log( a[2] );  //索引值從 0 的值為 cat
```

## 3. 更改陣列中某個元素的值



```text
var a = ["apple", "boy", "cat"];
a[1] = "banana";

console.log( a[1] );  //banana
```

