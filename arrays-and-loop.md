# Arrays and Loop

### 陣列

```typescript
let nums: number[] = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9];
let names: Array<string> = new Array<string>();
names = ["Cat", "Dog", "Bird", "Fish"];
```

### 迴圈

```typescript
//使用of是印出該陣列的元素值
function printNum() {
    for (let num of nums) {
        console.log(num); //結果是0~9
    }
}

function printName() {
    for (let name of names) {
        console.log(name); //結果是"Cat", "Dog", "Bird", "Fish"
    }
}

//使用in是印出該元素的位置
function printNum() {
    for (let num in nums) {
        console.log(num); //結果是0~9
    }
}

function printName() {
    for (let name in names) {
        console.log(name); //結果是0~3
    }
}
```
