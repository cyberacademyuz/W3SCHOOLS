# YouTube

HTML-da videolarni ijro qilishning eng oson yo'li YouTube-dan foydalanishdir.

### Video formatlari bilan kurashyapsizmi ?

Videolarni turli formatlarga aylantirish qiyin va ko'p vaqt talab qilishi mumkin.

Eng oson yechim - YouTube-ga veb-sahifangizdagi videolarni ijro etishga ruxsat berish.

### YouTube video identifikatori

Videoni yotubega yuklaganingizda YouTube uning identifikatorini (masalan, tgbNymZ7vqY) ko'rsatadi.

Siz ushbu identifikatordan foydalanishingiz va HTML kodidagi videongizga murojaat qilishingiz mumkin.

### YouTube videosini HTML formatida ijro etish

Videongizni veb-sahifada ijro etish uchun quyidagilarni bajaring:

* Videoni YouTube-ga yuklang
* Video identifikatoriga e'tibor bering
* Veb-sahifangizda `<iframe>` elementini yarating
* `src` atributiga videoning URL manzilini kiriting
* Pleyer o'lchamini belgilash uchun `width` va `height` atributlaridan foydalaning
* URL manziliga boshqa parametrlar ham qo'shing (pastga qarang)

```
<iframe width="420" height="315"
src="https://www.youtube.com/embed/tgbNymZ7vqY">
</iframe>
```

### YouTube avtomatik ijro + ovozsiz

YouTube URL manziliga `autoplay=1` qo‘shish orqali foydalanuvchi sahifaga tashrif buyurganida videongizni avtomatik tarzda ijro qilinishiga ruxsat berishingiz mumkin. Biroq, videoni avtomatik tarzda boshlash tashrif buyuruvchilaringiz uchun zerikarli!

{% hint style="warning" %}
**Eslatma:** Chromium brauzerlari ko'p hollarda avtomatik ijroga ruxsat bermaydi. Biroq, ovozsiz tarzda avtomatik ijro qilishga har doim ruxsat beriladi.
{% endhint %}

Videongiz avtomatik tarzda ijro qilinishini boshlash uchun `autoplay=1`dan keyin `mute=1`ni qoʻshing.

{% code title="YouTube - Avtomatik ijro + Ovozsiz" %}
```
<iframe width="420" height="315"
src="https://www.youtube.com/embed/tgbNymZ7vqY?autoplay=1&mute=1">
</iframe>
```
{% endcode %}

### YouTube pleylist

Ijro qilinadigan videolarning vergul bilan ajratilgan roʻyxati (asl URL manzilidan tashqari).

### Youtube Loop

Videongiz qayta qayta ijro qilinishiga imkon berish uchun `loop=1`ni qo'shing.

Qiymat 0 (standart): Video faqat bir marta ijro etiladi.

Qiymat 1: Video qayta qayta ijro etilaveradi (abadiy).

{% code title="Youtube-Loop" %}
```
<iframe width="420" height="315"
src="https://www.youtube.com/embed/tgbNymZ7vqY?playlist=tgbNymZ7vqY&loop=1">
</iframe>
```
{% endcode %}

### YouTube boshqaruvlari

Video pleyerda boshqaruv elementlarini ko‘rsatmaslik uchun `controls=0`ni qo‘shing.

Qiymat 0: Pleyer boshqaruvlari ko'rsatilmaydi.

Qiymat 1 (standart): Pleyer boshqaruvlari ko'rsatilani.

{% code title="YouTube - Boshqaruv" %}
```
<iframe width="420" height="315"
src="https://www.youtube.com/embed/tgbNymZ7vqY?controls=0">
</iframe>
```
{% endcode %}
