# Chaining

jQuery orqali, harakatlarni/metodlarni bir biriga ulashingiz mumkin.

Chaining bizga bitta steytment ichida bir nechta jQuery metodlarini (bir xil elementda) ishlatish imkonini beradi.

### jQuery metodlarini ulash <a href="#jquery-metodlarini-zanjirlash" id="jquery-metodlarini-zanjirlash"></a>

Hozirgacha jQuery statementlarini ketma-ketlikda yozib keldik (birin-ketin).

Biroq, **chaining** deb nomlangan texnika mavjud bo'lib, u bizga bir xil element(lar)da birin-ketin bir nechta jQuery buyruqlarini bajarishga imkon beradi.

**Maslahat:** Shu yo'l orqali Brauzerlar bir xil element(lar)ni bir necha marta qidirishi shart emas.

Harakatlarni bir biriga chaining qilish uchun oldingi harakatga keyingi harakatni qo'shishingiz kerak.

Quyidagi misol `css()`, `slideUp()` va `slideDown()` metodlarini birlashtiradi. "p1" elementi avval qizil rangga o'zgaradi, keyin tepaga ko'tariladi va keyin pastga tushadi:

```
$("#p1").css("color", "red").slideUp(2000).slideDown(2000); 
```

Kerak bo'lganda, bundan ham ko'p metodlarni kiritishimiz mumkin.

**Maslahat:** Agar chaining bir qatorda bo'lsa, unda bu ancha uzun bo'lib ketishi mumkin. O'sha qatorni o'zingiz xohlagan formatda yozishingiz mumkin, jQuery sintaksisi unchalik ham qiyin emas.

Bu ham juda yaxshi ishlaydi:

```
$("#p1").css("color", "red")
  .slideUp(2000)
  .slideDown(2000); 
```

jQuery bu yerdagi ortiqcha bo'sh joylarni olib tashlaydi va kodni ishga tushiradi.
