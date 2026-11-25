# ლექცია: პირობითი ოპერატორები

**კვირა 1 | ოთხშაბათი | 17:00–19:00 (2 სთ)**
**ლექციის ნაწილი: 1 სთ | პრაქტიკა: 1 სთ**

---

## 1. if / elif / else სინტაქსი (15 წთ)

### საკვანძო საკითხები

- `if` — პირობის შემოწმება: თუ True, კოდი შესრულდება
- `elif` — დამატებითი პირობა (რამდენიც გინდათ)
- `else` — ყველა სხვა შემთხვევა (არასავალდებულო)
- ინდენტაცია (4 სივრცე) = კოდის ბლოკი — Python-ში ფრჩხილების ნაცვლად
- ორწერტილი `:` ყოველი პირობის ბოლოს

### კოდის მაგალითები

**მარტივი if:**
```python
age = 20

if age >= 18:
    print("სრულწლოვანი ხართ")
```

**if / else:**
```python
temperature = 35

if temperature > 30:
    print("ცხელა, დალიეთ წყალი")
else:
    print("ნორმალური ტემპერატურაა")
```

**if / elif / else:**
```python
score = 75

if score >= 90:
    grade = "A"
elif score >= 80:
    grade = "B"
elif score >= 70:
    grade = "C"
elif score >= 60:
    grade = "D"
else:
    grade = "F"

print(f"შეფასება: {grade}")   # შეფასება: C
```

**input()-თან ერთად:**
```python
age = int(input("შეიყვანეთ ასაკი: "))

if age < 0:
    print("ასაკი არ შეიძლება იყოს უარყოფითი!")
elif age < 18:
    print("არასრულწლოვანი")
elif age < 65:
    print("სამუშაო ასაკი")
else:
    print("საპენსიო ასაკი")
```

### გავრცელებული შეცდომები

- ორწერტილის `:` დავიწყება `if`-ის ბოლოს → `SyntaxError`
- არასწორი ინდენტაცია → `IndentationError` (ძალიან ხშირი შეცდომა!)
- `=` ნაცვლად `==` → `if x = 5:` არის შეცდომა, სწორია `if x == 5:`
- `elif` ნაცვლად `else if` → Python-ში `else if` არ არსებობს
- `elif`-ების თანმიმდევრობა მნიშვნელოვანია — პირველი ჭეშმარიტი პირობა შესრულდება და დანარჩენი გამოტოვდება

### კავშირი მონაცემთა ანალიტიკასთან

- მონაცემების კატეგორიზაცია: ასაკის ჯგუფები, შეფასების სისტემები, რისკის დონეები
- მონაცემთა ვალიდაცია: შეყვანილი მნიშვნელობის შემოწმება სანამ დაამუშავებთ
- pandas-ში: `df["category"] = np.where(df["score"] > 50, "pass", "fail")`

> **გადასვლა:** მარტივი პირობები ვისწავლეთ — ახლა გავართულოთ: ჩადგმული და კომპლექსური პირობები.

---

## 2. ჩადგმული და კომპლექსური პირობები (15 წთ)

### საკვანძო საკითხები

- `and` — ორივე პირობა ერთდროულად ჭეშმარიტი უნდა იყოს
- `or` — ერთი მაინც ჭეშმარიტი
- `not` — პირობის უარყოფა
- ჩადგმული (nested) if — `if`-ის შიგნით `if`
- კომბინაციები ფრჩხილებით — სირთულის მართვა

### კოდის მაგალითები

**ლოგიკური ოპერატორები პირობებში:**
```python
age = 25
income = 3000

# and — ორივე პირობა
if age >= 21 and income >= 2000:
    print("სესხი დამტკიცებულია")

# or — ერთი მაინც
if age < 18 or age > 65:
    print("შეღავათიანი ტარიფი")

# not — უარყოფა
is_blocked = False
if not is_blocked:
    print("წვდომა ნებადართულია")
```

**კომპლექსური პირობა ფრჩხილებით:**
```python
age = 30
income = 4000
has_guarantee = True

if (age >= 21 and income >= 2000) or has_guarantee:
    print("სესხი დამტკიცებულია")
else:
    print("სესხი უარყოფილია")
```

