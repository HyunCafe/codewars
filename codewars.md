#### 6 Kyu Kata | 05.09.23
[link](https://www.codewars.com/kata/57b06f90e298a7b53d000a86/train/javascript)
```javascript
function queueTime(customers, n) {
// If the customers array is empty, return 0.
// If there is only one till (n === 1), return the sum of the customers array.
// Create an array tills and fill it with the processing times of the first n customers.
// Iterate through the remaining customers starting from index n.
// For each customer, find the till with the least processing time and add the current customer's processing time to that till.
// Return the maximum processing time from the tills array.
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
