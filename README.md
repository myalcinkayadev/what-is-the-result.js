# what-is-the-result.js

```javascript
!undefined
```

```javascript
!{}
```

```javascript
![]
```

```javascript
!""
```

```javascript
undefined == null
```

```javascript
NaN === NaN
```

```javascript
typeof undefined
```

```javascript
typeof null
```

```javascript
typeof NaN
```

```javascript
0 ?? 1
```

```javascript
0 || 1
```

```javascript
10 & 01
```

```javascript
10 | 01
```

```javascript
10 && 01
```

```javascript
10 || 01
```

```javascript
0.1 + 0.2
```

```javascript
undefined += 1
```

```javascript
10 == [10]
```

```javascript
10 / [10]
```

```javascript
10 * []
```


```javascript
undefined = 1
```

```javascript
let myStr = "Walk";
myStr[0] = "T";
myStr;
```

```javascript
let sisi; sisi?.[42];
```

```javascript
const myArray = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9],
  [[10, 11, 12], 13],
  [14, 15, 16]
];

const myData = myArray[3][0][2];
myData;
```

```javascript
let a = 8, b = 6;
[a, b] = [b, a]
```

```javascript
const deadSocrates = { role: 'gadfly', location: 'athens' };
const { role, ...unknownSocrates } = deadSocrates;
unknownSocrates 
```

```javascript
const deadSocrates = { role: 'gadfly', location: "" };
deadSocrates.role ||= "mýops"
deadSocrates.location ||= 'athens';
deadSocrates.role
deadSocrates.location
```

```javascript
const [l, r, f, ...kaboom] = [4, 8, 15, 16, 23, 42]
l;
r;
f;
kaboom;
```

```javascript
// Mary Poppins (1964) - "Supercalifragilisticexpialidocious"
[...'Supercalifragilisticexpialidocious'].reduce((prv, cur) => cur + prv);
```

```javascript
const coordinates = [[62.0842195, 9.7042283]];
const { 0: riverSide, 1: mountainView = [61.627706, 8.3809468] } = coordinates;
mountainView
```

```javascript
const bestLocation = new Proxy({ latitude: 62.0842195, longitude: 9.7042283 }, {
  get: function(object, property) {
    return property in object ? object[property] : "unknown";
  }
});
bestLocation.latitude;
bestLocation.longitude;
bestLocation.name;
```

```javascript
Math.max([0, 1])
```

```javascript
function getEmoji(n, i = 10, o = n, acc = []) {
  return (n < o + i ? getEmoji(n + 1, i, o, [...acc, String.fromCodePoint(n)]) : acc);
}
getEmoji(127761)
getEmoji(127761, 5)
getEmoji(127761, 0, 127781)
```

``` javascript
const twice = (f, x) => f(f(x));
const addThree = (x) => x + 3;
twice(addThree, 2);
```

```javascript
const eurekaReject = `Give yourself time. Ideas'll come. 
Life'll shake you, roll you, maybe embrace you. The music'll find you.`;
const eureka = (rejectMessage) => new Promise((resolve, reject) => { reject(rejectMessage) });
eureka(eurekaReject);
```

``` javascript
function Universe() {}
Universe.prototype = {
    earth: 'Pale Blue Dot'
}
const gaia = new Universe();

gaia instanceof Universe;
gaia.constructor === Universe;
gaia instanceof Object;
gaia.constructor === Object;
```

```javascript
function destroyer() {
  const [arr, ...rest] = arguments;
  return arr.filter(v => !rest.includes(v));
}
destroyer(['JAK2', 'V617F', 'Exon 12'], 'V617F', 'Exon 12');
```
