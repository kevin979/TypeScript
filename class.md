# Class

Class(類別)其實與多數後端OOP語言差不多，也是同時具有繼承、封裝、多型的特性，同樣可以做為資料結構、物件使用，也因此習慣Java、C#等語言的開發者在撰寫TS時可以快速上手，只是缺點就是IDE的支援度較差，無法協助開發者自動完成語法。

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

    public getName(): string {
        return this._name;
    }
    public setName(name: string) {
        this._name = name;
    }
    public getAge(): number {
        return this._age;
    }
    public setAge(age: number) {
        this._age = age;
    }
    public getAddress(): string {
        return this._address;
    }
    public setAddress(Address: string) {
        this._address = Address;
    }
    public getHeight(): number {
        return this._height;
    }
    public setHeight(height: number) {
        this._height = height;
    }
    public getWeight(): number {
        return this._weight;
    }
    public setWeight(weight: number) {
        this._weight = weight;
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