**ჩადგმული if:**
```python
has_ticket = True
age = 15

if has_ticket:
    if age >= 18:
        print("შედით, სრული ფასით")
    elif age >= 7:
        print("შედით, შეღავათიანი ბილეთი")
    else:
        print("შედით, უფასო")
else:
    print("ბილეთი საჭიროა!")
```

**ჩადგმული if → გამარტივება and-ით:**
```python
# ჩადგმული (ნაკლებად წაკითხვადი):
if has_ticket:
    if age >= 18:
        print("შედით")

# გამარტივებული (უკეთესი):
if has_ticket and age >= 18:
    print("შედით")
```

**პრაქტიკული მაგალითი — ფასდაკლების გამოთვლა:**
```python
total = float(input("შეკვეთის თანხა: "))
is_member = input("ხართ წევრი? (yes/no): ").lower() == "yes"

if total >= 200 and is_member:
    discount = 0.20
    print("20% ფასდაკლება (წევრი + 200₾+)")
elif total >= 200 or is_member:
    discount = 0.10
    print("10% ფასდაკლება")
else:
    discount = 0.0
    print("ფასდაკლება არ არის")

final_price = total * (1 - discount)
print(f"საბოლოო ფასი: {final_price:.2f} ₾")
```

### გავრცელებული შეცდომები

- `and`/`or` პრიორიტეტის დავიწყება — `and` პირველი სრულდება: `True or False and False` = `True`
- ზედმეტი ჩადგმა — 3+ დონის ჩადგმული if წაუკითხავია, გამოიყენეთ `and`/`or`
- `not` არასწორ ადგილას — `not x == 5` vs `x != 5` (მეორე უკეთესია)

### კავშირი მონაცემთა ანალიტიკასთან

- მრავალკრიტერიუმიანი ფილტრაცია: `df[(df["age"] > 25) & (df["salary"] > 3000)]`
- pandas-ში `and`/`or`-ის ნაცვლად `&`/`|` გამოიყენება (ფრჩხილებით!)
- ბიზნეს-ლოგიკის იმპლემენტაცია: ფასდაკლების წესები, რისკის შეფასება

> **გადასვლა:** კომპლექსური პირობები გავიარეთ — ახლა ვნახოთ კომპაქტური ჩაწერის ფორმა და truthy/falsy.

---

## 3. ტერნარული გამოთქმა და Truthy/Falsy (10 წთ)

### საკვანძო საკითხები

- ტერნარული (ternary): `result = value_if_true if condition else value_if_false`
- ერთ ხაზში if/else — მარტივი შემთხვევებისთვის
- Truthy/Falsy: Python-ში ყველა მნიშვნელობას აქვს ლოგიკური "ჭეშმარიტება"
- Falsy მნიშვნელობები: `0`, `0.0`, `""`, `None`, `False`, `[]`, `{}`, `()`
- დანარჩენი ყველაფერი Truthy-ა

### კოდის მაგალითები

**ტერნარული გამოთქმა:**
```python
age = 20

# ჩვეულებრივი if/else:
if age >= 18:
    status = "სრულწლოვანი"
else:
    status = "არასრულწლოვანი"

# ტერნარული — იგივე ერთ ხაზში:
status = "სრულწლოვანი" if age >= 18 else "არასრულწლოვანი"
print(status)   # სრულწლოვანი
```

**ტერნარული პრაქტიკაში:**
```python
score = 85
result = "ჩაბარებულია" if score >= 51 else "ჩაიჭრა"
print(result)   # ჩაბარებულია

temperature = -5
message = "ყინავს" if temperature < 0 else "არ ყინავს"

price = 150
shipping = 0 if price >= 100 else 10
print(f"მიტანის საფასური: {shipping} ₾")  # 0 ₾
```

**Truthy/Falsy:**
```python
name = ""
if name:
    print(f"გამარჯობა, {name}")
else:
    print("სახელი არ არის შეყვანილი")
# → "სახელი არ არის შეყვანილი" (ცარიელი სტრინგი = Falsy)

user_input = input("შეიყვანეთ რამე: ")
if user_input:
    print(f"თქვენ შეიყვანეთ: {user_input}")
else:
    print("ცარიელი შეყვანა!")
```

