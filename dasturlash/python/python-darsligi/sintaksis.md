# Sintaksis

### Python sintaksisi

Oldingi sahifada o'rganganimizdek, Python kodini terminalga to'g'ridan-to'g'ri yozish orqali bajarilishi mumkin:

```bash
>>> print("Hello, World!")
Hello, World!
```

Yoki serverda .py kengaytmali fayl yaratib uni terminalda ishga tushirish mumkin.

```
C:\Users\Your Name>python myfile.py
```

### Python indentatsiyasi

Indentatsiya kod qatorining boshidagi bo'sh joy hisoblanadi.

Boshqa dasturlash tillarida koddagi indentatsiya faqat kodni osonroq o'qish uchun bo'lsa, Python-da indentatsiya juda muhim.

Python kod blokini ko'rsatish uchun indentatsiyadan foydalanadi.

```python
if 5 > 2:
  print("Five is greater than two!") 
```

Agar indentatsiya qoldirmasangiz Python xatolik qaytaradi:

{% hint style="danger" %}
**Misol:**

Sintaksis xatolik:

<pre class="language-python"><code class="lang-python"><strong>if 5 > 2:
</strong><strong>print("Five is greater than two!") 
</strong></code></pre>
{% endhint %}

{% embed url="https://www.w3schools.com/python/trypython.asp?filename=demo_indentation_test" %}

```python
if 5 > 2:
 print("Five is greater than two!") 
if 5 > 2:
        print("Five is greater than two!") 
```

{% embed url="https://www.w3schools.com/python/trypython.asp?filename=demo_indentation2" %}

Siz bir kod blokida bir xil miqdordagi bo'sh joydan foydalanishingiz kerak, aks holda Python sizga xato beradi:

{% hint style="danger" %}
**Misol:**

Sintaksis xatolik:

<pre class="language-python"><code class="lang-python"><strong>if 5 > 2:
</strong><strong> print("Five is greater than two!")
</strong><strong>        print("Five is greater than two!")  
</strong></code></pre>
{% endhint %}

{% embed url="https://www.w3schools.com/python/trypython.asp?filename=demo_indentation_test" %}

### Python o'zgaruvchilari

Pythonda o'zgaruvchilar unga qiymat berganingizda yaratiladi:

{% hint style="info" %}
**Misol:**

Pythonda o'zgaruvchilar:

<pre class="language-python"><code class="lang-python"><strong>x = 5
</strong><strong>y = "Hello, World!"
</strong></code></pre>
{% endhint %}

{% embed url="https://www.w3schools.com/python/trypython.asp?filename=demo_syntax_variables" %}

Pythonda o'zgaruvchini e'lon qilish buyrug'i yo'q.

<mark style="color:green;">**Python o'zgaruvchilari**</mark> bo'limida o'zgaruvchilar haqida ko'proq bilib olasiz.

### Izohlar

Python kodlarni izohga ola oladi.

Izohlar **#** bilan boshlanadi va Python qatorning qolgan qismini izoh sifatida ko'rsatadi:

{% hint style="info" %}
**Misol:**\
Pythonda izohlar:

<pre class="language-python"><code class="lang-python"><strong>#This is a comment.
</strong><strong>print("Hello, World!")
</strong></code></pre>
{% endhint %}

{% embed url="https://www.w3schools.com/python/trypython.asp?filename=demo_comment" %}
