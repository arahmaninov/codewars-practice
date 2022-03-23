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
