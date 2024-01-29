# URL encode

URL bu veb-manzil uchun boshqa bir atama hisoblanadi.

URL so'zlardan (w3schools.com) yoki IP manzilidan (192.68.20.50) iborat bo'lishi mumkin.

Ko'pchilik ma'lum bir saytga kirish paytida sayt nomini kiritishadi, chunki uni eslab qolish raqamlarga qaraganda osonroq.

## URL - Uniform Resource Locator

Veb-brauzerlar URL manzildan foydalanib veb-serverlardan sahifalarni so'raydi.

URL Internetdagi sahifa (yoki boshqa ma'lumotlar)ga murojaat qilish uchun ishlatiladi.

[https://www.w3schools.com/html/default.asp](https://www-w3schools-com.translate.goog/html/default.asp?\_x\_tr\_sl=en&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) kabi URL quyidagi sintaksis qoidalariga amal qiladi:

```
sxema://prefiks.domen:port/joylashuv/faylnomi
```

Tushuntirish:

* sxema - Internet xizmat turini bildiradi (eng keng tarqalganlari http yoki https )
* **prefiks** - domen prefiksini bildiradi (http uchun www standart prefiks hisoblanadi)
* domen - Internetdagi domen nomini bildiradi (masalan, w3schools.com)
* port - hostdagi port raqamini bildiradi (http uchun standart port 80)
* joylashuv - serverdagi joylashuvni bildiradi
* fayl nomi - hujjat yoki resurs nomini bildiradi

### Umumiy URL sxemalari

Quyidagi jadvalda bir nechta umumiy sxemalar keltirilgan:

| Sxema | To'liq shakli                      | Shu maqsadda foydalaniladi          |
| ----- | ---------------------------------- | ----------------------------------- |
| http  | HyperText Transfer Protocol        | Umumiy veb-sahifalar. Shifrlanmagan |
| https | Secure HyperText Transfer Protocol | Xavfsiz veb-sahifalar. Shifrlangan  |
| ftp   | File Transfer Protocol             | Fayllarni yuklab olish yoki yuklash |
| file  |                                    | Kompyuteringizda fayl               |

## URL kodlash

URL manzillarni faqat [ASCII belgilar to'plami](https://www.w3schools.com/charsets/ref\_html\_ascii.asp)dan foydalangan holdagina Internet orqali uzatish mumkin. Agar URLda ASCII to'plamidan tashqari boshqa belgilar ham mavjud bo'lsa, URL kovertatsiya qilinishi kerak.

URL encoding ASCII to'plamida bo'lmagan belgilarni Internet orqali uzatish mumkin bo'lgan formatga o'tkazadi.

URLni kodlash ASCII bo'lmagan belgilarni "%" va keyin o'n oltilik sanoq sistemasidagi raqamlar bilan almashtiradi.

URL manzillarda boʻsh joy boʻlmasligi kerak. URL encoding odatda bo'sh joyni qo'shimcha **+** belgisi yoki **%20** ga o'zgartiradi.



### O'zingiz uchun sinab ko'ring

Agar siz "Yuborish" tugmasini bossangiz, brauzer URL serverga yuborilishidan oldin kiritilgan ma'lumotlarni kodlaydi.

Serverdagi sahifa qabul qilingan ma'lumotni ko'rsatadi.

Boshqa ma'lumotni ham kiritib sinab koʻring va “Yuborish” tugmasini bosing.

***

### ASCII encoding-ga misollar

Brauzeringiz sahifangizda ishlatiladigan belgilar to'plamiga ko'ra kiritilgan ma'lumotni kodlaydi.

HTML5 da standart belgilar to'plami UTF-8 dir.

| Belgi | Windows-1252-da | UTF-8-da  |
| ----- | --------------- | --------- |
| €     | %80             | %E2%82%AC |
| £     | %A3             | %C2%A3    |
| ©     | %A9             | %C2%A9    |
| ®     | %AE             | %C2%AE    |
| À     | %C0             | %C3%80    |
| Á     | %C1             | %C3%81    |
| Â     | %C2             | %C3%82    |
| Ã     | %C3             | %C3%83    |
| Ä     | %C4             | %C3%84    |
| Å     | %C5             | %C3%85    |
