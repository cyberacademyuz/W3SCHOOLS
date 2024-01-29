# React Props

***

Props React komponentlariga uzatiladigan argumentlardir.

Props komponentlarga HTML atributlari orqali uzatiladi.

{% hint style="warning" %}
`props` properties (xususiyatlar)ni bildiradi.
{% endhint %}

### React props

_Props JavaScript-dagi funksiya argumentlari va_ HTML-dagi atributlar kabidir.

Propsni komponentga yuborish uchun HTML atributlari bilan bir xil sintaksisdan foydalaniladi:

{% code title="Car elementiga "brand" atributini qo'shish:" %}
```jsx
const myElement = <Car brand="Ford" />;
```
{% endcode %}

Komponent argumentni `props` obyekti sifatida qabul qiladi:

{% code title="Komponentda brend atributidan foydalanish:" %}
```jsx
function Car(props) {
  return <h2>I am a { props.brand }!</h2>;
}
```
{% endcode %}

{% embed url="https://www.w3schools.com/react/showreact.asp?filename=demo2_react_props" %}

### Ma'lumotlarni uzatish

Bundan tashqari, Props ma'lumotlarni bir komponentdan ikkinchisiga parametr sifatida o'tkazish usuli hamdir.&#x20;

{% code title=""Brand" xususiyatini Garage komponentidan Car komponentiga yuborish:" %}
```jsx
function Car(props) {
  return <h2>I am a { props.brand }!</h2>;
}

function Garage() {
  return (
    <>
      <h1>Who lives in my garage?</h1>
      <Car brand="Ford" />
    </>
  );
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Garage />);
```
{% endcode %}

Agar sizda yuboriladigan qiymat yuqoridagi kabi string emas o'zgaruvchi bo'lsa, o'zgaruvchi nomini jingalak qavslar ichida yozing:

{% code title="carName nomli o'zgaruvchi yaratish va uni Car komponentiga yuborish:" %}
```jsx
function Car(props) {
  return <h2>I am a { props.brand }!</h2>;
}

function Garage() {
  const carName = "Ford";
  return (
    <>
      <h1>Who lives in my garage?</h1>
      <Car brand={ carName } />
    </>
  );
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Garage />);
```
{% endcode %}

Yoki obyekt bo'lsa:

{% code title="carInfo nomli obyekt yaratish va uni Car komponentiga yuborish:" %}
```jsx
function Car(props) {
  return <h2>I am a { props.brand.model }!</h2>;
}

function Garage() {
  const carInfo = { name: "Ford", model: "Mustang" };
  return (
    <>
      <h1>Who lives in my garage?</h1>
      <Car brand={ carInfo } />
    </>
  );
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Garage />);
```
{% endcode %}

{% hint style="warning" %}
**Eslatma:** Props faqat o'qish uchun mo'ljallangan! Agar ularning qiymatini o'zgartirmoqchi bo'lsangiz, xatolik yuzaga keladi.
{% endhint %}
