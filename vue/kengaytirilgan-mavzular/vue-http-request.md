# Vue HTTP Request

{% hint style="success" %}
HTTP **so'rovi** mijoz va server o'rtasidagi aloqaning bir qismidir.

Mijoz serverga **HTTP so'rovini yuboradi, u so'rovni bajaradi va HTTP javobini qaytaradi.**
{% endhint %}

### HTTP

**HTTP H** yper **T** ext **T** ransfer **P** rotocol degan ma'noni anglatadi .

Brauzerimiz Internetni ko'rib chiqayotganimizda har doim fonda HTTP so'rovlarini amalga oshiradi. Internet sahifasiga kirganimizda, brauzerimiz (mijoz) server bizga kerakli sahifani HTTP javoblari sifatida barcha tegishli fayllar va ma'lumotlar bilan yuborishi uchun bir nechta HTTP so'rovlarini yuboradi.

HTTP so'rovlarining eng keng tarqalgan turlari `POST`, `GET`, `PUT`, `PATCH`va `DELETE`. HTTP so'rovlarining turli turlari haqida bizning [HTTP so'rov usullari](https://www-w3schools-com.translate.goog/tags/ref\_httpmethods.asp?\_x\_tr\_sl=de&\_x\_tr\_tl=uz&\_x\_tr\_hl=ru&\_x\_tr\_pto=wapp) sahifamizda ko'proq bilib oling.

HTTP nima haqida bizning [HTTP nima](https://www-w3schools-com.translate.goog/whatis/whatis\_http.asp?\_x\_tr\_sl=de&\_x\_tr\_tl=uz&\_x\_tr\_hl=ru&\_x\_tr\_pto=wapp) sahifamizda ko'proq bilib oling.

### Qabul qilish usuli

Vue serveridan ma'lumotlarni olish uchun biz JavaScript `fetch()`usulidan foydalanishimiz mumkin.

Ushbu qo'llanmada usuldan foydalanganda `fetch()`biz HTTP so'rov usulini belgilamaymiz va bu standart so'rov usuli `GET`fonda ishlatiladigan narsa ekanligini anglatadi.

Usul `fetch()`URL manzilini argument sifatida kutadi, shunda u ma'lumotlarni qayerdan olishni biladi.

`fetch()`Bu erda HTTP so'rovini yuborish `GET`va ma'lumotlarni HTTP javobi sifatida qabul qilish usulidan foydalanadigan oddiy misol . Bu holda so'ralgan ma'lumotlar mahalliy fayl ichidagi matndir `file.txt`:

{% code title="App.vue:" lineNumbers="true" %}
```html
<template>
  <div>
    <button @click="fetchData">Fetch Data</button>
    <p v-if="data">{{ data }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      data: null,
    };
  },
  methods: {
    fetchData() {
      const response = fetch("file.txt");
      this.data = response;
    }
  }
};
</script>
```
{% endcode %}

Yuqoridagi misolda biz natijada faqat "\[object Promise]" ni olamiz, lekin bu biz xohlagan narsa emas.

Biz bu natijani olamiz, chunki `fetch()`va'da qilingan ob'ektni qaytaradigan va'da qilingan usul. Shunday qilib, usulning birinchi qaytishi `fetch()`faqat ob'ekt bo'lib, HTTP so'rovi yuborilganligini anglatadi. Bu "kutilayotgan" holat.

Usul `fetch()`biz xohlagan ma'lumotni olganida, va'da bajariladi.

Biz kerakli ma'lumotlar bilan javob bajarilishini kutish uchun biz usul `await`oldidagi operatordan foydalanishimiz kerak `fetch()`:

```js
const response = await fetch("file.txt");
```

Operator `await`usul ichida ishlatilsa, usul operator bilan e'lon qilinishi kerak `async`:

```js
async fetchData() {
  const response = await fetch("file.txt");
  this.data = response;
}
```

Operator `async`brauzerga usulning asinxron ekanligini aytadi, ya'ni u biror narsani kutadi va brauzer usul tugashini kutayotganda boshqa vazifalarni bajarishda davom etishi mumkin.

Endi biz oladigan narsa "Javob" va endi shunchaki "Va'da" emas, ya'ni biz fayl ichidagi haqiqiy matnni olishga bir qadam yaqinroqmiz `file.txt`:

{% code title="" %}
```html
<template>
  <div>
    <button @click="fetchData">Fetch Data</button>
    <p v-if="data">{{ data }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      data: null,
    };
  },
  methods: {
    async fetchData() {
      const response = await fetch("file.txt");
      this.data = response;
    }
  }
};
</script> 
```
{% endcode %}

Fayl ichidagi matnni olish uchun javob usulidan `file.txt`foydalanishimiz kerak . `text()`Usul va'daga asoslangan usul bo'lgani uchun biz uning oldida operatordan `text()`foydalanishimiz kerak .`await`

**Nihoyat!** Endi biz fayl ichidagi matnni `file.txt`usul bilan olishimiz kerak bo'lgan narsaga egamiz `fetch()`:

{% code title="App.vue:" %}
```html
<template>
  <div>
    <button @click="fetchData">Fetch Data</button>
    <p v-if="data">{{ data }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      data: null,
    };
  },
  methods: {
    async fetchData() {
      const response = await fetch("file.txt");
      this.data = await response.text();
    }
  }
};
</script> 
```
{% endcode %}

***

### JSON faylidan ma'lumotlarni olish

Oldingi misolda biz fayldan matn oldik `.txt`. Ammo ma'lumotlarni saqlashning ko'plab usullari mavjud va endi biz fayldan qanday ma'lumot olishimiz mumkinligini ko'rib chiqamiz `.json`.

[`JSON`](https://www-w3schools-com.translate.goog/js/js\_json\_intro.asp?\_x\_tr\_sl=de&\_x\_tr\_tl=uz&\_x\_tr\_hl=ru&\_x\_tr\_pto=wapp)Bu oddiy fayl formati boʻlib, u bilan ishlash oson, chunki maʼlumotlar matn sifatida saqlanadi, shuning uchun uni odamlar oʻqishi oson va format `JSON`dasturlash tillari tomonidan ham keng qoʻllab-quvvatlanadi, shuning uchun biz, masalan, qaysi maʼlumotlarni belgilashimiz mumkin. fayldan chiqarib olish `.json`.

Fayldan ma'lumotlarni o'qish uchun `.json`yuqoridagi misolga qilishimiz kerak bo'lgan yagona o'zgarish faylni olish `.json`va javobdagi usul `json()`o'rniga usuldan foydalanishdir.`text()`

Usul `json()`HTTP so'rovidan javobni o'qiydi va JavaScript ob'ektini qaytaradi.

[`<pre>`](https://www-w3schools-com.translate.goog/tags/tag\_pre.asp?\_x\_tr\_sl=de&\_x\_tr\_tl=uz&\_x\_tr\_hl=ru&\_x\_tr\_pto=wapp)Formatlangan matnni ko'rsatish uchun biz bu erda tegdan foydalanamiz `JSON`, chunki u bo'shliqlar va qatorlarni o'qishni osonlashtiradi.

#### Misol

`App.vue`:

```html
<template>
  <div>
    <button @click="fetchData">Fetch Data</button>
    <pre v-if="data">{{ data }}</pre>
  </div>
</template>

<script>
export default {
  data() {
    return {
      data: null,
    };
  },
  methods: {
    async fetchData() {
      const response = await fetch("bigLandMammals.json");
      this.data = await response.json();
    }
  }
};
</script>
 
 
```

Usulning natijasi `json()`JavaScript ob'ekti bo'lganligi sababli, fayldan tasodifiy hayvonni ko'rsatish uchun yuqoridagi misolni o'zgartirishimiz mumkin `bigLandMammals.json`:

#### Misol

`App.vue`:

```html
<template>
  <p>Try clicking the button more than once to see new animals picked randomly.</p>
  <button @click="fetchData">Fetch Data</button>
  <div v-if="randomMammal">
    <h2>{{ randomMammal.name }}</h2>
    <p>Max weight: {{ randomMammal.maxWeight }} kg</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      randomMammal: null
    };
  },
  methods: {
    async fetchData() {
      const response = await fetch("bigLandMammals.json");
      const data = await response.json();
      const randIndex = Math.floor(Math.random()*data.results.length);
      this.randomMammal = data.results[randIndex];
    }
  }
};
</script>
```

***

### API maʼlumotlari

API qisqartmasi **Application Programming Interface** degan ma'noni anglatadi . [Bu erda](https://www-w3schools-com.translate.goog/js/js\_api\_intro.asp?\_x\_tr\_sl=de&\_x\_tr\_tl=uz&\_x\_tr\_hl=ru&\_x\_tr\_pto=wapp) API haqida ko'proq bilib olishingiz mumkin .

Biz bog'lanishimiz va ob-havo ma'lumotlari, birja ma'lumotlari va hokazolarni olish uchun foydalanishimiz mumkin bo'lgan juda ko'p qiziqarli bepul APIlar mavjud.

HTTP so'rovi bilan API chaqirganimizda oladigan javobimiz barcha turdagi ma'lumotlarni o'z ichiga olishi mumkin, lekin ko'pincha formatdagi ma'lumotlarni o'z ichiga oladi `JSON`.

#### Misol

[Random-data-api.com](https://translate.google.com/website?sl=de\&tl=uz\&hl=ru\&client=webapp\&u=https://random-data-api.com/) API dan tasodifiy foydalanuvchi olish uchun tugmani bosish mumkin .

`App.vue`:

```html
<template>
  <h1>Example</h1>
  <p>Click the button to fetch data with an HTTP request.</p>
  <p>Each click generates an object with a random user from <a href="https://random-data-api.com/" target="_blank">https://random-data-api.com/</a>.</p>
  <p>The robot avatars are lovingly delivered by <a href="http://Robohash.org" target="_blank">RoboHash</a>.</p>
  <button @click="fetchData">Fetch data</button>
  <pre v-if="data">{{ data }}</pre>
</template>

<script>
  export default {
    data() {
      return {
        data: null,
      };
    },
    methods: {
      async fetchData() {      
        const response = await fetch("https://random-data-api.com/api/v2/users"); 
        this.data = await response.json();
      }   
    }
  };
</script>
 
 
 
 
```

Oldingi misolimizni tasodifiy foydalanuvchini qulayroq tarzda kiritish uchun biroz o'zgartirishimiz mumkin:

#### Misol

`<pre>`Tugma bosilganda biz tasodifiy foydalanuvchi nomini ish nomi va rasmi bilan birga tegda ko'rsatamiz .

`App.vue`:

```html
<template>
  <h1>Example</h1>
  <p>Click the button to fetch data with an HTTP request.</p>
  <p>Each click generates an object with a random user from <a href="https://random-data-api.com/" target="_blank">https://random-data-api.com/</a>.</p>
  <p>The robot avatars are lovingly delivered by <a href="http://Robohash.org" target="_blank">RoboHash</a>.</p>
  <button @click="fetchData">Fetch data</button>
  <div v-if="data" id="dataDiv">
    <img :src="data.avatar" alt="avatar">
    <pre>{{ data.first_name + " " + data.last_name }}</pre>
    <p>"{{ data.employment.title }}"</p>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        data: null,
      };
    },
    methods: {
      async fetchData() {      
        const response = await fetch("https://random-data-api.com/api/v2/users"); 
        this.data = await response.json();
      },    
    }
  };
</script>

<style>
#dataDiv {
  width: 240px;
  background-color: aquamarine;
  border: solid black 1px;
  margin-top: 10px;
  padding: 10px;
}
#dataDiv > img {
  width: 100%;
}
pre {
  font-size: larger;
  font-weight: bold;
}
</style>
 
 
 
```

***

### "Axios" kutubxonasi bilan Vue-da HTTP so'rovi

"Axios" JavaScript kutubxonasi bizga HTTP so'rovlarini ham qilish imkonini beradi.

O'zingizning mashinangizda misol yaratish va ishga tushirish uchun avval loyiha papkangizdagi terminaldan foydalanib, "axios" kutubxonasini o'rnatishingiz kerak, masalan:

npm install axios

Tasodifiy foydalanuvchini olish uchun Vue-dagi "axios" kutubxonasidan shunday foydalanishimiz mumkin:

#### Misol

Buning o'rniga "axios" kutubxonasi bilan HTTP so'rovini bajarish uchun oldingi misolga faqat kichik o'zgarishlar kiritilgan.

`App.vue`:

```html
<template>
  <h1>Example</h1>
  <p>Click the button to fetch data with an HTTP request.</p>
  <p>Each click generates an object with a random user from <a href="https://random-data-api.com/" target="_blank">https://random-data-api.com/</a>.</p>
  <p>The robot avatars are lovingly delivered by <a href="http://Robohash.org" target="_blank">RoboHash</a>.</p>
  <button @click="fetchData">Fetch data</button>
  <div v-if="data" id="dataDiv">
    <img :src="data.data.avatar" alt="avatar">
    <pre>{{ data.data.first_name + " " + data.data.last_name }}</pre>
    <p>"{{ data.data.employment.title }}"</p>
  </div>
</template>

<script>
  import axios from 'axios'

  export default {
    data() {
      return {
        data: null,
      };
    },
    methods: {
      async fetchData() {      
        this.data = await axios.get("https://random-data-api.com/api/v2/users");
      }
    }
  };
</script>

<style>
#dataDiv {
  width: 240px;
  background-color: aquamarine;
  border: solid black 1px;
  margin-top: 10px;
  padding: 10px;
}
#dataDiv > img {
  width: 100%;
}
pre {
  font-size: larger;
  font-weight: bold;
}
</style>
```
