# Slice & Array

### Array
#### 说明
一般翻译为数组，长度固定，使用前必须确定长度
#### 特点
- Golang 中的数组是**值类型**，也就是说，如果将一个数组赋值给另一个数组，那么实际上是将整个数组拷贝了一份
- 如果将数组作为函数参数，那么实际传递的是数组的拷贝，而不是数组的指针
- array 的长度是 Type 的一部分，也就是说 `[10]int` 与 `[20]int` 不一样

### Slice
#### 特点
- slice 是一个引用类型，是一个动态的指向数组切片的指针
- slice 是一个不定长的，总是指向底层数组`array`的指针
- 因为 slice 只是一个指针，是一个指向 array 的指针，自己并没有数据，因此如果通过 slice 修改数据，对应 array 中的值也会被修改

### 区别
- 声明时，如果方括号内写明了长度，则是数组，没有写明长度就是 slice
- 作为函数参数时，数组传递的是副本，而 slice 传递的是指针

### 示例
#### 创建 slice
``` Go
// 创建 slice
var value []int

// 创建有 10 个元素的 slice
value := make([]int, 10)

// 创建有初始化元素的 slice
value := []int{1,2,3}

```

#### 创建 array
``` Go
// 创建 array
var value = [5]{1,2,3,4,5}

// 根据 array 创建 slice
sl := value[2:5]
```

### 参考
> [slice 与 array 的区别](https://segmentfault.com/a/1190000013148775)  
> [Part 11: Arrays and Slices](https://golangbot.com/arrays-and-slices/)