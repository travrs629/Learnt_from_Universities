# Python-related-practical
## 2021.03.12
**1. How to initialize an array**
   - ans: 
      - Initialize an empty array: `arr = []`
      - Using `for` loop and Python `range()` function: `arr = [0 for i in range(5)]`
      - numpy method: `arr = np.empty(10, dtype = object)`
      - Direct method: `arr = [0]*5`
      
**2. How to access multi-dimensional array**
   - ans: `array[][]`
   - explanation:
      - first `[]`: the outer array (column)
      - second `[]`: the inside array (row)
     
**3. How to replace a specific value in a list**
   - ans: 
      - the easiest way is by using a `for` loop.
      - `[String].replace([oldValue], [newValue], [countLimit])`: returns a copy of the string where all occurrences of a substring is replaced with another substring.

**4. How to accept multiple inputs in just one line**
   - ans: by using `[String].split([separator], [maxSplit])` function
   - explanation: This functions splits a `String` into a `list`.

**5. About appending into an empty array**
   - ans: the `append` values(even another array) would directly insert into the original one(without creating a empty value).

**6. What is a `None` keyword?**
   - ans: used to define a `null` variable or an object.
   - explanation: It is an object in Python and a data type of the class `NoneType`.

**7. What is `int()` function?**
   - ans: converts the specified value into an `int` number.
   - explanation: It only accepts `String`, a `byte-like` object or a `num`(cannot accept an `array`).

**8. What is a `map()` function?**
   - ans: `map([function], [iterable])`
   - explanation: returns a map object(which is an iterator) of the results after applying the given function to each item of a given iterable(e.g. `list`, `tuple`, etc.) 

**9. How to  modify a `global` variable in a function?**
   - ans: Use a `global` keyword
   - explanation: This allows modification of the variable outside of the current scope.
      - All variables created inside a function is `local`.
      - All variables defined outside a function is `global`.
      - `global` keyword is used to read and write to a `global` variable(by declaring the global variable inside the function e.g. `global [variableNmae]`).
         - However, functions like `append` can go pass this restrictions.
      - Use of `global` keyword has no effects outside a function.
      

**10. How to convert all values inside a `list` into another data type?**
   - ans: `results = list(map(int, results))`

**11. About new-declared variables in a `for` loop**
   - ans: Cannot directly assign the preferred values to the new-declared variables
   - explanation:
   ```
   For example:
   list = [0, 1, 2, 3]
   for element in list:
    element = 5
   print(list)
   
   The ans is [0, 1, 2, 3]
   
   But if you add print(element) right after element = 5, you can get a bunch of 5.
   That means the assignment is towards the variable element and it is being replaced in every for loop happened.
   ```

**12. How to print on the same line in Python?**
   - ans: `print([Text], end=' ')`
   - explanation:
      - Every time `print` is called, a new separated line would automatically be drawn out.
      - As a result, `end=' '` is used to only separate every `print` with one spacing.

##2021.03.14
**13. About the properties of `if...in...` statement with multi-dimensional array**
   - ans: the statement can only detect one layer of the array
   - explanation: It would only detect every inner array as a whole.

**14. How to copy a list without linking both contents?**
   - ans: Use `[newArray] = [oldArray].copy()` function instead of `[newArray] = [oldArray]`.
   - explanation: `.copy` function returns a shallow copy of the list.

**15. How to turn a `list` into a `tuple`?**
   - ans:
      - Using `tuple([listName])` (Typecasting method)
      - Using `tuple(i for i in [listName])` (A small variation to the first one, but reasons are unknown)
      - Using `(*list, )`(Unpacks the list inside a tuple literal, Fastest approach but with worse readability)

##2021.03.15
**16. How to copy a multi-dimension array?**
   - ans: `[newArray] = copy.deepcopy([oldArray])`
   - explanation: 
      - Use normal methods like `[newArray] = [oldArray].copy()` would just equal to `=`.
         - Which the modification of the new array would also affects the original array.

**17. What is the `assert()` statement?**
   - ans: `assert [condition], [messageDisplay]`helps detect problems early in the program.
   - explanation:
      - `assert [condition]`: To test the `[condition]`, and immediately trigger an error if the condition is false.
      - `if not [condition]: raise AssertionError()`
      - Remember not to use parenthesis `()`, as it is a statement.

**18. How to count if all values in a `list` is the same or not?**
   - ans:
      - The simpliest method: `[listName].count([specificValues] == len([listName]))`
      - The `numpy` method: `np.equal([arrayOne], [arrayTwo].all())`
   - explanation:
   - 
