---
title: C++ 基本資料型態
description: Basic Data Types of C++
date: "2023-03-18"
publishDate: "2023-03-18"
---

算術運算、關係運算、邏輯運算、位元處理運算

<!--more-->
# 第一個 C++ 程式

輸入：

```cpp
#include <iostream> // preprocessor directives
using namespace std; // using declaration

int main()
{
	cout << "Hello, my name is Alan !" << endl;
	return 0;
}
```

輸出：

```cpp
Hello, my name is Alan !
```

## 前處理指令（preprocessor directives）

將掌管「輸入輸出資料流」的標頭檔（header file）匯入程式內

## Using 宣告（using declaration）

說明「cout」及「endl」是名稱空間 std 中的標準元件

# 整數 & 浮點數

輸入：

```cpp
#include <iostream>
using namespace std;

int main()
{
	// integer values
	cout << " 48U : "  << 48U  << endl; // unsigned int
	cout << " 75UL : " << 75UL << endl; // unsigned long
	cout << " 372L : " << 372L << endl; // long
	cout << " 012 : "  << 012  << endl; // 12 in Octal
	cout << " 0x12 : " << 0x12 << endl; // 12 in Hexadecimal

	//  floating point numbers
	cout << " 4.7 : "       << 4.7       << endl; // double
	cout << " 48.0F : "     << 48.0F     << endl; // float
	cout << " 48.0f : "     << 48.0f     << endl; // float
	cout << " 3.75L : "     << 3.75L     << endl; // long double
	cout << " 4.26e12 : "   << 4.26e12   << endl; // double
	cout << " 4.26e+12L : " << 4.26e+12L << endl; // long double
	cout << " 4.26E-12 : "  << 4.26E-12  << endl; // double

	return 0;
}
```

輸出：

```cpp
48U : 48
75UL : 75
372L : 372
012 : 10
0x12 : 18
4.7 : 4.7
48.0F : 48
48.0f : 48
3.75L : 3.75
4.26e12 : 4.26e+12
4.26e+12L : 4.26e+12
4.26E-12 : 4.26e-12
```

# 變數 & 常數

輸入：

```cpp
#include <iostream>
using namespace std;

int main()
{
	const int number = 3;
	float var_1 = 12.84, var_2 = 15.67, var_3 = 25.39;
	float average;

	average = (var_1 + var_2 + var_3) / number;

	cout << "var_1、var_2、var_3 的平均為 " << average << endl;

	return 0;
}
```

輸出：

```cpp
var_1、var_2、var_3 的平均為 17.9667
```

## 變數宣告

變數（variables）經過宣告（declaration）後，就會依指定資料型態配置記憶體

## 常數宣告

宣告常數的關鍵字為 const，常數（constants）可避免重複輸入，以減少輸入的錯誤

# 算術運算

| 算數運算子 | 可進行的運算 |
| --- | --- |
| + | 加法 |
| - | 減法 |
| * | 乘法 |
| / | 除法 |
| % | 餘數 |
| ++ | 累加 |
| — | 累減 |

## 整數除法

1/2   得到 0

3/7   得到 0

15/2 得到 7

## 累加累減

M = i++ * 5 相當於 M = i * 5; i++;

M = ++i * 5 相當於 i++; M = i*5

## 指派運算子（assignment operators）

| 敘述 | 具有相同結果的敘述 |
| --- | --- |
| x = x +y | x += y |
| x = x * y | x *= y |
| x = x / y | x /= y |
| x = x % y | x %= y |

## 資料型態轉換

- （資料型態）變數名稱 ⇒  x = float (a) + 3.8f
- 資料型態（變數名稱） ⇒  x = (float) a + 3.8f

# sizeof() 運算子

輸入：

```cpp
#include <iostream>
using namespace std;

int main()
{
	int x = 5;

	cout << "Size of int is : "        << sizeof(int)      << " bytes" << endl;
	cout << "Size of short is : "      << sizeof(short)    << " bytes" << endl;
	cout << "Size of unsigned is : "   << sizeof(unsigned) << " bytes" << endl;
	cout << "Size of long is : "       << sizeof(long)     << " bytes" << endl;
	cout << "Size of float is : "      << sizeof(float)    << " bytes" << endl;
	cout << "Size of double is : "     << sizeof(double)   << " bytes" << endl;
	cout << "Size of char is : "       << sizeof(char)     << " bytes" << endl;
	cout << "Size of 3.8 is : "        << sizeof(3.8)      << " bytes" << endl;
	cout << "Size of (3.8 + x) is : "  << sizeof(3.8 + x)  << " bytes" << endl;
	cout << "Size of 3.8f is : "       << sizeof(3.8f)     << " bytes" << endl;
	cout << "Size of x is : "          << sizeof(x)        << " bytes" << endl;
	cout << "Size of (3.8f + x) is : " << sizeof(3.8f + x) << " bytes" << endl;

	return 0;
}
```

