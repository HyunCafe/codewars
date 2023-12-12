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

#### 7 Kyu Kata | 10.11.23
[link}(https://www.codewars.com/kata/52b5247074ea613a09000164/train/javascript)
```javascript
function cookingTime(eggs) {
  // if total eggs is less than or equal to 8 return eggs * 5
  // if total eggs is greater than 8 then store it to variable capacity
  // capacity will check if eggs is divisble by 8 and if its fraction round up to the nearest
  // whole number
 if (eggs > 0 && eggs <= 8) {
    return 5;
  } else {
    // If there are more than 8 eggs, calculate the capacity
    let capacity = Math.ceil(eggs / 8);
    return capacity * 5;
  }
}
```

#### 6 Kyu Kata | 11.17.23
[link](https://www.codewars.com/kata/5277c8a221e209d3f6000b56/train/javascript)
```javascript
function validBraces(braces) {
  const stack = [];
  const openers = {
    '(': ')',
    '[': ']',
    '{': '}',
  };

  for (const character of braces) {
    if (openers.hasOwnProperty(character)) {
      // Push the opening brace onto the stack
      stack.push(openers[character]);
    } else if (!stack.length || stack.pop() !== character) {
      // If the stack is empty or the top element doesn't match, the braces are invalid
      return false;
    }
  }

  // If the stack is empty after processing all braces, the braces are valid
  return stack.length === 0;
}  
```

#### 6 Kyu Kata | 11.18.23
[link](https://www.codewars.com/kata/5208f99aee097e6552000148/train/javascript)
```javascript
// complete the function
function solution(string) {
    // input is a string in camelCasing
  // output should be the same string with a space between each camelcase
  // if empty string return empty string
  
  if(string === '') {
    return '';
  }
  
  let spacedCamelCase = string.split('').map((letter) => {
    if (letter === letter.toUpperCase()) {
      return ` ${letter.toUpperCase()}`
    } else {
      return letter;
    }
  }).join('')
  
  return spacedCamelCase;
  
}
```

#### 6 Kyu Kata | 11.18.23
[link](https://www.codewars.com/kata/550498447451fbbd7600041c/train/javascript)
```javascript
function comp(array1, array2) {
  if (!array1 || !array2 || array1.length !== array2.length) {
    return false;
  }

  const hashCheck = {};
  const arr1Squared = array1.map((number) => number * number);

  for (const num of arr1Squared) {
    hashCheck[num] = (hashCheck[num] || 0) + 1;
  }

  return array2.every((num) => hashCheck[num] && hashCheck[num]--);
}
```

#### 6 Kyu Kata | 11.20.23
[link](https://www.codewars.com/kata/52efefcbcdf57161d4000091/train/javascript)
```javascript
function count(string) {
  // input are strings
  // output should be how many times a char appears in object format
  // empty string returns empty object
  
  // so initial thinking is that i can seperate out the string into an array
  // then im thinking to sort the array 
  // declare a blank object, then  use map to push each element into the blank object
  // and keep track of each same element by incremting a counter by 1 and pushing it as
  // a number as the value for the corresending element as a property for the blank object
  const trackValues = {};
  
  let spreadString = [...string].sort();
  
  spreadString.map((prop) => {
    trackValues[prop] = (trackValues[prop] || 0) + 1;
  })
  
  return trackValues;
}
```
#### 6 Kyu Kata | 11.20.23
[link](https://www.codewars.com/kata/587731fda577b3d1b0001196/train/javascript)
```javascript
String.prototype.camelCase = function () {
  const strArr = this.split(' ');

  return strArr.map((word) => {
    if (!word) { 
      return '';
    } else {
      return word[0].toUpperCase() + word.slice(1);
    }
  }).join('');
};

// Solution 2
String.prototype.camelCase=function(){
 // so i am thinking of seperating the string into an array w/ individual elements
  // then using map to target the first index of the grouped elem, and slice to combine
  // then join it back into a string and return it
  
  return this.split(' ').map((words) => {
    return words.charAt(0).toUpperCase() + words.slice(1);
  }).join('')
}
```

#### 6 Kyu Kata | 11.21.23
[link](https://www.codewars.com/kata/52b757663a95b11b3d00062d/train/javascript)
```javascript
function toWeirdCase(string){
  // input: will be a string
  // output: should be a string but all even index capitalized && all odd index lower case
  // 0 based, meaning 0 index = uppercase, and should start over for each word
  
  // so i'm thinking of spreading the string with split' ' to seperate
  // the string into an array of word strings
  // then using map to indicate toUpperCase each even index starting with 0
  // and toLowerCase() all odd index
  // then join the array back into a string of words seperated by a space
  
  let strArr = string.split(' ');

  return strArr.map((words) => {
    return words.split('').map((letter, index) => {
      if (index % 2 === 0) {
        return letter.toUpperCase();
      } else {
        return letter.toLowerCase();
      }
    }).join('')
  }).join(' ')
}

```

#### 6 Kyu Kata | 11.24.23
[link](https://www.codewars.com/kata/5202ef17a402dd033c000009/train/javascript)
```javascript
function titleCase(title, minorWords) {
  if (!title) return '';

  let words = title.toLowerCase().split(' ');

  let minorWordsArray = minorWords ? minorWords.toLowerCase().split(' ') : '';

  return words.map((word, index) => {
    if (index === 0 || !minorWordsArray.includes(word)) {
      return word[0].toUpperCase() + word.slice(1);
    }
    return word;
  }).join(' ');
}
```

#### 6 Kyu Kata | 11.24.23
[link](https://www.codewars.com/kata/51e0007c1f9378fa810002a9/train/javascript)
```javascript
// Return the output array, and ignore all non-op characters
function parse(data) {
  let arr = [];

  data.split('').reduce((acc, curr) => {
    switch (curr) {
      case 'i':
        return acc + 1;
      case 'd':
        return acc - 1;
      case 's':
        return acc * acc;
      case 'o':
        arr.push(acc);
        return acc;
      default:
        return acc;
    }
  }, 0);

  return arr;
}
```

### 6 Kyu Kata | 11.25.23 
[link](https://www.codewars.com/kata/5ce399e0047a45001c853c2b/train/javascript)
```javascript
function partsSums(ls) {
  // input will be an array of numbers
  // we will gather the sum of the array
  // then we will remove the first index and fine the sum again
  // keep repeating this until the array is empty
  // then return a new array with the sum of the values as elements
  // in descending order
  
  // i will use reduce to find the sum, then push it into a new array
  // then will pop the first element out and do reduce again
  // keep repeating the process till the array is empty then return the new array
  
  const arr = [];
  let spreadArr = [...ls]
  
  while (spreadArr.length > 0) {
    let sum = spreadArr.reduce((acc, num) => acc + num);
    arr.push(sum);
    spreadArr.shift();
  }
 arr.push(0)
  return arr;
}

// Solution 2:
function partsSums(ls) {
  let newArr = [];
  let totalSum = ls.reduce((acc, curr) => acc + curr, 0);  // Calculate total sum once

  // Push the total sum and then reduce it in each iteration
  newArr.push(totalSum);
  for (let i = 0; i < ls.length; i++) {
    totalSum -= ls[i];  // Subtract the current element
    newArr.push(totalSum);  // Push the new sum after subtraction
  }

  return newArr;
}
```

#### 6 Kyu Kata | 12.01.23
[Link](https://www.codewars.com/kata/54dc6f5a224c26032800005c/train/javascript)
```javascript
function stockList(listOfArt, listOfCat) {
  if (listOfArt.length === 0 || listOfCat.length === 0) return '';

  const hashObject = {};

  listOfArt.forEach((book) => {
    let [code, quantity] = book.split(' ');
    let category = code[0];
    quantity = +quantity;
    
    if (hashObject[category]) {
      hashObject[category] += quantity;
    } else {
      hashObject[category] = quantity;
    }
  });

  let results = listOfCat.map(cat => {
    let quantity = hashObject[cat] || 0;
    return `(${cat} : ${quantity})`;
  });

  return results.join(' - ');
}

```

#### 6 Kyu Kata | 12.01.23
[link](https://www.codewars.com/kata/59df2f8f08c6cec835000012/train/javascript)
```javascript
function meeting(s) {
    // input will be a string of first:lastname seperated by ;
  // output = sorted (lastname, firstname) capitalized no space
  
  let splitFullNames = s.split(';')
  let reformatedNames = splitFullNames.map((names) => {
    let [firstName, lastName] = names.split(':')
    return `(${lastName.toUpperCase()}, ${firstName.toUpperCase()})`
  })
  
  return reformatedNames.sort().join('');
}

// Solution 2 redid another day
function meeting(s) {
    // input: will be a string of first:last names seperated by ;
  // output: (LAST, FIRST)
  
  const names = s.split(';');
  
  const splitNames = names.map((name) => {
     const [firstName, lastName] = name.split(':')
     return `(${lastName.toUpperCase()}, ${firstName.toUpperCase()})`
  })
  
  return splitNames.sort().join('')
}
```

#### 6 Kyu Kata | 12.03.23
[link](https://www.codewars.com/kata/56a5d994ac971f1ac500003e/train/javascript)
```javascript
function longestConsec(strarr, k) {
    // input: an array of strings and numbers
  // output: concat of the word elements based on k number that is the longest char length
  
  // map through strarr and concat elements k times using slice to indicate index start and index + k end 
  // then join back into one string
  
  // use reduce on that to return the longest string
  
  
  if (!strarr.length || k > strarr.length || k <= 0 ) return '';
  
  let concatStr = strarr.map((_, index) => {
    return strarr.slice(index, index + k).join('')
  });
  
  return concatStr.reduce((acc, curr) => {
    return curr.length > acc.length ? curr : acc;
  })
 }

// solution 2 next day
function longestConsec(strarr, k) {
  // input: array of strings and number
  // output: strings concat k number of times with the longest combination of .length after

  if (!strarr.length || k > strarr.length || k <= 0) return '';
  
  let combinedStr = strarr.map((_, index) => {
    return strarr.slice(index, index + k).join('')
  });
  
    let longestStr = combinedStr.reduce((acc, curr) => {
      return curr.length > acc.length ? curr : acc;
    });
  
  return longestStr;
}
```

#### 6 Kyu Kata | 12.11.23
[link](https://www.codewars.com/kata/56b5afb4ed1f6d5fb0000991/train/javascript)
```javascript
function revrot(str, sz) {
   // input = string of digits
  // operation to do = cut string into chunks
  // chunks = substring of the string of size (sz) 
  // ignore last chunk if chunk < sz
  // if chunk === intger sum of the cubes of its digits / 2  -- then reverse
  // if not move the last chunk to the left by one index/position
  // sz is <= 0 or if str is empty return ""
   // sz is greater (>) than the length of str it is impossible to take a chunk of size sz hence return "".
  if (sz <= 0 || !str || sz > str.length) return '';
  
  const chunks = [];
  
  for (let i = 0; i <= str.length; i += sz) {
    if (i + sz <= str.length) {
      chunks.push(str.slice(i, i + sz))
    }
  }
    
   return chunks.map(chunk => {
        // Calculate the sum of the cubes of the digits in the chunk
        const sumOfCubes = [...chunk].reduce((acc, curr) => acc + Math.pow(parseInt(curr), 3), 0);

        // Reverse the chunk if sum of cubes is divisible by 2, otherwise rotate
        if (sumOfCubes % 2 === 0) {
            return chunk.split('').reverse().join('');
        } else {
            return chunk.slice(1) + chunk[0];
        }
    }).join('');
  }
```