**Falsy მნიშვნელობების დემონსტრაცია:**
```python
falsy_values = [0, 0.0, "", None, False]

for val in falsy_values:  # ციკლები ხვალ ვისწავლით
    if val:
        print(f"{val!r} → Truthy")
    else:
        print(f"{val!r} → Falsy")
# 0 → Falsy
# 0.0 → Falsy
# '' → Falsy
# None → Falsy
# False → Falsy
```

### გავრცელებული შეცდომები

- ტერნარულის გადამეტება — 2+ პირობის ჩადგმა წაუკითხავია: `a if x else b if y else c`
- `0` არის Falsy → `if count:` ნიშნავს "თუ count არ არის 0", არა "თუ count არსებობს"
- `""` (ცარიელი სტრინგი) და `" "` (სივრცე) განსხვავდება — სივრცე Truthy-ა!

### კავშირი მონაცემთა ანალიტიკასთან

- ტერნარული გამოთქმა pandas-ში: `df["label"] = df["value"].apply(lambda x: "high" if x > 100 else "low")`
- Truthy/Falsy ხშირია მონაცემთა ვალიდაციაში: "თუ ცარიელი არ არის, დაამუშავე"
- `None` და ცარიელი მნიშვნელობები — missing data-ს ფუნდამენტი

---

## 4. ცოცხალი კოდირება (20 წთ)

### დემო 1: კალკულატორი შეფასებით

```python
print("=== გამოცდის შედეგების ანალიზი ===\n")

student_name = input("სტუდენტის სახელი: ").strip().title()
score = int(input("ქულა (0-100): "))

# ვალიდაცია
if score < 0 or score > 100:
    print("შეცდომა: ქულა უნდა იყოს 0-დან 100-მდე!")
else:
    # შეფასება
    if score >= 91:
        grade = "A (ფრიადი)"
    elif score >= 81:
        grade = "B (კარგი)"
    elif score >= 71:
        grade = "C (საშუალო)"
    elif score >= 61:
        grade = "D (დამაკმაყოფილებელი)"
    else:
        grade = "F (ჩაიჭრა)"

    passed = "ჩაბარებულია" if score >= 51 else "ჩაიჭრა"
    high_achiever = score >= 91

    print(f"\n--- შედეგი ---")
    print(f"სტუდენტი: {student_name}")
    print(f"ქულა: {score}/100")
    print(f"შეფასება: {grade}")
    print(f"სტატუსი: {passed}")

    if high_achiever:
        print("🏆 წარჩინებული სტუდენტი!")
```

### დემო 2: ბილეთის ფასის გამოთვლა

```python
print("=== კინოს ბილეთის კალკულატორი ===\n")

age = int(input("ასაკი: "))
is_student = input("სტუდენტი ხართ? (yes/no): ").lower().strip() == "yes"
day = input("კვირის დღე (mon/tue/.../sun): ").lower().strip()

base_price = 15.0

# ასაკის ფასდაკლება
if age < 7:
    price = 0
    category = "ბავშვი (უფასო)"
elif age < 16:
    price = base_price * 0.5
    category = "მოზარდი (50%)"
elif age >= 65:
    price = base_price * 0.6
    category = "პენსიონერი (40%)"
else:
    price = base_price
    category = "სრული ფასი"

# სტუდენტის ფასდაკლება
if is_student and price > 0:
    price *= 0.8
    category += " + სტუდენტი (-20%)"

# კვირის შუა დღის ფასდაკლება
if day in ("mon", "tue", "wed") and price > 0:
    price *= 0.85
    category += " + სამუშაო დღე (-15%)"

print(f"\nკატეგორია: {category}")
print(f"ფასი: {price:.2f} ₾")
```

---

## შეჯამება

| თემა | რა ვისწავლეთ |
|------|-------------|
| if/elif/else | სინტაქსი, ინდენტაცია, ორწერტილი |
| ლოგიკური ოპერატორები | `and`, `or`, `not`, კომპლექსური პირობები |
| ჩადგმული if | როდის გამოვიყენოთ, როდის გავამარტივოთ |
| ტერნარული | `x = a if cond else b` |
| Truthy/Falsy | `0`, `""`, `None` = False; დანარჩენი = True |

**შემდეგი ლექცია (ხუთშაბათი):** while ციკლი, break/continue — განმეორებადი ოპერაციები.
