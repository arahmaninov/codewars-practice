# Count of positives / sum of negatives
https://www.codewars.com/kata/576bb71bbbcf0951d5000044/javascript

### My code

```JavaScript
function countPositivesSumNegatives(input) {
    console.log(input);
    result = [];
    if (Array.isArray(input) && input.length > 0) {
      let countPositive = 0;
      let sumNegative = 0;
      input.forEach( (element) => {
          if (element > 0) countPositive += 1;
          if (element < 0) sumNegative += element;
      })
      result.push(countPositive);
      result.push(sumNegative);
      return result;
    }
    return result;
}
```

### From comments

```JavaScript
function countPositivesSumNegatives(input) {
  if (!Array.isArray(input) || !input.length) return [];
  return input.reduce((arr, n) => {
    if (n > 0) arr[0]++;
    if (n < 0) arr[1] += n;
    return arr;
  }, [0, 0]);
}
```
