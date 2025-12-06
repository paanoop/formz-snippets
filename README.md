# 📦 Formz Snippets  
### Clean & Complete Formz Input Generators for Flutter

A curated set of **ready-to-use Formz input snippets** designed for Flutter & BLoC developers.  
This extension eliminates boilerplate and helps you create **strongly-typed, reusable, scalable input models** for Formz (0.8.0+).

---

## 🚀 Features

- 15+ production-ready Formz input templates  
- Consistent naming and structure  
- Strongly typed validation logic  
- Supports **String, Int, Double, Email, Mobile, Date, Enum, JSON, Regex, OTP**, and more  
- Highly reusable patterns for BLoC + Formz apps  
- All snippets follow **FormzInput<T, ErrorType>** pattern  
- Written to avoid constructor issues in newer Formz versions  

---

## 🧠 Why This Extension?

Formz is powerful — but writing input classes repeatedly is not.  
This extension provides **everything you need**, instantly:

- Cleaner forms  
- Cleaner states  
- Cleaner Cubits/BLoCs  
- Cleaner validators  
- Zero repeating boilerplate  

If you use BLoC + Formz, this extension saves **hours**.

---

## ⌨️ Snippet Prefixes

| Prefix | Description |
|--------|-------------|
| `formzInputString` | String input with basic validation |
| `formzInputNullable` | Nullable string input |
| `formzInputInt` | Integer input |
| `formzInputDouble` | Double input |
| `formzInputEmail` | Email validator (regex) |
| `formzInputPassword` | Password with length rules |
| `formzInputMobile` | Indian mobile validator |
| `formzInputEnum` | Enum-based Formz input |
| `formzInputDate` | DateTime input |
| `formzInputOptional` | Optional-but-validated string |
| `formzInputRegex` | Custom regex validator |
| `formzInputPhoneCC` | Mobile with country code |
| `formzInputUsername` | Username rules |
| `formzInputOtp` | OTP input (4–6 digits) |
| `formzInputUrl` | URL validator |
| `formzInputJson` | JSON validation input |

---

## 📝 Example Output (String Input)

Typing:

```
formzInputString → TAB
```

Produces:

```dart
enum NameValidationError { invalid }

class NameInput extends FormzInput<String, NameValidationError> {
  const NameInput.pure() : super.pure('');
  const NameInput.dirty([String value = '']) : super.dirty(value);

  @override
  NameValidationError? validator(String value) {
    if (value.isEmpty) return NameValidationError.invalid;
    return null;
  }
}
```

100% Formz-correct.  
100% BLoC-compatible.

---

## 📥 Installation

1. Open VS Code  
2. Go to **Extensions → Search: “Formz Snippets”**  
3. Install  
4. Start typing a snippet like:  
   ```
   formzInputEmail
   ```  
5. Press **TAB**

Done. 🎉

---

## 🎬 Demo

![Formz Snippets Demo](media/demo.gif)


---

## 🛠️ Requirements

- Flutter  
- Dart  
- Formz 0.8.0+  
- VS Code

---

## 🐛 Issues / Feature Requests

Have ideas or found something to improve?

👉 https://github.com/paanoop/formz-snippets/issues

Contributions welcome.

---

## ❤️ Author

**Anoop P. A**  
Publisher: `paanoop`  
Passionate about Flutter, clean architecture, and developer tooling.

---

## 📄 License

MIT — free to use in commercial and open-source projects.
