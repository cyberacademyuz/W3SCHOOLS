# CSS Sintaksis

CSS qoidasi selektor va deklaratsiya blokidan iborat.

## CSS Sintaksisi  <a href="#css-sintaksisi-2" id="css-sintaksisi-2"></a>

<figure><img src="../../.gitbook/assets/img_selector.gif" alt=""><figcaption></figcaption></figure>

Selektor siz still bermoqchi bo'lgan HTML elementini tanlaydi.

Deklaratsiya bloki nuqta-vergul bilan ajratilgan bir yoki bir nechta deklaratsiyalardan iborat.

Har bir deklaratsiyada CSS xususiyati nomi va qiymati, ikki nuqta bilan ajratilgan holda bo'ladi.

Bir nechta CSS deklaratsiyalari nuqta-vergul bilan ajratiladi va deklaratsiya bloki jingalak qavslar bilan o'ralgan bo'ladi.

{% code title="Ushbu misolda barcha <p> elementlari o'rtaga joylashadi va qizil rangda bo'ladi:" %}
```
p {
  color: red;
  text-align: center;
}
```
{% endcode %}

Misolni tushuntirish:

* `p` bu CSS selektori (Still bermoqchi bo'lgan HTML elementingizni bildiradi: \<p>)
* `color` bu xususiyat va `red`  esa uning qiymati.
* `text-align`  xususiyat va `center` uning qiymati.

{% hint style="warning" %}
CSS selektorlari va CSS xususiyatlari haqida keyingi bo'limlarda batafsil o'rganasiz!
{% endhint %}
