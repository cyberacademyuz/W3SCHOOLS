# React Formalar

Xuddi HTML-da bo'lgani kabi, React foydalanuvchilarga veb-sahifa bilan o'zaro aloqada bo'lish uchun formalardan foydalanadi.

### Reactda formalar qo'shish

Boshqa har qanday element kabi React bilan forma qo'shasiz:

Foydalanuvchilarga o'z ismlarini kiritish imkonini beruvchi forma qo'shing:

```jsx
function MyForm() {
  return (
    <form>
      <label>Enter your name:
        <input type="text" />
      </label>
    </form>
  )
}
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<MyForm />);
```

Bu odatdagidek ishlaydi, forma yuboriladi va sahifa yangilanadi.

Ammo bu, odatda, React-da sodir bo'lishi kerak bo'lmagan holat.

Bu oldini olishni va Reactga forma boshqarishga ruxsat berishimiz kerak.

### Fromalarni boshqarish

Formalarni boshqarish ma'lumotlar qiymatni o'zgartirganda yoki topshirilganda qanday boshqarish kerakligi haqidadir.

HTMLda forma ma'lumotlari odatda DOM tomonidan boshqariladi.

Reactda forma ma'lumotlari odatda komponentlar tomonidan boshqariladi.

Ma'lumotlar komponentlar tomonidan boshqarilganda, barcha ma'lumotlar komponent holatida saqlanadi.

`onChange` atributiga hodisa boshqaruvchilarini qo'shish orqali o'zgarishlarni boshqarishingiz mumkin.

`useState` hooki-dan har bir input qiymatini kuzatib borish va butun dastur uchun "yagona haqiqat manbasini" taqdim qilish uchun foydalanishimiz mumkin.

{% hint style="warning" %}
Hooks haqida qo'shimcha ma'lumot olish uchun <mark style="color:green;">React Hooks</mark> bo'limiga qarang .
{% endhint %}

{% code title="Inputni boshqarish uchun useState hookidan foydalaning:" %}
```jsx
import { useState } from 'react';
import ReactDOM from 'react-dom/client';

function MyForm() {
  const [name, setName] = useState("");

  return (
    <form>
      <label>Enter your name:
        <input
          type="text" 
          value={name}
          onChange={(e) => setName(e.target.value)}
        />
      </label>
    </form>
  )
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<MyForm />);
```
{% endcode %}

### Formalarni topshirish

`<form>` uchun `onSubmit` atributga hodisa boshqaruvchisini qo‘shish orqali yuborish amalini boshqarishingiz mumkin:

{% code title="onSubmit atributiga submit tugmasi va hodisa boshqaruvchisini qo'shing:" %}
```jsx
import { useState } from 'react';
import ReactDOM from 'react-dom/client';

function MyForm() {
  const [name, setName] = useState("");

  const handleSubmit = (event) => {
    event.preventDefault();
    alert(`The name you entered was: ${name}`)
  }

  return (
    <form onSubmit={handleSubmit}>
      <label>Enter your name:
        <input 
          type="text" 
          value={name}
          onChange={(e) => setName(e.target.value)}
        />
      </label>
      <input type="submit" />
    </form>
  )
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<MyForm />);
```
{% endcode %}

### Bir nechta input maydonlari

Har bir elementga `name` atributini qo'shish orqali bir nechta input maydonlarining qiymatlarini boshqarishingiz mumkin.

Biz steytimizni bo'sh obyekt bilan ishga tushiramiz.

Hodisa ishlov beruvchisidagi maydonlarga murojaat qilish uchun `event.target.name` va `event.target.value` sintaksisidan foydalaning.

Steytni yangilash uchun xususiyat nomining atrofida kvadrat qavslardan \[qavs belgisi]dan foydalaning.

{% code title="Ikkita input maydoniga ega forma tuzish:" %}
```jsx
import { useState } from 'react';
import ReactDOM from 'react-dom/client';

function MyForm() {
  const [inputs, setInputs] = useState({});

  const handleChange = (event) => {
    const name = event.target.name;
    const value = event.target.value;
    setInputs(values => ({...values, [name]: value}))
  }

  const handleSubmit = (event) => {
    event.preventDefault();
    alert(inputs);
  }

  return (
    <form onSubmit={handleSubmit}>
      <label>Enter your name:
      <input 
        type="text" 
        name="username" 
        value={inputs.username || ""} 
        onChange={handleChange}
      />
      </label>
      <label>Enter your age:
        <input 
          type="number" 
          name="age" 
          value={inputs.age || ""} 
          onChange={handleChange}
        />
        </label>
        <input type="submit" />
    </form>
  )
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<MyForm />);
```
{% endcode %}

{% hint style="warning" %}
**Eslatma:** Biz ikkala input maydonlari uchun bir xil hodisani boshqaruvchi funksiyasidan foydalanamiz, har biri uchun bitta hodisa boshqaruvchi yaratishimiz mumkin, ammo bunda kod ancha tartibli bo'ladi va React-da afzal usul hisoblanadi.
{% endhint %}

### Textarea

React-dagi matn maydoni elementi HTML-dagidan biroz farq qiladi.

HTMLda matn maydonining qiymati ochiluvchi `<textarea>` teg va yopiluvchi `</textarea>` tegi orasidagi matn edi.

```jsx
<textarea>
  Content of the textarea.
</textarea>
```

Reactda matn maydoning qiymati qiymat atributiga joylashtiriladi. Matn maydoning qiymatini boshqarish uchun `useState` Hook-idan foydalanamiz:

{% code title="Ba'zi kontentga ega oddiy matn maydoni:" %}
```jsx
import { useState } from 'react';
import ReactDOM from 'react-dom/client';

function MyForm() {
  const [textarea, setTextarea] = useState(
    "The content of a textarea goes in the value attribute"
  );

  const handleChange = (event) => {
    setTextarea(event.target.value)
  }

  return (
    <form>
      <textarea value={textarea} onChange={handleChange} />
    </form>
  )
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<MyForm />);
```
{% endcode %}

### Select

React-dagi dropdown ro'yhat yoki select box ham HTML-dan biroz farq qiladi.

HTMLda dropdown ro'yxatdagi tanlangan qiymat `selected` atributi bilan ifodalanadi:

{% code title="HTML:" %}
```html
<select>
  <option value="Ford">Ford</option>
  <option value="Volvo" selected>Volvo</option>
  <option value="Fiat">Fiat</option>
</select>
```
{% endcode %}

Reactda tanlangan qiymat `select` tegidagi `value` atributi bilan ifodalanadi:

{% code title="Oddiy select boxga misol, bu yerda tanlangan "Volvo" qiymati konstruktorda ishga tushiriladi:" %}
```jsx
function MyForm() {
  const [myCar, setMyCar] = useState("Volvo");

  const handleChange = (event) => {
    setMyCar(event.target.value)
  }

  return (
    <form>
      <select value={myCar} onChange={handleChange}>
        <option value="Ford">Ford</option>
        <option value="Volvo">Volvo</option>
        <option value="Fiat">Fiat</option>
      </select>
    </form>
  )
}
```
{% endcode %}

Ushbu kichik o'zgarishlarni `<textarea>` va `<select>` ga kiritib, React barcha input elementlarini xuddi shu tarzda boshqarishga qodir.
