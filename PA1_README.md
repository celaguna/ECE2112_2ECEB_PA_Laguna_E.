# Programming Assignment 1

**Student Name:** Laguna, Carlvinz E.  
**Section:** 2ECE-B  
**Course Code:** ECE2112  

---

## What to Expect
This README documents three Python programs:
- **Alphabet Soup Problem** (string sorting)
- **Emoticon Soup Problem** (string replacement)
- **Unpacking List Problem** (indexing and slicing)

Each section includes the **actual code with line-by-line explanations inside the code comments**, describing the process and why each function or operation is used.

---

## Table of Contents
1. [Alphabet Soup Problem](#alphabet-soup-problem)
2. [Emoticon Soup Problem](#emoticon-soup-problem)
3. [Unpacking List Problem](#unpacking-list-problem)
4. [Programming Assingment 1 .ipynb file](https://github.com/celaguna/ECE2112_2ECEB_PA_Laguna_E./blob/main/PA1_LAGUNA.ipynb)

---

## Alphabet Soup Problem
### Problem Description
The goal of this problem is to take a word given by the user and rearrange its letters in alphabetical order.
This introduces the concept of **string manipulation** and the use of built-in Python functions like `sorted()` and `"".join()`.

### Code

```python
# Function definition: alphabet_soup takes a string input 'word'
def alphabet_soup(word):
    
    # sorted(word) arranges the letters of 'word' in alphabetical order
    # "".join(...) combines the sorted letters back into a single string
    return "".join(sorted(word))

# The word "hello" is passed to the function
# Expected output: "ehllo"
print(alphabet_soup("hello"))

# The word "hacker" is passed to the function
# Expected output: "acehkr"
print(alphabet_soup("hacker"))
```

**Step 1: Define the Function**

We define a function called alphabet_soup that takes one parameter, word.
- Functions allow us to reuse code.
- The parameter word will hold any string we want to alphabetize.

```python
def alphabet_soup(word):
```
**Step 2: Sort and Rejoin the Letters**
- sorted(word) breaks the string into characters and arranges them in alphabetical order.
  - Example: "hello" → ['e', 'h', 'l', 'l', 'o'].
- "".join(...) combines the characters back into one continuous string.
- The return statement sends this new, alphabetized string back to whoever called the function.
  
```python
return "".join(sorted(word))
```
Step 3: Test the Function with the Word "hello"
- Input: "hello"
- Sorted result: "ehllo"
- The print() function shows the output to the screen.

```python
print(alphabet_soup("hello"))
```
Step 4: Test the Function with the Word "hacker"
- Input: "hacker"
- Sorted result: "acehkr"
- Again, print() displays the result.
  
```python
print(alphabet_soup("hacker"))
```

## Takeaways
1. def is used to define a function.
2. sorted() rearranges letters of a string alphabetically.
3. "".join() glues the list of characters back into a string.
4. Functions make the logic reusable for multiple test cases.

---

## Emoticon Soup Problem  
### Problem Description  
The goal of this problem is to take a sentence and replace specific words (`smile`, `grin`, `sad`, `mad`) with their corresponding emoticons.  
This demonstrates the use of the **string method `.replace()`** and how we can transform text into more expressive forms.  

### Code  

```python
# Function definition: emotify takes a string input 'statement'
def emotify(statement):

    # Replace the word "smile" with its emoticon ":)"
    statement = statement.replace("smile", ":)")

    # Replace the word "grin" with its emoticon ":D"
    statement = statement.replace("grin", ":D")

    # Replace the word "sad" with its emoticon ":(("
    statement = statement.replace("sad", ":((")

    # Replace the word "mad" with its emoticon ">:("
    statement = statement.replace("mad", ">:(")

    # Return the modified statement with any replaced words
    return statement
    
# Test cases to show how the function works
print(emotify("Make me smile")) # Expected output: Make me :)
print(emotify("Make me grin"))  # Expected output: Make me :D
print(emotify("I am sad"))      # Expected output: I am :((
print(emotify("I am mad"))      # Expected output: I am >:(
```

**Step 1: Define the Function**
- We define a function called emotify with one parameter, statement.
- The parameter holds the full sentence (string) we want to transform.
  
```python
def emotify(statement):
```
**Step 2: Replace the Word "smile"**
- The .replace() method looks for the word "smile" inside the string.
- If found, it replaces it with the emoticon ":)".
  - Example: "Make me smile" → "Make me :)".

```python
statement = statement.replace("smile", ":)")
```
**Step 3: Replace the Word "grin"**
- Similar logic, but now "grin" is replaced by the emoticon ":D".
  - Example: "Make me grin" → "Make me :D".

```python
statement = statement.replace("grin", ":D")
```
**Step 4: Replace the Word "sad"**
- "sad" gets replaced with ":((".
  - Example: "I am sad" → "I am :((".

```python
statement = statement.replace("sad", ":((")
```
**Step 5: Replace the Word "mad"**
- "mad" gets replaced with ">:(".
  - Example: "I am mad" → "I am >:(".

```python
statement = statement.replace("mad", ">:(")
```
**Step 6: Return the Modified Statement**
- After all replacements, the modified string is returned.
- Returning allows us to capture the result or display it later.
  
```python
return statement
```
**Step 7: Test the Function with Example Cases**
- Each test case runs the function with different input.
- The expected results confirm the function works correctly.

```python
print(emotify("Make me smile")) # Output: Make me :)
print(emotify("Make me grin"))  # Output: Make me :D
print(emotify("I am sad"))      # Output: I am :((
print(emotify("I am mad"))      # Output: I am >:(
```

## Takeaways
1. The .replace(old, new) method replaces all occurrences of old with new in a string.
2. Reassigning statement = statement.replace(...) ensures changes are stored.
3. Functions make the code reusable for multiple sentences.
4. This problem shows how text processing can make outputs more expressive.

---

## Unpacking List Problem  
### Problem Description  
The goal of this problem is to take a list of elements and split it into three parts:  
1. The first element  
2. The middle elements (everything except the first and last)  
3. The last element  

This problem demonstrates **list indexing**, **slicing**, and how functions can **return multiple values** in Python.  

### Code

```python
# Function definition: unpack_list takes a list input 'lst'
def unpack_list(lst):
    
    # Get the first element of the list
    first = lst[0]

    # Get all elements except the first and last (slicing from index 1 to -1)
    middle = lst[1: -1]

    # Get the last element of the list
    last = lst[-1]

    # Return the three parts as a tuple (first, middle, last)
    return first, middle, last

# Example list
lst = [1, 2, 3, 4, 5, 6]

# Call the function and unpack the result into three variables
first, middle, last = unpack_list(lst)

print("first:", first)   # Output: first: 1
print("middle:", middle) # Output: middle: [2, 3, 4, 5]
print("last:", last)     # Output: last: 6
```

**Step 1: Define the Function**
- We define a function unpack_list that takes a list lst as its input.
- Using a function makes the code reusable for any list.

```python
def unpack_list(lst):
```
**Step 2: Get the First Element**
- Python uses zero-based indexing, so lst[0] is always the first element.
  - Example: [1, 2, 3, 4, 5, 6] → 1.

```python
first = lst[0]
```
**Step 3: Get the Middle Elements**
- Slicing lst[1:-1] means: start at index 1 (second element) and go up to (but not including) index -1 (last element).
  - Example: [1, 2, 3, 4, 5, 6] → [2, 3, 4, 5].

```python
middle = lst[1:-1]
```
**Step 4: Get the Last Element**
- Negative indexing lets us access elements from the end.
- lst[-1] gives the last item of the list.
  - Example: [1, 2, 3, 4, 5, 6] → 6.

```python
last = lst[-1]
```
**Step 5: Return All Three Parts**
- We return all three parts at once as a tuple (first, middle, last).
- This is a Python feature: one function can return multiple values.

```python
return first, middle, last
```
**Step 6: Example Usage**
- The function is called with the list [1, 2, 3, 4, 5, 6].
- The returned values are unpacked into three variables: first, middle, and last.

```python
lst = [1, 2, 3, 4, 5, 6]
first, middle, last = unpack_list(lst)
```
**Step 7: Display the Results**
- The results are printed so the user can see each part clearly.

```python
print("first:", first)   # first: 1
print("middle:", middle) # middle: [2, 3, 4, 5]
print("last:", last)     # last: 6
```

## Takeaways
1. Lists use indexing (lst[0]) and slicing (lst[start:end]).
2. Negative indices like -1 allow quick access to the last element.
3. Python functions can return multiple values at once.
4. Unpacking lets us store those multiple return values into separate variables.

---

# 📌 Conclusion  

In this assignment, I implemented and explained three Python problems in detail:  

1. **Alphabet Soup Problem** → Demonstrated **string manipulation** using `sorted()` and `"".join()` to reorder characters alphabetically.  
2. **Emoticon Soup Problem** → Showed the use of **string replacement methods** (`.replace()`) to transform text into emoticons.  
3. **Unpacking List Problem** → Explained **list indexing, slicing, and tuple returns**, highlighting Python’s ability to handle multiple values.  

Across all three problems, a few common programming concepts were reinforced:  
- **Functions** make code reusable, modular, and easier to test.  
- **Built-in Python methods** (`sorted()`, `.replace()`, slicing) simplify solving real-world problems.  
- **Step-by-step problem solving** ensures clarity and maintainability.  

Overall, these exercises taught me not just how to code solutions, but also how to **explain the reasoning** behind each line, making the learning process deeper and more practical.

---





























