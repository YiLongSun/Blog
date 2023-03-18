---
title: Linux 常用指令
description: Basic Ideas of Linux
date: "2023-02-27"
publishDate: "2023-02-27"
---

Linux shell 常用指令

<!--more-->
# 關機

```bash
$ sudo shutdown -h now
```
<br>

# 重開機

```bash
$ sudo reboot
```
<br>

# 安裝套件

```bash
$ sudo apt-get install XXX
```
<br>

# 更新套件資訊

```bash
$ sudo apt-get update
```
<br>

# 更新軟體至最新版本

```bash
$ sudo apt-get upgrade
```
<br>

# 移除套件

```bash
$ sudo apt-get --purge autoremove XXX
```
<br>

# 線上說明手冊

查看 ls 指令如何使用

```bash
$ man ls
```
<br>

# 查看當前路徑

```bash
$ pwd
```
<br>

# 列出檔案

列出檔案詳細資訊

```bash
$ ls -l
```

列出路徑或檔案大小

```bash
$ ls -h
```

顯示全部檔案

```bash
$ ls -a
```
<br>

# 建立空檔案

建立 python 檔案

```bash
$ touch test.py
```
<br>

# 切換路徑

切換至上一層路徑

```bash
$ cd ..
```

切換至指定路徑

```bash
$ cd XXX
```
<br>

# 刪除

刪除檔案

```bash
$ rm XXX
```

刪除資料夾

```bash
$ rm -rf XXX
```

刪除特定檔案（刪除 python 檔）

```bash
$ rm -f *.py
```
<br>

# 移動

複製檔案（複製 test.py 到 /test/ 路徑）

```bash
cp test.py /test/
```

複製資料夾（複製 source 內所有檔案到 destination）

```bash
$ cp -r source/ destination/
```

複製資料夾（保留檔案權限）

```bash
$ cp -r --preserve=all source/ destination/
```
<br>

# 壓縮

.tar 壓縮

```bash
$ tar cvf dir.tar dir
```

.tar 解壓縮

```bash
$ tar xvf dir.tar
```

.tar.gz 壓縮

```bash
$ tar zcvf dir.tar dir
```

.tar.gz 解壓縮

```bash
$ tar zxvf dir.tar
```

.zip 安裝

```bash
$ sudo apt-get install zip unzip
```

.zip 壓縮

```bash
$ zip -r dir.zip dir
```

.zip 解壓縮

```bash
$ unzip dir.zip -d dir
```
<br>

# 權限

修改檔案權限

```bash
$ chmod u=rwx,g=rx,o=r XXX
```

<table style="border:3px black dashed;">
  <tr>
    <td></td>
    <td>擁有者 (user)</td>
    <td>所屬群組 (group)</td>
    <td>其他使用者 (other)</td>
  </tr>
  <tr>
    <td>d</td>
    <td>rwx</td>
    <td>r-x</td>
    <td>r-x</td>
  </tr>
  <tr>
    <td>代表是一個目錄</td>
    <td>擁有讀、寫、執行權限</td>
    <td>擁有讀、執行權限</td>
    <td>擁有讀、執行權限</td>
  </tr>
</table>