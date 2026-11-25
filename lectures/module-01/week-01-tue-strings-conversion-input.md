# ლექცია: სტრინგები, ტიპის კონვერტაცია და input()

**კვირა 1 | სამშაბათი | 18:00–21:00 (3 სთ)**
**ლექციის ნაწილი: 1.5 სთ | პრაქტიკა: 1.5 სთ**

---

## 1. სტრინგის ოპერაციები (25 წთ)

### საკვანძო საკითხები

- სტრინგი = სიმბოლოების მიმდევრობა, ბრჭყალებში (`"..."` ან `'...'`)
- ინდექსირება: `s[0]` — პირველი სიმბოლო, `s[-1]` — ბოლო
- სლაისინგი: `s[start:stop:step]` — ქვესტრინგის ამოჭრა
- შეერთება (concatenation): `+`, გამრავლება: `*`
- სიგრძე: `len()`, შემოწმება: `in`
- სტრინგები immutable-ია (შეუცვლელი) — ვერ შეცვლით ცალკეულ სიმბოლოს

### კოდის მაგალითები

**სტრინგის შექმნა და ინდექსირება:**
```python
city = "Tbilisi"

print(city[0])      # T    — პირველი სიმბოლო (ინდექსი 0-დან იწყება!)
print(city[1])      # b
print(city[-1])     # i    — ბოლო სიმბოლო
print(city[-2])     # s    — ბოლოდან მეორე
print(len(city))    # 7    — სიგრძე
```

**სლაისინგი:**
```python
text = "Data Analytics"

print(text[0:4])      # "Data"       — 0-დან 4-მდე (4 არ შედის!)
print(text[5:])       # "Analytics"  — 5-დან ბოლომდე
print(text[:4])       # "Data"       — დასაწყისიდან 4-მდე
print(text[::2])      # "Dt nltc"    — ყოველი მეორე სიმბოლო
print(text[::-1])     # "scitylanA ataD" — უკუღმა
```

**შეერთება და გამრავლება:**
```python
first_name = "თათია"
last_name = "გაბუნია"
full_name = first_name + " " + last_name
print(full_name)    # "თათია გაბუნია"

separator = "-" * 30
print(separator)    # "------------------------------"
```

**`in` ოპერატორი:**
```python
email = "user@example.com"
print("@" in email)         # True
print("gmail" in email)     # False
print("example" not in email)  # False
```

### გავრცელებული შეცდომები

- ინდექსი 0-დან იწყება, არა 1-დან → `"hello"[1]` არის `"e"`, არა `"h"`
- `IndexError` — ინდექსი სტრინგის სიგრძეს სცილდება: `"abc"[5]`
- სტრინგი + რიცხვი → `TypeError`: `"age: " + 25` არ მუშაობს (საჭიროა `str(25)`)
- სლაისინგში `stop` ინდექსი არ შედის: `"hello"[0:3]` = `"hel"`, არა `"hell"`

### კავშირი მონაცემთა ანალიტიკასთან

- მონაცემთა ბაზებში ტექსტური სვეტების დამუშავება (სახელები, მისამართები, ელ-ფოსტები)
- სლაისინგი ხშირია: თარიღის, კოდის, ID-ის ნაწილის ამოჭრა
- `in` ოპერატორი — ტექსტში ძიება, ფილტრაცია

> **გადასვლა:** ვიცით სტრინგის სტრუქტურა — ახლა ვნახოთ ჩაშენებული მეთოდები.

---

## 2. სტრინგის მეთოდები (20 წთ)

### საკვანძო საკითხები

- მეთოდი = ფუნქცია, რომელიც ეკუთვნის ობიექტს: `object.method()`
- მეთოდი არ ცვლის ორიგინალს — აბრუნებს ახალ სტრინგს (immutable!)
- რეგისტრი: `upper()`, `lower()`, `title()`, `capitalize()`
- ძიება: `find()`, `count()`, `startswith()`, `endswith()`
- ტრანსფორმაცია: `strip()`, `replace()`, `split()`, `join()`

### კოდის მაგალითები

