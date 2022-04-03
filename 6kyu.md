# Handshake problem
https://www.codewars.com/kata/handshake-problem

**Python**
```Python
from math import ceil

def get_participants(handshakes):
    return ceil((1 + (8 * handshakes + 1) ** 0.5) / 2)
```

**JavaScript**
```JavaScript
function getParticipants(handshakes){
  return Math.ceil((1 + Math.sqrt(8 * handshakes + 1)) / 2);
}
```

# Duplicate Encoder
https://www.codewars.com/kata/duplicate-encoder

**Python**
```Python
def duplicate_encode(word):
    result = ''
    word = word.lower()
    for i in word:
        if word.count(i) == 1:
            result += '('
        else:
            result += ')'
            
    return result
```

**JavaScript**
```JavaScript
function duplicateEncode(word){
  result = '';
  word = word.toLowerCase();
  
  for (let letter of word) {
  let count = 0;
    for (let i = 0; i < word.length; i++) {

        if (word.charAt(i) == letter) {
            count += 1;
        }
    }

  if (count == 1) {
    result += '(';
  } else {
    result += ')';
  }
  }
    
  return result;
}

```

# N-th Fibonacci
https://www.codewars.com/kata/n-th-fibonacci

**Python**
```Python
def nth_fib(n):
    start_arr = [0, 1]
    for i in range(n - 2):
        start_arr.append(start_arr[-1] + start_arr[-2])

    return start_arr[n - 1]
```

**JavaScript**
```JavaScript
function nthFibo(n) {
  startArr = [0, 1];
  for (let i = 0; i < n - 2; i++) {
      startArr.push(startArr[startArr.length - 1] + startArr[startArr.length - 2]);
  }
  
  return startArr[n - 1];
}
```

# Multiples of 3 or 5
https://www.codewars.com/kata/multiples-of-3-or-5

**Python**
```Python
def solution(number):
    result = 0
    for i in range(1, number):
        if i % 3 == 0 or i % 5 == 0:
            result += i
            
    return result
```
**JavaScript**
```JavaScript
function solution(number){
  let result = 0;
  for (let i = 1; i < number; i++) {
      if (i % 3 == 0 || i % 5 == 0) {
          result += i;
      }
  }
  
  return result
}
```

# Array Deep Count
https://www.codewars.com/kata/array-deep-count

**JavaScript**
```JavaScript
function deepCount(a){ 
    let count = 0; 
    const recursion = arr => { 
        count += arr.length;
        for ( let i of arr ) {
            if ( Array.isArray(i) ) {
                recursion(i);
                }             
        }         
    } 
    recursion(a);
    
    return count;     
}
```
# Length of missing array


**JavaScript**
```JavaScript
function getLengthOfMissingArray(arr) {
  console.log(`This is original array: ${arr}`);
  console.log('---------')
  let lenArray = [];
  if (arr === null) {
    return 0;
  }
  if (arr.length == 0) {
      return 0;
  } else {
      for (let i of arr) {
          if (Boolean(i) != true || i.length == 0) {
              return 0;
          } else {
              lenArray.push(i.length);
          }
      }
  }
  //console.log(lenArray);
  lenArray.sort();
  console.log(lenArray);
  
  if (lenArray.length == 0) {
      return 0;
  } else {
      for (let j = Math.min(...lenArray); j <= Math.max(...lenArray); j++) {
          if (lenArray.includes(j) === false) {
              console.log('complete!')
              return j;
          }
      }
  }
}
```
