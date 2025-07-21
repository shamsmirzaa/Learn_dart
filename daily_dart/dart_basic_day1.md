- Dart is case sensitive language.

# Void:

You have a **robot friend** 🤖.

You can give it commands like:

- **Say Hello**
- **Clap hands**
- **Dance**

Now... sometimes your robot just **does things** — but it **doesn’t give anything back** to you.

### 👶 That’s what `void` means in Dart:

> It means: "Do something, but don’t give me anything back."
> 

# Main:

## What is `main()` in Dart?

> main() is the entry point — the first thing Dart runs when your app or script starts.
> 

Just like a story starts on page 1, your Dart program **starts from `main()`**.

## 🧾 Syntax of `main()`

```dart
void main() {
  // your code here
}
```

- `void` → means main doesn’t return anything.
- `main` → is the special name Dart looks for.
- `()` → means it’s a function.
- `{}` → holds the code that runs.

## 🛠️ What Can You Put in `main()`?

Almost **anything!** Like:

- Print something
- Call other functions
- Do calculations
- Create variables
- Start your app logic

# Variables:

# what is a variable

In programming, a variable is like a container or a storage location that holds a value. You give this container a name, and you can put different types of data into it, such as numbers, text, or even more complex structures.

## 🧠 Imagine This:

You have a **magic box 🧰** where you can **store anything** — your toys, candies, or even your name!

That **magic box** is called a **variable** in Dart.

| Type | Use for... | Example |
| --- | --- | --- |

| `int` | Whole numbers | `int age = 20;` |
| --- | --- | --- |

| `double` | Decimal numbers | `double temp = 36.6;` |
| --- | --- | --- |

| `String` | Text | `String name = "Shams";` |
| --- | --- | --- |

| `bool` | True/False | `bool isOn = true;` |
| --- | --- | --- |

| `var` | Let Dart decide the type | `var x = "hello";` |
| --- | --- | --- |

| `dynamic` | Can change type any time | `dynamic x = 10; x = "Hi";` |
| --- | --- | --- |

| `final` | Fixed after assignment (runtime) | `final city = "Mumbai";` |
| --- | --- | --- |

| `const` | Fixed and known at compile time | `const pi = 3.14;` |
| --- | --- | --- |

```dart
void main(){
  String name = 'shams';
  int age =34;
  double height=43.5;
  bool likesDart=false;
  print(name);
  print(age);
  print(height);
  print(likesDart);
}
```

## To run dart in vs code

```markdown
//to allow dart to read from the terminal you should use
import 'dart:io';

//to run dart file in the terminal
dart run filename.dart
```

## To build an simple calculator

we have to use stdin.readLineSync(); to read the user inputs.

```dart
import 'dart:io';

void main() {
  print("Enter first number:");
  int a = int.parse(stdin.readLineSync()!);

  print("Enter second number:");
  int b = int.parse(stdin.readLineSync()!);

  print("Enter operation (+, -, *, /):");
  String? op = stdin.readLineSync();

  if (op == "+") {
    print("Result: ${a + b}");
  } else if (op == "-") {
    print("Result: ${a - b}");
  } else if (op == "*") {
    print("Result: ${a * b}");
  } else if (op == "/") {
    print("Result: ${a / b}");
  } else {
    print("Invalid operation");
  }

```

`stdin.readLineSync()` **always returns a `String?`** (nullable `String`).

So if you want to get an **int** from user input, you must convert it manually using:

```dart
num = int.parse(stdin.readLineSync()!);
```

### 🧠 Here's what's happening:

1. `stdin.readLineSync()` → reads input as a `String?` (can be `null`)
2. `!` → tells Dart “don’t worry, it’s not null” (null check)
3. `int.parse(...)` → converts that string (like `"42"`) to an integer (`42`)

## Var and dynamic

### What is a Var?

Imagine you have a **box**. You can put **toys**, **books**, or **candy** in it.

- If you put a **toy**, the box becomes a *toy box*.
- If you put a **book**, it becomes a *book box*.

This "box" is what we call a **variable** in programming.

## `var` – The Smart Box 🧠📦

`var` is like a **smart box**.

- If you first put a **number** in it, Dart remembers: “Okay! This is a number box now.”
- You **cannot** put anything else later.

### ✨ Example:

```dart
void main() {
  var name = "Shams"; // Dart says: This is a String box!
  print(name);

  // name = 123; ❌ Error! You can’t change it to a number.
}
```

