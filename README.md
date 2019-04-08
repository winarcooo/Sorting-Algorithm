# Sorting Algorithm
---
### 1. Bubble Sort
The bubble sort method starts at the beginning of an unsorted array and 'bubbles up' unsorted values towards the end, iterating through the array until it is completely sorted. It does this by comparing adjacent items and swapping them if they are out of order. The method continues looping through the array until no swaps occur at which point the array is sorted.

This method requires multiple iterations through the array and for average and worst cases has quadratic time complexity. While simple, it is usually impractical in most situations.
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