# Sorting Algorithm
---
### 1. Bubble Sort
Bubble sort membandingan 2 value yang bersebelahan (adjacent value), ini berulang terus menerus sampai list sudah tersorting. 
```js
function bubbleSort(array) {
  var isSwap = true;
  var nextIndex;

  do {
    isSwap = false;
    for (var index = 0; index < array.length - 1; index++) {
      nextIndex = index + 1;
      if (array[index] > array[nextIndex]) {
        array = swap(array, index, nextIndex)
        isSwap = true;
      }
    }
  } while(isSwap == true);

  return array;
}
function swap(array, from, to) {
  temp = array[from];
  array[from] = array[to];
  array[to] = temp;
  return array;
}
```