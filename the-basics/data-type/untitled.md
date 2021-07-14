# String 字串

1. 字串會用 `' '` \(單引號\) 或 `" "` \(雙引號\) 包夾住，兩者不可混用。

2. 單引號和雙引號在 JavaScript 使用上是沒有差異的。

```javascript
const carName1 = "Volvo XC60";   //使用雙引號
const carName2 = 'Volvo XC60';   //使用單引號
```

3. 在了解字串的一些特性前，先介紹樣板字面值（Template literals）。是ES6 新增的特殊字串，他允許嵌入運算式、多行字串及字串內插（string interpolation）功能。他由反引號``` ``` 字元封閉，代替了雙或單引號。樣板字面值除了字串，也包含錢字元 `$` 及花括號`{}`所組成， 這個特性增加了字串處理的便利性。

```javascript
const carName3 = `Volvo XC60`;
```

  
4. 若要在單引號內包覆單引號，或是雙引號內包覆雙引號就會出現問題：

```javascript
const str1 = 'Mike's pet.';  //error
```

我們可以這樣改，雙引號裡面可以有單引號，或單引號裡面可以有雙引號。  
或是用跳脫字元 \(escape character\) 反斜線 \(backslash\) `\`。  
或是樣板字面值反引號``` ```來解決。

```javascript
const str1 = "Mike's pet.";  // 雙引號裡面可以有單引號 Mike's pet.
const str2 = 'Mike\'s pet.'; // 跳脫字元反斜線 Mike's pet.
const str3 = `Mike's pet.`;  // 板字面值反引號 Mike's pet.
```



5. 字串相加   
遇到了多組的字串時，你可以用 `+` \(加號\) 來連接字串。

```javascript
const name = "iris";
const hello = "hello my name is" + name + ". Nice to meet you.";
console.log(hello); //"hello my name is iris.  Nice to meet you.
```

  
5. 多行字串

有如果想要換行，可以使用   `\` 或是```````` 樣板字串進行換行。

## 

## 創建字串 reate Strings

有三種方法可以創建字串  
  
1. 單引號 'text'  
2. 雙引號 "text"  
3. 反引號 \`text\`

```javascript
const singleQuotes = 'hello';
const doubleQuotes = "my";
const backticks = `friend`;
```

## 特殊字元 Special Characters

因為字串必須包在單引號或雙引號裡面，但是要特別注意的雙引號裡面不能有雙引號、單引號裡面不能有單引號。

會發生錯誤：

```javascript
const str1 = 'Mike's pet.'; //error
const str2 = "This is a "book"."; //error
```

可以這樣改，雙引號裡面可以有單引號，或單引號裡面可以有雙引號。  
或是 用跳脫字元 \(escape character\) 反斜線 \(backslash\) `\`，來跳脫引號

```javascript
const str1 = "Mike's pet.";   // Mike's pet.
varconst str1 str = 'This is a "book".';   //This is a "book".
var str = 'Mike\'s pet.';    // Mike's pet
var str = "This is a \"book\".";   // This is a "book".
```

## 字串相加 \(String Concatenation\) / 字串內插 （String Interpolation）

我們可以用 `+` 和 `+=` 運算子來將多個字串接起來變成一個。

```javascript
const name = "iris";
const hello = "hello my name is" + name + ". Nice to meet you.";
console.log(hello); //"hello my name is iris.  Nice to meet you.
```

我們也可以使用反引號穿插 name 的值。

```javascript
const name = 'iris';
const hello = `hello my name is ${name}. Nice to meet you`;
```

## 多行字串 / 換行  Putting String on Multiple Lines

有如果想要換行，可以使用   `\` 或是```````` 樣板字串進行換行。

```javascript
const song = 'Ohhh\
\
ya\
\
I like\
\
pizza';
```

```javascript
const song = `Ohhh
ya
I like
pizza`;
```

```````` 樣板字串是不是更方便呢？  如果有時候需要修改 HTML 內容元素，也可以```````` 樣板字串。

```javascript
const html = `
  <div>
    <h2></h2>
  </div>
`;
```

## String\(\) 函數 - 型別轉換

#### 數字轉字串 <a id="&#x6578;&#x5B57;&#x8F49;&#x5B57;&#x4E32;"></a>

```text
String(123) // '123'
String(100 + 23) // '123'

