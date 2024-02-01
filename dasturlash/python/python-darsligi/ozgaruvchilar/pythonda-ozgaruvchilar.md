# Pythonda o'zgaruvchilar

### gO'zgaruvchilar

O'zgaruvchilar ma'lumot qiymatlarini saqlovchi kenteynerlardir.

### O'zgaruvchi yaratish

Pythonda o'zgaruvchini e'lon qiluvchi kalit so'z yo'q.&#x20;

O'zgaruvchi unga ilk qiymat bergan vaqtingizdayoq yaratiladi.

{% code title="Misol" %}
```python
x = 5
y = "John"
print(x)
print(y)
```
{% endcode %}

{% embed url="https://www.w3schools.com/python/trypython.asp?filename=demo_variables1" %}

O'zgaruvchilarni ma'lum bir turda e'lon qilish shart emas va ular e'lon qilinganidan keyin ham uning turini o'zgartirish mumkin.

```python
x = 4       # x ning ma'lumot turi int
x = "Sally" # x ning ma'lumot turi str
print(x)
```

{% embed url="https://www.w3schools.com/python/trypython.asp?filename=demo_variables2" %}

### Casting

Agar siz o'zgaruvchining ma'lumotlar turini belgilamoqchi bo'lsangiz, bu casting yordamida amalga oshirilishi mumkin.

```python
x = str(3)    # x ning qiymati '3'
y = int(3)    # y ning qiymati 3
z = float(3)  # z ning qiymati 3.0 
```

### O'zgaruvchi turini ko'rish

O'zgaruvchining ma'lumot turini `type()` funksiyasi orqali olishinigiz mumkin.

```python
x = 5
y = "John"
print(type(x))
print(type(y)) 
```

{% embed url="https://www.w3schools.com/python/trypython.asp?filename=demo_variables_type" %}

{% hint style="warning" %}
<mark style="color:green;">Ma'lumot turlari</mark> va casting haqida ushbu qo'llanmada o'rganasiz.
{% endhint %}

### Birtirnoq yoki qo'shtirnoq ?

String o'zgaruvchilari bir yoki qo'shtirnoq yordamida e'lon qilinadi:

```python
x = "John"
# bular bir xil
x = 'John'
```

{% embed url="https://www.w3schools.com/python/trypython.asp?filename=demo_variables7" %}

### Case-Sensitive

O'zgaruvchi nomlari katta kichik harfligiga qarab farq qiladi.

{% code title="Bu 2ta o'zgaruvchi yaratadi" %}
```
a = 4
A = "Sally"
#A kichik a ning o'rniga qayta yozilmaydi
```
{% endcode %}

{% embed url="https://www.w3schools.com/python/trypython.asp?filename=demo_variables_cs" %}
