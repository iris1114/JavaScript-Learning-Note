# Functions - Built-in

JavaScript 有內建物件之外，也有內建函式，下面來紀錄常使用的內建函式。

|  |  |
| :--- | :--- |
| parseInt\(string, radix\) | 將字串轉為整數 |
| parseFloat\(string\) | 將字串轉為浮點數 |
| eval\(string\) | 將字串當作敘述來執行 |
| isFinite\(number\) | 是否為有限大的數字 |
| isNaN\(\) | 是否為非有效的數值 |

## **parseInt\(\) : 將字串轉為整數**

```javascript
parseInt(string, radix);
```

如果 radix 參數被省略，JavaScript 假定如下：

* 如果字符串以“0x”開頭，則基數為16（十六進制）
* 如果字符串以任何其他值開頭，則基數為 10（十進制）
* 只返回字符串中的第一個數字！
* 允許前導和尾隨空格。
* 如果第一個字符不能轉換為數字，parseInt\(\) 返回 NaN。

不過還是建議加radix, 可以加個10。

```javascript
parseInt("10") //10
parseInt("10.33")  //10
parseInt("34 45 66") //34
parseInt("   60   ") //64
parseInt("40 years") //40
parseInt("He was 40") //NaN
parseInt("10", 10) //10
parseInt("010") //10
parseInt("10", 8) //8
parseInt("0x10") //16
parseInt("10", 16)  //16
```

## **parseFloat\(\) : 將字串轉為數字\(浮點數\)**

* 只返回字符串中的第一個數字！
* 允許前導和尾隨空格。
* 如果第一個字符不能轉換為數字，parseFloat\(\) 返回 NaN。

```text
parseFloat("10") //10
parseFloat("10.00") //10
parseFloat("10.33") //10.33
parseFloat("10.33.11") //10.33
parseFloat("34 45 66")  //34
parseFloat(" 60 ") //60
parseFloat("40 years") //40
parseFloat("He was 40") //NaN
```

## **parseInt\(\) 和parseFloat\(\) 的區別在於：**

parseFloat\(\) 所解析的字串中第一個小數點是有效的，而parseInt\(\) 遇到小數點會停止解析，因為小數點並不是有效的數字字元。  
parseFloat\(\) 始終會忽略前導的零，十六進位制格式的字串始終會被轉換成0，而parseInt\(\) 第二個引數可以設定基數，按照這個基數的進位制來轉換。  
  
 

## eval\(\) :是把一串字串，當作一般 script 來進行計算。

 語法： `eval(string)`

```text
var x = 2;
var y = 39;
var z = "42";
eval("x + y + 1"); // returns 42
eval(z);           // returns 42
```



## isFinite\(\) : 是否為有限大的數字

如果值為 +infinity、-infinity 或 NaN（非數字），則此函數返回 false，否則返回 true。

```text
isFinite(123)  //true
isFinite(-1.23) //true
isFinite(5-2) //true
isFinite(0) //true
isFinite("123") //true
isFinite("Hello") //false
isFinite("2005/12/12") //false
```

## isNaN\(\) : 是否為非有效的數值

* isNaN\(\) 函數確定一個值是否為非法數字（Not-a-Number）。
* 如果該值等於 NaN，則此函數返回 true。否則返回false。
* 此函數不同於 Number 特定的 [Number.isNaN\(\)](https://www.w3schools.com/jsref/jsref_isnan_number.asp)方法。
* 全局 isNaN\(\) 函數將測試值轉換為數字，然後對其進行測試。
* Number.isNaN\(\) 不會將值轉換為數字，並且不會為任何非數字類型的值返回 true。

```text
isNaN(123) //false
isNaN(-1.23) //false
isNaN(5-2) //false
isNaN(0) //false
isNaN('123') //false
isNaN('Hello') //true
isNaN('2005/12/12') //true
isNaN('') //false
isNaN(true) //false
isNaN(undefined) //true
isNaN('NaN') //true
isNaN(NaN) //true
isNaN(0 / 0) //true
isNaN(null) //false
```

## 參考資料

[https://codertw.com/%E5%89%8D%E7%AB%AF%E9%96%8B%E7%99%BC/250542/](https://codertw.com/%E5%89%8D%E7%AB%AF%E9%96%8B%E7%99%BC/250542/)  
[https://www.w3schools.com/jsref/jsref\_parsefloat.asp](https://www.w3schools.com/jsref/jsref_parsefloat.asp)

