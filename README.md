# Recursion Exercises

- ### Sum of all from 1 to n

Write a function that takes in a number as input and recursively finds the sum of all numbers up to and including that number.

```
function sum(n) {
    return n && n  + sum(n - 1);
}

```


- ### Multiply array

Write a function called `multArr` that takes in an array of numbers as an argument and recursively multiplies together all of the values in the array.

```
const multArr = (arr) => {
    if(arr.length === 0) return 1
    let lastNum = arr.pop()
    return multArr(arr) * lastNum
}


```

- ### Concatenate array

Write a function called `concatArr` that takes in an array of strings as an argument and recursively concatenates the strings together into a single string, with spaces between each original string.

```

const concatArr = (str) => {
    if(arr.length === 0) return " ";
    let shift = `${arr.shift}`
    return shift + concatArr(arr)
    
}

```

- ### Sum evens

Write a function called `sumEvens` that takes in an array of numbers as an argument and recursively sums only the even numbers in the array.

```

const sumEvens = arr => {
    if(arr.length === 0) return 0;
    let el = arr.pop();
    if(el % 2 === 0){
        return sumEvens(arr) + el;
    } else {
        return sumEvens(arr);
    }
}


```

- ### Recursive range

Write a function called `range` which takes in two numbers (num1, num2) as arguments. The function should return an array of numbers between num1 and num2.

```
const range = (num1, num2, arr = []) => {
    if(num1 === num2){
        arr.unshift(num1);
        return arr;
    }
    arr.unshift(num2);
    num2--;
    return range(num1,num2,arr);
}

```


- ### Triple Step

A child is running up a staircase with n steps and can hop either 1 step 2 steps or 3 steps at a time. Write a function called 'tripleStep', that takes in an argument `n` that represents the number of steps in the staircase, and returns a count of how many possible ways the child can run up the stairs.

```
const tripleStep = n => {
    if(n === 1 || n === 0) return 1;
    else if(n === 2) return 2;
    else {
        return tripleStep(n-3) + tripleStep(n-2) + tripleStep(n-1);
    }
}
```