**რეგისტრის ცვლილება:**
```python
name = "  taTia Gabunia  "

print(name.upper())       # "  TATIA GABUNIA  "
print(name.lower())       # "  tatia gabunia  "
print(name.title())       # "  Tatia Gabunia  "
print(name.strip())       # "taTia Gabunia"      — ზედმეტი სივრცეების წაშლა
print(name.strip().title())  # "Tatia Gabunia"   — მეთოდების ჯაჭვი (chaining)
```

**ძიება და დათვლა:**
```python
sentence = "Python is great and Python is free"

print(sentence.find("Python"))      # 0  — პირველი ნაპოვნის ინდექსი
print(sentence.find("Java"))        # -1 — ვერ იპოვა
print(sentence.count("Python"))     # 2  — რამდენჯერ გვხვდება
print(sentence.startswith("Python")) # True
print(sentence.endswith("free"))     # True
```

**ჩანაცვლება:**
```python
phone = "555-12-34-56"
print(phone.replace("-", " "))    # "555 12 34 56"
print(phone.replace("-", ""))     # "555123456"
```

**გაყოფა და გაერთიანება:**
```python
csv_line = "თბილისი,ბათუმი,ქუთაისი,რუსთავი"
cities = csv_line.split(",")
print(cities)       # ['თბილისი', 'ბათუმი', 'ქუთაისი', 'რუსთავი']
print(len(cities))  # 4

# join — split-ის საპირისპირო
result = " | ".join(cities)
print(result)       # "თბილისი | ბათუმი | ქუთაისი | რუსთავი"
```

**split() სხვადასხვა სეპარატორით:**
```python
text = "სახელი:გვარი:ასაკი"
parts = text.split(":")
print(parts)   # ['სახელი', 'გვარი', 'ასაკი']

words = "  hello   world  ".split()   # პარამეტრის გარეშე — ნებისმიერი whitespace
print(words)   # ['hello', 'world']
```

### გავრცელებული შეცდომები

- `name.upper()` არ ცვლის `name`-ს → შედეგი უნდა შეინახოთ: `name = name.upper()`
- `find()` აბრუნებს `-1`-ს (არა შეცდომას) თუ ვერ იპოვა → ყოველთვის შეამოწმეთ
- `split()` პარამეტრის გარეშე vs `split(" ")` — პირველი ჭრის ნებისმიერ whitespace-ს

### კავშირი მონაცემთა ანალიტიკასთან

- `strip()` — მონაცემების გაწმენდა (data cleaning) ყოველთვის იწყება ზედმეტი სივრცეების მოშორებით
- `split()` / `join()` — CSV ფორმატის ხელით დამუშავება, ტექსტის ანალიზი
- `replace()` — მონაცემთა ნორმალიზაცია (ფორმატის გათანაბრება)
- მეთოდების ჯაჭვი (chaining) — pandas-შიც ზუსტად ასე ვმუშაობთ: `df.dropna().reset_index()`

> **გადასვლა:** ტექსტის დამუშავება ვისწავლეთ — ახლა ვნახოთ როგორ ჩავსვათ ცვლადები ტექსტში.

---

## 3. f-strings და ფორმატირება (15 წთ)

### საკვანძო საკითხები

- f-string: `f"ტექსტი {ცვლადი}"` — ყველაზე მოსახერხებელი გზა Python 3.6+
- `.format()` მეთოდი — ძველი, მაგრამ გხვდება კოდში
- Escape სიმბოლოები: `\n`, `\t`, `\\`
- მრავალხაზოვანი სტრინგი: `"""..."""`

### კოდის მაგალითები

**f-string — ძირითადი:**
```python
name = "ანა"
age = 23
print(f"სახელი: {name}, ასაკი: {age}")
# სახელი: ანა, ასაკი: 23
```

**f-string — გამოთვლები ბრჭყალებში:**
```python
price = 49.99
quantity = 3
print(f"ჯამი: {price * quantity} ლარი")
# ჯამი: 149.97 ლარი

print(f"{'Python':>20}")    # მარჯვნივ სწორება 20 სიმბოლოში
print(f"{'Python':<20}")    # მარცხნივ სწორება
print(f"{'Python':^20}")    # ცენტრში
```

