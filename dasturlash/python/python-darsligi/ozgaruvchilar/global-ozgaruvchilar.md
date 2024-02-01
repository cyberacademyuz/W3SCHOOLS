# Global o'zgaruvchilar

Funksiyadan tashqarida yaratilgan o'zgaruvchilar (yuqoridagi barcha misollarda bo'lgani kabi) global o'zgaruvchilar deb ataladi.

Global o'zgaruvchilar funksiyalar ichida ham, tashqarisida ham hamma tomonidan foydalanishi mumkin.

{% code title="Funksiya tashqarisida o'zgaruvchi yaratish va undan funksiya ichida foydalanish:" %}
```python
x = "awesome"

def myfunc():
  print("Python is " + x)

myfunc()
```
{% endcode %}

{% embed url="https://www.w3schools.com/python/trypython.asp?filename=demo_variables_global" %}

Agar funksiya ichida ham global o'zgaruvchi nomi bir xil nomdagi o‘zgaruvchi yaratsangiz, bu o‘zgaruvchi local o'zgaruvchi bo‘ladi va u faqat funksiya ichida ishlatilishi mumkin. Xuddi shu nomdagi global o'zgaruvchi avvalgidek, global bo'lib qoladi va qiymatini yo'qoymaydi.

{% code title="Funksiya ichida global o'zgaruvchi nomi bilan bir xil bo'lgan o'zgaruvchi yaratish:" %}
```python
x = "awesome"

def myfunc():
  x = "fantastic"
  print("Python is " + x)

myfunc()

print("Python is " + x) 
```
{% endcode %}

{% embed url="https://www.w3schools.com/python/trypython.asp?filename=demo_variables_global2" %}

### Global kalit so'zi

Odatda, funksiya ichida o'zgaruvchi yaratganingizda, bu o'zgaruvchi local holatda bo'ladi, va faqatgina funksiya ichida ishlatilishi mumkin.

Funksiya ichida global o'zgaruvchi yaratish uchun, `global` kalit so'zidan foydalanishingiz mumkin.

{% code title="Agar siz global kalit so'zdan foydalansangiz, o'zgaruvchi global qamrovga tegishli bo'ladi:" %}
```python
def myfunc():
  global x
  x = "fantastic"

myfunc()

print("Python is " + x)
```
{% endcode %}

{% embed url="https://www.w3schools.com/python/trypython.asp?filename=demo_variables_global3" %}

Bundan tashqari, global o'zgaruvchi qiymayini funksiya ichida o'zgartirmoqchi bo'lsangiz, `global` kalit so'zdan foydalaning.

{% code title="Global o'zgaruvchini funksiya ichida o'zgartirish uchun, o'zgaruvchiga global kalit so'zi orqali murojaat qilish:" %}
```python
x = "awesome"

def myfunc():
  global x
  x = "fantastic"

myfunc()

print("Python is " + x) 
```
{% endcode %}

{% embed url="https://www.w3schools.com/python/trypython.asp?filename=demo_variables_global4" %}
