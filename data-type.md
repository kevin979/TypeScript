# Data Type

### 資料型別介紹

TypeScript的基礎型別與多數後端語言相同，不外乎就是字串、數值、布林等，但也有著只有TS才有的獨特型別。

* 布林值：資料型別-boolean、物件-Boolean
* 字串：資料型別-string、物件-String
* 數值：資料型別-number、物件-Number

資料型別與物件的差異在於物件是將資料型別包裝後增加了Function可以使用。

除了上述三種常用的資料型別外，TS還有另外三種特別的資料型別。

* any - 可以做為任意型別，但必須有值，以後端語言來說就是noNull
* null - 這是所有型別的基礎資料型別，與any相同都是作為任意型別使用，只是可以允許使用null
* undefined - 這與null是相似的型別，只是這是屬於js的null(畢竟js沒有null只有undefined)

### 資料型別宣告

```typescript
let isRunning: boolean = false;
let count: number = 0;
let address: string;
```

進行變數宣告時建議給予變數預設值，避免後續coding時該變數會出現不可預期錯誤，如null之類的。

### 特殊資料型別宣告

再來是介紹any、null、undefined這三者的使用情境以及如何使用，通常會使用這三種資料型別多數是在進行資料介接時，因為值是從外部接回來的，所以不能保證一定會有值，除非對方文件有明確表示有值，否則再進行變數宣告時會建議連同特殊資料型別一併宣告。

```typescript
let age: number | null | undefined;
```

如果不確定介接回來的值是哪種資料型態，但卻一定有值，可使用any進行資料宣告

```typescript
let birthDay: any;
```

但是非必要時請不要使用any，如果通篇宣告都是any，那就與寫js並無差異了。

### 型別推論

在TS中會有一樣很特別的功能，就是型別推論，也就是說宣告變數時不指定型別，但會給予預設值，此時TS會依據給予的預設值強制給該變數對應的資料型別。

```typescript
// 以下兩種是相同意思
let count: number = 0;
let count = 0;
```

另外在TS中一個變數的資料型別是可以多種，也就是說一個變數可以是字串也可以是數值，只要在宣告時進行多型別宣告即可，但宣告後就不能更換型別了！

```typescript
let phone: number | string;
```
