# React Conditional-lar

React-da komponentlarni shartli ravishda ko'rsatishingiz mumkin.

Buni bir necha usullari bor.

### `if` steytmenti

Qaysi komponentni ko'rsatishni tanlash uchun JavaScriptning `if` operatoridan foydalanishimiz mumkin.

{% code title="Ushbu ikki komponentdan foydalanamiz:" %}
```jsx
function MissedGoal() {
  return <h1>MISSED!</h1>;
}

function MadeGoal() {
  return <h1>Goal!</h1>;
}
```
{% endcode %}

Endi shartga qarab qaysi komponentni ko'rsatishni tanlaydigan boshqa komponent yaratamiz:

```jsx
function Goal(props) {
  const isGoal = props.isGoal;
  if (isGoal) {
    return <MadeGoal/>;
  }
  return <MissedGoal/>;
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Goal isGoal={false} />);
```

{% embed url="https://www.w3schools.com/react/showreact.asp?filename=demo2_react_conditionals_if" %}

`isGoal` atributini `true` ga o'zgartirib ko'ring:

```jsx
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Goal isGoal={true} />);
```

{% embed url="https://www.w3schools.com/react/showreact.asp?filename=demo2_react_conditionals_if2" %}

### Mantiqiy `&&` operatori

React komponentini shart asosida ko'rsatishning yana bir usuli `&&` operatoridan foydalanish.

{% code title=" JSX-da jingalak qavslar yordamida JavaScript steytmentlarini joylashtirishimiz mumkin:" %}
```jsx
function Garage(props) {
  const cars = props.cars;
  return (
    <>
      <h1>Garage</h1>
      {cars.length > 0 &&
        <h2>
          You have {cars.length} cars in your garage.
        </h2>
      }
    </>
  );
}

const cars = ['Ford', 'BMW', 'Audi'];
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Garage cars={cars} />);
```
{% endcode %}

{% embed url="https://www.w3schools.com/react/showreact.asp?filename=demo2_react_conditionals_logical" %}

Agar `cars.length > 0` qiymati `true`ga teng bo'lsa, `&&`dan keyingi expression ko'rsatiladi.

`cars` arrayi ichidagi ma'lumotlarni o'chirib sinab ko'ring:

```jsx
const cars = [];
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Garage cars={cars} />);
```

{% embed url="https://www.w3schools.com/react/showreact.asp?filename=demo2_react_conditionals_logical2" %}

### Ternary operatori

Elementlarni shart asosida ko'rsatishning yana bir usuli ternary operatoridan foydalanishdir.

```jsx
condition ? true : false
```

Goal misoliga qaytamiz.

{% code title="Agar isGoal true bo'lsa MadeGoal komponenti qaytariladi, false bo'lsa MissedGoal komponenti qaytariladi:" %}
```jsx
function Goal(props) {
  const isGoal = props.isGoal;
  return (
    <>
      { isGoal ? <MadeGoal/> : <MissedGoal/> }
    </>
  );
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Goal isGoal={false} />);
```
{% endcode %}

Ko'proq ma'lumot olish uchun <mark style="color:green;">ternary operatori</mark> bo'limiga qarang.
