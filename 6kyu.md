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
