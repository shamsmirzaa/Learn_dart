
# Null Safety:

**Null safety** in Dart — it's one of Dart’s superpowers to **avoid errors** in your apps.

## 🧠 What is "null"?

In programming, `null` means **"nothing"** or **"no value yet"**.

Example:

```dart
String name = null; // ❌ This causes an error if null safety is on
```

Dart wants to protect you from using **"nothing"** where **"something"** is expected.

## 🛡️ What is Null Safety?

**Null safety** means:

- Dart **won’t let you use null accidentally**.
- You must tell Dart **if a variable is allowed to be null**.

### **Example:**

Imagine a **box** that holds something — like a toy.

Now, imagine someone asks you: *“What’s inside the box?”*

And you say: *“Nothing.”*

That “nothing” is like `null` in Dart.

But what if you **open the box expecting a toy**, and **there’s nothing**? You might get upset, or things might break — like your app!

Null safety is Dart's way of saying:

> “Don’t try to open a box unless you’re sure there’s something inside!”
> 

A **null dereference error** occurs when you try to **access a method or property** on a variable that is null. In Dart, **null safety** helps avoid such errors by making sure you **can’t use a variable** that might be null unless you explicitly check it or handle it safely (e.g. using ?,!, or default values).

## 🔑 3 Key Things You Must Know

---

### 1. Nullable vs Non-Nullable Variables

### 🟢 Non-nullable (default):

```dart
String name = "Shams"; // Must always have something (not null)
```

> You can't leave this empty.
> 

---

### 🔵 Nullable (add `?` to allow null):

```dart
String? name = null; // This is okay
```

> This means: “I might keep it empty, and that’s okay.”
> 

---

### 2. Variables Must Be Initialized

Dart **forces you to assign a value** to a variable **before using it**, especially if it’s **non-nullable**.

```dart
int age; // ❌ Error: Not initialized

int age = 20; // ✅ OK
```

But nullable ones are **automatically `null`**, so they are fine:

```dart
int? age; // ✅ OK, it's null by default
```

---

### 3. You Can’t Use Nullable Variables Directly

If Dart **thinks your variable might be empty**, you can’t use it like it has a value.

### ❌ Wrong:

```dart
String? name = null;
print(name.length); // ❌ Error! What if name is null?
```

### ✅ Right:

```dart
String? name = null;
print(name?.length); // ✅ Safe. It prints null if name is null
```

Or use a fallback value:

```dart
print(name ?? "No Name"); // ✅ "No Name" if name is null
```

---

## 📌 Bonus Tools Dart Gives You

| Tool | What it does | Example |
| --- | --- | --- |
| `?` | Nullable type | `String? name;` |
| `!` | I know it's not null! | `print(name!)` |
| `??` | Default if null | `name ?? "Guest"` |
| `??=` | Assign if null | `name ??= "Guest"` |
| `?.` | Call if not null | `name?.length` |

# Late variables

## 🐢 What is a `late` variable?

Normally in Dart, if a variable **must have a value** (not nullable), Dart asks you to give it **right away**:

```dart
int age = 5; // ✅ Dart is happy
int age;      // ❌ Error! Not given value yet
```

But sometimes, you **want to give the value later** — just not **too late!**

That’s where `late` comes in! 🎉

---

## 🎁 Think Like a Gift Box

Imagine you say:

> “I promise I’ll put a toy in this box before opening it, just not right now.”
> 

That’s what `late` means:

> “I will give you the value later — before I use it!”
> 

---

### ✅ Example:

```dart
late String name;

void main() {
  name = "Shams"; // Assigning value later
  print("My name is $name");
}
```

- 🧠 Dart says: “Okay! I trust you’ll give it before using.”
- ✅ You **assigned before printing** → All good!

---

### ❌ Wrong Way:

```dart
late String name;

void main() {
  print(name); // ❌ You didn't assign yet!
}
```

- ❗ This will crash — because you said “late”, but never actually gave the value before using.

---

## ⚠️ When to Use `late`?

Use `late` when:

1. You **can’t give a value at the start**, but
2. You **promise to assign it before using**.

This is useful when:

- You need to fetch some data first (like from a database or API)
- You initialize something **inside** a function or constructor