**რიცხვების ფორმატირება:**
```python
pi = 3.14159265
print(f"Pi = {pi:.2f}")        # Pi = 3.14      — 2 ათწილადი
print(f"Pi = {pi:.4f}")        # Pi = 3.1416    — 4 ათწილადი

big_number = 1500000
print(f"ბიუჯეტი: {big_number:,} ₾")    # ბიუჯეტი: 1,500,000 ₾
print(f"ბიუჯეტი: {big_number:_} ₾")    # ბიუჯეტი: 1_500_000 ₾

percentage = 0.8567
print(f"წარმატება: {percentage:.1%}")    # წარმატება: 85.7%
```

**`.format()` მეთოდი:**
```python
template = "სახელი: {}, ასაკი: {}"
print(template.format("ლუკა", 25))
# სახელი: ლუკა, ასაკი: 25
```

**Escape სიმბოლოები და მრავალხაზოვანი სტრინგი:**
```python
print("პირველი ხაზი\nმეორე ხაზი")
print("სახელი\tასაკი\tქალაქი")
print("ფაილის გზა: C:\\Users\\data")

report = """
=== ანგარიში ===
სახელი: ანა
ასაკი: 23
ქალაქი: თბილისი
"""
print(report)
```

### გავრცელებული შეცდომები

- f-string-ში `f` პრეფიქსის დავიწყება → `"name: {name}"` დაბეჭდავს ტექსტს `{name}`, არა მნიშვნელობას
- ბრჭყალების კონფლიქტი → `f"He said "hi""` — გამოიყენეთ `f'He said "hi"'`
- `\n` არ მუშაობს `r"..."` (raw string) ში

### კავშირი მონაცემთა ანალიტიკასთან

- ანგარიშების ფორმატირება: რიცხვების ლამაზი ჩვენება (ათწილადები, მძიმეები, პროცენტები)
- f-string ფორმატირება იგივეა pandas-ში: `df.style.format("{:.2f}")`
- მონაცემთა ვიზუალიზაციაში ღერძების ლეიბლები ხშირად f-string-ით ფორმატდება

> **გადასვლა:** ვიცით ტექსტის ფორმატირება — ახლა ვისწავლოთ ტიპების გარდაქმნა და მომხმარებლისგან მონაცემების მიღება.

---

## 4. ტიპის კონვერტაცია და input() (15 წთ)

### საკვანძო საკითხები

- `int()`, `float()`, `str()`, `bool()` — ტიპის გარდაქმნა (casting)
- `input()` ყოველთვის აბრუნებს `str`-ს — თუ რიცხვი გჭირდებათ, გარდაქმენით
- `ValueError` — თუ კონვერტაცია შეუძლებელია
- `bool()` — რა არის truthy და falsy

### კოდის მაგალითები

**ძირითადი კონვერტაციები:**
```python
# str → int
age_str = "25"
age = int(age_str)
print(age + 5)       # 30

# str → float
price_str = "49.99"
price = float(price_str)
print(price * 2)     # 99.98

# int → str
count = 42
message = "შედეგი: " + str(count)
print(message)       # შედეგი: 42

# float → int (წილადი ნაწილი იკარგება!)
pi = 3.99
print(int(pi))       # 3 (არა 4! არ ამრგვალებს, წყვეტს)
```

**bool() — truthy/falsy:**
```python
print(bool(0))       # False
print(bool(42))      # True  — ნებისმიერი არანულოვანი რიცხვი

print(bool(""))      # False — ცარიელი სტრინგი
print(bool("hello")) # True  — არაცარიელი სტრინგი

print(bool(None))    # False
print(bool([]))      # False — ცარიელი სია (შემდეგ კვირას)
```

**input() — მომხმარებლის შეყვანა:**
```python
name = input("შეიყვანეთ სახელი: ")
print(f"გამარჯობა, {name}!")

# input() ყოველთვის str-ს აბრუნებს!
age_str = input("შეიყვანეთ ასაკი: ")
print(type(age_str))    # <class 'str'>

# რიცხვისთვის — გარდაქმენით
age = int(input("შეიყვანეთ ასაკი: "))
print(f"მომავალ წელს იქნებით {age + 1} წლის")
```

