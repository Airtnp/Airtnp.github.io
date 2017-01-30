---
layout:     post
title:      "Retrospect on C++ Templates Ch.13"
subtitle:   "Templates"
date:       2017-01-29 15:48:00
author:     "Airtnp"
header-img: "img/cpp_templates.jpg"
tags:
    - C++
    - Metaprogramming
---

在《C++ Templates: A Complete Guide》的第十三章， 作者提到了C++模板未来的方向，由于此书成书于2002年，C++03, C++0x(11), C++1y(14), C++1z(17)的新特性都尚未成稿，在此记录一下，哪些特性被实现了，哪些还没有或是有了替代品。

## 13.1 尖括号Hack

C++0x(11)中已经支持对形如`std::vector<std::list<int>>`中的`>>`不加空格的情形([wiki](https://en.wikipedia.org/wiki/C%2B%2B11#Right_angle_bracket))。 

* 然而C++ Primer 5th Edition还是加了空格..
* Lexer直接将`>>`作为一个token丢给parser处理，大概这也是C++是一个context-sensitive语言的范例之一(知乎来源清求)

还有一个是digraph和trigraph的处理。举个例子就是形如`<:`可以看做`[`，`??=`可以看做`#`。C++1z(17)已经有去除trigraph的提案([wiki](https://en.wikipedia.org/wiki/Digraphs_and_trigraphs))

## 13.2 放松typename的原则

Dependent name使用typename的原则:

* 名称出现在模板中
* 名称是受限的
* 名称不是用于指定基类继承的列表中
* 名称不是位于引入构造函数的成员初始化列表中
* （可选）名称依赖于模板参数

一个例子是全特化模板中的typename，
```c++

template<>
void clear(typename Array<int>::ElementT& p) //Error
```

没有找到相关typename的新变化，接下来（不摸的时候）会去查找ISO/IEC:14882 C++14 final draft, wg21 proposals, 以及各大编译器实现(下同)。

## 13.3 缺省函数模板实参

从[cppreference](http://en.cppreference.com/w/cpp/language/template_argument_deduction)来看，C++1z(17)似乎能支持乱序的模板参数推导了


但缺省在前的情况不明。

## 13.4 字符串文字和浮点型模板实参

从[cppreference](http://en.cppreference.com/w/cpp/language/template_parameters#Template_template_parameter)来看，模板的实参(non-type parameter)应该为converted constant expression（编译期可确定常量）。字符串字面量和浮点字面量仍不能作为模板实参（用constexpr限制）

## 13.5 放松模板的模板参数的匹配

似乎没有实现，可以用Parameter Pack(C++0x(11))来作为模板的模板参数(Type, Allocator, Traits)

## 13.6 typedef模板

C++0x(11)用扩展using来代替typedef模板，比如我们可以用如下方式使用`using`

```c++

template<size_t N>
using Vector = Matrix<N, 1>

```

## 13.7 函数模板的局部特化

似乎没有实现，可以用overload或者SFINAE来规避

## 13.8 typeof运算符

gcc在C++0x(11)引入[`decltype`](http://en.cppreference.com/w/cpp/language/decltype)之前就有了`typeof`运算符，另外还要注意`decltype`, [`typeid`](http://en.cppreference.com/w/cpp/language/typeid)的区别

* typeof(=decltype) is a compile time construct and returns the type as defined at compile time

* typeid(RTTI) is a runtime construct and hence gives information about the runtime type of the value.

针对函数返回值，还有[`result_of`](http://en.cppreference.com/w/cpp/types/result_of)


```c++

std::result_of_t<F(Args...)>;

==

decltype(std::declval<F>()(std::declval<Args>()...)

```

## 13.9 命名模板实参

[using](http://en.cppreference.com/w/cpp/language/type_alias)可替代。

## 13.10 静态属性

C++0x(11)引入了一套[type_traits](http://en.cppreference.com/w/cpp/types)

## 13.11 客户端的实例化诊断信息

诊断还是一坨坨的，这里有个[例子](https://zhuanlan.zhihu.com/p/24328534)

## 13.12 重载类模板

Nope.

## 13.13 List参数

C++0x(11)引入了[`initializer_list`](http://en.cppreference.com/w/cpp/utility/initializer_list)和[Template Parameter Pack](http://en.cppreference.com/w/cpp/language/parameter_pack)解决了这个问题，但是unpack的语法是个谜，没有切片/索引...

## 13.14 （内存）布局控制

C++0x(11)引入了[`alignment_of`](http://en.cppreference.com/w/cpp/types/alignment_of)来解决这个问题。

## 13.15 初始化器的演绎

C++0x(11)引入了[`auto`](http://en.cppreference.com/w/cpp/language/auto)关键字，现在可以编译器自动推导表达式类型了（函数C++0x(11)`auto`可以后置，C++1y(14)`auto`可以推导）（模板C++1z(17)`auto`可以推导)

## 13.16 函数表达式

C++0x(11)引入了[Lambda表达式](http://en.cppreference.com/w/cpp/language/lambda)，另外还有[Range_based for loop](http://en.cppreference.com/w/cpp/language/range-for)和[Structured Binding](https://skebanga.github.io/structured-bindings/)

## 结语

C++难的一比！上面都是我瞎扯的，请多指正！
