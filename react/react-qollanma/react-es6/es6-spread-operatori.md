# ES6 Spread operatori

### Spread operatori

JavaScriptning spread operatori (`...`) bizga mavjud array yoki obyektning to'liq yoki bir qismini tezda boshqa array yoki obyektga nusxalash imkonini beradi.

```jsx
const numbersOne = [1, 2, 3];
const numbersTwo = [4, 5, 6];
const numbersCombined = [...numbersOne, ...numbersTwo];
```

Spread operatori ko'pincha destructuring bilan birgalikda ishlatiladi.

{% code title="numbers-dagi birinchi va ikkinchi elementlarni o'zgaruvchilarga tayinlang va qolganlarini arrayga joylashtiring:" %}
```jsx
const numbers = [1, 2, 3, 4, 5, 6];

const [one, two, ...rest] = numbers;
```
{% endcode %}

Spread operatoridan obyektlarda ham foydalanishimiz mumkin:

{% code title="Ushbu ikkita obyektni birlashtiring:" %}
```jsx
const myVehicle = {
  brand: 'Ford',
  model: 'Mustang',
  color: 'red'
}

const updateMyVehicle = {
  type: 'car',
  year: 2021, 
  color: 'yellow'
}

const myUpdatedVehicle = {...myVehicle, ...updateMyVehicle}
```
{% endcode %}

{% hint style="warning" %}
E'tibor bering, bir biriga mos kelmaydigan xususiyatlar birlashtirildi, lekin bir biriga mos keladigan `color` xususiyati oxirgi `updateMyVehicle` obyekti tomonidan qayta o'zgartirildi. Olingan rang endi sariq rang bo'ladi.
{% endhint %}
