# Solutions Collection: Edabit Algorithms

Hey there, I'm Luis Uribe, specializing in solutions engineering and data analysis. Here's a set of algorithmic challenges sourced from [Edabit](https://edabit.com/), that I solved for practice and fun.

**Disclaimer:**  
As per Edabit's policies, I'm only able to provide the title, author, and the solution to the problem listed.

Thank you for taking the time to explore these solutions! For any questions or concerns (including request for removal), feel free to connect with me on [LinkedIn](https://www.linkedin.com/in/luisuribezam/).

**List last updated as of 12-26-23*

## Algorithms Solved
**Edabit Difficulty:** *Hard*



---

**Disclaimer:**
As per Edabit's policies, I'm only able to provide the title, author, and the solution solution I created to the problem listed.

---

**Problem Title:** Seven Boom!  
**Author:** [Alon](https://edabit.com/user/Q69qbJ2JtmQFkMXqz)  
**Solution:**

```javascript
function sevenBoom(arr) {
    let stringConverstion = arr.toString();
    
    if (stringConverstion.includes(7)) {
        return "Boom!";
    } else {
        return "there is no 7 in the array";
    }
}
```

---

**Problem Title:** Tower of Hanoi  
**Author:** [Ruud Peter Boelens](https://edabit.com/user/Akq3fQcPRgPrWfsye)  
**Solution:**

```javascript
function towerHanoi(discs) {
    return Math.pow(2, discs) - 1;
}
```

---

**Problem Title:** Number of Boomerangs  
**Author:** [Helen Yu](https://edabit.com/user/mNMQvcxKSSvqqMYCH)  
**Solution:**

```javascript
function countBoomerangs(arr) {
    let counter = 0;
    
    for (let i = 0; i < arr.length; i++) {
        if (arr[i] !== arr[i + 1] && arr[i] === arr[i + 2]) {
            counter++;
        }
    }
    
    return counter;
}
```

---

**Problem Title:** Oddish vs. Evenish  
**Author:** [Helen Yu](https://edabit.com/user/mNMQvcxKSSvqqMYCH)  
**Solution:**

```javascript
function oddishOrEvenish(num) {
    const strConv = num.toString();
    const words = strConv.split('');
    var arrayOfNumbers = words.map(Number);
    const initialValue = 0;
    const sumWithInitial = arrayOfNumbers.reduce(
        (previousVal, currentVal) => previousVal + currentVal, initialValue);
    
    if (sumWithInitial % 2 === 0) {
        return 'Evenish';
    } else {
        return 'Oddish';
    }
}
```

---

**Problem Title:** How Many Days Between Two Dates  
**Author:** [Alon](https://edabit.com/user/Q69qbJ2JtmQFkMXqz)  
**Solution:**

```javascript
function getDays(date1, date2) {
    const oneDay = 1000 * 60 * 60 * 24;
    const start = Date.UTC(date2.getFullYear(), date2.getMonth(), date2.getDate());
    const end = Date.UTC(date1.getFullYear(), date1.getMonth(), date1.getDate());
    
    return (start - end) / oneDay;
}
```

---

**Problem Title:** Length of a Nested Array  
**Author:** [Helen Yu](https://edabit.com/user/mNMQvcxKSSvqqMYCH)  
**Solution:**

```javascript
function getLength(arr) {
    function flattenDeep(arr1) {
        return arr1.reduce((acc, val) => Array.isArray(val) ? acc.concat(flattenDeep(val)) : acc.concat(val), []);
    }
    
    return flattenDeep(arr).length;
}
```

---

**Problem Title:** Up the Hill, Down the Hill  
**Author:** [Isaac Pak](https://edabit.com/user/yaL57wdXmgAZTvKfX)  
**Solution:**

```javascript
function aveSpd(uphillTime, uphillRate, downhillRate) {
    return (uphillRate * (uphillTime / 60) + downhillRate * (uphillTime / 60)) / (uphillTime / 60 * 2);
}
```

--- 
**Edabit Difficulty:** *Intermediate/Medium*



---

**Disclaimer:**
As per Edabit's policies, I'm only able to provide the title, author, and the solution I created to the problem listed.

---

**Problem Title:** Right Shift by Division  
**Author:** [Deep Xavier](https://edabit.com/user/a777e8chPvJkY3tKa)  
**Solution:**

```javascript
function shiftToRight(x, y) {
    let eq1 = Math.floor(2 ** y);
    let eq2 = Math.floor(x / eq1);
    return eq2;
}
```

---

**Problem Title:** Perimeters with a Catch  
**Author:** [BijogFc24](https://edabit.com/user/Nb6LYPoQP6KJZt8mz)  
**Solution:**

```javascript
function perimeter(l, num) {
    return (l === 's' ?  num *= 4 : num *= 6.28);
}
```

---

**Problem Title:** Find the nth Tetrahedral Number  
**Author:** [Matt](https://edabit.com/user/BkPgkDQGHm66X4Qai)  
**Solution:**

```javascript
function tetra(n) {
    return (n * (n + 1) * (n + 2)) / 6;
}
```

---

**Problem Title:** Concatenate Variable Number of Input Arrays  
**Author:** [Helen Yu](https://edabit.com/user/mNMQvcxKSSvqqMYCH)  
**Solution:**

```javascript
function concat(...args) {
    return args.flat();
}
```

---

**Problem Title:** Triangular Number Sequence  
**Author:** [Matt](https://edabit.com/user/BkPgkDQGHm66X4Qai)  
**Solution:**

```javascript
function triangle(n) {
    return n * (n + 1) / 2;
}
```

---

**Problem Title:** Make a Circle with OOP  
**Author:** [joe111](https://edabit.com/user/E3bAbAjwFzekBoMGD)  
**Solution:**

```javascript
class Circle {
    constructor(radius) {
        this.radius = radius;
    }
    
    getArea() {
        return Math.PI * this.radius ** 2;
    }

    getPerimeter() {
        return 2 * Math.PI * this.radius;
    }
}
```


---

**Problem Title:** Return the Objects Keys and Values  
**Author:** [Matt](https://edabit.com/user/BkPgkDQGHm66X4Qai)  
**Solution:**

```javascript
function keysAndValues(obj) {
    const keys = Object.keys(obj).sort();
    const values = keys.map(key => obj[key]);
    return [keys, values];
}
```

---

**Problem Title:** Integer in Range?  
**Author:** [Matt](https://edabit.com/user/BkPgkDQGHm66X4Qai)  
**Solution:**

```javascript
function intWithinBounds(n, lower, upper) {
    return Number.isInteger(n) && n >= lower && n < upper;
}
```

---

**Problem Title:** Is the Number a Repdigit  
**Author:** [Eduard Diakunenko](https://edabit.com/user/KcpfY4XZ7fNamyLd3)  
**Solution:**

```javascript
function isRepdigit(num) {
    return new Set(String(num)).size === 1;
}
```

---

**Problem Title:** Volume of a Cone  
**Author:** [Ruud Peter Boelens](https://edabit.com/user/Akq3fQcPRgPrWfsye)  
**Solution:**

```javascript
function coneVolume(h, r) {
    return +(Math.PI * r * r * h / 3).toFixed(2);
}
```

---

**Problem Title:** Square Every Digit  
**Author:** [Enkuryo](https://edabit.com/user/Nc23QyxhdeFRwzj5W)  
**Solution:**

```javascript
function squareDigits(n) {
    return +String(n).split('').map(digit => digit * digit).join('');
}
```

---

**Problem Title:** Folding a Piece of Paper  
**Author:** [mkjlong](https://edabit.com/user/rgmhomEQqsnngdSJZ)  
**Solution:**

```javascript
function numLayers(n) {
    return `${0.0005 * Math.pow(2, n)}m`;
}
```

---

**Problem Title:** Algebra Sequence — Boxes  
**Author:** [Ruud Peter Boelens](https://edabit.com/user/Akq3fQcPRgPrWfsye)  
**Solution:**

```javascript
function boxSeq(step) {
    return step % 2 === 0 ? step : step + 2;
}
```

---

**Problem Title:** Move Capital Letters to the Front  
**Author:** [Helen Yu](https://edabit.com/user/mNMQvcxKSSvqqMYCH)  
**Solution:**

```javascript
function capToFront(s) {
    const capitalLetters = s.match(/[A-Z]/g) || [];
    const restLetters = s.replace(/[A-Z]/g, '');
    return capitalLetters.join('') + restLetters;
}
```

---

**Problem Title:** 25-Mile Marathon  
**Author:** [BijogFc24](https://edabit.com/user/Nb6LYPoQP6KJZt8mz)  
**Solution:**

```javascript
function marathonDistance(d) {
    return d.reduce((acc, curr) => acc + Math.abs(curr), 0) === 25;
}
```

---

**Problem Title:** Currying Functions  
**Author:** [Mubashir Hassan](https://edabit.com/user/T6iBEE2jp7f7iEF2P)  
**Solution:**

```javascript
function multiply(arr) {
    return function (num) {
        return arr.map(x => x * num);
    };
}
```


---
