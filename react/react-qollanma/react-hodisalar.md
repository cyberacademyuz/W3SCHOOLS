# React Hodisalar

HTML DOM hodisalari kabi, Reactda ham foydalanuvchi eventlari asosida amallar bajarishi mumkin.

React HTML bilan bir xil eventlarga ega: click, change, mouseover va h.k.

### Hodisalar qo'shish

Reactda eventlar camelCase sintaksisida yoziladi:

`onclick` o'rniga `onClick` yoziladi.

Reactning event handler-lari jingalak qavslar ichida yoziladi:

&#x20;`onClick="shoot()"` o'rniga `onClick={shoot}`

{% code title="React:" %}
```jsx
<button onClick={shoot}>Take the Shot!</button>
```
{% endcode %}

{% code title="HTML:" %}
```html
<button onclick="shoot()">Take the Shot!</button>
```
{% endcode %}

`shoot` funktsiyasini `Football` komponentining ichida chaqirish:

```jsx
function Football() {
  const shoot = () => {
    alert("Great Shot!");
  }

  return (
    <button onClick={shoot}>Take the shot!</button>
  );
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Football />);
```

{% embed url="https://www.w3schools.com/react/showreact.asp?filename=demo2_react_events_handler" %}

### Argumentlarni o'tkazish

Argumentni event handler-ga o'tkazish uchun arrow funksiyadan foydalaniladi.

{% code title="Arrow funksiyadan foydalanib, "Goal" ni shoot funksiyasiga parametr sifatida yuboring:" %}
```jsx
function Football() {
  const shoot = (a) => {
    alert(a);
  }

  return (
    <button onClick={() => shoot("Goal!")}>Take the shot!</button>
  );
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Football />);
```
{% endcode %}

### Event obyekti

Event handler-lar funksiyani ishga tushirgan React eventiga murojaat qilish huquqiga ega.

Bizning misolimizdagi event "click" hodisasidir.

{% code title="Arrow funksiya: hodisa obyektini qo'lda yuborish:" %}
```jsx
function Football() {
  const shoot = (a, b) => {
    alert(b.type);
    /*
    'b' represents the React event that triggered the function,
    in this case the 'click' event
    */
  }

  return (
    <button onClick={(event) => shoot("Goal!", event)}>Take the shot!</button>
  );
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Football />);
```
{% endcode %}

{% embed url="https://www.w3schools.com/react/showreact.asp?filename=demo2_react_events_event" %}

Keyingi bo'limda Formani ko'rib chiqsak foydali bo'ladi.
