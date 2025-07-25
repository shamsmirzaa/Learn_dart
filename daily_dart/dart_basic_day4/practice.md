### 🔥 **Basic Questions**

1. ❓ What will the following code print?
    
    ```dart
    print("She said: \"Hello!\"");
    ```
    
2. ❓ How do you write a new line in a normal Dart string?
3. ❓ What does the `r` in `r"Hello\nWorld"` mean?
4. ❓ What's the difference between these two lines?
    
    ```dart
    print("C:\\Program Files\\App");
    print(r"C:\Program Files\App");
    ```
    
5. ❓ Which one is correct to print this **exact output**?
    
    ```
    Path: C:\Users\Shams\Documents
    ```
    
    a) `print("C:\Users\Shams\Documents");`
    
    b) `print("C:\\Users\\Shams\\Documents");`
    
    c) `print(r"C:\Users\Shams\Documents");`
    

---

### 🧠 **Intermediate**

1. ❓ What does this print?
    
    ```dart
    print("Line1\nLine2\tTabbed");
    ```
    
2. ❓ How would you print:
    
    ```
    $100 is not enough!
    ```
    
    a) `print("$100 is not enough!");`
    
    b) `print("\$100 is not enough!");`
    
    c) `print(r"$100 is not enough!");`
    
3. ❓ Will this code compile and run correctly?
    
    ```dart
    print(r"This is a \"quote\"");
    ```
    

---

### 🚀 **Code Debugging**

1. ❓ What’s wrong with this code?
    
    ```dart
    print("He said: "I love Dart"");
    ```
    
    ✅ Fix it using **escaping** or **raw strings**.
    

---

### 🧪 **True or False**

1. ❓ True or False:
    
    A raw string interprets escape characters like `\n` and `\t`.
    
2. ❓ True or False:
    
    You must escape backslashes in a raw string.


   # **Answer**
   ### 🔥 **Basic Questions**

1. ✅ `She said: "Hello!"`
2. ✅ Use `\n` for a new line:
    
    ```dart
    
    print("Line1\nLine2");
    ```
    
3. ✅ `r` makes it a **raw string**, so escape characters like `\n` are not processed.
4. ✅ First one prints with double backslashes, second one prints as-is:
    - `"C:\\Program Files\\App"` → `C:\Program Files\App`
    - `r"C:\Program Files\App"` → `C:\Program Files\App`
5. ✅ **c)** `print(r"C:\Users\Shams\Documents");`

---

### 🧠 **Intermediate**

1. ✅
    
    ```
    Line1
    Line2	Tabbed
    ```
    
2. ✅ **b)** `print("\$100 is not enough!");`
    
    (**OR**) **c)** `print(r"$100 is not enough!");`
    
    (Both give the same output.)
    
3. ✅ Yes, it compiles and prints:
    
    ```
    This is a \"quote\"
    ```
    

---

### 🚀 **Code Debugging**

1. ❌ Wrong:
    
    ```dart
    print("He said: "I love Dart""); // ❌ Error
    ```
    
    ✅ Fix:
    
    - Using escape characters:
        
        ```dart
        print("He said: \"I love Dart\"");
        ```
        
    - OR using raw string and escaping not needed:
        
        ```dart
        print(r'He said: "I love Dart"');
        ```
        

---

### 🧪 **True or False**

1. ❌ **False** – Raw strings **do not** interpret escape characters.
2. ✅ **False** – In raw strings, you **do not need** to escape backslashes.
