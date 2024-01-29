# Komentariyalar

HTMLdagi komentariyalar brauzerda ko'rsatilmaydi, ammo sizning HTML kodingizni chunishni osonlashtiradi.

## HTMLning komentariya tegi

Quyidagi sintaksisdan foydalanish orqali HTML kodingizga komentariya qo'sha olasiz.

```
<!-- Write your comments here -->
```

Boshlang'ich tegda undov belgisi (!) bor ekanligiga va u oxirgi tegda yo'q ekanligiga e'tibor bering.

{% hint style="warning" %}
HTMLdagi komentariyalar brauzerda ko'rsatilmaydi, ammo sizning HTML kodingizni chunishni osonlashtiadi.
{% endhint %}

## Kommentlar qo'shish

Komentlar yordamida HTML kodingizga bildirishnomalar va eslatmalar qoldirishingiz mumkin.

```
<!-- This is a comment -->

<p>This is a paragraph.</p>

<!-- Remember to add more information here -->
```

## Kontentni yashirish

Kommentlardan kontentni yashirish uchun ham foydalaniladi.

Agar kodni vaqtinchalik yashirishni hohlasangiz bu sizga qo'l keladi.

```
<p>This is a paragraph.</p>

<!-- <p>This is another paragraph </p> -->

<p>This is a paragraph too.</p>
```

Bundan tashqari, bir nechta qatorlarni ham yashirishingiz mumkin. `<!--` va `-->` o'rtasidagi barcha narsa ekrandan yashiriladi.

```
<p>This is a paragraph.</p>
<!--
<p>Look at this cool image:</p>
<img border="0" src="pic_trulli.jpg" alt="Trulli">
-->
<p>This is a paragraph too.</p>
```

Kommentlar HTML kodlarni debug qilish uchun ham juda yaxshi, chunki xatolarni qidirish uchun kod qatorlarini birma-bir komentga olishingiz mumkin.

## Qatordagi kontentni yashirish

Paragrafning bir qimini yashirish:

```
<p>This <!-- great text --> is a paragraph.</p>
```
