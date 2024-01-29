# React Ro'yxatlar

React-da ro'yxatlarni biror loop yordamida ko'rsatasiz.

Bu uchun odatda JavaScriptning `map()` array metodi afzal metod deb hisoblanadi.

{% hint style="warning" %}
Agar `map()` metodi bo'yicha bilimlaringizni takrorlamoqchi bo'lsangiz, <mark style="color:green;">ES6 bo'limi</mark>ga o'ting.
{% endhint %}

{% code title="Keling, Garage-imizdagi barcha Carlarni render qilaylik:" %}
```jsx
function Car(props) {
  return <li>I am a { props.brand }</li>;
}

function Garage() {
  const cars = ['Ford', 'BMW', 'Audi'];
  return (
    <>
      <h1>Who lives in my garage?</h1>
      <ul>
        {cars.map((car) => <Car brand={car} />)}
      </ul>
    </>
  );
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Garage />);
```
{% endcode %}

Agar ushbu kodni o'zingizning `create-react-app`-ingizda ishlatsangiz, u ishlaydi, lekin ro'yxat elementlari uchun "key" yo'qligi haqida ogohlantirish olasiz.

### Keylar

Keylar Reactga elementlarni kuzatish imkonini beradi. Agar biror element yangilangan yoki o'chirilgan bo'lsa, butun ro'yxat emas faqat o'sha element qayta render qilinadi.

Keylar har bir sibling uchun unikal bo'lishi kerak. Ammo ular global miqyosda dublikat bo'la oladi.

{% hint style="warning" %}
Odatda, key har bir elementga tayinlangan unikal id bo'lishi kerak. Bunda array indeksidan kalit sifatida foydalanishingiz mumkin.
{% endhint %}

{% code title="Keylarni kiritish uchun oldingi misolimizni qayta ko'rib chiqamiz:" %}
```jsx
function Car(props) {
  return <li>I am a { props.brand }</li>;
}

function Garage() {
  const cars = [
    {id: 1, brand: 'Ford'},
    {id: 2, brand: 'BMW'},
    {id: 3, brand: 'Audi'}
  ];
  return (
    <>
      <h1>Who lives in my garage?</h1>
      <ul>
        {cars.map((car) => <Car key={car.id} brand={car.brand} />)}
      </ul>
    </>
  );
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Garage />);
```
{% endcode %}