輸出：

```cpp
Size of int is : 4 bytes
Size of short is : 2 bytes
Size of unsigned is : 4 bytes
Size of long is : 4 bytes
Size of float is : 4 bytes
Size of double is : 8 bytes
Size of char is : 1 bytes
Size of 3.8 is : 8 bytes
Size of (3.8 + x) is : 8 bytes
Size of 3.8f is : 4 bytes
Size of x is : 4 bytes
Size of (3.8f + x) is : 4 bytes
```

# 標準數學函數

輸入：

```cpp
#include <cmath>
#include <iostream>
using namespace std;

int main()
{
	double x = 5;

	cout << "Result of abs(x) is "    << abs(x) << endl;
	cout << "Result of exp(x) is "    << exp(x) << endl;
	cout << "Result of pow(x, 3) is " << pow(x, 3) << endl;
	cout << "Result of sqrt(x) is "   << sqrt(x) << endl;
	cout << "Result of log(x) is "    << log(x) << endl;
	cout << "Result of log10(x) is "  << log10(x) << endl;
	cout << "Result of ceil(x) is "   << ceil(x) << endl;  // 大於等於 x 最小整數
	cout << "Result of floor(x) is "  << floor(x) << endl; // 小於等於 x 最大整數
	cout << "Result of sin(x) is "    << sin(x) << endl;
	cout << "Result of cos(x) is "    << cos(x) << endl;
	cout << "Result of tan(x) is "    << tan(x) << endl;

	return 0;
}
```

輸出：

```cpp
Result of abs(x) is 5
Result of exp(x) is 148.413
Result of pow(x, 3) is 125
Result of sqrt(x) is 2.23607
Result of log(x) is 1.60944
Result of log10(x) is 0.69897
Result of ceil(x) is 5
Result of floor(x) is 5
Result of sin(x) is -0.958924
Result of cos(x) is 0.283662
Result of tan(x) is -3.38052
```

# 關係運算

| 關係運算子 | 意義 |
| --- | --- |
| > | 大於 |
| < | 小於 |
| <= | 小於等於 |
| >= | 大於等於 |
| == | 相等 |
| != | 不相等 |

# 邏輯運算

| 邏輯運算子 | 邏輯意涵 |
| --- | --- |
| && | AND |
| || | OR |
| ! | NOT |

# Bool 資料型態

輸入：

```cpp
#include <iostream>
using namespace std;

int main()
{
	bool b1, b2, b3, b4;

	b1 = true;
	b2 = false;
	b3 = (3 > 1);
	b4 = (3 < 1);

	cout << "b1 = "            << b1 << endl;
	cout << "b2 = "            << b2 << endl;
	cout << "b3 = "            << b3 << endl;
	cout << "b4 = "            << b4 << endl;
	cout << "Size of bool is " << sizeof(bool) << endl;
	cout << "Size of b1 is   " << sizeof(b1) << endl;

	return 0;
}
```

輸出：

```cpp
b1 = 1
b2 = 0
b3 = 1
b4 = 0
Size of bool is 1
Size of b1 is   1
```

# 字元字串

## 字元

char CH = ‘a’

## 字串

“ABCDE”

## 逃離序列（escape sequences）

| escape sequence | 意義 |
| --- | --- |
| \n | 跳到下一行 |
| \t | 跳到下個 tab |
| \b | 退回一格 |
| \f | 跳到下一頁 |
| \r | 輸入 |
| \\ | 反斜線 \ |
| \’ | 單引號 ‘ |
| \” | 雙引號 “ |
| \0 | 字串結束符號 |

# 位元處理運算

| 位元處理運算子 | 意義 |
| --- | --- |
| ~ | 補數 |
| << | 左移 |
| >> | 右移 |
| & | AND |
| ^ | XOR |
| | | OR |

## AND 運算

| 表示式 | 計算結果 |
| --- | --- |
| a | 01000001 |
| b | 01100010 |
| a & b | 01000000 |

## XOR 運算

| 表示式 | 計算結果 |
| --- | --- |
| a | 01000001 |
| b | 01100010 |
| a ^ b | 00100011 |

## OR 運算

| 表示式 | 計算結果 |
| --- | --- |
| a | 01000001 |
| b | 01100010 |
| a | b | 01100011 |

## 補數運算

| 表示式 | 計算結果 |
| --- | --- |
| a | 01000001 |
| ~a | 10111110 |

## 右移運算

| 表示式 | 計算結果 |
| --- | --- |
| a | 10011010 |
| a >> 2 | 00100110 |

## 左移運算

| 表示式 | 計算結果 |
| --- | --- |
| a | 10011010 |
| a << 3 | 11010000 |