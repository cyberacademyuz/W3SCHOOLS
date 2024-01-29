# Vue $emit()

{% hint style="success" %}
Vue-da o'rnatilgan **`$emit()`**usul yordamida biz asosiy elementda yozib olinishi mumkin bo'lgan bola komponentida maxsus hodisa yaratishimiz mumkin.

Rekvizitlar asosiy elementdan asosiy komponentga ma'lumotlarni jo'natish uchun ishlatiladi va **`$emit()`**buning aksi uchun ishlatiladi: ma'lumotni asosiy komponentdan ota-onaga o'tkazish.
{% endhint %}

**Biz bundan keyin qiladigan ishlarning maqsadi** , hozirgi vaqtda o'zgarish sodir bo'layotgan bola komponentida `App.vue`emas, balki ota-onada o'zgartirilishi kerak bo'lgan oziq-ovqat mahsulotining "sevimli" maqomiga ega bo'lishdir .`FoodItem.vue`

Sevimli holatni in `App.vue`o'rniga o'zgartirishning **sababi**`FoodItem.vue` shundaki, `App.vue`sevimli holat birinchi navbatda saqlanadi, shuning uchun uni yangilash kerak. Kattaroq loyihada ma'lumotlar biz bilan bog'langan ma'lumotlar bazasidan olinishi mumkin `App.vue`va biz ma'lumotlar bazasiga o'zgartirish kiritish uchun komponentda sodir bo'layotgan o'zgarishlarni xohlaymiz, shuning uchun biz ota-ona bilan bola komponentidan qayta aloqa qilishimiz kerak.

### Maxsus hodisani chiqaring

`$emit()`Komponentdan ota-onaga ma'lumot yuborish zarurati bor va buning uchun biz o'rnatilgan usuldan foydalanamiz .

Bizda allaqachon almashtirish tugmasi bosilganda ishlaydigan komponent `toggleFavorite`ichida usul mavjud. `FoodItem.vue`Keling, mavjud qatorni olib tashlaymiz va "toggle-favorite" maxsus hodisamizni chiqarish uchun qator qo'shamiz:

{% code title="FoodItem.vue:" %}
```js
methods: {
  toggleFavorite() {
    this.foodIsFavorite = !this.foodIsFavorite;
    this.$emit('toggle-Favorite');
  }
} 
```
{% endcode %}

Biz maxsus tadbirimiz nomini tanlashimiz mumkin, ammo emitatsiya hodisalari uchun kabob qutisidan foydalanish odatiy holdir.

### Emissiya hodisasini oling

Maxsus emit hodisasi "toggle-favorite" endi komponentdan chiqariladi `FoodItem.vue`, lekin biz ota-onadagi voqeani tinglashimiz `App.vue`va voqea sodir bo'lganligini ko'rishimiz uchun biror narsa qiladigan usulni chaqirishimiz kerak.

Biz hodisani komponent yaratilgan joyda emas `@`, stenografiya bilan tinglaymiz:`v-on:App.vue`

<pre class="language-html" data-title="&#x22;Sevimli o&#x27;zgartirish&#x22; hodisasini tinglang App.vue:"><code class="lang-html">&#x3C;food-item
  v-for="x in foods"
  :key="x.name"
  :food-name="x.name"
  :food-desc="x.desc"
  :is-favorite="x.favorite"
<strong>  @toggle-favorite="receiveEmit"
</strong>/>
 
</code></pre>

`App.vue`Bizning maxsus "sevimli o'zgartirish" hodisamiz sodir bo'lganda, biz voqea sodir bo'lganligini ko'rishimiz uchun "testEmit" usulini yaratishimiz kerak :

```js
methods: {
  receiveEmit() {
    alert('Hello World!');
  }
}
```

### Ota-onadagi oziq-ovqat mahsulotining "sevimli" holatini o'zgartiring

`App.vue`Endi bizda bola komponentdan "Sevimli" tugmasi bosilganda xabar beruvchi hodisa mavjud .

`App.vue`Biz “Sevimli” tugmasi bosilganda, “ovqatlar” qatoridagi “sevimli” xususiyatini to‘g‘ri oziq-ovqat mahsuloti uchun o‘zgartirmoqchimiz . Buning uchun biz oziq-ovqat mahsuloti nomini `FoodItem.vue`quyidagi manzilga yuboramiz `App.vue`, chunki bu har bir oziq-ovqat mahsuloti uchun noyobdir:

