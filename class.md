# Class

Class(類別)其實與多數後端OOP語言差不多，也是同時具有繼承、封裝、多型的特性，同樣可以做為資料結構、物件使用，也因此習慣Java、C#等語言的開發者在撰寫TS時可以快速上手，只是缺點就是IDE的支援度較差，無法協助開發者快速完成語法。

### 建構子constructor

```typescript
class Person {
    private _name: string;
    private _age: number;
    private _address: string;
    private _height: number;
    private _weight: number;

    constructor(name: string, height: number, weight: number) {
        this._name = name;
        this._height = height;
        this._weight = weight;
    }
}

let person:Person = new Person("John", 180, 65);
```

以Person這個class範例來看，當要使用Person時就必須傳入三個參數，否則IDE檢查時會有錯誤。

### 修飾詞

* private
* public
* protected

### 靜態方法

* static

### 存取器

```typescript
class Person {
    private _name: string;
    private _age: number;
    private _address: string;
    private _height: number;
    private _weight: number;

    public get name(): string {
        return this._name;
    }

    public set name(value: string) {
        this._name = value;
    }

    public get age(): number {
        return this._age;
    }

    public set age(value: number) {
        this._age = value;
    }

    public get address(): string {
        return this._address;
    }

    public set address(value: string) {
        this._address = value;
    }

    public get height(): number {
        return this._height;
    }

    public set height(value: number) {
        this._height = value;
    }

    public get weight(): number {
        return this._weight;
    }

    public set weight(value: number) {
        this._weight = value;
    }
}
```

### 唯讀(readonly)

其實就是Java中的final

```typescript
class Constants {
    private readonly _PROJECT_NAME = "TYPE_SCRIPT";

    public getProjectName(): string {
        return this._PROJECT_NAME;
    }
}
```

### 繼承(extends)

```typescript
abstract class Dog {
    private _name: string;
    public get name(): string {
        return this._name;
    }
    public set name(value: string) {
        this._name = value;
    }
    private _age: number;
    public get age(): number {
        return this._age;
    }
    public set age(value: number) {
        this._age = value;
    }

    abstract size: BodySizeEnum;
}

class Maltese extends Dog {
    size: BodySizeEnum = BodySizeEnum.Small;
}

enum BodySizeEnum {
    Small,
    Medium,
    Large
}
```

其實撰寫過程會跟一般寫Java、C#等語言非常雷同，如同範例會有一個dog的class，而Maltese是dog的一個品種，因此會繼承dog的一切屬性跟函式。

### 實作(implements)

```typescript
interface Animal {
    run();
    fly();
}

class Dog implements Animal {
    run() {
        console.log("fast");
    }
    fly() {
        throw new Error("Can't Fly");
    }
}
```