**კონვერტაციის შეცდომები:**
```python
# ეს ვერ იმუშავებს:
# int("hello")       # ValueError
# int("3.14")        # ValueError (პირველად float!)
# float("abc")       # ValueError

# სწორი გზა float → int:
value = int(float("3.14"))    # 3
```

### გავრცელებული შეცდომები

- `input()` შედეგზე არითმეტიკის შესრულება კონვერტაციის გარეშე → `"5" + "3"` = `"53"`, არა `8`
- `int("3.14")` → `ValueError` — პირველად `float()`, შემდეგ `int()`
- `int()` არ ამრგვალებს — `int(3.99)` = `3`, არა `4`
- `input()` prompt-ის ბოლოს სივრცის დავიწყება → `input("სახელი:")` ნაცვლად `input("სახელი: ")`

### კავშირი მონაცემთა ანალიტიკასთან

- CSV ფაილიდან წაკითხული მონაცემები ხშირად ტექსტურია — კონვერტაცია აუცილებელია
- pandas ავტომატურად ცდილობს ტიპების ამოცნობას, მაგრამ ხშირად ხელით გარდაქმნა სჭირდება: `df["price"].astype(float)`
- `bool()` ლოგიკა pandas-ის ფილტრაციის საფუძველია

> **გადასვლა:** ყველაფერი გავაერთიანოთ ერთ პროგრამაში.

---

## 5. ცოცხალი კოდირება — ყველაფრის ერთად (15 წთ)

### დემო: მარტივი მონაცემთა შეგროვება და ანალიზი

```python
# === მომხმარებლისგან მონაცემების შეგროვება ===
name = input("სახელი: ").strip().title()
city = input("ქალაქი: ").strip().title()
age = int(input("ასაკი: "))
salary = float(input("ხელფასი (ლარი): "))

# === მონაცემების დამუშავება ===
email_prefix = name.lower().replace(" ", ".")
birth_year = 2026 - age
annual_salary = salary * 12
tax = annual_salary * 0.20
net_annual = annual_salary - tax

# === ფორმატირებული ანგარიში ===
print("\n" + "=" * 40)
print(f"{'პროფილი':^40}")
print("=" * 40)
print(f"სახელი:        {name}")
print(f"ქალაქი:        {city}")
print(f"ასაკი:          {age} (დაბადების წელი: {birth_year})")
print(f"ელ-ფოსტა:      {email_prefix}@example.com")
print(f"თვიური ხელფასი: {salary:,.2f} ₾")
print(f"წლიური ხელფასი: {annual_salary:,.2f} ₾")
print(f"გადასახადი:     {tax:,.2f} ₾ (20%)")
print(f"წმინდა შემოსავალი: {net_annual:,.2f} ₾")
print("=" * 40)
```

### დამატებითი დემო: ტექსტის ანალიზი

```python
text = input("შეიყვანეთ წინადადება: ")

word_count = len(text.split())
char_count = len(text)
char_no_spaces = len(text.replace(" ", ""))

print(f"\nსიტყვების რაოდენობა: {word_count}")
print(f"სიმბოლოების რაოდენობა: {char_count}")
print(f"სიმბოლოები (სივრცეების გარეშე): {char_no_spaces}")
print(f"პირველი სიტყვა: {text.split()[0]}")
print(f"ბოლო სიტყვა: {text.split()[-1]}")
print(f"დიდი ასოებით: {text.upper()}")
```

---

## შეჯამება

| თემა | რა ვისწავლეთ |
|------|-------------|
| სტრინგის ოპერაციები | ინდექსირება, სლაისინგი, `len()`, `in` |
| მეთოდები | `upper()`, `lower()`, `strip()`, `split()`, `join()`, `replace()`, `find()` |
| ფორმატირება | f-strings, `:.2f`, `:,`, `:.1%` |
| კონვერტაცია | `int()`, `float()`, `str()`, `bool()`, truthy/falsy |
| input() | ყოველთვის `str` → გარდაქმნა საჭიროებისამებრ |

**შემდეგი ლექცია (ოთხშაბათი):** პირობითი ოპერატორები — `if/elif/else`, ლოგიკური პირობები, ტერნარული გამოთქმა.
