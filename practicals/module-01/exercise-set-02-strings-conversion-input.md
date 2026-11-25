# სავარჯიშო ნაკრები 02 — სტრიქონები, ტიპის კონვერტაცია და input()

## ინსტრუქცია
- ამოხსენით ამოცანები რიგითობის მიხედვით
- 🟢 = მარტივი, 🟡 = საშუალო, 🔴 = რთული
- ამოხსნები ჩაწერეთ `.py` ფაილში
- გაუშვით ფაილი შედეგის შესამოწმებლად

---

## 🟢 მარტივი

### ამოცანა 1: სტრიქონის სიგრძე

მოცემულია ცვლადი:
```python
city = "Tbilisi"
```

დაბეჭდეთ ქალაქის სახელი და მისი სიგრძე (ასოების რაოდენობა).

**მოსალოდნელი შედეგი:**
```
Tbilisi
7
```

---

### ამოცანა 2: დიდი და პატარა ასოები

მოცემულია:
```python
product = "iPhone 15 Pro Max"
```

დაბეჭდეთ პროდუქტის სახელი:
1. მთლიანად დიდი ასოებით
2. მთლიანად პატარა ასოებით
3. სათაურის ფორმატით (title case)

**მოსალოდნელი შედეგი:**
```
IPHONE 15 PRO MAX
iphone 15 pro max
Iphone 15 Pro Max
```

---

### ამოცანა 3: სტრიქონების გაერთიანება

მოცემულია:
```python
first_name = "Nino"
last_name = "Beridze"
```

გააერთიანეთ სახელი და გვარი ერთ ცვლადში `full_name` და დაბეჭდეთ.

**მოსალოდნელი შედეგი:**
```
Nino Beridze
```

---

### ამოცანა 4: სტრიქონის ამოჭრა (Slicing)

მოცემულია:
```python
phone = "+995-555-12-34-56"
```

ამოჭერით და დაბეჭდეთ:
1. ქვეყნის კოდი (პირველი 4 სიმბოლო)
2. ბოლო 8 სიმბოლო

**მოსალოდნელი შედეგი:**
```
+995
12-34-56
```

---

### ამოცანა 5: სტრიქონის გამეორება

მოცემულია:
```python
pattern = "=-"
```

დაბეჭდეთ ეს პატერნი 20-ჯერ გამეორებული, რათა მიიღოთ ვიზუალური გამყოფი ხაზი.

**მოსალოდნელი შედეგი:**
```
=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-
```

---

## 🟡 საშუალო

### ამოცანა 6: ელფოსტის ნაწილები

მოცემულია:
```python
email = "giorgi.melia@example.com"
```

ამოიღეთ და დაბეჭდეთ:
1. მომხმარებლის სახელი (`@`-მდე ნაწილი) — გამოიყენეთ `find()` და slicing
2. დომენი (`@`-ის შემდეგ ნაწილი)

**მოსალოდნელი შედეგი:**
```
მომხმარებელი: giorgi.melia
დომენი: example.com
```

---

### ამოცანა 7: ბინძური მონაცემების გაწმენდა

მოცემულია სტუდენტის მიერ შეყვანილი მონაცემი:
```python
user_input = "   tBiLiSi   "
```

გაასუფთავეთ: წაშალეთ ზედმეტი ცარიელი ადგილები და გადაიყვანეთ სწორ ფორმატში (title case). დაბეჭდეთ შედეგი.

**მოსალოდნელი შედეგი:**
```
Tbilisi
```

---

### ამოცანა 8: f-string ფორმატირება

მოცემულია:
```python
product = "ლეპტოპი"
price = 2499.9
quantity = 3
```

დაბეჭდეთ f-string-ით ფორმატირებული ანგარიში. ფასი უნდა იყოს 2 ათწილადის სიზუსტით.

**მოსალოდნელი შედეგი:**
```
პროდუქტი: ლეპტოპი
ფასი: 2499.90 ლარი
რაოდენობა: 3
სულ: 7499.70 ლარი
```

---

### ამოცანა 9: ტიპის კონვერტაცია

მოცემულია სტრიქონის სახით შენახული მონაცემები:
```python
price_str = "49.99"
quantity_str = "12"
discount_str = "True"
```

გარდაქმენით შესაბამის ტიპებში (`float`, `int`, `bool`) და გამოთვალეთ ჯამური ფასი. თუ `discount` არის `True`, გამოაკელით 10%.

**მოსალოდნელი შედეგი:**
```
ჯამი ფასდაკლებით: 539.89
```

---

### ამოცანა 10: input() და გათვლა

