# Object 物件

JavaScript 物件 \(object\) 是一個複合資料型態 \(composite data type\)，可以儲存不定數量的鍵值對 \(key-value paris\)，而一組鍵值對我們稱做物件的一個屬性 \(property\)。一個屬性的值 \(value\) 可以是任何[資料型態](https://www.fooish.com/javascript/data-types.html) \(也可以是[函數](https://www.fooish.com/javascript/function.html)\)；而屬性的名稱 \(key / name\) 是一個字串型態。

## 1. 物件宣告 \(Creating Objects\)

有兩種方式可以建立一個物件：

* **Object Constructor \(物件建構式\)** 用 new 關鍵字加上 Object\(\) 來宣告一個物件：

```javascript
const myObj = new Object();  
```

* **Object Literal \(物件實字\)** object literal 是最常用也最方便的語法，用 `{}` 就可以宣告一個物件：

```javascript
const myObj = {};  
```

## 2. 物件的屬性 \(Object Properties\)

用 object literal 我們也可以在宣告物件時，同時建立屬性！例如：

```javascript
const myObj = {'color': 'blue', 'height': 101};
```

我們可以用 `.` 運算子或 `[]` 來存取物件的屬性。語法：

```javascript
objectName.propertyName
objectName['propertyName']
```

example:

```javascript
myObj.color // blue
myObj["color"]  // blue
```

後者的好處是，當物件的索引鍵剛好是不合法的 JavaScript 的識別字 \(如帶有**空白的字串或是數字**\) 時，執行就會出現錯誤：

```javascript
var obj = {
  "001": "Hello"
}

obj.001;        //  SyntaxError: Unexpected number

obj["001"];     // "Hello"
```

但我好像都是比較常用 `.`  , 除了方便之外，應該一般人的key應該不會這樣取吧 XD

## 3.  新增屬性

若想為物件新增屬性的話，直接用 `=` 指定就可以了：

```javascript
var obj = { };
obj.name = 'Object';

obj.name;       // 'Object'
```

## 4. 刪除屬性

要是想刪除屬性，則是透過 `delete` 關鍵字來刪除：

```javascript
var obj = { };
obj.name = 'Object';

obj.name;       // 'Object'

delete obj.name;

obj.name;       // 刪除屬性後變成 undefined
```

## 5. 判斷屬性是否存在

最簡單的方式就是檢查該屬性是不是 `undefined`。

```javascript
var obj = {};

console.log( obj.name );      // undefined
```

但這麼做會有個例外，就是當該屬性剛好就是 `undefined` 時，這招就沒用了。

除了檢查 `undefined` 之外，還有 `in` 運算子 與 `hasOwnProperty()` 方法，  


```javascript
var obj = {
  name: 'Object'
};

// 透過 in 檢查屬性
console.log( 'name' in obj );     // true
console.log( 'value' in obj );    // false

// 透過 hasOwnProperty() 方法檢查
obj.hasOwnProperty('name');       // true
obj.hasOwnProperty('value');      // false
```

## 6. 物件的方法 \(Object Methods\)

物件的屬性值如果是一個[函數](https://www.fooish.com/javascript/function.html)，我們稱它是物件的方法 \(method\)。

```javascript
const me = {
    firstName: 'Mike',
    lastName: 'Lee',
    age: 30,
    fullName: function() {
        return this.firstName + ' ' + this.lastName;
    }
}
```

`this` 是物件方法中可以使用的關鍵字，this 是一個物件參考，當物件在執行時，可以使用 this 來代表 "自己"。  


## 7. JavaScript 內建物件 \(JavaScript Native Objects\)

JavaScript 有一些內建物件，也可以稱作資料型態，包含：

* Number 物件: 數字型態的物件，如整數 \(5, 10\) 或浮點數 \(3.14\)
* Boolean 物件: 表示邏輯真假值的物件，真就是 true，假就是 false
* String 字串物件: 任何字元 \(Unicode\)
* Array 陣列物件: 可用來容納任何其他物件
* Math 物件: 提供許多常用的數學常數及數學計算函數
* Date 物件: 專門處理時間和日期的物件
* RegExp 物件: 即正規表示式 \(regular expression\) 物件

每一種物件都有各自的屬性 \(attribute\) 和方法 \(method\) 可以使用。

## 參考資料

[https://ithelp.ithome.com.tw/articles/10190962](https://ithelp.ithome.com.tw/articles/10190962)  
[https://www.fooish.com/javascript/object.html](https://www.fooish.com/javascript/object.html)  
[https://wesbos.com/javascript/01-the-basics/types-objects](https://wesbos.com/javascript/01-the-basics/types-objects)

