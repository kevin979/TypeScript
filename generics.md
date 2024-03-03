# Generics

```typescript
class ArrayGenerics<T> {
    private _array: T[] = [];

    public add(...elements: T[]) {
        for (let element of elements) {
            this._array.push(element);
        }
    }

    public get array(): T[] {
        return this._array;
    }

    public size(): number {
        return this._array.length;
    }
}

let numArray: ArrayGenerics<number> = new ArrayGenerics<number>();
numArray.add(1, 2, 3);
numArray.add(4);
console.log(numArray.size()); //結果4
console.log(numArray.array); //結果[ 1, 2, 3, 4 ]
```
