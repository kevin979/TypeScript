# Function

### 函式宣告

<pre class="language-typescript"><code class="lang-typescript">function add(num1: number, num2: number): number {
    return num1 + num2;
}

<strong>let result = add(9, 6);
</strong></code></pre>

### 函式表示式

```typescript
let add = function (num1: number, num2: number): number {
    return num1 + num2;
}

let result = add(9, 6);
```

### 可選引數

```typescript
function power(num: number, power?: number): number {
    if (power == null) {
        power = 0;
    }
    return Math.pow(num, power);
}

console.log(power(2, 9)); // 結果512
console.log(power(2)); // 結果2
```

### 引數預設

```typescript
function division(dividend: number, divisor: number = 1): number {
    return dividend / divisor;
}

console.log(division(2, 10)); //結果0.2
console.log(division(2)); //結果2
```

### 不定長度引數

```typescript
function mutiplication(...nums: number[]): number {
    let result = 0;
    for (let num of nums) {
        result *= num;
    }
    return result;
}

console.log(mutiplication(1, 2, 3, 4, 5, 6, 7, 8, 9));
```

### 覆寫(overwrite)

```typescript
function sameType(a: string): string;
function sameType(a: boolean): boolean;
function sameType(a: number): number;
function sameType(a: string | boolean | number): string | boolean | number | null {
    if (typeof a == "string") {
        return "string";
    } else if (typeof a == "boolean") {
        return false;
    } else if (typeof a == "number") {
        return 0;
    }
    return null;
}

console.log(sameType("a")); //結果string
console.log(sameType(9)); //結果0
console.log(sameType(true)); //結果false
```
