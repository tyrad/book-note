## 第3章 处理数据
- 位：计算机内存的基本单元是位（bit）。
- 字节：字节（byte）通常指的是8位的存储单元。从这个意义上说，字节指的就是描述计算机内存量的度量单位。1KB等于1024字节，1MB等于1024KB。
- 内置的C++类型分两组：
	- 基本类型：整型和浮点类型。
	- 复合类型：数组、字符串、指针和结构。
- 命名规则
	- 以两个下划线或下划线和大写字母打头的名称被保留给实现编译器及其使用的资源使用。
	- 以一个下划线开头的名称被保留，用作全局标识符。
- 内置的整型
	- unsigened long
	- long
	- unsigened int
	- int
	- unsigened short
	- short
	- unsigned char
	- char
	- signed char
	- bool
- C++ 11新增整型
	- unsigned long long
	- long long
- 内置浮点类型
	- float
	- double
	- long double
- 宽字符类型
	- wchar_t
- C++ 11新增宽字符类型
	- char16_t
	- char32_t
- const 常量限定符
- 后缀是放在数字常量后面的字母，用于表示类型。
	- 整数后面的l或L后缀表示该整型为long常量
	- u或U后缀表示unsigned int常量
	- ul（可以采用任何一种顺序，大小写均可）表示unsigned long常量。
- 强制类型转换
	- 强制类型转换不会修改thorn变量本身，而是创建一个新的、指定类型的值，可以在表达式中使用这个值。
	
    		(long) thron
            long(thron)
	- C++还引入了4个强制类型转换运算符，`static_cast<>`可用于从一种数值类型转换为另一种数值类型。
	
    		static_cast<long> (thron)
- C++ 11新增了一个工具，让编译器能够根据初始值的类型推断变量的类型。