var x = 123;
String(x) // '123
```

#### 布林值轉字串

```text
String(true) // 'true'
String(false) // 'false'
```



## String 物件內建的屬性 \(Properties\) 

| Property | Description |
| :--- | :--- |
| [constructor](https://www.w3schools.com/jsref/jsref_constructor_string.asp) | Returns the string's constructor function |
| [length](https://www.w3schools.com/jsref/jsref_length_string.asp) | Returns the length of a string |
| [prototype](https://www.w3schools.com/jsref/jsref_prototype_string.asp) | Allows you to add properties and methods to an object |

## String 物件內建的方法 \(Methods\)

| Method | Description |
| :--- | :--- |
| [charAt\(\)](https://www.w3schools.com/jsref/jsref_charat.asp) | Returns the character at the specified index \(position\) |
| [charCodeAt\(\)](https://www.w3schools.com/jsref/jsref_charcodeat.asp) | Returns the Unicode of the character at the specified index |
| [concat\(\)](https://www.w3schools.com/jsref/jsref_concat_string.asp) | Joins two or more strings, and returns a new joined strings |
| [endsWith\(\)](https://www.w3schools.com/jsref/jsref_endswith.asp) | Checks whether a string ends with specified string/characters |
| [fromCharCode\(\)](https://www.w3schools.com/jsref/jsref_fromcharcode.asp) | Converts Unicode values to characters |
| [includes\(\)](https://www.w3schools.com/jsref/jsref_includes.asp) | Checks whether a string contains the specified string/characters |
| [indexOf\(\)](https://www.w3schools.com/jsref/jsref_indexof.asp) | Returns the position of the first found occurrence of a specified value in a string |
| [lastIndexOf\(\)](https://www.w3schools.com/jsref/jsref_lastindexof.asp) | Returns the position of the last found occurrence of a specified value in a string |
| [localeCompare\(\)](https://www.w3schools.com/jsref/jsref_localecompare.asp) | Compares two strings in the current locale |
| [match\(\)](https://www.w3schools.com/jsref/jsref_match.asp) | Searches a string for a match against a regular expression, and returns the matches |
| [repeat\(\)](https://www.w3schools.com/jsref/jsref_repeat.asp) | Returns a new string with a specified number of copies of an existing string |
| [replace\(\)](https://www.w3schools.com/jsref/jsref_replace.asp) | Searches a string for a specified value, or a regular expression, and returns a new string where the specified values are replaced |
| [search\(\)](https://www.w3schools.com/jsref/jsref_search.asp) | Searches a string for a specified value, or regular expression, and returns the position of the match |
| [slice\(\)](https://www.w3schools.com/jsref/jsref_slice_string.asp) | Extracts a part of a string and returns a new string |
| [split\(\)](https://www.w3schools.com/jsref/jsref_split.asp) | Splits a string into an array of substrings |
| [startsWith\(\)](https://www.w3schools.com/jsref/jsref_startswith.asp) | Checks whether a string begins with specified characters |
| [substr\(\)](https://www.w3schools.com/jsref/jsref_substr.asp) | Extracts the characters from a string, beginning at a specified start position, and through the specified number of character |
| [substring\(\)](https://www.w3schools.com/jsref/jsref_substring.asp) | Extracts the characters from a string, between two specified indices |
| [toLocaleLowerCase\(\)](https://www.w3schools.com/jsref/jsref_tolocalelowercase.asp) | Converts a string to lowercase letters, according to the host's locale |
| [toLocaleUpperCase\(\)](https://www.w3schools.com/jsref/jsref_tolocaleuppercase.asp) | Converts a string to uppercase letters, according to the host's locale |
| [toLowerCase\(\)](https://www.w3schools.com/jsref/jsref_tolowercase.asp) | Converts a string to lowercase letters |
| [toString\(\)](https://www.w3schools.com/jsref/jsref_tostring_string.asp) | Returns the value of a String object |
| [toUpperCase\(\)](https://www.w3schools.com/jsref/jsref_touppercase.asp) | Converts a string to uppercase letters |
| [trim\(\)](https://www.w3schools.com/jsref/jsref_trim_string.asp) | Removes whitespace from both ends of a string |
| [valueOf\(\)](https://www.w3schools.com/jsref/jsref_valueof_string.asp) | Returns the primitive value of a String object |

## 參考資料

[https://www.fooish.com/javascript/string/](https://www.fooish.com/javascript/string/)  
[https://wesbos.com/javascript/01-the-basics/types-strings](https://wesbos.com/javascript/01-the-basics/types-strings)  
[https://developer.mozilla.org/zh-TW/docs/Web/JavaScript/Reference/Global\_Objects/String](https://developer.mozilla.org/zh-TW/docs/Web/JavaScript/Reference/Global_Objects/String)

