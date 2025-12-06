# Lexical Analyzer in C Using Flex

This project implements a simple lexical analyzer using **Flex**.  
It reads an input file (`input.txt`), tokenizes the content, and classifies tokens into:

- Keywords  
- Identifiers  
- Numbers (int & float)  
- Operators  
- Unknown tokens  

A summary of token counts is displayed after processing.

---

## 📂 Files Included
- **lexical.l** — Flex source code for the lexical analyzer  
- **input.txt** — (Create your own or add sample input)  
- **README.md** — Documentation for the project  

---

## ▶️ How to Run

### **1. Install Flex**
Linux:
```bash
sudo apt install flex
```

Mac (Homebrew):
```bash
brew install flex
```

---

### **2. Generate the Lexer**
Run:
```bash
flex lexical.l
```

This produces `lex.yy.c`.

---

### **3. Compile**
```bash
gcc lex.yy.c -o lexer
```

---

### **4. Run the Program**
Make sure you have an `input.txt` file in the same directory.

```bash
./lexer
```

---

## 📘 Sample Input (input.txt)
```
int x = 10;
float y = 20.5;
if (x < y) x = x + 1;
```

---

## 📊 Sample Output
```
Keyword: int
Identifier: x
Operator: =
Number: 10
...
===== TOKEN SUMMARY =====
Total Tokens     : 18
Keywords         : 2
Identifiers      : 5
Operators        : 6
Numbers          : 3
```

---

## 📝 Notes
- Floats must include a dot (`3.14`), or they will be counted as integers.
- Identifiers must start with a letter.
- Only basic operators are supported: `= + - * / %`

---

## 👤 Author
Created as part of a compiler design lab assignment.

