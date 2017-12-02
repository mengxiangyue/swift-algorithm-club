# Stack 栈

栈像一个功能受到一定限制的数组。你只能使用 *push* 新的元素到栈顶，*pop* 移除栈顶元素，和 *peek* 获取栈顶元素但是不会移除该元素。

为什么要这样设计？在许多算法中，在某个时刻你想讲对象添加到一个临时列表中，然后在之后的时间再把它们取出来。通常添加和删除对象的顺序很重要。

栈提供了后进先出（LIFO or last-in first-out）顺序。最后被 push 的元素，是下一次 pop 出来的元素。（和数据结构  [queue](../Queue/) 有些相似，只是它是先进先出（FIFO or first-in first-out））

例如，push 一个数字到栈中：

```swift
stack.push(10)
```

栈现在是 `[ 10 ]`。push 下一个数字：

```swift
stack.push(3)
```

栈现在是 `[ 10, 3 ]`。再 push 一个数字：

```swift
stack.push(57)
```

栈现在是 `[ 10, 3, 57 ]`。让我 pop 最顶部的数字出栈：

```swift
stack.pop()
```

这个返回 `57`，因为它是最近的一个被我们 push 进栈的数字。栈现在又是 `[ 10, 3 ]` 了。

```swift
stack.pop()
```

这个返回 `3`，以此类推。如果栈空了，pop 会返回 `nil` 或者在某些实现中会返回一个错误消息（例如 "stack underflow"）。

栈在 Swift 中是很容易创建的。仅仅需要包装一下数组（arrayt），提供 push、pop 和查看栈顶元素的方法就可以了：

```swift
public struct Stack<T> {
  fileprivate var array = [T]()

  public var isEmpty: Bool {
    return array.isEmpty
  }

  public var count: Int {
    return array.count
  }

  public mutating func push(_ element: T) {
    array.append(element)
  }

  public mutating func pop() -> T? {
    return array.popLast()
  }

  public var top: T? {
    return array.last
  }
}
```

注意 push 是将新的元素放到数组的尾部，不是头部。在数组的头部插入元素是代价昂贵的， **O(n)** 级，因为它需要将所有已经存在的元素在内存里面往后移动。在尾部添加是  **O(1)** 级，不管数组的大小是多少，它总是消耗相同的时间。

关于堆栈的有趣事实：每次调用函数或方法时，CPU 都会将返回地址放在堆栈上。当函数结束时，CPU 使用该返回地址跳回到调用者。这就是为什么如果你调用了太多的函数 -- 例如在一个永不结束的递归函数中 -- 当CPU堆栈空间不足时，你会得到一个所谓的“堆栈溢出”。


*Written for Swift Algorithm Club by Matthijs Hollemans*


