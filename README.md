# Effective C++ Note

- 01 视C++为一个语言的联邦 : View C++ as a federation of languages 
  - Basic C
  - Object-Oriented C++ 包含 class 封装 继承 多态 virtual动态绑定等
  - Templates C++ ，范型编程generic programming 部分
  - STL ，容器 迭代器 算法 函数对象等
- 02 用const,enum,inline 替代#define : Prefer const,enum,and inline to #define
  - #define 不会进入符号表，造成Debug困难
  - #define 造成代码膨胀
  - 定义常量指针时，指针本身和所指都需要const : const char* const authorName = "Scott Meyers"
  - class内常量要加static 确保只有一份实体
  - enum hack 很常用，相比const 它没有地址，且往往这是个优点
  - 