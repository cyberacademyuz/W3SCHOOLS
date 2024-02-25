---
description: CSS qoidasi selektor va deklaratsiya blokidan iborat.
---

# CSS Sintaksis

## <mark style="color:green;">CSS Sintaksisi</mark> <a href="#css-sintaksisi-2" id="css-sintaksisi-2"></a>

<figure><img src="../../.gitbook/assets/img_selector.gif" alt=""><figcaption></figcaption></figure>

Selektor siz still bermoqchi bo'lgan HTML elementini tanlaydi.

Deklaratsiya bloki nuqta-vergul bilan ajratilgan bir yoki bir nechta deklaratsiyalardan iborat.

Har bir deklaratsiyada CSS xususiyati nomi va qiymati, ikki nuqta bilan ajratilgan holda bo'ladi.

Bir nechta CSS deklaratsiyalari nuqta-vergul bilan ajratiladi va deklaratsiya bloki jingalak qavslar bilan o'ralgan bo'ladi.

{% tabs %}
{% tab title="CSS" %}
Ushbu misolda barcha <mark style="color:red;">`<p>`</mark> elementlari o'rtaga joylashadi va qizil rangda bo'ladi:

```css
p {
  color: red;
  text-align: center;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_syntax1" %}
{% endtab %}
{% endtabs %}

Misolni tushuntirish:

* <mark style="color:red;">`p`</mark> bu CSS selektori (Still bermoqchi bo'lgan HTML elementingizni bildiradi: <mark style="color:red;">`<p>`</mark>)
* <mark style="color:red;">`color`</mark> bu xususiyat, <mark style="color:red;">`red`</mark> esa uning qiymati.
* <mark style="color:red;">`text-align`</mark> xususiyat, <mark style="color:red;">`center`</mark> uning qiymati.

{% hint style="warning" %}
CSS selektorlari va CSS xususiyatlari haqida keyingi bo'limlarda batafsil o'rganasiz!
{% endhint %}
