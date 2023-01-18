### 什么是 TypeScript
#### --- TypeScript 的特性 (类型系统)
1. TypeScript 是静态类型
> 静态类型是指编译阶段就能确定每个变量的类型，这种语言的类型错误往往会导致语法错误。\
> TypeScript 在运行前需要先编译为 JavaScript，而在编译阶段就会进行类型检查，所以 TypeScript 是静态类型
```typescript
let foo = 1;
foo.split(' ');
// Property 'split' does not exist on type 'number'.
// 编译时会报错（数字没有 split 方法），无法通过编译
```
> TypeScript有强大的**类型推论**，即使不去手动声明变量 foo 的类型，也能在变量初始化时自动推论出它是一个 number 类型。
```typescript
let foo: number = 1;
foo.split(' ');
// Property 'split' does not exist on type 'number'.
// 编译时会报错（数字没有 split 方法），无法通过编译
```
2. TypeScript 是弱类型
```typescript
console.log(1 + '1');
// 打印出字符串 '11'
```
> 运行时数字 1 会被隐式类型转换为字符串 '1'，加号 + 被识别为字符串拼接，所以打印出结果是字符串 '11'。
