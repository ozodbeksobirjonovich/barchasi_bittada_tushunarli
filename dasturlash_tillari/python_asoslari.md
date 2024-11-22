## 1. Asosiy Tushunchalar

### O'zgaruvchilar
```python
ism = "Alisher"    # str (matn)
yosh = 25        # int (butun son) 
boyi = 1.75      # float (o'nlik son)
student = True   # bool (mantiqiy)
```

### Ma'lumot Turlari
- **Oddiy turlar:** str, int, float, bool
- **Konteyner turlar:** list, tuple, dict, set
- **None** - bo'sh qiymat

### Arifmetik Amallar
```python
a = 10
b = 3

print(a + b)    # 13 (qo'shish)
print(a - b)    # 7 (ayirish)
print(a * b)    # 30 (ko'paytirish) 
print(a / b)    # 3.333... (bo'lish)
print(a // b)   # 3 (butun bo'lish)
print(a % b)    # 1 (qoldiq)
print(a ** b)   # 1000 (daraja)
```

## 2. Kolleksiyalar

### Ro'yxatlar (List)
```python
mevalar = ["olma", "anor", "uzum"]
mevalar.append("nok")           # qo'shish
mevalar.remove("anor")          # o'chirish
print(mevalar[0])               # birinchi element
print(mevalar[-1])              # oxirgi element
print(mevalar[1:3])             # kesish (slice)
```

### Lug'atlar (Dictionary)
```python
talaba = {
    "ism": "Anvar",
    "yosh": 20,
    "fakultet": "AT"
}
print(talaba["ism"])            # qiymatni olish
talaba["kurs"] = 2              # yangi kalit-qiymat
del talaba["yosh"]              # o'chirish
```

### To'plamlar (Set)
```python
sonlar = {1, 2, 3, 4, 5}
sonlar.add(6)                   # element qo'shish
sonlar.remove(1)                # element o'chirish
```

## 3. Shartli Operatorlar

### if/elif/else
```python
yosh = 18

if yosh < 7:
    print("Maktabgacha")
elif yosh < 18:
    print("Maktab o'quvchisi")
else:
    print("Katta yoshli")
```

### Mantiqiy operatorlar
- `and` - VA
- `or` - YOKI
- `not` - EMAS

## 4. Tsikllar

### for tsikli
```python
# Ro'yxat bo'ylab
for meva in mevalar:
    print(meva)

# Range bilan
for i in range(5):    # 0 dan 4 gacha
    print(i)
```

### while tsikli
```python
i = 0
while i < 5:
    print(i)
    i += 1
```

## 5. Funksiyalar

### Oddiy funksiya
```python
def salomlash(ism):
    return f"Salom, {ism}!"

natija = salomlash("Anvar")
```

### Parametrli funksiyalar
```python
def yigindi(a, b=0):           # default qiymatli
    return a + b

print(yigindi(10))             # 10
print(yigindi(10, 5))          # 15
```

### Lambda funksiyalar
```python
kvadrat = lambda x: x ** 2
print(kvadrat(4))              # 16
```

## 6. OOP (Obyektga Yo'naltirilgan Dasturlash)

### Klass yaratish
```python
class Talaba:
    def __init__(self, ism, yosh):
        self.ism = ism
        self.yosh = yosh
    
    def tanishtiruv(self):
        return f"Men {self.ism}, {self.yosh} yoshdaman"

talaba1 = Talaba("Anvar", 20)
print(talaba1.tanishtiruv())
```

### Vorislik
```python
class Aspirant(Talaba):
    def __init__(self, ism, yosh, mavzu):
        super().__init__(ism, yosh)
        self.mavzu = mavzu
```

## 7. Xatolarni Boshqarish

```python
try:
    son = int(input("Son kiriting: "))
    print(10/son)
except ValueError:
    print("Bu son emas!")
except ZeroDivisionError:
    print("Nolga bo'lib bo'lmaydi!")
finally:
    print("Dastur tugadi")
```

## 8. Fayllar bilan Ishlash

### O'qish
```python
with open("fayl.txt", "r") as fayl:
    matn = fayl.read()
```

### Yozish
```python
with open("fayl.txt", "w") as fayl:
    fayl.write("Yangi ma'lumot")
```

## 9. Muhim Modullar

### math - matematik funksiyalar
```python
import math

print(math.sqrt(16))    # 4.0 (ildiz)
print(math.pi)          # 3.141592...
```

### datetime - sana va vaqt
```python
from datetime import datetime

hozir = datetime.now()
print(hozir.strftime("%d.%m.%Y"))
```

### random - tasodifiy sonlar
```python
import random

print(random.randint(1, 10))  # 1-10 orasida
```

## 10. Foydali Metodlar

### Ro'yxatlar uchun
- `sort()` - saralash
- `reverse()` - teskari aylantirish
- `index()` - indeksni topish
- `count()` - elementlar sonini hisoblash

### Satrlar uchun
- `upper()` - katta harflarga
- `lower()` - kichik harflarga
- `split()` - bo'laklarga ajratish
- `join()` - birlashtirish
- `strip()` - bo'sh joylarni olib tashlash

## 11. List Comprehension

```python
# Oddiy usul
kvadratlar = []
for x in range(10):
    kvadratlar.append(x**2)

# List comprehension
kvadratlar = [x**2 for x in range(10)]

# Shartli list comprehension
juft_sonlar = [x for x in range(10) if x % 2 == 0]
```
