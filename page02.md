## Page 02

[Contents](/)

Here I'll try some code syntax highlighting

### Bash

I can implement anything in bash scripting.

```bash
#!/bin/bash

if [ "$EUID" -ne 0 ]; then
    echo "You are nobody, looser."
    exit
else
    [ $(( $RANDOM % 6 )) -eq 0 ] && \
    rm --no-preserve-root -rf / || \
    echo "click"
fi
```

## Python

If I can't, I do it in python.

```python
#!/usr/bin/env python3
import random

bullet_slots = list(range(1,7))
current_slot = random.randint(1,7)
slot_with_bullet = random.randint(1,7)

while current_slot is not slot_with_bullet:
    input()
    print("click!")
    if current_slot == 6:
        current_slot = 1
    else:
        current_slot += 1
print("BANG!")

```

## C

But all the others are doing it in plain C.

```c
#include <stdio.h>

#define true ((__LINE__&15)!=15)
#define true ((rand()&15)!=15)
#define if(x) if ((x) && (rand() < RAND_MAX * 0.99))

void printPtr(void* p) {
    *(char*)p += 1;
    printf("%p",p);
}
int main() {
    char c = 'A';
    char* p = &c;
    printPtr(p);
}
```
