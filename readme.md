# super-agent-prac

## 当前时间

- 北京时间（Asia/Shanghai，UTC+8）：2026-11-06 18:30:08
- UTC 时间：2026-11-06 10:30:08

> 该时间为此 readme.md 创建时记录的当前时间。

## JS 冒泡排序

冒泡排序会反复比较相邻的两个元素，如果顺序不对就交换它们，每一轮结束后最大的元素会“冒泡”到末尾。

```js
function bubbleSort(arr) {
  const result = [...arr];
  for (let i = 0; i < result.length - 1; i++) {
    let swapped = false;
    for (let j = 0; j < result.length - 1 - i; j++) {
      if (result[j] > result[j + 1]) {
        [result[j], result[j + 1]] = [result[j + 1], result[j]];
        swapped = true;
      }
    }
    // 如果本轮没有发生交换，说明数组已经有序，可以提前结束
    if (!swapped) break;
  }
  return result;
}

// 示例
console.log(bubbleSort([5, 2, 9, 1, 5, 6])); // [1, 2, 5, 5, 6, 9]
```

- 时间复杂度：最坏和平均为 O(n²)，最好（数组已有序）为 O(n)。
- 空间复杂度：O(n)（复制了一份输入数组）。
- 该实现不会修改传入的原数组。
