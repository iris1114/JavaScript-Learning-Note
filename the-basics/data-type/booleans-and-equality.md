# Booleans and Equality

Boolean 用來表示兩種值：

1. `true` - 表示真
2. `false` - 表示假

在 JavaScript 中，只有這些值會被當作是 false：

1. `null`
2. 數值 `0`
3. `NaN`
4. 空字串 `''`
5. `undefined`

除此以外的值都是 true！

## Boolean\(\) 函數 - 型別轉換 <a id="boolean-&#x51FD;&#x6578;---&#x578B;&#x5225;&#x8F49;&#x63DB;"></a>

Boolean\(\) 可以用來將其他的資料型態轉型 \(type conversion\) 成布林值型態。

```javascript
var x = 0;
Boolean(x); // false
x = 100;
Boolean(x); // true

x = '';
Boolean(x); // false
x = 'hi';
Boolean(x); // true

x = null;
Boolean(x); // false
```

## Equality \(equal sign, double equal sign, triple equal sign = / == / ===\) 

最簡單的一個等於 = ， 當我們宣告變數賦值時所使用。

```javascript
const age = 100;
```

== 為一般相等, 一般相等會_先將_比較值轉換成同型別後比較。轉換後（可能一個或兩個都被轉換），接著進行的幾乎和嚴格比較（`===`）一樣。   


=== 為嚴格相等， 被比較的兩個值都不會轉換成其他型別。如果值是不同型別，就會被視為不相等。如果兩值型別相同但不是數字，若值相同，則為相等。此外，如果兩個值皆為數字，只要他們是 NaN 以外的同一值，或者 +0 和 -0，則為相等。  
  
簡單來說，一般相等會將型別一致化後比較；嚴格相等則不會（也就是說若型別不同，就會回傳 fasle）；`Object.is` 會和嚴格相等做同樣的事，但會將 `NaN`、`-0 和 +0` 獨立處理，因此這三個不會相等，而 `Object.is(NaN, NaN)` 則會回傳 true 。

```javascript
100 == "100"  //true
100 === "100"  //false
Object.is(100, "100"); //false
```

| x | y | `==` | `===` | `Object.is` |
| :--- | :--- | :--- | :--- | :--- |
| `undefined` | `undefined` | `true` | `true` | `true` |
| `null` | `null` | `true` | `true` | `true` |
| `true` | `true` | `true` | `true` | `true` |
| `false` | `false` | `true` | `true` | `true` |
| `"foo"` | `"foo"` | `true` | `true` | `true` |
| `{ foo: "bar" }` | `x` | `true` | `true` | `true` |
| `0` | `0` | `true` | `true` | `true` |
| `+0` | `-0` | `true` | `true` | `false` |
| `0` | `false` | `true` | `false` | `false` |
| `""` | `false` | `true` | `false` | `false` |
| `""` | `0` | `true` | `false` | `false` |
| `"0"` | `0` | `true` | `false` | `false` |
| `"17"` | `17` | `true` | `false` | `false` |
| `[1,2]` | `"1,2"` | `true` | `false` | `false` |
| `new String("foo")` | `"foo"` | `true` | `false` | `false` |
| `null` | `undefined` | `true` | `false` | `false` |
| `null` | `false` | `false` | `false` | `false` |
| `undefined` | `false` | `false` | `false` | `false` |
| `{ foo: "bar" }` | `{ foo: "bar" }` | `false` | `false` | `false` |
| `new String("foo")` | `new String("foo")` | `false` | `false` | `false` |
| `0` | `null` | `false` | `false` | `false` |
| `0` | `NaN` | `false` | `false` | `false` |
| `"foo"` | `NaN` | `false` | `false` | `false` |
| `NaN` | `NaN` | `false` | `false` | `true` |

## 資料參考

[https://developer.mozilla.org/zh-TW/docs/Web/JavaScript/Equality\_comparisons\_and\_sameness\#%E5%9A%B4%E6%A0%BC%E7%9B%B8%E7%AD%89%EF%BC%88%EF%BC%89](https://developer.mozilla.org/zh-TW/docs/Web/JavaScript/Equality_comparisons_and_sameness#%E5%9A%B4%E6%A0%BC%E7%9B%B8%E7%AD%89%EF%BC%88%EF%BC%89)  
[https://wesbos.com/javascript/01-the-basics/types-booleans-and-equality](https://wesbos.com/javascript/01-the-basics/types-booleans-and-equality)

