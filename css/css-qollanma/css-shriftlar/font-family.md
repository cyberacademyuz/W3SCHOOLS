# Font family

Web saytingiz uchun to'g'ri shrift tanlash muhim hisoblanadi!

### Shrift tanlash muhim <a href="#font-tanlash-muhim" id="font-tanlash-muhim"></a>

To'g'ri tanlangan shrift web sayt foydalanuvchilariga katta ta'sir ko'rsatadi

To'g'ri shrift brendingiz uchun kuchli identifikatsiya yaratishi mumkin.

O'qish oson bo'lgan shriftdan foydalanish muhimdir. Shrift matningizga joziba beradi. Shrift uchun to'g'ri rang va matn o'lchamini tanlash ham muhimdir.

### Asosiy shrift oilalari <a href="#umumiy-font-oilalari" id="umumiy-font-oilalari"></a>

CSS da 5 ta asosiy font family mavjud:

1. **Serif** shriftlarida har bir harfning chetida kichik chiziq mavjud. Ular sinchkovlik va nafislik tuyg'usini uyg'otadi.
2. **Sans-serif** shriftlarida hech qanday kichik chiziq mavjud emas. Ular asosan minimalistik va zamonaviylik uchun ishlatiladi
3. **Monospace** shriftlaridagi barcha harflar bir xil kenglikga ega bo'ladi. Ular mexanik ko'rinish hosil qiladi.
4. **Cursive** shriftlari inson yozuviga o'xshaydi
5. **Fantasy** shriftlari dekoratsiya/ajoyib shriftlar hisoblanadi.

Barcha turli shrift nomlari biror bir asosiy font oilasiga tegishli bo'ladi.

### Sans-serif va Serif oilalari orasidagi farq <a href="#sans-serif-va-serif-oilalari-orasidagi-farq" id="sans-serif-va-serif-oilalari-orasidagi-farq"></a>

![](<../../../.gitbook/assets/image (527).png>)

{% hint style="warning" %}
**Note:** _Sans-serif_ fontlari kompyuter ekranida serif fontlariga qaraganda yaxshiroq o'qiladi.
{% endhint %}

### Ba'zi shriftlardan misollar <a href="#bazi-fontlardan-misollar" id="bazi-fontlardan-misollar"></a>

<figure><img src="../../../.gitbook/assets/image (493).png" alt=""><figcaption></figcaption></figure>

### CSS font-family xususiyati <a href="#css-font-family-xususiyati" id="css-font-family-xususiyati"></a>

Matnga shrift tanlash uchun CSSda `font-family` xususiyatidan foydalanamiz.

{% hint style="warning" %}
**Note:** Agar biror bir shriftning nomi bitta so'zdan ko'p bo'lsa, u qo'shtirnoqqa olinishi kerak, masalan "Times New Roman"
{% endhint %}

**Tip:** Brauzerlar/operatsion tizimlar o'rtasida muvofiqlikni maksimal tarzda ta'minlash uchun `font-family` xususiyati bir nechta shrift nomlariga ega bo'lishi kerak. O'zingiz xohlagan shriftdan boshlang va shrift oila bilan yakunlang (agar boshqa shriftlar mavjud bo'lmasa, brauzerga shrift oilasda o'xshash shriftni tanlashiga ruxsat berish uchun). Shrift nomlari vergul bilan ajratilishi kerak. Qayta shriftlar haqida keyingi bobda o'qing.

{% code title="Uchchala paragraf uchun turli xil shriftlar berish:" %}
```
.p1 {
  font-family: "Times New Roman", Times, serif;
}

.p2 {
  font-family: Arial, Helvetica, sans-serif;
}

.p3 {
  font-family: "Lucida Console", "Courier New", monospace;
}
```
{% endcode %}
