# O'zgaruvchi qiymatini chiqarish

Pythonning <mark style="color:red;">`print()`</mark> funskiyasidan o'zgaruvchilarning qiymatini chiqarishda tez tez foydalaniladi.

```python
x = "Python is awesome"
print(x)
```

{% embed url="https://www.w3schools.com/python/trypython.asp?filename=demo_variables_print" %}

`print()` funksiyasida bir qancha o'zgaruvchilarni vergul bilan ajratib ham ularning qiymatini chiqarishingiz mumkin.

```python
x = "Python"
y = "is"
z = "awesome"
print(x, y, z)
```

{% embed url="https://www.w3schools.com/python/trypython.asp?filename=demo_variables3" %}

Bir nechta o'zgaruvchilarni + operatoridan foydalanib ham ekranga chiqara olasiz.

```python
x = "Python "
y = "is "
z = "awesome"
print(x + y + z)
```

{% embed url="https://www.w3schools.com/python/trypython.asp?filename=demo_variables4" %}

{% hint style="warning" %}
"Python" va "is" dan keyin bo'sh joy tashlanganiga e'tibor bering, ularsiz natija "Pythonisawesome" bo'ladi.
{% endhint %}

Raqamlar uchun, `+` operatori matematik amal bajaradi:

```python
x = 5
y = 10
print(x + y)
```

{% embed url="https://www.w3schools.com/python/trypython.asp?filename=demo_variables5" %}

`print()` funksiyasida string yoki raqamni `+` operatori bilan birga ishlatmoqchi bo'lsangiz, Python sizga xatolik qaytaradi:

{% hint style="danger" %}
### Misol

<pre class="language-python"><code class="lang-python"><strong>x = 5
</strong><strong>y = "John"
</strong><strong>print(x + y)
</strong></code></pre>
{% endhint %}

{% embed url="https://www.w3schools.com/python/trypython.asp?filename=demo_variables_test" %}

`print()` funksiyasida, bir nechta o'zgaruvchilarning qiymatini chiqarishning eng yaxshi yo'li ularni vergul bilan ajratishdir, ular hatto turli xil ma'lumotlar turlarini qo'llab-quvvatlaydi:

```python
x = 5
y = "John"
print(x, y)
```

{% embed url="https://www.w3schools.com/python/trypython.asp?filename=demo_variables_comma" %}
