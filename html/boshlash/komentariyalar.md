# Komentariyalar

HTMLdagi komentariyalar brauzerda ko'rsatilmaydi, ammo sizning HTML kodingizni chunishni osonlashtiradi.

## <mark style="color:green;">HTMLning komentariya tegi</mark>

Quyidagi sintaksisdan foydalanish orqali HTML kodingizga komentariya qo'sha olasiz.

```html
<!-- Write your comments here -->
```

Boshlang'ich tegda undov belgisi (!) bor ekanligiga va oxirgi tegda esa yo'q ekanligiga e'tibor bering.

{% hint style="warning" %}
HTMLdagi komentariyalar brauzerda ko'rsatilmaydi, ammo sizning HTML kodingizni chunishni osonlashtiadi.
{% endhint %}

## <mark style="color:green;">Kommentlar qo'shish</mark>

Komentlar orqali HTML kodingizga bildirishnomalar va eslatmalar qoldirishingiz mumkin.

```html
<!-- This is a comment -->

<p>This is a paragraph.</p>

<!-- Remember to add more information here -->
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_comment" %}

## <mark style="color:green;">Kontentni yashirish</mark>

Kommentlardan kontentni yashirish uchun ham foydalaniladi.

Agar kodni vaqtinchalik yashirishni hohlasangiz bu sizga qo'l keladi.

```html
<p>This is a paragraph.</p>

<!-- <p>This is another paragraph </p> -->

<p>This is a paragraph too.</p>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_comment_hide" %}

Bundan tashqari, bir nechta qatorlarni ham yashirishingiz mumkin. `<!--` va `-->` o'rtasidagi barcha narsa ekrandan yashiriladi.

```html
<p>This is a paragraph.</p>
<!--
<p>Look at this cool image:</p>
<img border="0" src="pic_trulli.jpg" alt="Trulli">
-->
<p>This is a paragraph too.</p>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_comment_out" %}

Kommentlar HTML kodlarni debug qilish uchun ham juda yaxshi, chunki xatolarni qidirish uchun kod qatorlarini birma-bir kommentga olishingiz mumkin.

## <mark style="color:green;">Qatordagi kontentni yashirish</mark>

Paragrafning bir qismini yashirish:

```html
<p>This <!-- great text --> is a paragraph.</p>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_comment_inline" %}