## `dynamic` – The Magic Box 🎩📦

`dynamic` is a **magic box**. You can change what's inside whenever you want!

- It can hold a string now,
- a number later,
- a list later again — all okay.

### ✨ Example:

```dart
void main() {
  dynamic item = "Book";
  print(item);  // Book

  item = 42;
  print(item);  // 42

  item = true;
  print(item);  // true
}
```

## ⚖️ `var` vs `dynamic` – Key Differences

| Feature | `var` | `dynamic` |
| --- | --- | --- |
| Type Inference | Yes (fixed after first use) | No (can change anytime) |
| Type Safety | Yes | No (less safe) |
| Error if type changed | ✅ Yes | ❌ No |
| Performance | Faster | Slightly slower |
| Use When | You know the type | You don’t know the type |

## Final and Const

### What are `final` and `const`?

Both are used to create variables **that cannot be changed** once they are set.

Imagine you **write something with a permanent marker** — you can’t erase or change it. That’s what `final` and `const` do in Dart!

### `final` – "Set Once, Use Forever"

- You can **set the value only once**, but **at runtime** (when the program is running).
- After that, it cannot be changed.

### ✅ Example:

```dart
void main() {
  final city = "Mumbai";
  print(city);

  // city = "Delhi"; ❌ Error: Can't change final variable
}
```

### ✅ Also works with calculated values:

```dart
void main() {
  final currentTime = DateTime.now(); // allowed
  print(currentTime);
}
```

### `const` – "Forever Frozen"

- **Compile-time constant**: Dart needs to know its value **before the app runs**.
- Value must be **known and fixed**.

### ✅ Example:

```dart
void main() {
  const pi = 3.14159;
  const name = "Shams";

  print(pi);
  print(name);
}
```

### ❌ NOT allowed:

```dart
void main() {
  const timeNow = DateTime.now(); // ❌ Error: not a constant value
}
```

## ✅ Summary Table

| Feature | `final` | `const` |
| --- | --- | --- |
| Set Once | ✅ Yes | ✅ Yes |
| Known at Compile | ❌ No | ✅ Yes |
| Runtime Calculation | ✅ Allowed | ❌ Not allowed |
| Example | `final age = 25;` | `const pi = 3.14;` |
| Common Use | Dates, API keys, configs | Math values, UI fixed sizes |

---

## 🧠 Rule of Thumb:

- Use **`const`** when the value **never changes** and is known in advance.
- Use **`final`** when the value **doesn't change**, but you get it **at runtime**.

---

## The Core Differences

| Keyword | Can Change Value? | Must Know Value at Compile Time? | Use When... |
| --- | --- | --- | --- |
| `var` | ✅ Yes | ❌ No | You want a normal variable |
| `final` | ❌ No | ❌ No | You want a variable that doesn’t change (runtime allowed) |
| `const` | ❌ No | ✅ Yes | You want a forever fixed value known before app runs |

---

## 🧸 Imagine This:

- `var` is a **box** you can open and **change what’s inside anytime**.
- `final` is a **sealed box**: once you put something in, you **can’t change it**, but you can **decide later** what goes in.
- `const` is a **frozen box**: it must be filled **before the game even starts**, and you **can’t change it — ever**.

---

## 🔍 Let’s See in Code:

```dart
void main() {
  var name = "Shams";
  name = "Mirza"; // ✅ Allowed

  final city = "Mumbai";
  // city = "Delhi"; ❌ Not allowed — final can't change

  const country = "India";
  // country = "USA"; ❌ Not allowed — const can't change

  final today = DateTime.now(); // ✅ OK — allowed in final
  // const now = DateTime.now(); ❌ Error — const needs known values
}
```

---

## 🧠 Deep Comparison

| Feature | `var` | `final` | `const` |
| --- | --- | --- | --- |
| Can assign again? | ✅ Yes | ❌ No | ❌ No |
| Known at compile time? | ❌ Not needed | ❌ Not needed | ✅ Required |
| Value calculated later? | ✅ Yes | ✅ Yes | ❌ No |
| Good for...? | Normal variables | Values that don’t change | Fixed constants (e.g., pi) |
| Example | `var x = 5;` | `final name = "Ali";` | `const pi = 3.14;` |

---

## ✅ Final Advice

- Use `var` → when value can **change** later.
- Use `final` → when value will **never change**, but is decided **during program**.
- Use `const` → when value is **completely fixed** and known **before app starts**.
