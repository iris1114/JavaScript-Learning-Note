# Command Line Basics

對於剛開始接觸程式的人，是真的不會 command line，我是直到轉職第一份工作後，才慢慢學會一些指令，多用的時候也才自然而然記起來。  
  
大致分類為：  
位址相關： `pwd` 、 `ls` 、`cd`  
檔案相關： `mkdir` 、 `touch` 、`mv` 、 `cp` 、`rm`  
編輯檔案相關： `vim`  
查閱檔案相關： `cat` 、 `less` 、`more`  
其他： `clear`、 `date`   


## 位址相關

### **`pwd` - print working directory**  印出所在目錄

```text
$ pwd  
// 印出目前所在目錄
// ex.印出 /Users/iris.chew/，表示目前在 home 目錄
```

### `ls` - list  印出清單

```text
$ ls  
 // 印出所有資料夾清單 
```

```text
$ ls -a 
// 印出所有資料夾清單（包括隱藏檔）
// 可簡寫 la
```

```text
$ ls -l
// 印出所有資料夾詳細資料 (包含檔名、日期、容量等) 
// 可簡寫 ll
```

### `cd`- change directory  切換目錄

```text
$ cd Desktop/project/
// 切換目錄 
// ex.切換至 Desktop 的 project 資料夾
```

```text
$ cd ~/Desktop/project/
// 切換絕對路徑資料夾
// 可直接將資料夾拖拉至 terminal ，自動產生資料夾絕對路徑 ，節省打字時間 
```

```text
$ cd ..
// 回到上一層資料夾
```

```text
$ cd ~ 
// 回到 home 目錄
```

## 資料夾及檔案相關

### **`mkdir` - make directory  建立新資料夾**

```text
$ mkdir folder1  
// 建立新資料夾， 在指令後加上資料夾名稱
```

```text
$ mkdir folder2 folder3 folder4
// 同時新增多個資料夾
```

### `touch` - 建立新檔案

```text
$ touch test.txt
// 建立新檔案，指令後面加上檔案名稱
```

### **`mv` - move  移動與修改檔名**

`mv` 具有兩個功能，為移動檔案或資料夾及修改檔名。

```text
$ mv test.txt folder2
// 移動檔案或資料夾
// ex. 將 test.txt 檔案移動至 folder2 資料夾
```

```text
$ mv test.txt demo.txt
// 當找不到該檔案時，則會更改檔案名稱，把 test.txt 改為 demo.txt 檔名
```

### `cp` - copy 複製檔案及資料夾

複製檔案及資料夾的指令有所不同， 資料夾要加 `-r` , 指令後面則為想複製的檔案名稱及新複製後的檔案名稱。

```text
$ cp demo.txt copy.txt
// 複製檔案 指令後面則為想複製的檔案名稱及新複製後的檔案名稱
// ex. 用 demo.txt 複製出 copy.txt 檔案 
```

```text
$ cp -r folder1 folderCopy
// 複製資料夾
// 用 folder1 資料夾複製出 folderCopy 資料夾
```

### **`rm` - remove 刪除檔案及資料夾**

```text
$ rm cop.txt 
// 刪除檔案
```

```text
$ rm -r folderCopy 
// 刪除資料夾
```

## 編輯檔案相關

### `vim` -  Vi IMproved

  
vim 是从 vi 發展出來的一個文本編輯器。1992年1.22版本的 vim 被移植到了UNIX 和 MS-DOS 上。从那个时候开始，Vim的全名就变成Vi IMproved（改良）了。其實你可以將 vim 視作 vi 的進階版本，vim 可以用顏色或底線等方式來顯示一些特殊的資訊。

```text
$ vim demo.txt
// 進入文字編輯器內編輯檔案
```

```text
i
// 會看到該檔案內容，輸入i進行編輯
```

```text
輸入 esc 鍵盤
// 離開編輯模式
```

```text
:wq
// 儲存後離開
```

```text
:q!
// 不儲存強制離開
```

更多 vim 操作指令可參考： [http://www.vixual.net/blog/archives/234](http://www.vixual.net/blog/archives/234)  
目前我使用到的 vim 指令好像就那麼多 XD  但還是比較常用 vs code 編輯就是了。

## 查閱檔案相關

### `cat` - 快速查閱檔案

```text
$ cat demo.txt
// 不用進入編輯器，即可在介面快速瀏覽
```

### `less` -  分頁顯示檔案內容

less 與 more 類似，在 more 的時候，我們並沒有辦法向前面翻檔案內容， 只能往後面看，但若使用了 less 時，就可以使用 \[pageup\] \[pagedown\] 等按鍵的功能來往前往後翻看文件，更容易用來查看一個文件的內容。  
  
macbook 的 pageup pagedown 按鍵為 ：`fn` + 上下鍵

```text
$ less demo.txt
// 分頁上下鍵盤查閱檔案
// q 則離開指令
// space 按鍵可跳至下一頁
```

### `more` -  全屏顯示檔案內容

more 無法分頁，只能往後看。

```text
$ more demo.txt
// q 則離開指令
// space 按鍵可跳至下一頁
```

## 其他常用

### `clear` 清除介面

```text
$ clear
// 清除介面
// 其實我更常用 command + k ，達一樣效果
```

### `date` 顯示日期

```text
$ date
```

## 參考資料

[https://jtliu.coderbridge.io/2020/06/14/command-line-codediary/](https://jtliu.coderbridge.io/2020/06/14/command-line-codediary/)  
[https://hackmd.io/@Yu040419/B1KCuoiaE](https://hackmd.io/@Yu040419/B1KCuoiaE)  
[https://zh.wikipedia.org/wiki/Vim](https://zh.wikipedia.org/wiki/Vim)  
[http://happystreet.com.tw/index.php/system-dynamic-teaching/unix-linux/178-a-day-of-school-a-unix-command-less](http://happystreet.com.tw/index.php/system-dynamic-teaching/unix-linux/178-a-day-of-school-a-unix-command-less)  
[https://www.itread01.com/content/1545977108.html](https://www.itread01.com/content/1545977108.html)  
[https://www.ctomczyk.pl/zsh-command-not-found-wget-macos/910/](https://www.ctomczyk.pl/zsh-command-not-found-wget-macos/910/)







\*\*\*\*