დაწერეთ პროგრამა, რომელიც:
1. ჰკითხავს მომხმარებელს სახელს
2. ჰკითხავს დაბადების წელს
3. გამოთვლის ამჟამინდელ ასაკს (2026 წელი)
4. დაბეჭდავს მისალმებას ასაკით

**მაგალითი:**
```
შეიყვანეთ სახელი: Luka
შეიყვანეთ დაბადების წელი: 2000
გამარჯობა, Luka! შენ ხარ 26 წლის.
```

---

## 🔴 რთული

### ამოცანა 11: სტრუქტურირებული მონაცემის გარჩევა

მოცემულია სტრიქონი:
```python
data = "Name: Mariam, Age: 28, City: Kutaisi"
```

ამოიღეთ და ცალ-ცალკე დაბეჭდეთ სახელი, ასაკი და ქალაქი. გამოიყენეთ `split()` და slicing.

**მოსალოდნელი შედეგი:**
```
სახელი: Mariam
ასაკი: 28
ქალაქი: Kutaisi
```

---

### ამოცანა 12: სიტყვების შებრუნება

მოცემულია წინადადება:
```python
sentence = "Python is great for data analytics"
```

შეაბრუნეთ სიტყვების რიგი (ბოლო სიტყვა — პირველი, პირველი — ბოლო). გამოიყენეთ `split()` და slicing.

**მოსალოდნელი შედეგი:**
```
analytics data for great is Python
```

---

### ამოცანა 13: სიმბოლოების დათვლა

მოცემულია:
```python
text = "Data Analytics with Python Programming"
```

დაითვალეთ და დაბეჭდეთ:
1. სიმბოლოების რაოდენობა (ცარიელი ადგილების გარეშე)
2. სიტყვების რაოდენობა
3. რამდენჯერ გვხვდება ასო "a" (დიდი და პატარა ჯამში)

**მოსალოდნელი შედეგი:**
```
სიმბოლოები (ცარიელის გარეშე): 34
სიტყვები: 5
ასო 'a'-ს რაოდენობა: 5
```

---

### ამოცანა 14: პაროლის შემოწმება (ძირითადი)

მოცემულია:
```python
password = "MyPass123"
```

შეამოწმეთ და დაბეჭდეთ:
1. სიგრძე 8-ზე მეტია? (`len()`)
2. შეიცავს ციფრს? (გამოიყენეთ `any()` არ არის საჭირო — შეგიძლიათ `isdigit()` ცალკეულ სიმბოლოზე, ან `password` != `password` ბოლო კიდევ)
3. შეიცავს დიდ ასოს? (`.isupper()` ცალკეულ სიმბოლოზე, ან `password != password.lower()`)
4. შეიცავს პატარა ასოს?

**მინიშნება:** ციფრის შემოწმებისთვის: `password != password.replace("0","").replace("1","")...` ძალიან გრძელია. ამ ეტაპზე შეამოწმეთ ისე, რომ: თუ `password.lower() != password` → შეიცავს დიდ ასოს; თუ `password.upper() != password` → შეიცავს პატარა ასოს; ციფრისთვის: `not password.isalpha()` (თუ მხოლოდ ასოები და ციფრებია).

**მოსალოდნელი შედეგი:**
```
სიგრძე >= 8: True
შეიცავს ციფრს: True
შეიცავს დიდ ასოს: True
შეიცავს პატარა ასოს: True
```

---

### ამოცანა 15: ანგარიშ-ფაქტურის გენერატორი

`input()`-ის გამოყენებით მოითხოვეთ:
1. კლიენტის სახელი
2. პროდუქტის სახელი
3. ფასი (ტექსტი → float)
4. რაოდენობა (ტექსტი → int)

დაბეჭდეთ ლამაზად ფორმატირებული ანგარიშ-ფაქტურა გამყოფი ხაზებით, დღგ-ით (18%) და ჯამით.

**მაგალითი:**
```
კლიენტის სახელი: Dato Lomidze
პროდუქტი: მონიტორი
ფასი: 899.99
რაოდენობა: 2

====================================
        ანგარიშ-ფაქტურა
====================================
კლიენტი: Dato Lomidze
პროდუქტი: მონიტორი
ფასი: 899.99 ლარი
რაოდენობა: 2
------------------------------------
ქვეჯამი: 1799.98 ლარი
დღგ (18%): 324.00 ლარი
სულ გადასახდელი: 2123.98 ლარი
====================================
```

---

## ამოხსნები

<details>
<summary>🟢 ამოცანა 1</summary>

```python
city = "Tbilisi"
print(city)
print(len(city))
```
</details>

<details>
<summary>🟢 ამოცანა 2</summary>

