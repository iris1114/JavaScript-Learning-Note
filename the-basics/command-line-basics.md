# Command Line Basics

對於剛開始接觸程式的人，是真的不會 command line，我是直到轉職第一份工作後，才慢慢學會一些指令，多用的時候也才自然而然記起來。

## 

{% code title="Desktop" %}
```text
project
│   file01.txt    
│
└───folder1
│   │   file011.txt
│   │   file012.txt
│   
└───folder2
    │   file021.txt
    │   file022.txt
```
{% endcode %}

## 位置相關

### **`pwd` - print working directory**

印出目前所在位置 

```text
$ pwd  
// 印出目前所在位置 
// ex.印出 /Users/iris.chew/，表示目前在 home 目錄
```

### `ls` - list

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

### `cd`- change directory

```text
$ cd Desktop/project/
// 切換資料夾 
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

## 檔案相關



### **`mkdir` - make directory**

```text
$ mkdir folder1  
// 建立新資料夾， 在指令後加上資料夾名稱
```

```text
$ mkdir folder2 folder3 folder4
// 同時新增多個資料夾
```

### `touch` 

```text
$ touch test.txt
// 建立新檔案，指令後面加上檔案名稱
```



### **`mv` - move**

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

### cp - copy

複製檔案及資料夾的指令有所不同， 資料夾要加 `-r` , 指令後面則為想複製的檔案名稱及新複製後的檔案名稱。

```text
$ cp demo.txt copy.txt
// 複製檔案
// ex. 用 demo.txt 複製出 copy.txt 檔案 
```

```text
$ cp -r folder1 folderCopy
// 複製資料夾
// 用 folder1 資料夾複製出 folderCopy 資料夾
```



### **rm - remove**

\*\*\*\*









\*\*\*\*