<pre class="language-js" data-title="FoodItem.vue:"><code class="lang-js">methods: {
  toggleFavorite() {
<strong>    this.$emit('toggle-favorite', this.foodName);
</strong>  }
} 
</code></pre>

Endi biz oziq-ovqat mahsuloti nomini `App.vue`"sevimli o'zgartirish" hodisasi sodir bo'lganda chaqiriladigan usulga argument sifatida olishimiz mumkin, masalan:

<pre class="language-js" data-title="App.vue:"><code class="lang-js">methods: {
<strong>  receiveEmit(foodId) {  
</strong><strong>    alert( 'You clicked: ' + foodId );
</strong>  }
}
</code></pre>

Endi biz qaysi oziq-ovqat mahsuloti bosilganini bilganimizdan so'ng, "ovqatlar" qatoridagi to'g'ri oziq-ovqat mahsuloti uchun "sevimli" holatini yangilashimiz mumkin:

{% code title="App.vue:" %}
```js
methods: {
  receiveEmit(foodId) {
    const foundFood = this.foods.find(
      food => food.name === foodId
    );
    foundFood.favorite = !foundFood.favorite;
  }
}
```
{% endcode %}

Yuqoridagi kodda "topish" massiv usuli "foods" massividan o'tadi va biz bosgan oziq-ovqat mahsulotiga teng nom xususiyatiga ega ob'ektni qidiradi va bu ob'ektni "foundFood" sifatida qaytaradi. Shundan so'ng biz "foundFood.health" ni oldingisiga qarama-qarshi qilib o'rnatishimiz mumkin, shunda u `true`va orasida o'tadi `false`.

[Bu yerda](https://www-w3schools-com.translate.goog/jsref/jsref\_find.asp?\_x\_tr\_sl=de&\_x\_tr\_tl=uz&\_x\_tr\_hl=ru&\_x\_tr\_pto=wapp) JavaScript massivining "topish" usuli haqida ko'proq bilib oling .

[Bu yerda](https://www-w3schools-com.translate.goog/js/js\_arrow\_function.asp?\_x\_tr\_sl=de&\_x\_tr\_tl=uz&\_x\_tr\_hl=ru&\_x\_tr\_pto=wapp) JavaScript o'q funktsiyalari haqida ko'proq bilib oling .

"Oziq-ovqatlar" qatoridagi to'g'ri oziq-ovqat endi "sevimli" holatini yangilaydi. Qolgan yagona narsa - sevimli taomni ko'rsatadigan rasmni yangilash.

Oziq-ovqat mahsuloti komponentlari allaqachon "oziq-ovqatlar" massividan "sevimli" maqomi bilan yaratilgan va "is-sevimli" yorlig'i sifatida yuborilganligi sababli , biz ushbu element joylashgan joydan `App.vue`"isFavorite" yorlig'iga murojaat qilishimiz kerak. rasmni yangilang:`FoodItem.vuev-show<img>`

<pre class="language-html"><code class="lang-html"><strong>&#x3C;img src="/img_quality.svg" v-show="isFavorite">
</strong></code></pre>

Bundan tashqari, "foodIsFavorite" ma'lumotlar xususiyatini o'chirib tashlashimiz mumkin, `FoodItem.vue`chunki u endi ishlatilmaydi.

#### Misol

Ushbu yakuniy misol kodida oziq-ovqat mahsulotlarining sevimli holati avvalgidek o'zgartirilishi mumkin, ammo endi sevimli holat to'g'ri joyda, ichida o'zgartirilgan `App.vue`.

### "Emissiya" varianti

Komponent ichida rekvizitlarni e'lon qilganimiz kabi `FoodItem.vue`, Vue "emits" opsiyasidan foydalanib, komponent nima chiqaradiganini ham hujjatlashimiz mumkin.

Rekvizitlar komponentda e'lon qilinishi kerak, emissiyalarni esa hujjatlashtirish tavsiya etiladi.

Komponentda emissiyamizni shunday hujjatlashimiz mumkin `FoodItem.vue`:

<pre class="language-html"><code class="lang-html">&#x3C;script>
export default {  
  props: ['foodName','foodDesc','isFavorite'],
<strong>  emits: ['toggle-favorite'],
</strong>  methods: {
    toggleFavorite() {
      this.$emit('toggle-favorite', this.foodName);
    }
  }
};
&#x3C;/script>
</code></pre>

Emissiyalar hujjatlashtirilganda komponentdan boshqalardan foydalanish osonroq bo'ladi.
