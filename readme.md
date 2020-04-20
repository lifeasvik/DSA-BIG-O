## Drills

1. Dog Friend

- The O notation for this would be constant, as we're only doing one operation.
- The O notation for this would be O(n), because we're repeating the same operation for as many people are in the room, so the amount of operations is dependent on the amount of people.

2.  Even or Odd?

```
function isEven(value) {
  // is called one time, regardless of the input
    if (value % 2 === 0) {
        return true;
    }
    else
        return false;
    }
}
```

The O notation/complexity is constant, it doesn't matter what the input is, we're running one operation, is it divisible by 2 with an outcome of 0.

3. Are you here?

```
function areYouHere(arr1, arr2) {
  // 4 * n
    for (let i = 0; i < arr1.length; i++) {
        const el1 = arr1[i]; // 1
        // 4 * n
        for (let j = 0; j < arr2.length; j++) {
            const el2 = arr2[j]; // 1
            if (el1 === el2) return true; // 1
        }
    }
    return false;
}
```

This is log(n^2), we're running a nested for loop, T = (4 _ n) + 1 + (4 _ n) + 1 + 1 => O(n^2)

4. Doubler

```
function doubleArrayValues(array) {
    for (let i = 0; i < array.length; i++) {
        array[i] *= 2;
    }
    return array;
}
```

O(n), T = (4 \* n) + 1, number of iterations is dependant on the length of the input, so therefore its linear.

5. Naive Search

```
function naiveSearch(array, item) {
    for (let i = 0; i < array.length; i++) { // 4 * n
        if (array[i] === item) { // 2
            return i; // 1
        }
    }
}
```

O(n), the amount of operations is depedant on the length input, so therefore its linear.

6. Creating pairs

```
function createPairs(arr) {
    for (let i = 0; i < arr.length; i++) { // 4 * n
        for(let j = i + 1; j < arr.length; j++) { // 4 * n
            console.log(arr[i] + ", " +  arr[j] ); // 5
        }
    }
}
```

0(n^2), t = 4 _ n _ (4 \* n ) + 5, because its a nested for loop, the amount of operations is polynomial.

7. Compute the sequence

```
function compute(num) {
    let result = []; // 1
    for (let i = 1; i <= num; i++) { //4 * n

        if (i === 1) {
            result.push(0); // 2
        }
        else if (i === 2) {
            result.push(1); // 2
        }
        else {
            result.push(result[i - 2] + result[i - 3]); // 4
        }
    }
    return result;
}
```

O(n), t = ~~1 +~~ 4 \* n ~~|| + 2 || + 4~~, because we're dependant on the input to determine the number of operations through the one loop, its a linear complexity.

8. Effcient Search

```
function efficientSearch(array, item) {
    let minIndex = 0; // 1
    let maxIndex = array.length - 1; // 2
    let currentIndex; //1
    let currentElement; // 1

    while (minIndex <= maxIndex) { // n
        currentIndex = Math.floor((minIndex + maxIndex) / 2); // 3
        currentElement = array[currentIndex]; // 2

        if (currentElement < item) { // 1
            minIndex = currentIndex + 1; // 1
        }
        else if (currentElement > item) { // 1
            maxIndex = currentIndex - 1; // 1
        }
        else {
            return currentIndex; // 1
        }
    }
    return -1;
}
```

O(log n) becuase we're adjusting the minvalue, we're reducing the size of the searchable input each iteration, the longer we go the less we have to search, and the less operations.

9. Random Element

```
function findRandomElement(arr) {
    return arr[Math.floor(Math.random() * arr.length)]; // 4
}
```

O(1), preforming one operation, the size of the input doesn't matter.

10. What am I?

```
function isWhat(n) {
    if (n < 2 || n % 1 !== 0) { // 2
        return false; // 1
    }
    for (let i = 2; i < n; ++i) { // 4 * n
        if (n % i === 0) return false; // 2
    }
    return true; // 1
}
```

O(n), the best case is, we break on the if, or the first iteration, worst case we iterate through the entire array, therefore the number of operations is dependant on the input, making it linear. This function is checking to see if the supplied number is prime.

---

## Recursive Big O

Take your solutions from the recursive exercises that you
completed in the previous checkpoint and identify the time
complexities (big O) of each of them.

=============================================================================
1
O(n) Linear time complexity
=============================================================================
2
O(n) Linear time complexity
=============================================================================
3
O(n) Linear time complexity
=============================================================================
4
O(n) Linear time complexity
=============================================================================
5
O(n) Linear time complexity
=============================================================================
6
O(n) Linear time complexity
=============================================================================
7
O(n) Linear time complexity
=============================================================================
8
O(n^2) Polynomial time complexity
=============================================================================
9
O(n^2) Polynomial time complexity
=============================================================================
10
O(2^n) Exponential time complexity
=============================================================================
11
O(2^n) Exponential time complexity
=============================================================================
12
O(logn) Logarithmic time complexity
=============================================================================

## Iterative Big O

Take your solutions from the iterative exercises today
and identify the time complexities (big O) of each of them.

=============================================================================
1
O(n) Linear time complexity
=============================================================================
2
O(n) Linear time complexity
=============================================================================
3
O(n) Linear time complexity
=============================================================================
4
O(n) Linear time complexity
=============================================================================
5
O(n) Linear time complexity
=============================================================================
6
O(n) Linear time complexity
=============================================================================
7
O(n) Linear time complexity
=============================================================================
