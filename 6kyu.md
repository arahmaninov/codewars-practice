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
