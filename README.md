# HarvardX CS50P's Introduction to Programming with Python

This repo contains the solution to the problem sets.

- Week 0: Functions, Variables
- Week 1: Loops






### Week 0: Functions, Variables

Link to Problem Set 0: https://cs50.harvard.edu/python/2022/psets/0/

**Indoor Voice**
```python
voice = input("Use your indoor voice! ").lower()

print(voice)
```

**Playback Speed**
```python
playback = input("Display 0.75 playback speed ").split()

print('...'.join(playback))
```

**Making Faces**
```python
def main():
    face = str(input("What's your input? ")).replace(":)","🙂").replace(":(","🙁")
    convert(face)

def convert(to="emojis"):
    print(to)

main()
```

**Einstein**
```python
m = int(input("m: "))
c = int(300000000)
energy = m * c ** 2

print(f"E: {energy}")
```

**Tip Calculator**
```python
def main():
    dollars = dollars_to_float(input("How much was the meal? "))
    percent = percent_to_float(input("What percentage would you like to tip? "))
    tip = dollars * percent
    print(f"Leave ${tip:.2f}")

def dollars_to_float(d):
    return float(d.replace("$", ""))

def percent_to_float(p):
    return float(p.replace("%",""))/100

main()
```

***

### Week 1: Loops

Link to Problem Set 1: https://cs50.harvard.edu/python/2022/psets/1/

Deep Thought
```python
answer = input("What's your answer? ").strip().lower()

if answer == "42" or answer == "forty-two" or answer == "forty two":
    print("Yes")
else:
    print("No")
```

Home Federal Savings Bank
```python
greeting = input("Greeting: ")

if "hello" in greeting.lower().strip():
    print("$0")
elif greeting[0].lower().strip() == "h":
    print("$20")
else:
    print("$100")
```

File Extensions
```python
file = input("File name: ").lower().strip()

if ".gif" in file:
    print("image/gif")
elif ".jpg" in file or ".jpeg" in file:
    print("image/jpeg")
elif ".png" in file:
    print("image/png")
elif ".pdf" in file:
    print("application/pdf")
elif ".txt" in file:
    print("text/plain")
elif ".zip" in file:
    print("application/zip")
else:
    print("application/octet-stream")
```

Math Interpreter

Meal Time
```python
def main():
    time = input("What time is it? ")
    meal_time = convert(time)

    if 7.00 <= meal_time <= 8.00:
        print("breakfast time")
    elif 12.00 <= meal_time <= 13.00:
        print("lunch time")
    elif 18.00 <= meal_time <= 19.00:
        print("dinner time")
    else:
        pass

def convert(time):
    hours, minutes = time.split(":")
    converted_time = ((int(hours) * 60) + int(minutes))/60
    return float(converted_time)

if __name__ == "__main__":
    main()
```

***

### Week 2: Loops

Link to Problem Set 2: https://cs50.harvard.edu/python/2022/psets/2/

camelCase
```python
# Solution 1
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

```python
# Solution 2
variable = input("camelCase: ")

def main():
    word = ""
    # Iterate over alphabet in variable

    for alphabet in variable:
        if alphabet.isupper():
            word += "".join("_" + alphabet.lower())
        else:
            word += "".join(alphabet)

    print(word)

main()
```

Coke Machine

Just setting up my twttr
```python
string = input("Input: ")

vowels = ("a", "e", "i", "o", "u")
new_string = ""

for s in string:
    if s.lower() in vowels:
        new_string += "".join(s.replace(s, ""))
    if s.lower() not in vowels:
        new_string += "".join(s)

print(f"Output: {new_string}")
```

Vanity Plates
Nutrition Facts
```python
item = input("Item: ").lower()

fruits = {
    "apple": 130, "avocado": 50, "banana": 110, "cantaloupe": 50, "grapefruit": 60, "grapes": 90,
    "honeydew melon": 50, "kiwifruit": 90, "lemon": 15, "lime": 20, "nectarine": 60, "orange": 80,
    "peach": 60, "pear": 100, "pineapple": 50, "plums": 70, "strawberries": 50, "sweet cherries": 100,
    "tangerine": 50, "watermelon": 80
}

if item in fruits:
    print(f"Calories: {fruits[item]}")
```

***

### Week 3: Exceptions

Link to Problem Set 3: https://cs50.harvard.edu/python/2022/psets/3/

Fuel Gauge
```python
def main():
    x = get_fuel("Fraction: ")
    if x <= 1:
        print("E")
    if 99 <= x < 101:
        print("F")
    if 1 < x < 99:
        print(x, '%', sep='')

def get_fuel(prompt):
    while True:
        try:
            fuel = input(prompt)
            x, y = fuel.split("/")
            fuel_gauge = round(int(x)/int(y)*100)

            if int(y) == 0 or int(x) > int(y):
                continue
            elif fuel_gauge <= 1:
                return fuel_gauge
            elif 99 <= fuel_gauge < 101:
                return fuel_gauge
            else: # 1 < fuel_gauge < 99:
                return fuel_gauge

        except (ValueError, ZeroDivisionError):
            pass

main()
```

Felipe’s Taqueria
Grocery List
Outdated

***
