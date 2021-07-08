# Functions - Built-in

JavaScript 有內建物件之外，也有內建函式，下面來紀錄常使用的內建函式。


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

## **parseFloat() : 將字串轉為整數**

* 函數解析一個字符串並返回一個浮點數


1. eval\(\) : 是把一串字串，當作一般 script 來進行計算。 語法： `eval(string)`

```text
var x = 2;
var y = 39;
var z = "42";
eval("x + y + 1"); // returns 42
eval(z);           // returns 42
```



