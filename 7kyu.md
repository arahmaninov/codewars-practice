# Highest and lowest
https://www.codewars.com/kata/highest-and-lowest

**Python**
```Python
def high_and_low(numbers):
    new_list = [int(i) for i in numbers.split()]
            
    low_number = new_list[0]
    high_number = new_list[0]
    
    for i in new_list:
        if i < low_number:
            low_number = i
        if i > high_number:
            high_number = i
            
    result = f"{high_number} {low_number}"
            
    return result
```

**JavaScript**
```JavaScript
function highAndLow(numbers) {
	const myArray = numbers.split(' ');

	const myArrayMax = Math.max(...myArray);
	const myArrayMin = Math.min(...myArray);

	return `${myArrayMax} ${myArrayMin}`;

}
```

# Disemvowel Trolls
https://www.codewars.com/kata/disemvowel-trolls

**Python**
```Python
def disemvowel(string_):
    result = ''
    for i in string_:
        if i not in 'aoeuiAOEUI':
            result += i
    return result
```

**JavaScript**
```JavaScript
function disemvowel(str) {
  let result = '';
  let letters = ['a', 'A', 'e', 'E', 'u', 'U', 'i', 'I', 'o', 'O'];
  for (let i of str) {
  	if(letters.indexOf(i) == -1) {
  		result += i;
  	}
  }

  return result;
}
```

# Isograms
https://www.codewars.com/kata/isograms

**Python**
```Python
def is_isogram(string):
    return len(string.lower()) == len(set(string.lower()))
```

**JavaScript**
```JavaScript
function isIsogram(str){
  let mySet = new Set(str.toLowerCase());
  return str.length == mySet.size;
}
```

# Digits explosion
https://www.codewars.com/kata/digits-explosion

**Python**
```Python
def explode(s):
    result = ''
    for i in s:
        result += i * int(i)
    return result
```

**JavaScript**
```JavaScript
function explode(s) {
  result = ''
  
  for (let i of s) {
	  for (let j = 0; j < +i; j++) {
		  result += i;
	  }
  }
  
  return result;
}
```

# Head, Tail, Init and Last
https://www.codewars.com/kata/head-tail-init-and-last

**Python**
```Python
def head(arr):
    return arr[0]

def tail(arr):
    return arr[1:]

def init(arr):
    return arr[:-1]

def last(arr):
    return arr[-1]
```

**JavaScript**
```JavaScript
function head(arr) {
	return arr[0];
}

function tail(arr) {
	return arr.slice(1);
}

function init(arr) {
	return arr.slice(0, -1);
}

function last(arr) {
	return arr[arr.length - 1];
}
```

# Javascript Mathematician

???

# The Coupon Code
https://www.codewars.com/kata/the-coupon-code

**Python**
```Python
import datetime

def check_coupon(entered_code, correct_code, current_date, expiration_date):
    current_date_obj = datetime.datetime.strptime(current_date, "%B %d, %Y")
    expiration_date_obj = datetime.datetime.strptime(expiration_date, "%B %d, %Y")
    return entered_code == str(correct_code) and current_date_obj <= expiration_date_obj
```

**JavaScript**
```JavaScript
function checkCoupon(enteredCode, correctCode, currentDate, expirationDate){
  return enteredCode === correctCode && Date.parse(expirationDate) >= Date.parse(currentDate)
}
```

# Unlucky Days

???

# My Language Skills
https://www.codewars.com/kata/my-language-skills

**Python**
```Python
def my_languages(results):
    languages = {key: value for key, value in results.items() if value > 59}
    
    return sorted(languages, key=languages.__getitem__, reverse=True)
```
