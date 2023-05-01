# HarvardX CS50P's Introduction to Programming with Python

### Week 1: Functions, Variables


***


### Week 2: Loops

Link to Problem Set 2: https://cs50.harvard.edu/python/2022/psets/2/

camelCase

```python
variable = input("camelCase: ")
print("snake_case: ")

# Iterate over alphabet in variable
for alphabet in variable:

    # If alphabet is uppercase, print "_" followed by alphabet in lowercase
    if alphabet.isupper():
        print("_", alphabet.lower(), end="", sep="")

    # Otherwise, print alphabet as it is
    else:
        print(alphabet, end="")

print()
```


