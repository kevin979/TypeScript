# Enum

列舉有兩種做法，一種是直接使用ts內建的enum，另一種是使用class製作出仿enum的效果，絕大多數情況使用enum應就足夠應付，最主要差異在於enum無法設定多個屬性。

* enum

```typescript
enum DogVarietyEnum {
  LabradorRetriever = "拉布拉多犬",
  GoldenRetriever = "黃金獵犬",
  Dalmatian = "大麥町犬",
  Beagle = "米格魯",
  YorkshireTerrier = "約克夏",
  Pomerarian = "博美犬",
}

console.log(DogVarietyEnum.Beagle); \\米格魯
```

* class

```typescript
class DogVariety {
  public static readonly LabradorRetriever = new DogVariety("拉布拉多犬", "大");
  public static readonly GoldenRetriever = new DogVariety("黃金獵犬", "大");
  public static readonly Dalmatian = new DogVariety("大麥町犬", "大");
  public static readonly Beagle = new DogVariety("米格魯", "中");
  public static readonly YorkshireTerrier = new DogVariety("約克夏", "小");
  public static readonly Pomerarian = new DogVariety("博美犬", "小");

  constructor(public name: string, public size: string) {}
}

console.log(DogVariety.Beagle); \\DogVariety { name: '米格魯', size: '中' }
console.log(DogVariety.Beagle.name); \\米格魯
console.log(DogVariety.Beagle.size); \\中
```
