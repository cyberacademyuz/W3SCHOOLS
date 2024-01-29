# Font web safe

### Web safe fontlar nima? <a href="#web-xavfsiz-fontlar-ozi-nima" id="web-xavfsiz-fontlar-ozi-nima"></a>

Web safe fontlar barcha brauzerlar va qurilmalarda universal tarzda o'rnatiladigan shriftlardir.

### Fallback fontlar <a href="#qayta-fontlar" id="qayta-fontlar"></a>

Biroq, 100% to'liq Web safe shriftlar mavjud emas. Shrift topilmasligi yoki to'g'ri o'rnatilmaslik ehtimoli har doim bor.

Shu sababdan ham doimo fallback shriftlardan foydalanish muhim.

Bu `font-family` xususiyatiga asosiy shriftga o'xshash "zaxira shriftlar" qo'shishingiz kerakligini anglatadi. Agar birinchi shrift ishlamasa, brauzer keyingisini, keyingisini va hokazolarni sinab ko'radi. Roʻyxatni har doim asosiy shrift oilasi bilan tugating.

{% code title="Quyida uch xil shrift keltirilgan: Tahoma, Verdana va sans-serif. Agarda birinchi font topilmasa, Ikkinchi va uchinchi fontlar zaxira sifatida ishlaydi." %}
```
p {
font-family: Tahoma, Verdana, sans-serif;
}
```
{% endcode %}

### HTML va CSS uchun eng yaxshi web safe shriftlar <a href="#html-va-css-uchun-eng-yaxshi-web-xavfsiz-fontlar" id="html-va-css-uchun-eng-yaxshi-web-xavfsiz-fontlar"></a>

Quyidagi ro'yhatdagi shriftlar HTML va CSS uchun eng yaxshi web safe shriftlar hisoblanadi:

* Arial (sans-serif)
* Verdana (sans-serif)
* Tahoma (sans-serif)
* Trebuchet MS (sans-serif)
* Times New Roman (serif)
* Georgia (serif)
* Garamond (serif)
* Courier New (monospace)
* Brush Script MT (cursive)

{% hint style="warning" %}
**Note:** Web saytni yuklashdan oldin har xil brauzerlarda, qurilmalarda shriftlar qanday ko'rinayotganligini tekshiring va har doim fallback shriftlaridan foydalaning.
{% endhint %}

### Arial (sans-serif) <a href="#arial-sans-serif" id="arial-sans-serif"></a>

Arial nashriyotda ham internetda ham keng qo'llaniladigan shrift hidoblanadi. Shuningdek Arial Google Docs ning standart shrifti hisoblanadi.

Arial eng xavfsiz web shriftlardan biri va u bir qancha operatsion tizimlarda mavjud.

<figure><img src="../../../.gitbook/assets/image (332).png" alt=""><figcaption></figcaption></figure>

### Verdana (sans-serif) <a href="#verdana-sans-serif" id="verdana-sans-serif"></a>

Verdana mashxur shriftlardan biri. Verdana hatto kichik o'lchamda ham o'qishga oson bo'lgan shrift hisoblanadi.

<figure><img src="../../../.gitbook/assets/image (133).png" alt=""><figcaption></figcaption></figure>

### Tahoma (sans-serif) <a href="#tahoma-sans-serif" id="tahoma-sans-serif"></a>

Tahoma shriftida belgilar orasidagi masofa juda ham qisqa.

<figure><img src="../../../.gitbook/assets/image (505).png" alt=""><figcaption></figcaption></figure>

### Trebuchet MS <a href="#trebuchet-ms" id="trebuchet-ms"></a>

**Trebuchet MS** 1996-yilda Microsoft tomonidan ishlab chiqilgan. Bu shriftdan ehtiyotkorlik bilan foydalaning. Chunki, u barcha mobil operatsion tizimlar tomonidan qo'llab-quvvatlanmasligi mumkin.

<figure><img src="../../../.gitbook/assets/image (467).png" alt=""><figcaption></figcaption></figure>

### Times New Roman <a href="#times-new-roman" id="times-new-roman"></a>

TImes New Roman dunyodagi eng taniqli shriftlardan biri. U gazetalarda va "yangiliklar" web saytlarida ko'p ishlatiladi. Shuningdek u Windows qurilmalarda va dasturlarda asosiy shrift hisoblanadi.

<figure><img src="../../../.gitbook/assets/image (492).png" alt=""><figcaption></figcaption></figure>

### Georgia (serif) <a href="#georgia-serif" id="georgia-serif"></a>

Georgia - elegant serif font hisoblanadi. Uni turli o'lchamlarda ham o'qish oson, shu sababdan ham u mobil qurilmalardagi moslashuvchan dizaynlar uchun yaxshi nomzod.

<figure><img src="../../../.gitbook/assets/image (90).png" alt=""><figcaption></figcaption></figure>

### Garamond (serif) <a href="#garamond-serif" id="garamond-serif"></a>

Garamond ko'plab nashr qilingan kitoblarda ishlatilgan klassik shriftlardan biri. U o'qishga juda oson va ajoyib ko'rinishga ega.

<figure><img src="../../../.gitbook/assets/image (80).png" alt=""><figcaption></figcaption></figure>

### Courier New (monospace) <a href="#courier-new-monospace" id="courier-new-monospace"></a>

Courier New keng qamrovda ishlatiladigan **monospace serif** shriftlaridan biri. Courier New ko'pincha kodlash ekranlarida ishlatiladi va ko'plab elektron pochta provayderlari undan standart shrift sifatida foydalanadilar. Bundan tashqari **Courier New** kino boshlanishida ham ishlatiladigan standart shrift hisoblanadi.

<figure><img src="../../../.gitbook/assets/image (439).png" alt=""><figcaption></figcaption></figure>

### Brush Script MT (cursive) <a href="#brush-script-mt-cursive" id="brush-script-mt-cursive"></a>

Brush Script MT shrifti qo'lbola yozuvlarga o'xshatish uchun ishlab chiqilgan. U elegant ko'rinishi mumkin, lekin o'qish uchun qiyin. Shu sababdan ehtiyotkorlik bilan ularni ishlating.

<figure><img src="../../../.gitbook/assets/image (510).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
**Maslahat:** Google fonts qanday ishlashini ko'rib chiqing va ularni ishlatishni o'rganing.
{% endhint %}
