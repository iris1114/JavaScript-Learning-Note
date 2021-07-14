# 變數

1.變數是用來儲存資料及進行運算的基本單位。

2. 變數的第一個字母必須為英文字母、底線 `_` 或是錢字號 `$` 。

```javascript
var hello = "world"
var _hello = "world"
var $hello = "world"
```

3. 變數名稱不可以是保留字 \(Reserved Words\) 與關鍵字 \(keyword\)。請參考 MDN [關鍵字與保留字列表](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#Keywords)。

4. 在 ES6 之後宣告「變數」與「常數」，除了 `var` 之外，還可以透過 `let` 與 `const` 做宣告。

```javascript
var m = 1;
let i = 1;
const x = 1;
```

5. 所有沒有透過 `var` 宣告的變數都會自動變成全域變數。

```javascript
// 對未宣告的變數 m 賦值
m = 1;

console.log(m);  //1
```

6. 宣告變數`a`, 但沒給他值，則 `a` 就會是`undefined` 。

```javascript
var a;
console.log(a); // undefined
```

7. `var` 變數可以重複宣告，而 `let` 及 `const` 無法。

```javascript
var m = 1;
var m = 2;
console.log(m); //2

let i = 1;
let i = 2; //Uncaught SyntaxError: Identifier 'i' has already been declared

const j = 3; 
const j = 4; //Uncaught SyntaxError: Identifier 'j' has already been declared
```

## 參考資料

[https://ithelp.ithome.com.tw/articles/10190873?sc=rss.qu](https://ithelp.ithome.com.tw/articles/10190873?sc=rss.qu)



