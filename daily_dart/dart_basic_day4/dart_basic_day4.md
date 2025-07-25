# String Escaping

## 🔐 What is **String Escaping**?

> Escaping is how we tell Dart:
> 
> 
> *“Hey! I want to include a special character in my string — don’t treat it like code!”*
> 

Think of it like **telling a secret** in a special way so Dart understands.

---

## 🧠 When do we need to escape?

You need to escape **special characters** like:

| Character | Why it’s special | Escape like this |
| --- | --- | --- |
| `"` | Ends a string | `\"` |
| `'` | Ends a string (if single-quoted) | `\'` |
| `\` | Escape character itself | `\\` |
| `\n` | New line (not escape, but used a lot) | - |
| `\t` | Tab space | - |
| `$` | Used in interpolation | `\$` |

---

## ✅ Examples:

### 1. **Quotes inside strings**

```dart
void main() {
  print("She said, \"Hello!\"");
  print('It\'s a beautiful day!');
}
```

🧒 Like this:

> “Put quote marks inside a quote by using a backslash first.”
> 

---

### 2. **Backslash `\`**

```dart
void main() {
  print("C:\\Users\\shams");
}
```

🧒 Backslashes are used to **escape**…

So to **write a real backslash**, we need **two** of them: `\\`

---

### 3. **Dollar Sign `$` inside a string**

```dart
void main() {
  print("This item costs \$10");
}
```

🧒 Dart thinks `$` means interpolation.

Use `\$` if you **don’t want to show a variable**, just the symbol.

---

### 4. **New Line and Tab**

```dart
void main() {
  print("Hello\nWorld");  // \n = new line
  print("Name:\tShams");  // \t = tab
}
```

# Raw String

## 🧪 What is a **Raw String**?

> A raw string treats everything literally — even escape characters like \n, \t, \\, etc.
> 

You create a raw string by adding a lowercase **`r`** **before the opening quote**.

---

### 🧸 Regular String:

```dart
void main() {
  print("Hello\nWorld");
}
```

➡️ Output:

```
Hello
World
```

---

### 🪵 Raw String:

```dart
void main() {
  print(r"Hello\nWorld");
}
```

➡️ Output:

```
Hello\nWorld
```

🧒 See? The `\n` **doesn't make a new line** in raw string. It just **prints as it is**.

---

## ✅ Why use raw strings?

- For **file paths** (like in Windows)
- For **regular expressions** (regex)
- When you don’t want to escape every `\`

---

### 📁 Example with file paths:

```dart
void main() {
  print("C:\\Users\\shams\\Documents");     // normal way
  print(r"C:\Users\shams\Documents");       // raw string way ✅ easier!
}
```
