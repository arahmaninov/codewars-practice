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
