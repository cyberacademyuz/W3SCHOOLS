# Custom Hooklar

Hooklar qayta foydalanish mumkin bo'lgan funktsiyalardir.

Agar sizda bir nechta komponentlar tomonidan ishlatilishi kerak bo'lgan komponentlar logikasi mavjud bo'lsa, ushbu logikani maxsus Hookga chiqarishimiz mumkin.

Maxsus hooklar "use" bilan boshlanadi. Misol: `useFetch`.

### Hook tuzish

Quyidagi kodda `Home` komponentimizdagi ma'lumotlarni olamiz va uni ko'rsatamiz.

Biz soxta maʼlumotlar olish uchun JSONPlaceholder xizmatidan foydalanamiz. Ushbu xizmat kerakli ma'lumotlar hozircha mavjud bo'lmaganda ilovalarni sinab ko'rish uchun juda yaxshi.

Batafsil ma’lumot olish uchun JavaScript <mark style="color:green;">Fetch API</mark> bo‘limiga o'ting.

{% code title="index.js: JSONPlaceholder xizmatidan soxta "todo" elementlarini olish va sahifadagi sarlavhalarni ko'rsatish uchun foydalaning:" %}
```jsx
import { useState, useEffect } from "react";
import ReactDOM from "react-dom/client";

const Home = () => {
  const [data, setData] = useState(null);

  useEffect(() => {
    fetch("https://jsonplaceholder.typicode.com/todos")
      .then((res) => res.json())
      .then((data) => setData(data));
 }, []);

  return (
    <>
      {data &&
        data.map((item) => {
          return <p key={item.id}>{item.title}</p>;
        })}
    </>
  );
};

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Home />);
```
{% endcode %}

Qabul qilish logikasi boshqa komponentlarda ham kerak bo'lishi mumkin, shuning uchun uni maxsus Hookga chiqaramiz.

Maxsus Hook sifatida foydalanish uchun olish logikasini yangi faylga o'tkazing:

{% code title="useFetch.js:" %}
```jsx
import { useState, useEffect } from "react";

const useFetch = (url) => {
  const [data, setData] = useState(null);

  useEffect(() => {
    fetch(url)
      .then((res) => res.json())
      .then((data) => setData(data));
  }, [url]);

  return [data];
};

export default useFetch;
```
{% endcode %}

{% code title="index.js:" %}
```jsx
import ReactDOM from "react-dom/client";
import useFetch from "./useFetch";

const Home = () => {
  const [data] = useFetch("https://jsonplaceholder.typicode.com/todos");

  return (
    <>
      {data &&
        data.map((item) => {
          return <p key={item.id}>{item.title}</p>;
        })}
    </>
  );
};

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Home />);
```
{% endcode %}

### Misolni tushuntirish

Biz useFetch.js nomli yangi fayl yaratdik, unda useFetch funksiyasi mavjud boʻlib, unda maʼlumotlarimizni olish uchun zarur boʻlgan barcha logikalar mavjud.

Biz qattiq kodlangan URL manzilini olib tashladik va uni maxsus Hook-ga uzatilishi mumkin bo'lgan `url` o'zgaruvchisi bilan almashtirdik.

Nihoyat, biz Hook-dan ma'lumotlarimizni qaytaramiz.

`index.js`-da `useFetch` Hook-ni import qilamiz va uni boshqa Hook kabi ishlatamiz. Bu yerda  ma'lumotlarni olish uchun URL manziliga o'takazamiz.

Endi ushbu maxsus Hook-dan istalgan URL-dan ma'lumotlarni olish uchun istalgan komponentda qayta renderlashimiz mumkin.