```python
product = "iPhone 15 Pro Max"
print(product.upper())
print(product.lower())
print(product.title())
```
</details>

<details>
<summary>🟢 ამოცანა 3</summary>

```python
first_name = "Nino"
last_name = "Beridze"
full_name = first_name + " " + last_name
print(full_name)
```
</details>

<details>
<summary>🟢 ამოცანა 4</summary>

```python
phone = "+995-555-12-34-56"
print(phone[:4])
print(phone[-8:])
```
</details>

<details>
<summary>🟢 ამოცანა 5</summary>

```python
pattern = "=-"
print(pattern * 20)
```
</details>

<details>
<summary>🟡 ამოცანა 6</summary>

```python
email = "giorgi.melia@example.com"
at_index = email.find("@")
username = email[:at_index]
domain = email[at_index + 1:]

print(f"მომხმარებელი: {username}")
print(f"დომენი: {domain}")
```
</details>

<details>
<summary>🟡 ამოცანა 7</summary>

```python
user_input = "   tBiLiSi   "
cleaned = user_input.strip().title()
print(cleaned)
```
</details>

<details>
<summary>🟡 ამოცანა 8</summary>

```python
product = "ლეპტოპი"
price = 2499.9
quantity = 3

print(f"პროდუქტი: {product}")
print(f"ფასი: {price:.2f} ლარი")
print(f"რაოდენობა: {quantity}")
print(f"სულ: {price * quantity:.2f} ლარი")
```
</details>

<details>
<summary>🟡 ამოცანა 9</summary>

```python
price_str = "49.99"
quantity_str = "12"
discount_str = "True"

price = float(price_str)
quantity = int(quantity_str)
discount = discount_str == "True"

total = price * quantity
if discount:
    total = total * 0.9

print(f"ჯამი ფასდაკლებით: {round(total, 2)}")
```
</details>

<details>
<summary>🟡 ამოცანა 10</summary>

```python
name = input("შეიყვანეთ სახელი: ")
birth_year = input("შეიყვანეთ დაბადების წელი: ")
age = 2026 - int(birth_year)
print(f"გამარჯობა, {name}! შენ ხარ {age} წლის.")
```
</details>

<details>
<summary>🔴 ამოცანა 11</summary>

```python
data = "Name: Mariam, Age: 28, City: Kutaisi"
parts = data.split(", ")

name = parts[0].split(": ")[1]
age = parts[1].split(": ")[1]
city = parts[2].split(": ")[1]

print(f"სახელი: {name}")
print(f"ასაკი: {age}")
print(f"ქალაქი: {city}")
```
</details>

<details>
<summary>🔴 ამოცანა 12</summary>

```python
sentence = "Python is great for data analytics"
words = sentence.split()
reversed_words = words[::-1]
result = " ".join(reversed_words)
print(result)
```
</details>

<details>
<summary>🔴 ამოცანა 13</summary>

```python
text = "Data Analytics with Python Programming"

char_count = len(text.replace(" ", ""))
word_count = len(text.split())
a_count = text.lower().count("a")

print(f"სიმბოლოები (ცარიელის გარეშე): {char_count}")
print(f"სიტყვები: {word_count}")
print(f"ასო 'a'-ს რაოდენობა: {a_count}")
```
</details>

<details>
<summary>🔴 ამოცანა 14</summary>

```python
password = "MyPass123"

has_length = len(password) >= 8
has_digit = not password.isalpha()
has_upper = password != password.lower()
has_lower = password != password.upper()

print(f"სიგრძე >= 8: {has_length}")
print(f"შეიცავს ციფრს: {has_digit}")
print(f"შეიცავს დიდ ასოს: {has_upper}")
print(f"შეიცავს პატარა ასოს: {has_lower}")
```
</details>

<details>
<summary>🔴 ამოცანა 15</summary>

```python
client = input("კლიენტის სახელი: ")
product = input("პროდუქტი: ")
price = float(input("ფასი: "))
quantity = int(input("რაოდენობა: "))

subtotal = price * quantity
vat = subtotal * 0.18
total = subtotal + vat

print()
print("=" * 36)
print("        ანგარიშ-ფაქტურა")
print("=" * 36)
print(f"კლიენტი: {client}")
print(f"პროდუქტი: {product}")
print(f"ფასი: {price:.2f} ლარი")
print(f"რაოდენობა: {quantity}")
print("-" * 36)
print(f"ქვეჯამი: {subtotal:.2f} ლარი")
print(f"დღგ (18%): {vat:.2f} ლარი")
print(f"სულ გადასახდელი: {total:.2f} ლარი")
print("=" * 36)
```
</details>
