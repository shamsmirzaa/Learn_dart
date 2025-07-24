# **String Concatenation**

> 👉 Joining strings manually using the + operator.
> 

### ✅ Example:

```dart
void main() {
  String firstName = "Shams";
  String lastName = "Mirza";

  String fullName = firstName + " " + lastName;
  print(fullName); // Output: Shams Mirza
}
```

### 🧒 Like a 5-year-old:

> You're gluing two words together like LEGO blocks using +.
> 

### 💡 Pros:

- Easy for very small joins.

### ⚠️ Cons:

- Can get messy with many variables or long strings.

### **String Interpolation**

> 👉 Embedding variables directly inside a string using $ or ${}.
> 

### ✅ Example:

```dart
void main() {
  String name = "Shams";
  int age = 25;

  print("My name is $name and I am $age years old.");
  // Output: My name is Shams and I am 25 years old.

  print("Next year, I’ll be ${age + 1} years old!");
}
```

### 🧒 Like a 5-year-old:

> It’s like magic! You just say the variable name inside the sentence and Dart fills it in.
> 

---

### 🧠 When to use `${}` instead of `$`?

- Use `${}` when you need to do **expressions** (math, functions):
    
    ```dart
    "${age + 5}"
    ```
    
- Just use `$` for simple variable values:
    
    ```dart
    "$name"
    ```
    

### 🧾 Summary Table:

| Feature | Concatenation | Interpolation |
| --- | --- | --- |
| **Syntax** | `str1 + str2` | `"Hello $name"` or `"Age: ${age + 1}"` |
| **Code clarity** | ❌ Messy with many variables | ✅ Clean and readable |
| **Supports logic** | ❌ No expressions directly | ✅ Supports expressions |
| **Preferred?** | ❌ Less recommended | ✅ Modern, recommended way |

---

### 🚀 Pro Tip:

> ✅ Always prefer string interpolation in Dart. It's cleaner, safer, and more readable!
>
