# 关于大O表示法笔记

清楚一个算法运行多快，和需要多少空间还是十分有用的。这些允许你能为你的工作选择出正确的算法。

大O表示法提供了一种粗略的关于算法运行时间和使用内存多少的表示方法。当一个人说：“这个算法有一个最低的运行时间**O(n^2)**和**O(n)**空间。”它意味着这个算法有几分慢，但是不需要太多额外的内存空间。

计算一个算法的大O，经常是通过数学分析完成的。在这里我们跳过了数学部分，但是知道这些不同的值得意义还是十分有用的，所以我们提供了一份便利的表格。**n**表示你处理的数据条目的多少的数字。例如，当你存储一个100个元素的数组时候，**n = 100**。

Big-O | Name | Description
------| ---- | -----------
**O(1)** | constant 常数级 | **这是最好的。** 不管数据量有多大，这个算法总是使用相同的时间。例如：通过索引查找数组中的某个元素。
**O(log n)** | logarithmic 对数级 | **相当好。** 这类算法每次迭代都会减少一半的数据量。如果你又100个元素，它将用7次找到结果。1000个元素，它用10次。1000000个元素，它仅需要20次。对于大量的数据，这是一个超级快的算法了。例如：二分查找。
**O(n)** | linear 线性的 | **性能良好** 如果你有100个条目，它将进行100个单位的工作（If you have 100 items, this does 100 units of work.）。如果条目的数量翻倍也会使算法工作翻倍（200个单位工作）。例如： 顺序查找。
**O(n log n)** | "linearithmic" “直线的” | **性能较好** 这比线性的稍差，但也不太坏。 Example: the fastest general-purpose sorting algorithms.
**O(n^2)** | quadratic 二次方的 | **有几分慢** 如果你有100个条目，它需要做100^2 = 10,000个单位工作。条目的数量翻倍，将会使它慢4倍（因为2的平方是4）。例如：使用嵌套循环的算法，比如插入排序。
**O(n^3)** | cubic 立方的 | **性能差** 如果你有100个条目，它需要做100^3 = 1,000,000个单位工作。条目的数量翻倍，将会使它慢8倍。例如：矩阵乘法。
**O(2^n)** | exponential 指数的 | **性能很差** 你应该尽量避免使用这类的算法，但是有时候你别无选择。只添加一点东西到输入中，将使运行时间增加一倍。例如：旅行商问题。
**O(n!)** | factorial 阶乘的 | **难以忍受的慢** 做任何事情都需要一百万年的时间。
  

下面是每一类运行性能的一些例子：

**O(1)**

  最普通的O(1)复杂度的例子是通过索引访问数组元素。
  
  ```swift
  let value = array[5]
  ```
    
  另外一个O(1)级的例子是在Stack中push和pop元素。
  
 
**O(log n)**

  ```swift
  var j = 1
  while j < n {
    // do constant time stuff
    j *= 2
  }
  ```  
  
  不是简单的递增，每次循环 'j' 会增加两倍。
  
  二分查找是O(log n)复杂度的一个例子。
  
  
**O(n)**

  ```swift
  for i in stride(from: 0, to: n, by: 1) {
    print(array[i])
  }
  ```
  
  数组遍历和线性搜索是O(n)复杂度的例子。
  
  
**O(n log n)**

  ```swift
  for i in stride(from: 0, to: n, by: 1) {
  var j = 1
    while j < n {
      j *= 2
      // do constant time stuff
    }
  }
  ```
  
  OR
  
  ```swift
  for i in stride(from: 0, to: n, by: 1) {
    func index(after i: Int) -> Int? { // multiplies `i` by 2 until `i` >= `n`
      return i < n ? i * 2 : nil 
    }
    for j in sequence(first: 1, next: index(after:)) {
      // do constant time stuff
    }
  }
  ```
  
  归并排序和堆排序是O(n log n)复杂度的例子。
  
  
**O(n^2)**

  ```swift
  for i  in stride(from: 0, to: n, by: 1) {
    for j in stride(from: 1, to: n, by: 1) {
      // do constant time stuff
    }
  }
  ```
  
  二维数组遍历和冒泡排序是O(n^2)复杂度的例子。
  
  
**O(n^3)**

  ```swift
  for i in stride(from: 0, to: n, by: 1) {
    for j in stride(from: 1, to: n, by: 1) {
      for k in stride(from: 1, to: n, by: 1) {
        // do constant time stuff
      }
    }
  }
  ```  
  
**O(2^n)**

  运行时间为O(2^N ) 的算法通常是递归算法，通过将大小为N的为题递归的转换成两个大小为N-1的更小的问题去解决。
  下面的示例打印了解决N个盘子的著名的“汉诺塔问题”必要的移动步骤。

  ```swift
  func solveHanoi(N: Int, from: String, to: String, spare: String) {
    guard n >= 1 else { return }
    if N > 1 {
      solveHanoi(N: N - 1, from: from, to: spare, spare: to)
    } else {
      solveHanoi(N: N-1, from: spare, to: to, spare: from)
    }
  }
  ```
  
  
**O(n!)**

  下面是最简单的 O(n!) 复杂度的例子。

  ```swift
  func nFacFunc(n: Int) {
    for i in stride(from: 0, to: n, by: 1) {
      nFactFunc(n - 1)
    }
  }
  ``` 
  
你经常不需要使用数学去计算出一个算法的大O是多少，简单点，你可以使用你的直觉。如果你的代码使用的一个循环，来查看所有的 **n** 个你输入的元素，这个算法的复杂度是 **O(n)**。如果你的代码有两层嵌套循环，它的复杂度是 **O(n^2)**。三层嵌套循环，它是 **O(n^3)**，以此类推。

注意，大O表示法是一个估计，仅对于 **n** 很大的时候，非常有用。例如：[insertion sort](Insertion%20Sort/) 最糟糕的运行时间是 **O(n^2)**。在理论上它比 [merge sort](Merge%20Sort/) 的 **O(n log n)** 更加糟糕。但是对于小数据量，插入排序是相当快的，尤其是这个数组的部分已经排好序的时候。

如果你对于这些比较困惑，不要让大O这些东西困扰你太多。当你比较两种算法哪个更好的时候，它比较有用。但是最终你仍然需要在实际中测试哪种算法最好。并且如果数据量相对较小，即使是比较慢的算法也会更快的在实际中应用。


