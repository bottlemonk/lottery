# Number Generatopr

Basic random number generator built in stages, each stage adds additional functionality.

## Version 1

Generates a single number between 1 and 50

```bash
function numbers_1() {
        number_1 = Math.floor(Math.random() * (50 - 0 + 1)); 
        number_1 = number_1;
    }
```

## Version 2

Generates 3 random numbers, inlcudes a check to see if the number generated is a duplicate and if it is adds a 1:

```bash
function addToArray() {
        const x = 0;
        num_array = [];
        while (num_array.length < 3) {
            const x = Math.floor(Math.random() * 50) + 1;
            if (num_array.includes(x)) {
                num_array.push(x + 1);
            }
            else {
                num_array.push(x);
            };
            num_array = num_array;
        }

    }

```