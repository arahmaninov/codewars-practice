# Handshake problem

**Python**
```Python
from math import ceil

def get_participants(handshakes):
    return ceil((1 + (8 * handshakes + 1) ** 0.5) / 2)
```
