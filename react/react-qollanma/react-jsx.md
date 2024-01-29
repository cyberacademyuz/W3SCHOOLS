# React JSX

### JSX nima ?

JSX **JavaScript XML** degan ma'noni anglatadi.

JSX bizga React ichida HTML kodlarini yozish imkonini beradi.

JSX React-da HTML elementlarini yozishni va qo'shishni osonlashtiradi.

### JSX&#x20;

JSX bizga HTML elementlarini JavaScript-da yozish va ularni DOM-ga hech qanday `createElement()`  yoki `appendChild()` metodlarisiz joylashtirish imkonini beradi.

JSX HTML teglarini React elementlariga aylantiradi.

{% hint style="warning" %}
JSX dan foydalanish shart emas, lekin JSX React ilovalarini yozishni osonlashtiradi.
{% endhint %}

Mana bunga ikkita misol. Birinchisida JSX dan foydalanilgan, ikkinchisida esa JSXdan foydalanilmagan:

{% code title="JSX orqali:" %}
```jsx
const myElement = <h1>I Love JSX!</h1>;

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(myElement);
```
{% endcode %}

{% code title="JSXsiz:" %}
```jsx
const myElement = React.createElement('h1', {}, 'I do not use JSX!');

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(myElement);
```
{% endcode %}

Birinchi misolda ko'rib turganingizdek, JSX bizga HTML kodini JavaScript kodiga to'g'ridan-to'g'ri yozish imkonini beradi.

JSX ES6 asosidagi JavaScript tilining kengaytmasi boʻlib, ishlash jarayonida oddiy JavaScript-ga o'giriladi.

### JSXda expressionlar

JSX yordamida expressionlarni jingalak qavslar `{}` ichida yozishingiz mumkin.

Expression React o'zgaruvchisi yoki property yoki boshqa har qanday JavaScript expressioni bo'lishi mumkin. JSX expression-ni bajaradi va natijani qaytaradi:

{% code title="5 + 5 expressionini bajaring:" %}
```jsx
const myElement = <h1>React is {5 + 5} times better with JSX</h1>;
```
{% endcode %}

### Kattaroq HTML kod blokini yozish

HTML elementlarini bir nechta qatorlarda yozish uchun uni qavslar ichida yozing:

{% code title="Uchta ro'yxat elementidan iborat ro'yxat yaratish:" %}
```jsx
const myElement = (
  <ul>
    <li>Apples</li>
    <li>Bananas</li>
    <li>Cherries</li>
  </ul>
);
```
{% endcode %}

### O'rab turuvchi ota element

HTML kodlar bita ota elementga o'ralgan bo'lishi kerak.

_Agar ikkita_ paragraf yozishni xohlasangiz, ularni `div` elementi kabi ota element ichiga qo'yishingiz kerak.

{% code title="Ikkita paragrafni bitta div elementiga o‘rash:" %}
```jsx
const myElement = (
  <div>
    <p>I am a paragraph.</p>
    <p>I am a paragraph too.</p>
  </div>
);
```
{% endcode %}

{% hint style="warning" %}
HTML kod noto'g'ri bo'lsa yoki ota element berilmasa, JSXda xatolik yuzga keladi.
{% endhint %}

Bundan tashqari, bir nechta qatorlarni o'rab olish uchun "fragment" dan foydalanishingiz mumkin. Bu DOM-ga keraksiz qo'shimcha nodelarni qo'shishni oldini oladi.

Fragment bo'sh HTML tegiga o'xshaydi: `<> </>`.

{% code title="Ikkita paragrafni fragment bilan o'rab olish:" %}
```jsx
const myElement = (
  <>
    <p>I am a paragraph.</p>
    <p>I am a paragraph too.</p>
  </>
);
```
{% endcode %}

### Elementlar yopilishi shart

JSX XML qoidalariga amal qiladi, shuning uchun HTML elementlari to'g'ri yopilishi kerak.

{% code title="Elementlarni /> bilan yoping." %}
```jsx
const myElement = <input type="text" />;
```
{% endcode %}

{% hint style="warning" %}
Agar HTML to'g'ri yopilmagan bo'lsa, JSXda xatolik yuzaga qiladi.
{% endhint %}

### class attributi = className

`class` atributi HTMLda juda koʻp ishlatiladigan atributdir, lekin JSX JavaScript sifatida koʻrsatilgani uchun va `class` kalit soʻzi JavaScriptdagi built-in kalit so'z boʻlgani uchun undan JSX da foydalanib bo'lmaydi.

`class` attributi o'rniga `className` atributidan foydalaniladi.

JSX bu mammoni `className` yordamida hal qildi. JSX render qilinganda, u `className` atributlarini class atributlariga aylantiradi.

{% code title="JSXda class o'rniga className atributidan foydalanish:" %}
```jsx
const myElement = <h1 className="myclass">Hello World</h1>;
```
{% endcode %}

### Shartlar - If steytmenti

React `if` steytmentlarini qo'llab-quvvatlaydi, lekin JSX _ichida emas._

JSX da shartli steytmentlardan foydalanish uchun `if` steytmentlarini JSXdan tashqariga qo'yishingiz kerak yoki uning o'rniga ternary expressiondan foydalanishingiz mumkin:

**Variant 1:**

`if` steytmentini JSX kodidan tashqarida yozing:

{% code title="Agar x 10 dan kichik bo'lsa "Hello" deb yozing, uning akssi bo'lsa "Goodbye" deb yozing:" %}
```jsx
const x = 5;
let text = "Goodbye";
if (x < 10) {
  text = "Hello";
}

const myElement = <h1>{text}</h1>;
```
{% endcode %}

**Variant 2:**

Ternay expressiondan foydalanish:

{% code title="Agar x 10 dan kichik bo'lsa "Hello" deb yozing, uning akssi bo'lsa "Goodbye" deb yozing:" %}
```jsx
const x = 5;

const myElement = <h1>{(x) < 10 ? "Hello" : "Goodbye"}</h1>;
```
{% endcode %}

{% hint style="warning" %}
**Eslatma:** JavaScript expressionini JSX ichiga yozish uchun JavaScript kodi `{}` jingalak qavslar bilan o'ralgan bo'lishi kerak.
{% endhint %}
