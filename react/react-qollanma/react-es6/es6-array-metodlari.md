# ES6 Array metodlari

### Array metodlari

JavaScriptda bir qancha array metodlari mavjud.

Reactda eng foydalilaridan biri `.map()` array metodidir.

`.map()` metodi arraydagi har bir elementda funksiyani ishga tushirishga imkon beradi, natijada yangi array qaytaradi.

React-da ro'yxatlar yaratish uchun ham `map()`dan foydalanish mumkin.

Arrayda elementlar ro'yxatini yarating:

```jsx
const myArray = ['apple', 'banana', 'orange'];

const myList = myArray.map((item) => <p>{item}</p>)
```
