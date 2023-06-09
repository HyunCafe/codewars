#### 6 Kyu Kata | 05.09.23
[link](https://www.codewars.com/kata/57b06f90e298a7b53d000a86/train/javascript)
```javascript
function queueTime(customers, n) {
  if (customers.length === 0) {
    return 0;
  }
  
  if (n === 1) {
    return customers.reduce((a, b) => a + b)
  }
  
  const tills = customers.slice(0, n)
  
  for (let i = n; i < customers.length; i++) {
    const minTillIndex = tills.indexOf(Math.min(...tills));
    tills[minTillIndex] += customers[i];
  }
  
  return Math.max(...tills)
}
```

#### 7 Kyu Kata | 05.11.23
[link](https://www.codewars.com/kata/563089b9b7be03472d00002b/javascript)
```javascript
Array.prototype.remove_ = function(integer_list, values_list){
  return integer_list.filter(elements => !values_list.includes(elements));
}
```

#### 7 Kyu Kata | 05.12.23
[link](https://www.codewars.com/kata/56e3cd1d93c3d940e50006a4/javascript)
```javascript
function makeValley(arr) {
  arr.sort((a, b) => b - a);

  const leftWing = [];
  const rightWing = [];

  for (let i = 0; i < arr.length; i++) {
    if (i % 2 === 0) {
      leftWing.push(arr[i]);
    } else {
      rightWing.unshift(arr[i]);
    }
  }

  return leftWing.concat(rightWing);
}
```

#### 6 Kyu Kata | 05.13.23
[link](https://www.codewars.com/kata/5825792ada030e9601000782/train/javascript)
```javascript
function zipWith(fn,a0,a1) {
 let results = [];
 let minLength = a0.length < a1.length ? a0.length : a1.length;
  for (let i = 0; i < minLength; i++) {
    const combinedValues = fn(a0[i], a1[i]);
    results.push(combinedValues)
  }
  return results;
}
```

#### 6 Kyu Kata | 05.14.23
[link](https://www.codewars.com/kata/550554fd08b86f84fe000a58/train/javascript)
```javascript
function inArray(array1,array2){
  return array1.filter((words) => array2.some((words2) => words2.includes(words))).sort();
}
```

#### 6 Kyu Kata | 05.16.23
[link](https://www.codewars.com/kata/514b92a657cdc65150000006/javascript)
```javascript
function solution(number){
  let sum = 0;
  for (let i = 0; i < number; i++) {
    if (i % 3 === 0 || i % 5 === 0) {
      sum += i;
    }
  }
  return sum;
}
```

#### 6 Kyu Kata |  05.24.23
[link](https://www.codewars.com/kata/525f50e3b73515a6db000b83/train/javascript)
```javascript
function createPhoneNumber(numbers){
  const areaCode = numbers.slice(0, 3).join('');
  const firstHalfNum = numbers.slice(3, 6).join('');
  const lastHalfNum = numbers.slice(6).join('');
  return `(${areaCode}) ${firstHalfNum}-${lastHalfNum}`
}
```

#### 7 Kyu Kata | 05.28.23
[link](https://www.codewars.com/kata/57ecf6efc7fe13eb070000e1/train/javascript)
```javascript
function outed(meet, boss) {
  let bossVal = meet[boss] * 2;
  let totalHappiness = Object.values(meet).reduce((a, b) => a + b) + bossVal - meet[boss];
  let averageHappiness = totalHappiness / (Object.keys(meet).length);
  return averageHappiness > 5 ? 'Nice Work Champ!' : 'Get Out Now!';
}
```

#### 7 Kyu Kata | 05.29.23
[link](https://www.codewars.com/kata/5784c89be5553370e000061b/train/javascript)
```javascript
function maxProduct(a) {
  let largestNum = a[0];
  let secondLargestNum = -Infinity;
  for (let i = 1; i < a.length; i++) {
    if (a[i] > largestNum) {
      secondLargestNum = largestNum;
      largestNum = a[i];
    } else if (a[i] > secondLargestNum) {
      secondLargestNum = a[i];
    }
  }
  return largestNum * secondLargestNum;
}
```

#### 7 Kyu Kata | 05.30.23
[link](https://www.codewars.com/kata/56576f82ab83ee8268000059/train/javascript)
```javascript
function spacey(array){
  return array.map((_, i) => array.slice(0, i + 1).join(''));
}
 ```

#### 7 Kyu Kata | 06.01.23
[link](https://www.codewars.com/kata/62a611067274990047f431a8/train/javascript)
```javascript
function alternate(n, firstValue, secondValue){
  const altArray = [];
  for (let i = 0; i < n; i++) {
    if(i % 2 == 0) {
      altArray.push(firstValue);
    } else {
      altArray.push(secondValue);
    }
  }
  return altArray;
}
```

#### 7 Kyu Kata | 06.03.23
[link](https://www.codewars.com/kata/56576f82ab83ee8268000059/train/javascript)
```javascript
function spacey(array){
  return array.map((_, i) => array.slice(0, i + 1).join(''));
}
```

#### 7 Kyu Kata | 06.05.23
[link](https://www.codewars.com/kata/54f9c37106098647f400080a/train/javascript)
```javascript
function dropWhile(arr, pred) {
  const dropIndex = arr.findIndex(num => !pred(num));
  return dropIndex >= 0 ? arr.slice(dropIndex) : [];
}
```
#### 7 Kyu Kata | 06.06.23
[link](https://www.codewars.com/kata/5ba38ba180824a86850000f7/train/javascript)
```javascript
function solve(arr) {
    return arr.reduceRight((accumulator, value) => {
        if (!accumulator.includes(value)) {
            accumulator.unshift(value);
        }
        return accumulator;
    }, []);
}
```

#### 7 Kyu Kata | 06.11.23
[link](https://www.codewars.com/kata/529f2d1c403a58f660000656/javascript)
```javascript
const Calculator = {
  add: (a, b) => {
    return a + b;
  },
  subtract: (a, b) => {
    return a - b;
  },
  multiply: (a, b) => {
    return a * b;
  },
  divide: (a, b) => {
    if (b !== 0) {
      return a / b;
    } else {
      return false;
    }
  }
};
```

#### 7 Kyu Kata | 06.16.23
[link](https://www.codewars.com/kata/54ff3102c1bad923760001f3/train/javascript)
```javascript
function getCount(str) {
  let vowels = ['a', 'e', 'i', 'o', 'u'];
  let count = 0;
  let spreadWord = str.split('');

  for (let i = 0; i < spreadWord.length; i++) {
    if (vowels.includes(spreadWord[i])) {
      count++;
    }
  }

  return count;
}
```

#### 7 Kyu Kata | 06.17.23
[link](https://www.codewars.com/kata/56747fd5cb988479af000028/train/javascript)
```javascript
function getMiddle(s) {
  if (s.length % 2 === 0) {
    let midIndex = s.length / 2;
    return s.slice(midIndex - 1, midIndex + 1);
  } else {
    let midIndex = Math.floor(s.length / 2);
    return s[midIndex];
  }
}
```

#### 7 Kyu Kata | 06.21.23
[link](https://www.codewars.com/kata/55908aad6620c066bc00002a)
```javascript
function XO(str) {
    const strLowerCase = str.toLowerCase();
    const validX = (strLowerCase.match(/x/g) || []).length;
    const validO = (strLowerCase.match(/o/g) || []).length;
  
    return validX === validO;
```

#### 7 Kyu Kata | 06.22.23
[link](https://www.codewars.com/kata/57f609022f4d534f05000024)
```javascript
function stray(numbers) {
  let orderedNumbers = numbers.sort((a, b) => a - b);

  if (orderedNumbers[0] !== orderedNumbers[1]) {
    return orderedNumbers[0];
  } else {
    return orderedNumbers[orderedNumbers.length - 1];
  }
}
```
