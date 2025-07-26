# Type Conversion

## 🧠 Why Type Conversion?

Sometimes you have:

- a **string that looks like a number** (`"42"`)
- or a **number that you want to show as text** (`42` → `"42"`)

So you need to **convert between them**!

---

## ✅ 1. **String → int**

```dart
String numberAsString = "42";
int number = int.parse(numberAsString);
print(number); // Output: 42
```

### ⚠️ Caution:

If the string is not a valid number, it will crash.

```dart
String s = "hello";
int n = int.parse(s); // ❌ Error!
```

✅ Use `tryParse()` for safety:

```dart
String s = "hello";
int? n = int.tryParse(s);
print(n); // Output: nul
```

---

## ✅ 2. **String → double**

```dart
String piAsString = "3.14";
double pi = double.parse(piAsString);
print(pi); // Output: 3.1
```

---

## ✅ 3. **int → String**

```dart
int age = 25;
String ageText = age.toString();
print(ageText); // Output: "25"
```

---

## ✅ 4. **double → String**

```dart
double price = 99.99;
String priceText = price.toString();
print(priceText); // Output: "99.99"
```

---

## ✅ 5. **double → int** (removes decimal part)

```dart
double pi = 3.14;
int wholePi = pi.toInt();
print(wholePi); // Output: 3
```

---

## ✅ 6. **int → double**

```dart
int x = 5;
double y = x.toDouble();
print(y); // Output: 5.0
```

---

