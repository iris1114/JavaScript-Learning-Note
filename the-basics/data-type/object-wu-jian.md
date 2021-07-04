# Object 物件

JavaScript 物件 \(object\) 是一個複合資料型態 \(composite data type\)，可以儲存不定數量的鍵值對 \(key-value paris\)，而一組鍵值對我們稱做物件的一個屬性 \(property\)。一個屬性的值 \(value\) 可以是任何[資料型態](https://www.fooish.com/javascript/data-types.html) \(也可以是[函數](https://www.fooish.com/javascript/function.html)\)；而屬性的名稱 \(key / name\) 是一個字串型態。

## 物件宣告 \(Creating Objects\)

有兩種方式可以建立一個物件：

* **Object Constructor \(物件建構式\)** 用 new 關鍵字加上 Object\(\) 來宣告一個物件：

```javascript
const myObj = new Object();  
```

* **Object Literal \(物件實字\)** object literal 是最常用也最方便的語法，用 `{}` 就可以宣告一個物件：

```javascript
const myObj = {};  
```

## 物件的屬性 \(Object Properties\)

我們可以用 `.` 運算子或 `[]` 來存取物件的屬性。語法：

```javascript
objectName.propertyName
objectName['propertyName']
```

example:

```javascript
myObj.color = "blue";
myObj["color"] = "blue";
```

用 object literal 我們也可以在宣告物件時，同時建立屬性！例如：

```javascript
const myObj = {'color': 'blue', 'height': 101};
```

## 物件的方法 \(Object Methods\)

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


## JavaScript 內建物件 \(JavaScript Native Objects\)

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

  
[https://www.fooish.com/javascript/object.html](https://www.fooish.com/javascript/object.html)  
[https://wesbos.com/javascript/01-the-basics/types-objects](https://wesbos.com/javascript/01-the-basics/types-objects)

