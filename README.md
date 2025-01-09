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
parseInt(0.0000003);
```

```javascript
Math.max([0, 1])
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
const asi = () => {
    return 
    {}
}
asi();
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

```javascript
function Follower(name, race, rank) {
	this.name = name;
	this.race = race;
	this.rank = rank;
}

Follower.prototype.speak = function() {
	return `${this.name}: If you wish to hunt with me, your feet need to be quick, and your eyes quicker.`;
}

Follower.prototype.toString = function() {
	return `[Name: ${this.name}] [Race: ${this.race.join('|')}] [Rank: ${this.rank}]`;
}

function fresh() {
    const obj = {};
    const [constructor, ...args] = arguments;
    Object.setPrototypeOf(obj, constructor.prototype);
    return constructor.apply(obj, args) || obj;
}

const aela = new Follower('Aela the Huntress', ['Nord','Werewolf'], 'Expert');
const aela2 = fresh(Follower, 'Aela the Huntress', ['Nord','Werewolf'], 'Expert');

aela.speak() === aela2.speak();
```

```javascript
// What is the order of execution and why?

setTimeout(() => {
  console.log("setTimeout executed - 1");
}, 0);

Promise.resolve().then(() => {
  console.log("Promise resolved - 1");
});

setTimeout(() => {
  console.log("setTimeout executed - 2");
}, 0);

Promise.resolve().then(() => {
  console.log("Promise resolved - 2");
});

for (let i = 0; i < 5; i++) {
    console.log(`It was run ${i + 1} times`);
}
```
