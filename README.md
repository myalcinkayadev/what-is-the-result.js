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
const deadSocrates = { role: 'gadfly', location: 'athens' };
const { role, ...unknownSocrates } = deadSocrates;
unknownSocrates 
```

```javascript
const coordinates = [[62.0842195, 9.7042283]];
const { 0: riverSide, 1: mountainView = [61.627706, 8.3809468] } = coordinates;
mountainView
```

```javascript
function getEmoji(n, i = 10, o = n, acc = []) {
  return (n < o + i ? getEmoji(n + 1, i, o, [ ...acc, String.fromCodePoint(n)]) : acc);
}
getEmoji(127761)
getEmoji(127761, 5)
getEmoji(127761, 0, 127781)

```
