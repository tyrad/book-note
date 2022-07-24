## 5 实现(Implementations)
### 条款26：尽可能延后变量定义式的出现时间(Postpone variable definitions as long as possible.)
- 尽可能延后变量定义的出现。这样做可增加程序的清晰度并改善程序效率。

### 条款27：尽量少做转型动作(Minimize casting.)
- C风格的转型动作：

		(T)expression //将expression转型为T
- 函数风格的转型动作：

		T(expression)  //将expression转型为T
- C++还提供四种新式转型
	- `const_cast<T>(expression)` 通常被用来将对象的常量性转除(cast away the constness)。它也是唯一有此能力的C++-style转型操作符。
	- `dynamic_cast<T>(expression)` 主要用来执行“安全向下转型”(safe downcasting)，也就是用来决定某对象是否归属继承体系中的某个类型。它是唯一无法由旧式语法执行的动作，也是唯一可能耗费重大运行成本的转型动作。
	- `reinterpret_cast<T>(expression)` 意图执行低级转型，实际动作（及结果）可能取决于编译器，这也就表示它不可移植、例如将一个pointer to int转型为一个int。这类转型在低级代码以外很少见。
	- `static_cast<T>(expression)` 用来强迫隐式转换(implicit conversions)，例如将non-const对象转为const对象，或将int转为doubile等等。它也可以用来执行上数转换的反向转换，例如将void*指针zhuanweityped指针，将pointer-to-base转为pointer-to-derived。但它无法将const转换为non-const--这个只有`const_cast`才办得到。
- 旧式转型仍然合法，但是新式转型较受欢迎。
	- 第一，它们很容易在代码中被辨识出来，因而得以简化“找出类型系统在哪个地点被破坏”的过程。
	- 第二，各转型动作的目标愈窄化，编译器愈可能诊断出错误的运用。
- 如果可以，尽量避免转型，特别是在注重效率的代码中避免`dynamic_cast`。如果有个设计需要转型动作，试着发展无需转型的代替设计。
- 如果转型是必要的，试着将它隐藏于某个函数背后。客户随后可以调用该函数，则不需要将转型放进他们自己的代码内。
- 宁可使用C++-style（新式）转型，不要使用旧式转型。前者很容易辨识出来，而且也比较有着分门别类的职掌。