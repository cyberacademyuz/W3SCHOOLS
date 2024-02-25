---
description: >-
  HTML elementlari, biror ma'lumotni o'z ichiga olgan ochiluvchi va yopiluvchi
  tegni bildiradi.
---

# Elementlar

## <mark style="color:green;">HTML elementlar</mark>

Ochiluvchi tegdan yopuvchi teggacha bo’lgan barcha narsa **element** deyiladi. Keling, buni misollar orqali ko'rib chiqamiz:

<mark style="color:blue;">`<`</mark><mark style="color:red;">`tegnomi`</mark><mark style="color:blue;">`>`</mark> Shu yerga biror ma'lumot kiritiladi <mark style="color:blue;">`<`</mark><mark style="color:red;">`/tegnomi`</mark><mark style="color:blue;">`>`</mark>

Ba'zi HTML elementlariga misollar:

<mark style="color:blue;">`<`</mark><mark style="color:red;">`h1`</mark><mark style="color:blue;">`>`</mark> Mening birinchi sarlavham <mark style="color:blue;">`<`</mark><mark style="color:red;">`/h1`</mark><mark style="color:blue;">`>`</mark>

<mark style="color:blue;">`<`</mark><mark style="color:red;">`p`</mark><mark style="color:blue;">`>`</mark> Mening birinchi paragrafim <mark style="color:blue;">`<`</mark><mark style="color:red;">`/p`</mark><mark style="color:blue;">`>`</mark>

| Ochiluvchi teg | Element kontenti           | Yopiluvchi teg |
| -------------- | -------------------------- | -------------- |
| \<h1>          | Mening birinchi sarlavham  | \</h1>         |
| \<p>           | Mening birinchi paragrafim | \</p>          |
| \<br>          | Yozilmaydi                 | Yozilmaydi     |

{% hint style="warning" %}
**Eslatma:** Ba'zi HTML elementlarida kontent bo'lmaydi (\<br> elementi kabi) Bu elementlar bo'sh elementlar deyiladi. Bo'sh elementlarda yopiluvchi teg ham bo'lmaydi.
{% endhint %}

## <mark style="color:green;">Ichki HTML Elementlar</mark>

HTML elemenlar ichma-ich bo'la oladi. (Ya'ni, elementlar boshqa bir elementning ichida bo'ladi oladi)

Barcha HTML hujjatlar, HTML elementlaridan iborat.

Quyida ko'rsatilgan misolda 4 ta HTML elementi mavjud (<mark style="color:red;">`<html>`</mark>, <mark style="color:red;">`<body>`</mark>, <mark style="color:red;">`<h1>`</mark> va <mark style="color:red;">`<p>`</mark> ):

{% tabs %}
{% tab title="Ruby" %}
```html
<!DOCTYPE html>
<html>
<body>

<h1>Mening birinchi sarlavham.</h1>
<p>Mening birinchi paragrafim..</p>

</body>
</html> 
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_elements" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">Misol orqali tushuntirish</mark>

<mark style="color:red;">`<html>`</mark> elementi root element va u butun HTML hujjatini belgilaydi.

U <mark style="color:red;">`<html>`</mark> tegi bilan boshlanadi va <mark style="color:red;">`</html>`</mark> tegi bilan tugaydi.

Keyin, <mark style="color:red;">`<html>`</mark> elementining ichida <mark style="color:red;">`<body>`</mark> elementi bo'ladi.

```html
<body>

<h1>Mening birinchi sarlavham.</h1>
<p>Mening birinchi paragrafim..</p>

</body> 
```

<mark style="color:red;">`<body>`</mark> elementi HTML hujjatning tana qismini ifodalaydi.

U <mark style="color:red;">`<body>`</mark> tegi bilan boshlanib, <mark style="color:red;">`</body>`</mark> tegi bilan tugaydi.

Keyin, <mark style="color:red;">`<body>`</mark> elementining ichida 2 ta boshqa element bor: <mark style="color:red;">`<h1>`</mark> va <mark style="color:red;">`<p>`</mark>

```html
<h1>Mening birinchi sarlavham.</h1>
<p>Mening birinchi paragrafim.</p>
```

<mark style="color:red;">`<h1>`</mark> elementi sarlavhani bildiradi.

U <mark style="color:red;">`<h1>`</mark> bilan boshlanib <mark style="color:red;">`</h1>`</mark> bilan tugagan.

```html
<h1>Mening birinchi sarlavham.</h1>
```

\<p> elementi paragrafni bildiradi.

U <mark style="color:red;">`<p>`</mark> tegi bilan boshlanib <mark style="color:red;">`</p>`</mark> tegi bilan tugagan.

```html
<p>Mening birinchi paragrafim.</p>
```

## <mark style="color:green;">Hech qachon yopuvchi tegni qoldirib ketmang</mark>

Ba'zi HTML elementlar, ularning yopiluvchi teglarini unutib qoldirsangiz ham to'g'ri ishlaydi.

{% tabs %}
{% tab title="HTML" %}
```html
<html>
<body>

<h1>Mening birinchi sarlavham.</h1>
<p>Mening birinchi paragrafim..</p>

</body>
</html>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_no_endtag" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">Bo'sh HTML elementlar</mark>

Hech qanday tarkibga ega bo’lmagan HTML elementlari bo’sh elementlar deb ataladi.

<mark style="color:red;">`<br>`</mark> tegi qatorni tugatishni ifodalaydi va bo'sh elementda yopuvchi teg bo'lmaydi:

```html
<p> Bu <br> qatori tugatilgan paragraf </p>
```

## <mark style="color:green;">HTML "Case Sensitive" emas</mark>

HTML case sensitive emas: <mark style="color:red;">`<P>`</mark> tegi <mark style="color:red;">`<p>`</mark> bilan bir xil ma'noni anglatadi.

HTML standartlari teglarni kichik harfda yozilishini talab qilmaydi, ammo W3C HTMLda kichik harflar bilan yozishni maslahat beradi va XHTML kabi hujjatlar uchun kichik harflarda yozish talab qilinadi.

## <mark style="color:green;">HTML Teg haqida ma'lumotnoma</mark>

HTML teg ma'lumotnomasi ushbu teglar va ularning atributlari haqida muhim ma'lumotlarni o'z ichiga olgan.

| Teg                     | Tarifi                                  |
| ----------------------- | --------------------------------------- |
| \<html> ⁽ˢᵒᵒⁿ⁾          | HTML hujjatning root qismini ifodalatdi |
| \<body> ⁽ˢᵒᵒⁿ⁾          | Hujjatning tana qismini ifodalaydi      |
| \<h1> ... \<h6> ⁽ ˢᵒᵒⁿ⁾ | HTML sarlavhani ifodalaydi              |
