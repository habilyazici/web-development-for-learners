# 📘 JAVASCRIPT KAPSAMLI DERS NOTLARI

## 📑 İÇİNDEKİLER

1. [JavaScript Nedir?](#1-javascript-nedir)
2. [Geliştirme Ortamı](#2-geliştirme-ortamı)
3. [Değişkenler (Variables)](#3-değişkenler-variables)
4. [Veri Tipleri (Data Types)](#4-veri-tipleri-data-types)
5. [Operatörler (Operators)](#5-operatörler-operators)
6. [Koşullu İfadeler (Conditionals)](#6-koşullu-i̇fadeler-conditionals)
7. [Döngüler (Loops)](#7-döngüler-loops)
8. [Fonksiyonlar (Functions)](#8-fonksiyonlar-functions)
9. [Diziler (Arrays)](#9-diziler-arrays)
10. [Objeler (Objects)](#10-objeler-objects)
11. [String Metodları](#11-string-metodları)
12. [Array Metodları](#12-array-metodları)
13. [DOM Manipülasyonu](#13-dom-manipülasyonu)
14. [Olaylar (Events)](#14-olaylar-events)
15. [ES6+ Modern JavaScript](#15-es6-modern-javascript)
16. [Asenkron JavaScript](#16-asenkron-javascript)
17. [Hata Yönetimi (Error Handling)](#17-hata-yönetimi-error-handling)
18. [JSON](#18-json)
19. [Local Storage](#19-local-storage)
20. [Fetch API](#20-fetch-api)
21. [Sınıflar (Classes)](#21-sınıflar-classes)
22. [Modüller (Modules)](#22-modüller-modules)
23. [Regular Expressions (Regex)](#23-regular-expressions-regex)
24. [Map, Set, WeakMap, WeakSet](#24-map-set-weakmap-weakset)
25. [Symbol ve Iterator](#25-symbol-ve-iterator)
26. [Generator Fonksiyonlar](#26-generator-fonksiyonlar)
27. [Proxy ve Reflect](#27-proxy-ve-reflect)
28. [Web API'leri](#28-web-apileri)
29. [Performans ve Optimizasyon](#29-performans-ve-optimizasyon)
30. [Pratik Projeler ve Örnekler](#30-pratik-projeler-ve-örnekler)

# 1. JavaScript Nedir?

JavaScript, web tarayıcılarında çalışan, **dinamik**, **yorumlanan** (interpreted) ve **nesne tabanlı** (object-oriented) bir programlama dilidir. 1995 yılında Brendan Eich tarafından Netscape için geliştirilmiştir.

### JavaScript'in Temel Özellikleri:

- **Dinamik tipli dil:** Değişken tipleri çalışma zamanında (runtime) belirlenir
- **Yorumlanan dil:** Derleme (compile) adımı olmadan doğrudan çalıştırılır
- **Prototip tabanlı nesne yönelimli:** Class yerine prototype zinciri kullanır (ES6 ile class sözdizimi eklendi)
- **First-class fonksiyonlar:** Fonksiyonlar değişkenlere atanabilir, parametre olarak geçilebilir
- **Event-driven:** Olay tabanlı programlama modeli
- **Single-threaded:** Tek iş parçacıklı çalışır (Event Loop ile asenkron işlemler yapılır)

### JavaScript Nerelerde Kullanılır?

```
✅ Web Tarayıcıları (Frontend)     → React, Vue, Angular
✅ Sunucu Tarafı (Backend)         → Node.js, Deno, Bun
✅ Mobil Uygulama                  → React Native, Ionic
✅ Masaüstü Uygulama               → Electron
✅ Oyun Geliştirme                 → Phaser, Three.js
✅ IoT (Nesnelerin İnterneti)      → Johnny-Five
✅ Yapay Zeka / ML                 → TensorFlow.js
``` 

## 1.2 JavaScript vs Java

| Özellik        | JavaScript         | Java               |
|----------------|--------------------|--------------------|
| Tip Sistemi    | Dinamik            | Statik             |
| Çalışma Ortamı | Tarayıcı + Node.js | JVM                |
| Derleme        | Yorumlanan         | Derlenen           |
| OOP            | Prototip tabanlı   | Sınıf tabanlı      |
| Sözdizimi      | C benzeri          | C benzeri          |
| Kullanım       | Web, Full-stack    | Enterprise, Android|

## 1.3 ECMAScript Nedir?

ECMAScript, JavaScript'in standartlaştırılmış halidir. ECMA International tarafından yönetilir.

| Sürüm            | Yıl | Önemli Özellikler |
|------------------|-----|-------------------|
| ES1              | 1997 | İlk sürüm |
| ES3              | 1999 | try/catch, RegExp |
| ES5              | 2009 | strict mode, JSON, Array metodları |
| ES6 (ES2015)     | 2015 | let/const, arrow functions, class, Promise, template literals |
| ES7 (ES2016)     | 2016 | Array.includes(), üs operatörü (**) |
| ES8 (ES2017)     | 2017 | async/await, Object.entries() |
| ES9 (ES2018)     | 2018 | Rest/Spread properties, for await...of |
| ES10 (ES2019)    | 2019 | Array.flat(), Object.fromEntries() |
| ES11 (ES2020)    | 2020 | Optional chaining (?.), Nullish coalescing (??) |
| ES12 (ES2021)    | 2021 | replaceAll(), Promise.any() |
| ES13 (ES2022)    | 2022 | Top-level await, .at() metodu |
| ES14 (ES2023)    | 2023 | Array findLast(), toSorted() |

# 2. Geliştirme Ortamı

## 2.1 Tarayıcı Konsolu

En hızlı yol: Tarayıcıda `F12` tuşuna basıp **Console** sekmesine geçmek.

```javascript
// Konsola yazdırma
console.log("Merhaba Dünya!");        // Normal mesaj
console.warn("Bu bir uyarıdır!");     // Sarı uyarı mesajı
console.error("Bu bir hatadır!");     // Kırmızı hata mesajı
console.info("Bu bir bilgidir.");     // Bilgi mesajı
console.table([1, 2, 3]);            // Tablo formatında gösterir
console.clear();                      // Konsolu temizler
```

## 2.2 HTML İçinde JavaScript

```html
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <title>JavaScript Temelleri</title>
</head>
<body>
    <h1>JavaScript Öğreniyorum</h1>

    <!-- Yöntem 1: Satır İçi (Inline) - ÖNERİLMEZ -->
    <button onclick="alert('Merhaba!')">Tıkla</button>

    <!-- Yöntem 2: Dahili (Internal) Script -->
    <script>
        console.log("Bu dahili script'tir.");
    </script>

    <!-- Yöntem 3: Harici (External) Script - EN İYİ YÖNTEM -->
    <script src="script.js"></script>
</body>
</html>
```

## 2.4 console Objesinin Tüm Metodları

```javascript
// 1. console.log() - Genel çıktı
console.log("Merhaba");
console.log("Ad:", "Ali", "Yaş:", 25);

// 2. console.warn() - Uyarı
console.warn("Dikkat! Bu işlem yavaş olabilir.");

// 3. console.error() - Hata
console.error("Bağlantı hatası oluştu!");

// 4. console.info() - Bilgi
console.info("Sistem başarıyla başlatıldı.");

// 5. console.table() - Tablo formatı
const ogrenciler = [
    { ad: "Ali", yas: 20 },
    { ad: "Ayşe", yas: 22 },
    { ad: "Mehmet", yas: 21 }
];
console.table(ogrenciler);

// 6. console.group() / console.groupEnd() - Gruplama
console.group("Kullanıcı Bilgileri");
console.log("Ad: Ali");
console.log("Yaş: 25");
console.groupEnd();

// 7. console.time() / console.timeEnd() - Süre ölçme
console.time("döngü süresi");
for (let i = 0; i < 1000000; i++) { }
console.timeEnd("döngü süresi"); // döngü süresi: 5.123ms

// 8. console.count() - Sayaç
console.count("tıklama"); // tıklama: 1
console.count("tıklama"); // tıklama: 2
console.count("tıklama"); // tıklama: 3

// 9. console.assert() - Koşullu hata
console.assert(1 === 2, "1, 2'ye eşit değil!"); // Hata mesajı gösterir
console.assert(1 === 1, "Bu mesaj gösterilmez"); // Koşul doğru, mesaj yok

// 10. console.dir() - Obje detayı
console.dir(document.body);

// 11. console.trace() - Çağrı yığını
function a() { b(); }
function b() { c(); }
function c() { console.trace("İz sürme"); }
a(); // Fonksiyon çağrı sırasını gösterir
```

# 3. Değişkenler (Variables)

### var (Eski Yöntem - ES5)

```javascript
var isim = "Ali";
var yas = 25;
var ogrenciMi = true;

// var ile aynı isimde tekrar tanımlama YAPILABILIR (sorunludur!)
var isim = "Veli"; // Hata vermez!
console.log(isim); // "Veli"

// var fonksiyon kapsamlıdır (function-scoped)
function ornek() {
    var x = 10;
    if (true) {
        var x = 20; // Aynı x'i değiştirir!
        console.log(x); // 20
    }
    console.log(x); // 20 (!)
}
ornek();
```

### let (Modern Yöntem - ES6)

```javascript
let isim = "Ali";
let yas = 25;

// let ile aynı isimde tekrar tanımlama YAPILAMAZ
// let isim = "Veli"; // ❌ SyntaxError: Identifier 'isim' has already been declared

// Ama değeri değiştirilebilir
isim = "Veli"; // ✅ Sorun yok
console.log(isim); // "Veli"

// let blok kapsamlıdır (block-scoped)
function ornek() {
    let x = 10;
    if (true) {
        let x = 20; // Farklı bir x! (blok kapsamı)
        console.log(x); // 20
    }
    console.log(x); // 10 (orijinal x korunur)
}
ornek();
```

### const (Sabit - ES6)

```javascript
const PI = 3.14159;
const SITE_ADI = "Öğrenci Portal";

// const ile tanımlanan değişkenin değeri DEĞİŞTİRİLEMEZ
// PI = 3.14; // ❌ TypeError: Assignment to constant variable

// const ile tanımlarken değer VERMEK ZORUNLUDUR
// const x; // ❌ SyntaxError: Missing initializer in const declaration

// DİKKAT: const ile tanımlanan obje ve dizilerin İÇERİĞİ değiştirilebilir!
const kullanici = { ad: "Ali", yas: 25 };
kullanici.yas = 26; // ✅ İçerik değiştirilebilir!
console.log(kullanici); // { ad: "Ali", yas: 26 }

// kullanici = {}; // ❌ Referans değiştirilemez!

const sayilar = [1, 2, 3];
sayilar.push(4); // ✅ İçerik değiştirilebilir!
console.log(sayilar); // [1, 2, 3, 4]

// sayilar = [5, 6]; // ❌ Referans değiştirilemez!
```

## 3.4 Hoisting (Kaldırma)

JavaScript, değişken ve fonksiyon tanımlamalarını kodun en üstüne "kaldırır".

```javascript
// === var ile Hoisting ===
console.log(mesaj); // undefined (hata vermez!)
var mesaj = "Merhaba";
console.log(mesaj); // "Merhaba"

// JavaScript yukarıdaki kodu şöyle yorumlar:
// var mesaj;              ← tanımlama kaldırıldı
// console.log(mesaj);     ← undefined
// mesaj = "Merhaba";      ← atama yerinde kaldı
// console.log(mesaj);     ← "Merhaba"

// === let ile Hoisting (TDZ - Temporal Dead Zone) ===
// console.log(isim); // ❌ ReferenceError: Cannot access 'isim' before initialization
let isim = "Ali";
console.log(isim); // "Ali"

// === const ile Hoisting (TDZ) ===
// console.log(YAS); // ❌ ReferenceError
const YAS = 25;

// === Fonksiyon Hoisting ===
selamla(); // ✅ "Merhaba!" - Fonksiyon tanımlamaları tamamen kaldırılır
function selamla() {
    console.log("Merhaba!");
}

// Fonksiyon ifadeleri kaldırılmaz!
// merhabaDe(); // ❌ TypeError: merhabaDe is not a function
var merhabaDe = function() {
    console.log("Merhaba!");
};
```

## 3.5 Değişken İsimlendirme Kuralları

```javascript
// ✅ GEÇERLİ İSİMLER
let isim = "Ali";
let _ozel = "özel değişken";
let $dolar = "jQuery tarzı";
let camelCase = "deve yazımı";
let isim2 = "sayı ile bitiyor";
let İsim = "Türkçe karakter (geçerli ama önerilmez)";

// ❌ GEÇERSİZ İSİMLER
// let 2isim = "Sayı ile başlayamaz";
// let my-name = "Tire (-) kullanılamaz";
// let my name = "Boşluk kullanılamaz";
// let class = "Ayrılmış kelime kullanılamaz";
// let return = "Ayrılmış kelime";

// 📝 İSİMLENDİRME KURALLARI (Convention)
let firstName = "Ali";         // camelCase → Değişkenler ve fonksiyonlar için
const MAX_SIZE = 100;          // UPPER_SNAKE_CASE → Sabitler için
let _privateVar = "gizli";    // Alt çizgi ile başlama → Özel/gizli değişkenler
// class UserProfile {}        // PascalCase → Sınıflar için
// let isActive = true;        // is/has prefix → Boolean değerler için

// 💡 ANLAMLI İSİMLER KULLANIN
// ❌ Kötü isimlendirme
let x = "Ali Yılmaz";
let d = new Date();
let arr = [1, 2, 3];

// ✅ İyi isimlendirme
let kullaniciAdi = "Ali Yılmaz";
let bugun = new Date();
let notlar = [90, 85, 95];
```

## 3.6 JavaScript Ayrılmış Kelimeleri (Reserved Words)

```
abstract  arguments  await     boolean   break     byte
case      catch      char      class     const     continue
debugger  default    delete    do        double    else
enum      eval      export    extends   false     final
finally   float     for       function  goto      if
implements import   in        instanceof int      interface
let       long      native    new       null      package
private   protected public    return    short     static
super     switch    synchronized this   throw     throws
transient true      try       typeof    undefined var
void      volatile  while     with      yield
```

# 4. Veri Tipleri (Data Types)

JavaScript'te 8 temel veri tipi vardır. Bunlar 2 ana kategoriye ayrılır:

## 4.1 İlkel (Primitive) Veri Tipleri

İlkel tipler **değiştirilemez** (immutable) ve **değer olarak kopyalanır**.

### 4.1.1 String (Metin)

```javascript
// String tanımlama yolları
let tek = 'Tek tırnak';
let cift = "Çift tırnak";
let sablon = `Şablon literal (Template Literal)`;

// Kaçış karakterleri (Escape Characters)
let yeniSatir = "Satır 1\nSatır 2";        // Yeni satır
let tab = "Sütun1\tSütun2";                // Tab
let tirnak = "O \"harika\" dedi.";           // Çift tırnak
let tekTirnak = 'It\'s a test';             // Tek tırnak
let tersBolme = "C:\\Users\\Ali";           // Ters bölme
let unicode = "\u0041";                     // 'A' (Unicode)

console.log(yeniSatir);
// Satır 1
// Satır 2

// Template Literals (Şablon Değişmezleri) - ES6
let ad = "Ali";
let yas = 25;
let mesaj = `Merhaba, ben ${ad} ve ${yas} yaşındayım.`;
console.log(mesaj); // "Merhaba, ben Ali ve 25 yaşındayım."

// Template Literal ile çok satırlı string
let html = `
    <div class="kart">
        <h2>${ad}</h2>
        <p>Yaş: ${yas}</p>
    </div>
`;

// Template Literal içinde ifade kullanma
let a = 10, b = 20;
console.log(`Toplam: ${a + b}`);           // "Toplam: 30"
console.log(`Çift mi? ${a % 2 === 0}`);   // "Çift mi? true"
console.log(`Büyük harf: ${ad.toUpperCase()}`); // "Büyük harf: ALİ"

// String uzunluğu
let kelime = "JavaScript";
console.log(kelime.length); // 10

// String indeksleme (0'dan başlar)
console.log(kelime[0]);     // "J"
console.log(kelime[4]);     // "S"
console.log(kelime[kelime.length - 1]); // "t" (son karakter)

// String değiştirilemez (immutable)
let str = "Merhaba";
str[0] = "m"; // Hata vermez ama değiştirmez!
console.log(str); // "Merhaba" (değişmedi)
```

### 4.1.2 Number (Sayı)

```javascript
// JavaScript'te tüm sayılar 64-bit kayan noktalı (float) sayıdır
let tamSayi = 42;
let ondalik = 3.14;
let negatif = -17;
let bilimsel = 2.5e6;    // 2500000 (2.5 × 10^6)
let kucuk = 7.3e-3;      // 0.0073
let hex = 0xFF;           // 255 (16'lık)
let oktal = 0o77;         // 63 (8'lik)
let binary = 0b1010;      // 10 (2'lik)

// Özel sayısal değerler
console.log(Infinity);         // Sonsuz
console.log(-Infinity);        // Negatif sonsuz
console.log(NaN);              // Not a Number (Sayı değil)

// NaN kontrolleri
console.log(NaN === NaN);          // false (!)
console.log(isNaN(NaN));           // true
console.log(isNaN("hello"));       // true (string → NaN)
console.log(isNaN("123"));         // false (string → 123)
console.log(Number.isNaN(NaN));    // true (daha güvenli)
console.log(Number.isNaN("hello")); // false (tip dönüşümü yapmaz)

// Sayı limitleri
console.log(Number.MAX_SAFE_INTEGER);  // 9007199254740991
console.log(Number.MIN_SAFE_INTEGER);  // -9007199254740991
console.log(Number.MAX_VALUE);         // 1.7976931348623157e+308
console.log(Number.MIN_VALUE);         // 5e-324
console.log(Number.POSITIVE_INFINITY); // Infinity
console.log(Number.NEGATIVE_INFINITY); // -Infinity
console.log(Number.EPSILON);           // 2.220446049250313e-16

// ⚠️ Kayan Nokta Hassasiyet Problemi
console.log(0.1 + 0.2);           // 0.30000000000000004 (!)
console.log(0.1 + 0.2 === 0.3);   // false (!)

// Çözüm 1: toFixed()
console.log((0.1 + 0.2).toFixed(1));       // "0.3" (string döner!)
console.log(parseFloat((0.1 + 0.2).toFixed(1))); // 0.3

// Çözüm 2: Epsilon karşılaştırma
console.log(Math.abs(0.1 + 0.2 - 0.3) < Number.EPSILON); // true

// Sayı dönüşümleri
console.log(Number("123"));       // 123
console.log(Number("12.5"));      // 12.5
console.log(Number(""));          // 0
console.log(Number(" "));         // 0
console.log(Number("hello"));     // NaN
console.log(Number(true));        // 1
console.log(Number(false));       // 0
console.log(Number(null));        // 0
console.log(Number(undefined));   // NaN

console.log(parseInt("123abc"));    // 123
console.log(parseInt("abc123"));    // NaN
console.log(parseInt("10", 2));     // 2 (ikili sistemden)
console.log(parseInt("FF", 16));    // 255 (16'lık sistemden)
console.log(parseFloat("3.14m"));   // 3.14
```

### 4.1.3 BigInt (Büyük Tamsayı)

```javascript
// Normal sayı limiti aşıldığında BigInt kullanılır
let buyukSayi = 9007199254740991n;
let digerBuyuk = BigInt("9007199254740992");

console.log(buyukSayi + 1n);  // 9007199254740992n
console.log(buyukSayi * 2n);  // 18014398509481982n

// ⚠️ BigInt ile normal sayı karıştırılamaz!
// console.log(buyukSayi + 1); // ❌ TypeError
console.log(buyukSayi + BigInt(1)); // ✅ 9007199254740992n
```

### 4.1.4 Boolean (Mantıksal)

```javascript
let dogruMu = true;
let yanlisMi = false;

// Truthy ve Falsy Değerler
// JavaScript'te her değer boolean bağlamda true veya false olarak değerlendirilir

// ❌ FALSY Değerler (false olarak değerlendirilen):
console.log(Boolean(false));      // false
console.log(Boolean(0));          // false
console.log(Boolean(-0));         // false
console.log(Boolean(0n));         // false (BigInt sıfır)
console.log(Boolean(""));         // false (boş string)
console.log(Boolean(null));       // false
console.log(Boolean(undefined));  // false
console.log(Boolean(NaN));        // false

// ✅ TRUTHY Değerler (true olarak değerlendirilen):
console.log(Boolean(true));       // true
console.log(Boolean(1));          // true
console.log(Boolean(-1));         // true
console.log(Boolean(42));         // true
console.log(Boolean("hello"));   // true
console.log(Boolean("0"));       // true (!) - "0" boş string değil!
console.log(Boolean("false"));   // true (!) - "false" boş string değil!
console.log(Boolean([]));        // true (!) - boş dizi bile truthy
console.log(Boolean({}));        // true (!) - boş obje bile truthy
console.log(Boolean(function(){})); // true

// Pratik kullanım
let kullaniciAdi = "";
if (kullaniciAdi) {
    console.log("Kullanıcı adı var");
} else {
    console.log("Kullanıcı adı boş"); // Bu çalışır
}
```

### 4.1.5 undefined

```javascript
// Değer atanmamış değişkenler undefined'dır
let x;
console.log(x);        // undefined
console.log(typeof x);  // "undefined"

// Fonksiyondan değer dönmezse undefined döner
function selamla() {
    console.log("Merhaba");
    // return ifadesi yok
}
let sonuc = selamla(); // "Merhaba" yazdırır
console.log(sonuc);    // undefined

// Objenin olmayan özelliği undefined döner
let obj = { ad: "Ali" };
console.log(obj.yas);  // undefined

// Dizi dışı indeks
let arr = [1, 2, 3];
console.log(arr[10]);  // undefined
```

### 4.1.6 null

```javascript
// null, bilinçli olarak "değer yok" anlamında kullanılır
let seciliOge = null;
console.log(seciliOge);        // null
console.log(typeof seciliOge); // "object" (!) - JavaScript'in bilinen bir bug'ı

// null vs undefined
console.log(null === undefined);  // false (tip farklı)
console.log(null == undefined);   // true (değer benzer)
console.log(null === null);       // true

// Pratik kullanım
let kullanici = null; // Henüz giriş yapılmamış

function girisYap(ad) {
    kullanici = { ad: ad, girisZamani: new Date() };
}

function cikisYap() {
    kullanici = null; // Kullanıcıyı temizle
}
```

### 4.1.7 Symbol (ES6)

```javascript
// Symbol, benzersiz ve değiştirilemez bir tanımlayıcıdır
let sym1 = Symbol();
let sym2 = Symbol();
console.log(sym1 === sym2);  // false (her Symbol benzersiz)

let sym3 = Symbol("açıklama");
let sym4 = Symbol("açıklama");
console.log(sym3 === sym4);  // false (açıklama aynı olsa bile)

console.log(sym3.toString());    // "Symbol(açıklama)"
console.log(sym3.description);   // "açıklama"

// Obje özellik anahtarı olarak kullanım
const ID = Symbol("id");
let kullanici = {
    ad: "Ali",
    [ID]: 12345
};
console.log(kullanici[ID]);  // 12345

// Symbol for-in döngüsünde görünmez
for (let key in kullanici) {
    console.log(key); // Sadece "ad" yazdırır, ID görünmez
}
```

## 4.2 Referans (Non-Primitive) Veri Tipleri

### 4.2.1 Object (Nesne)

```javascript
let kullanici = {
    ad: "Ali",
    yas: 25,
    hobiler: ["kitap", "müzik"],
    adres: {
        sehir: "İstanbul",
        ilce: "Kadıköy"
    }
};
```

### 4.2.2 Array (Dizi)

```javascript
let renkler = ["kırmızı", "yeşil", "mavi"];
let karisik = [1, "ali", true, null, { x: 1 }, [1, 2]];
```

### 4.2.3 Function (Fonksiyon)

```javascript
function topla(a, b) {
    return a + b;
}
```

> 📝 Bu tipler ilerleyen bölümlerde detaylı anlatılacaktır.

## 4.3 typeof Operatörü

```javascript
console.log(typeof "Merhaba");    // "string"
console.log(typeof 42);           // "number"
console.log(typeof 42n);          // "bigint"
console.log(typeof true);         // "boolean"
console.log(typeof undefined);    // "undefined"
console.log(typeof null);         // "object" (!) - tarihsel bug
console.log(typeof Symbol());     // "symbol"
console.log(typeof {});           // "object"
console.log(typeof []);           // "object" (!) - dizi de object
console.log(typeof function(){}); // "function"
console.log(typeof NaN);          // "number" (!) - NaN bir number

// Dizi kontrolü
console.log(Array.isArray([]));        // true
console.log(Array.isArray({}));        // false
console.log([] instanceof Array);      // true
```

## 4.4 Tip Dönüşümleri (Type Conversion)

### Açık (Explicit) Dönüşüm

```javascript
// String'e dönüşüm
String(123);         // "123"
String(true);        // "true"
String(null);        // "null"
String(undefined);   // "undefined"
(123).toString();    // "123"
(255).toString(16);  // "ff" (16'lık)
(10).toString(2);    // "1010" (2'lik)

// Number'a dönüşüm
Number("123");       // 123
Number("");          // 0
Number("abc");       // NaN
Number(true);        // 1
Number(false);       // 0
Number(null);        // 0
Number(undefined);   // NaN
parseInt("42px");    // 42
parseFloat("3.14m"); // 3.14
+"123";              // 123 (unary +)

// Boolean'a dönüşüm
Boolean(1);          // true
Boolean(0);          // false
Boolean("");         // false
Boolean("hello");    // true
Boolean(null);       // false
!!1;                 // true (double negation)
!!"hello";           // true
!!0;                 // false
!!"";                // false
```

### Örtük (Implicit) Dönüşüm - Type Coercion

```javascript
// String birleştirme (+ operatörü ile)
console.log("5" + 3);       // "53" (number → string)
console.log("5" + true);    // "5true"
console.log("5" + null);    // "5null"
console.log("5" + undefined); // "5undefined"

// Aritmetik işlemlerde (- * / ile)
console.log("5" - 3);       // 2 (string → number)
console.log("5" * 2);       // 10
console.log("5" / 2);       // 2.5
console.log("5" - true);    // 4 (true → 1)
console.log("abc" - 1);     // NaN

// Karşılaştırmalarda
console.log("5" == 5);      // true (tip dönüşümü yapılır)
console.log("5" === 5);     // false (tip dönüşümü yapılmaz)
console.log(null == undefined); // true
console.log(null === undefined); // false

// ⚠️ Garip durumlar
console.log([] + []);        // "" (boş string)
console.log([] + {});        // "[object Object]"
console.log({} + []);        // 0 veya "[object Object]" (bağlama göre)
console.log(true + true);    // 2
console.log(true + false);   // 1
console.log("" == false);    // true
console.log("" === false);   // false
```

---

# 5. Operatörler (Operators)

## 5.1 Aritmetik Operatörler

```javascript
let a = 10, b = 3;

console.log(a + b);   // 13  → Toplama
console.log(a - b);   // 7   → Çıkarma
console.log(a * b);   // 30  → Çarpma
console.log(a / b);   // 3.3333... → Bölme
console.log(a % b);   // 1   → Mod (kalan)
console.log(a ** b);  // 1000 → Üs alma (ES7)

// Artırma ve Azaltma
let x = 5;
console.log(x++);  // 5 (önce değeri döner, sonra artırır)
console.log(x);    // 6
console.log(++x);  // 7 (önce artırır, sonra değeri döner)
console.log(x--);  // 7 (önce değeri döner, sonra azaltır)
console.log(x);    // 6
console.log(--x);  // 5 (önce azaltır, sonra değeri döner)

// Unary + ve -
console.log(+"5");     // 5 (string → number)
console.log(+true);    // 1
console.log(+false);   // 0
console.log(+"hello"); // NaN
```

## 5.2 Atama Operatörleri

```javascript
let x = 10;       // Atama

x += 5;   // x = x + 5   → 15
x -= 3;   // x = x - 3   → 12
x *= 2;   // x = x * 2   → 24
x /= 4;   // x = x / 4   → 6
x %= 4;   // x = x % 4   → 2
x **= 3;  // x = x ** 3  → 8

// Logical Assignment (ES2021)
let a = null;
a ??= "varsayılan";  // a = a ?? "varsayılan" → "varsayılan"

let b = 0;
b ||= 42;    // b = b || 42 → 42 (0 falsy olduğu için)

let c = 1;
c &&= 99;    // c = c && 99 → 99 (1 truthy olduğu için)
```

## 5.3 Karşılaştırma Operatörleri

```javascript
// == (Eşitlik - tip dönüşümü YAPAR)
console.log(5 == "5");      // true (!)
console.log(0 == false);    // true (!)
console.log("" == false);   // true (!)
console.log(null == undefined); // true (!)
console.log(NaN == NaN);    // false (!)

// === (Katı Eşitlik - tip dönüşümü YAPMAZ) ✅ ÖNERİLEN
console.log(5 === "5");     // false
console.log(0 === false);   // false

// != (Eşit Değil - tip dönüşümü YAPAR)
console.log(5 != "5");      // false (!)

// !== (Katı Eşit Değil) ✅ ÖNERİLEN
console.log(5 !== "5");     // true

// Büyüklük - Küçüklük
console.log(5 > 3);         // true
console.log(5 >= 5);        // true

// String karşılaştırma (Unicode sırasına göre)
console.log("a" < "b");     // true
console.log("Z" < "a");     // true (büyük harfler önce gelir)
console.log("2" > "12");    // true (!) - string karşılaştırma!
console.log(2 > 12);        // false - sayı karşılaştırma

// 🎯 KURAL: Her zaman === ve !== kullan!
```

## 5.4 Mantıksal Operatörler

```javascript
// && (VE / AND) - Her iki koşul da true olmalı
console.log(true && true);   // true
console.log(true && false);  // false
console.log(false && false); // false

// || (VEYA / OR) - En az bir koşul true olmalı
console.log(true || false);  // true
console.log(false || false); // false

// ! (DEĞİL / NOT)
console.log(!true);   // false
console.log(!0);      // true
console.log(!"");     // true

// Kısa Devre Değerlendirme (Short-Circuit Evaluation)
// && → İlk falsy değeri veya son değeri döner
console.log("Ali" && "Veli");    // "Veli" (ikisi de truthy → son değer)
console.log(0 && "Veli");        // 0 (ilk falsy değer)

// || → İlk truthy değeri veya son değeri döner
console.log("" || "Veli");       // "Veli" (ilk truthy)
console.log(0 || "" || "Ali");   // "Ali" (ilk truthy)

// ?? (Nullish Coalescing - ES2020)
// Sadece null ve undefined için varsayılan değer atar
// || operatöründen farkı: 0, "", false gibi değerler korunur
console.log(null ?? "varsayılan");      // "varsayılan"
console.log(undefined ?? "varsayılan"); // "varsayılan"
console.log(0 ?? "varsayılan");         // 0 (!) - 0 korunur
console.log("" ?? "varsayılan");        // "" (!) - boş string korunur

// || ile ?? farkı
console.log(0 || 42);   // 42 (0 falsy olduğu için)
console.log(0 ?? 42);   // 0 (0 null/undefined olmadığı için)
```

## 5.5 Ternary (Üçlü) Operatör

```javascript
// koşul ? doğruysa : yanlışsa
let yas = 20;
let durum = yas >= 18 ? "Yetişkin" : "Çocuk";
console.log(durum); // "Yetişkin"

// İç içe ternary
let puan = 85;
let notHarfi = puan >= 90 ? "A"
             : puan >= 80 ? "B"
             : puan >= 70 ? "C"
             : puan >= 60 ? "D"
             : "F";
console.log(notHarfi); // "B"
```

## 5.6 Optional Chaining (?.) - ES2020

```javascript
let kullanici = {
    ad: "Ali",
    adres: { sehir: "İstanbul" }
};

// Eski yöntem
let ilce = kullanici && kullanici.adres && kullanici.adres.ilce;

// Yeni yöntem (optional chaining)
let ilce2 = kullanici?.adres?.ilce;       // undefined (hata vermez!)
let sehir = kullanici?.adres?.sehir;      // "İstanbul"

// Fonksiyon çağrısında
let obj = {};
obj.selamla?.();  // undefined (hata vermez)

// Dizi erişiminde
let arr = null;
console.log(arr?.[0]);   // undefined (hata vermez)

// ?? ile birlikte kullanım
let sehirAdi = kullanici?.adres?.ilce ?? "Bilinmiyor";
console.log(sehirAdi); // "Bilinmiyor"
```

## 5.7 Spread (...) ve Rest (...) Operatörleri

```javascript
// SPREAD: Dizi/objeyi yayar (açar)
let sayilar = [1, 2, 3];
let yeniSayilar = [...sayilar, 4, 5];
console.log(yeniSayilar); // [1, 2, 3, 4, 5]

// Dizi kopyalama
let kopya = [...sayilar];

// Dizi birleştirme
let a = [1, 2], b = [3, 4];
let birlesik = [...a, ...b]; // [1, 2, 3, 4]

// Obje yayma
let kisi = { ad: "Ali", yas: 25 };
let guncellenmis = { ...kisi, yas: 26, sehir: "İstanbul" };
console.log(guncellenmis); // { ad: "Ali", yas: 26, sehir: "İstanbul" }

// REST: Kalan elemanları toplar
function topla(...sayilar) {
    return sayilar.reduce((t, s) => t + s, 0);
}
console.log(topla(1, 2, 3, 4)); // 10

// Destructuring ile rest
let [ilk, ...kalanlar] = [1, 2, 3, 4, 5];
console.log(ilk);      // 1
console.log(kalanlar);  // [2, 3, 4, 5]

let { ad, ...digerBilgiler } = { ad: "Ali", yas: 25, sehir: "İstanbul" };
console.log(ad);             // "Ali"
console.log(digerBilgiler);  // { yas: 25, sehir: "İstanbul" }
```

## 5.8 Operatör Öncelikleri

```
Öncelik Sırası (Yüksekten Düşüğe):
1. ()           → Gruplama
2. ++ -- !      → Unary operatörler
3. **           → Üs alma
4. * / %        → Çarpma, bölme, mod
5. + -          → Toplama, çıkarma
6. < > <= >=    → Karşılaştırma
7. == != === !== → Eşitlik
8. &&           → Mantıksal VE
9. ||           → Mantıksal VEYA
10. ??          → Nullish coalescing
11. ? :         → Ternary
12. = += -= ... → Atama
```

---

# 6. Koşullu İfadeler (Conditionals)

## 6.1 if / if...else / if...else if...else

```javascript
// Basit if
let yas = 20;
if (yas >= 18) {
    console.log("Yetişkinsiniz.");
}

// if...else
let saat = 14;
if (saat < 12) {
    console.log("Günaydın!");
} else {
    console.log("İyi günler!");
}

// if...else if...else
let puan = 75;
if (puan >= 90) {
    console.log("Harf Notu: A");
} else if (puan >= 80) {
    console.log("Harf Notu: B");
} else if (puan >= 70) {
    console.log("Harf Notu: C");
} else if (puan >= 60) {
    console.log("Harf Notu: D");
} else {
    console.log("Harf Notu: F");
}

// Birden fazla koşul
let yas2 = 25;
let ehliyetVar = true;
if (yas2 >= 18 && ehliyetVar) {
    console.log("Araba kullanabilirsiniz.");
} else if (yas2 >= 18 && !ehliyetVar) {
    console.log("Ehliyet almanız gerekiyor.");
} else {
    console.log("Yaşınız yeterli değil.");
}
```

## 6.2 switch

```javascript
let gun = "Pazartesi";

switch (gun) {
    case "Pazartesi":
        console.log("Haftanın ilk günü");
        break;
    case "Salı":
    case "Çarşamba":
    case "Perşembe":
        console.log("Hafta ortası");
        break;
    case "Cuma":
        console.log("Neredeyse hafta sonu!");
        break;
    case "Cumartesi":
    case "Pazar":
        console.log("Hafta sonu! 🎉");
        break;
    default:
        console.log("Geçersiz gün");
}

// ⚠️ break unutulursa "fall-through" olur!
let sayi = 1;
switch (sayi) {
    case 1:
        console.log("Bir");   // Çalışır
        // break yok!
    case 2:
        console.log("İki");   // Bu da çalışır!
        break;
}
// Çıktı: "Bir" ve "İki" (break olmadığı için devam etti)
```

## 6.3 Guard Clause ve En İyi Uygulamalar

```javascript
// ❌ Kötü: İç içe if'ler
function islemYap(kullanici) {
    if (kullanici) {
        if (kullanici.aktif) {
            if (kullanici.yas >= 18) {
                return "İşlem başarılı";
            }
        }
    }
    return "Hata";
}

// ✅ İyi: Guard clause (Erken Çıkış)
function islemYap2(kullanici) {
    if (!kullanici) return "Kullanıcı bulunamadı";
    if (!kullanici.aktif) return "Kullanıcı aktif değil";
    if (kullanici.yas < 18) return "Yaş yeterli değil";
    return "İşlem başarılı";
}

// Obje lookup (switch/if-else alternatifi)
const gunler = {
    Monday: "Pazartesi", Tuesday: "Salı",
    Wednesday: "Çarşamba", Thursday: "Perşembe",
    Friday: "Cuma", Saturday: "Cumartesi", Sunday: "Pazar"
};
function gunTurkce(gun) {
    return gunler[gun] || "Bilinmiyor";
}
```

---

# 7. Döngüler (Loops)

## 7.1 for Döngüsü

```javascript
// Temel sözdizimi: for (başlangıç; koşul; artırma)
for (let i = 0; i < 5; i++) {
    console.log(i); // 0, 1, 2, 3, 4
}

// Geriye doğru sayma
for (let i = 10; i >= 0; i--) {
    console.log(i);
}

// 2'şer artırma
for (let i = 0; i <= 20; i += 2) {
    console.log(i); // 0, 2, 4, ..., 20
}

// Dizi üzerinde gezinme
let meyveler = ["elma", "armut", "kiraz", "üzüm"];
for (let i = 0; i < meyveler.length; i++) {
    console.log(`${i + 1}. ${meyveler[i]}`);
}

// İç içe döngü - Yıldız Üçgeni
for (let i = 1; i <= 5; i++) {
    let satir = "";
    for (let j = 1; j <= i; j++) {
        satir += "* ";
    }
    console.log(satir);
}
/*
*
* *
* * *
* * * *
* * * * *
*/
```

## 7.2 while ve do...while Döngüsü

```javascript
// while: Koşul doğru olduğu sürece çalışır
let sayac = 0;
while (sayac < 5) {
    console.log(sayac); // 0, 1, 2, 3, 4
    sayac++;
}

// do...while: En az 1 kez çalışır, sonra koşulu kontrol eder
let sayac2 = 10;
do {
    console.log(sayac2); // 10 (koşul false olsa bile 1 kez çalışır)
    sayac2++;
} while (sayac2 < 5);
```

## 7.3 for...of Döngüsü (ES6)

```javascript
// İterable objeler üzerinde gezinir (Array, String, Map, Set)

// Dizi
let renkler = ["kırmızı", "yeşil", "mavi"];
for (let renk of renkler) {
    console.log(renk);
}

// String
for (let harf of "Merhaba") {
    console.log(harf);
}

// Map
let harita = new Map([["ad", "Ali"], ["yas", 25]]);
for (let [anahtar, deger] of harita) {
    console.log(`${anahtar}: ${deger}`);
}

// entries() ile indeks alma
for (let [indeks, renk] of renkler.entries()) {
    console.log(`${indeks}: ${renk}`);
}
```

## 7.4 for...in Döngüsü

```javascript
// Obje anahtarları üzerinde gezinir
let kullanici = { ad: "Ali", yas: 25, sehir: "İstanbul" };

for (let anahtar in kullanici) {
    console.log(`${anahtar}: ${kullanici[anahtar]}`);
}

// ⚠️ DİKKAT: for...in diziler için ÖNERİLMEZ!
// Prototip zincirindeki özellikleri de gezer ve sıra garantisi yoktur
```

## 7.5 break ve continue

```javascript
// break → Döngüyü tamamen sonlandırır
for (let i = 0; i < 10; i++) {
    if (i === 5) break;
    console.log(i); // 0, 1, 2, 3, 4
}

// continue → Mevcut iterasyonu atlar
for (let i = 0; i < 10; i++) {
    if (i % 2 === 0) continue; // Çift sayıları atla
    console.log(i); // 1, 3, 5, 7, 9
}

// Etiketli break - İç içe döngülerde
dis: for (let i = 0; i < 3; i++) {
    for (let j = 0; j < 3; j++) {
        if (i === 1 && j === 1) break dis;
        console.log(`i=${i}, j=${j}`);
    }
}
```

## 7.6 forEach (Dizi Metodu)

```javascript
let meyveler2 = ["elma", "armut", "kiraz"];

meyveler2.forEach((meyve, indeks) => {
    console.log(`${indeks}: ${meyve}`);
});

// ⚠️ forEach'dan break ile çıkılamaz!
// ⚠️ forEach return ile değer döndürmez
```

## 7.7 Pratik Döngü Örnekleri

```javascript
// 1. FizzBuzz (Klasik mülakat sorusu)
for (let i = 1; i <= 100; i++) {
    if (i % 15 === 0) console.log("FizzBuzz");
    else if (i % 3 === 0) console.log("Fizz");
    else if (i % 5 === 0) console.log("Buzz");
    else console.log(i);
}

// 2. Asal sayı kontrolü
function asalMi(n) {
    if (n < 2) return false;
    for (let i = 2; i <= Math.sqrt(n); i++) {
        if (n % i === 0) return false;
    }
    return true;
}

// 3. Fibonacci dizisi
function fibonacci(n) {
    let fib = [0, 1];
    for (let i = 2; i < n; i++) {
        fib[i] = fib[i - 1] + fib[i - 2];
    }
    return fib;
}
console.log(fibonacci(10)); // [0, 1, 1, 2, 3, 5, 8, 13, 21, 34]

// 4. String ters çevirme
function tersCevir(str) {
    let sonuc = "";
    for (let i = str.length - 1; i >= 0; i--) {
        sonuc += str[i];
    }
    return sonuc;
}
console.log(tersCevir("Merhaba")); // "abahreM"
```

---

# 8. Fonksiyonlar (Functions)

## 8.1 Fonksiyon Nedir?

Fonksiyonlar, belirli bir görevi yerine getiren, yeniden kullanılabilir kod bloklarıdır. DRY (Don't Repeat Yourself) prensibinin temelidir.

## 8.2 Fonksiyon Tanımlama Yolları

### Function Declaration (Fonksiyon Bildirimi)

```javascript
// En temel yöntem - hoisting destekler
function selamla(isim) {
    return `Merhaba, ${isim}!`;
}
console.log(selamla("Ali")); // "Merhaba, Ali!"

// Hoisting sayesinde tanımlamadan önce çağrılabilir
console.log(topla(3, 5)); // 8 (hata vermez!)
function topla(a, b) {
    return a + b;
}
```

### Function Expression (Fonksiyon İfadesi)

```javascript
// Değişkene atanan fonksiyon - hoisting DESTEKLEMEZ
const selamla = function(isim) {
    return `Merhaba, ${isim}!`;
};
console.log(selamla("Ali")); // "Merhaba, Ali!"

// İsimli fonksiyon ifadesi (debugging için faydalı)
const faktoriyel = function fakt(n) {
    if (n <= 1) return 1;
    return n * fakt(n - 1); // İç isimle kendini çağırabilir
};
console.log(faktoriyel(5)); // 120
```

### Arrow Function (Ok Fonksiyonu) - ES6

```javascript
// Kısa ve modern sözdizimi
const selamla = (isim) => {
    return `Merhaba, ${isim}!`;
};

// Tek parametre ise parantez isteğe bağlı
const kare = x => x * x;
console.log(kare(4)); // 16

// Tek satır ise süslü parantez ve return gerekmez
const topla = (a, b) => a + b;
console.log(topla(3, 5)); // 8

// Parametresiz
const selamVer = () => "Merhaba!";

// Obje döndürme (parantez gerekli!)
const kullaniciOlustur = (ad, yas) => ({ ad, yas });
console.log(kullaniciOlustur("Ali", 25)); // { ad: "Ali", yas: 25 }

// ⚠️ Arrow function'ların farklılıkları:
// 1. Kendi `this` bağlamı YOKTUR (lexical this)
// 2. arguments objesi YOKTUR
// 3. new ile kullanılamaz (constructor olamaz)
// 4. prototype özelliği YOKTUR

// this farklılığı örneği:
const obje = {
    ad: "Ali",
    normalFonk: function() {
        console.log(this.ad); // "Ali" (objenin this'i)
    },
    arrowFonk: () => {
        console.log(this.ad); // undefined (dış scope'un this'i)
    }
};
```

## 8.3 Parametreler

```javascript
// Varsayılan Parametreler (Default Parameters) - ES6
function selamla(isim = "Misafir", saat = new Date().getHours()) {
    if (saat < 12) return `Günaydın, ${isim}!`;
    return `İyi günler, ${isim}!`;
}
console.log(selamla());        // "İyi günler, Misafir!"
console.log(selamla("Ali"));   // "İyi günler, Ali!"

// Rest Parametresi (...) - Sınırsız parametre alma
function toplam(...sayilar) {
    return sayilar.reduce((acc, val) => acc + val, 0);
}
console.log(toplam(1, 2, 3));       // 6
console.log(toplam(1, 2, 3, 4, 5)); // 15

// Rest ile normal parametrelerin birlikte kullanımı
function bilgiYazdir(baslik, ...icerikler) {
    console.log(`--- ${baslik} ---`);
    icerikler.forEach(icerik => console.log(`- ${icerik}`));
}
bilgiYazdir("Meyveler", "Elma", "Armut", "Kiraz");

// Destructuring Parametreleri
function kullaniciBilgi({ ad, yas, sehir = "Bilinmiyor" }) {
    return `${ad}, ${yas} yaşında, ${sehir}`;
}
console.log(kullaniciBilgi({ ad: "Ali", yas: 25 }));
// "Ali, 25 yaşında, Bilinmiyor"
```

## 8.4 Return (Dönüş Değeri)

```javascript
// Fonksiyonlar tek bir değer döndürür
function topla(a, b) {
    return a + b;
    console.log("Bu satır çalışmaz!"); // return sonrası kod çalışmaz
}

// Birden fazla değer döndürme (obje veya dizi ile)
function bolmeIslemi(bolunen, bolen) {
    return {
        sonuc: Math.floor(bolunen / bolen),
        kalan: bolunen % bolen
    };
}
const { sonuc, kalan } = bolmeIslemi(17, 5);
console.log(`Sonuç: ${sonuc}, Kalan: ${kalan}`); // "Sonuç: 3, Kalan: 2"

// return ifadesi yoksa undefined döner
function selamla() {
    console.log("Merhaba");
}
console.log(selamla()); // undefined
```

## 8.5 Scope (Kapsam)

```javascript
// Global Scope
let globalDegisken = "Ben globalim";

function disaridaki() {
    // Function Scope
    let fonksiyonDegisken = "Ben fonksiyon kapsamındayım";

    if (true) {
        // Block Scope
        let blokDegisken = "Ben blok kapsamındayım";
        console.log(globalDegisken);    // ✅ Erişilebilir
        console.log(fonksiyonDegisken); // ✅ Erişilebilir
        console.log(blokDegisken);      // ✅ Erişilebilir
    }

    console.log(globalDegisken);    // ✅ Erişilebilir
    console.log(fonksiyonDegisken); // ✅ Erişilebilir
    // console.log(blokDegisken);   // ❌ ReferenceError
}

// console.log(fonksiyonDegisken); // ❌ ReferenceError
```

## 8.6 Closure (Kapanış)

```javascript
// Closure: Bir fonksiyonun dış kapsamdaki değişkenlere erişimi korumasıdır
function sayacOlustur() {
    let deger = 0; // Bu değişken dışarıdan erişilemez (private)

    return {
        artir: () => ++deger,
        azalt: () => --deger,
        degerAl: () => deger
    };
}

const sayac = sayacOlustur();
console.log(sayac.artir());   // 1
console.log(sayac.artir());   // 2
console.log(sayac.artir());   // 3
console.log(sayac.azalt());   // 2
console.log(sayac.degerAl()); // 2
// console.log(deger); // ❌ Erişilemez

// Closure ile fabrika fonksiyonu
function carpanOlustur(carpan) {
    return function(sayi) {
        return sayi * carpan;
    };
}

const ikiKati = carpanOlustur(2);
const ucKati = carpanOlustur(3);
console.log(ikiKati(5));  // 10
console.log(ucKati(5));   // 15

// ⚠️ Döngü ve Closure sorunu
for (var i = 0; i < 3; i++) {
    setTimeout(() => console.log(i), 100);
}
// 3, 3, 3 (hepsi 3 yazdırır! var fonksiyon kapsamlı)

// ✅ Çözüm 1: let kullan
for (let i = 0; i < 3; i++) {
    setTimeout(() => console.log(i), 100);
}
// 0, 1, 2

// ✅ Çözüm 2: IIFE kullan
for (var i = 0; i < 3; i++) {
    (function(j) {
        setTimeout(() => console.log(j), 100);
    })(i);
}
// 0, 1, 2
```

## 8.7 Callback Fonksiyonlar

```javascript
// Callback: Başka bir fonksiyona parametre olarak geçirilen fonksiyon
function islemYap(a, b, callback) {
    const sonuc = callback(a, b);
    console.log(`Sonuç: ${sonuc}`);
}

islemYap(5, 3, (x, y) => x + y); // "Sonuç: 8"
islemYap(5, 3, (x, y) => x * y); // "Sonuç: 15"

// Gerçek dünya örneği: Dizi sıralama
let isimler = ["Zeynep", "Ali", "Mehmet", "Ayşe"];
isimler.sort((a, b) => a.localeCompare(b, "tr"));
console.log(isimler); // ["Ali", "Ayşe", "Mehmet", "Zeynep"]

// Asenkron callback
function veriGetir(url, basariliCallback, hataCallback) {
    // Simülasyon
    setTimeout(() => {
        const basarili = Math.random() > 0.3;
        if (basarili) {
            basariliCallback({ data: "Veri geldi!" });
        } else {
            hataCallback("Bağlantı hatası!");
        }
    }, 1000);
}

veriGetir(
    "https://api.example.com",
    (veri) => console.log(veri),
    (hata) => console.error(hata)
);
```

## 8.8 IIFE (Immediately Invoked Function Expression)

```javascript
// Tanımlandığı anda çalışan fonksiyon
(function() {
    let ozel = "Bu değişken dışarıdan erişilemez";
    console.log("IIFE çalıştı!");
})();

// Arrow function IIFE
(() => {
    console.log("Arrow IIFE çalıştı!");
})();

// Parametreli IIFE
((isim) => {
    console.log(`Merhaba, ${isim}!`);
})("Ali");
```

## 8.9 Higher-Order Functions (Yüksek Dereceli Fonksiyonlar)

```javascript
// Fonksiyon döndüren veya parametre alan fonksiyonlar
function tekrarla(n, eylem) {
    for (let i = 0; i < n; i++) {
        eylem(i);
    }
}
tekrarla(3, console.log); // 0, 1, 2

// Fonksiyon üreten fonksiyon
function selamlayiciOlustur(selam) {
    return function(isim) {
        return `${selam}, ${isim}!`;
    };
}

const turkce = selamlayiciOlustur("Merhaba");
const ingilizce = selamlayiciOlustur("Hello");
console.log(turkce("Ali"));     // "Merhaba, Ali!"
console.log(ingilizce("John")); // "Hello, John!"
```

## 8.10 Recursion (Özyineleme)

```javascript
// Kendini çağıran fonksiyonlar
function faktoriyel(n) {
    if (n <= 1) return 1;       // Base case (temel durum)
    return n * faktoriyel(n - 1); // Recursive case
}
console.log(faktoriyel(5)); // 120 (5 * 4 * 3 * 2 * 1)

// Fibonacci (recursive)
function fib(n) {
    if (n <= 1) return n;
    return fib(n - 1) + fib(n - 2);
}
console.log(fib(10)); // 55

// Derin obje arama
function derinAra(obje, anahtar) {
    if (anahtar in obje) return obje[anahtar];
    for (let key of Object.keys(obje)) {
        if (typeof obje[key] === "object" && obje[key] !== null) {
            const sonuc = derinAra(obje[key], anahtar);
            if (sonuc !== undefined) return sonuc;
        }
    }
    return undefined;
}

const data = {
    kullanici: {
        bilgi: {
            ad: "Ali",
            adres: { sehir: "İstanbul" }
        }
    }
};
console.log(derinAra(data, "sehir")); // "İstanbul"
```

## 8.11 Pure Functions (Saf Fonksiyonlar)

```javascript
// Saf fonksiyon: Aynı girdi için her zaman aynı çıktıyı verir, yan etkisi yoktur

// ✅ Saf fonksiyon
function topla(a, b) {
    return a + b;
}

// ❌ Saf olmayan fonksiyon (dış değişkene bağımlı)
let vergiOrani = 0.18;
function vergiHesapla(fiyat) {
    return fiyat * vergiOrani; // Dış değişkene bağımlı!
}

// ✅ Saf hale getirme
function vergiHesaplaSaf(fiyat, oran) {
    return fiyat * oran;
}

// ❌ Saf olmayan (yan etkili - diziyi değiştiriyor)
function elemanEkle(dizi, eleman) {
    dizi.push(eleman); // Orijinal diziyi değiştiriyor!
    return dizi;
}

// ✅ Saf hale getirme
function elemanEkleSaf(dizi, eleman) {
    return [...dizi, eleman]; // Yeni dizi oluşturuyor
}
```

---

# 9. Diziler (Arrays)

## 9.1 Dizi Oluşturma

```javascript
// Literal ile
let meyveler = ["elma", "armut", "kiraz"];

// Constructor ile
let sayilar = new Array(1, 2, 3);
let bos = new Array(5); // 5 elemanlı boş dizi

// Array.from()
let harfler = Array.from("Merhaba"); // ["M", "e", "r", "h", "a", "b", "a"]
let sifirdan = Array.from({ length: 5 }, (_, i) => i); // [0, 1, 2, 3, 4]
let kareler = Array.from({ length: 5 }, (_, i) => i * i); // [0, 1, 4, 9, 16]

// Array.of()
let dizi = Array.of(1, 2, 3); // [1, 2, 3]

// Fill ile doldurma
let sifirlar = new Array(5).fill(0); // [0, 0, 0, 0, 0]
let yildizlar = new Array(3).fill("★"); // ["★", "★", "★"]
```

## 9.2 Dizi Erişimi

```javascript
let renkler = ["kırmızı", "yeşil", "mavi", "sarı", "mor"];

console.log(renkler[0]);   // "kırmızı" (ilk eleman)
console.log(renkler[2]);   // "mavi"
console.log(renkler[renkler.length - 1]); // "mor" (son eleman)
console.log(renkler.at(-1));  // "mor" (ES2022 - negatif indeks!)
console.log(renkler.at(-2));  // "sarı"

// Eleman değiştirme
renkler[1] = "turuncu";
console.log(renkler); // ["kırmızı", "turuncu", "mavi", "sarı", "mor"]

// Dizi uzunluğu
console.log(renkler.length); // 5
```

## 9.3 Destructuring (Yapısöküm) - ES6

```javascript
let koordinatlar = [41.0082, 28.9784];
let [enlem, boylam] = koordinatlar;
console.log(enlem);  // 41.0082
console.log(boylam); // 28.9784

// Bazı elemanları atlama
let [ilk, , ucuncu] = [1, 2, 3];
console.log(ilk);    // 1
console.log(ucuncu); // 3

// Varsayılan değer
let [a = 0, b = 0, c = 0] = [1, 2];
console.log(c); // 0 (varsayılan değer)

// Rest ile kalan elemanları alma
let [baslangic, ...geriKalan] = [1, 2, 3, 4, 5];
console.log(baslangic);  // 1
console.log(geriKalan);  // [2, 3, 4, 5]

// Değişken takas (swap)
let x = 1, y = 2;
[x, y] = [y, x];
console.log(x, y); // 2, 1
```

---

# 10. Objeler (Objects)

## 10.1 Obje Oluşturma

```javascript
// Object Literal (en yaygın yöntem)
let kullanici = {
    ad: "Ali",
    soyad: "Yılmaz",
    yas: 25,
    aktif: true,
    hobiler: ["kitap", "müzik", "yüzme"],
    adres: {
        sehir: "İstanbul",
        ilce: "Kadıköy",
        postaKodu: "34710"
    },
    // Method (fonksiyon özelliği)
    tamAd: function() {
        return `${this.ad} ${this.soyad}`;
    },
    // Kısa method tanımlama (ES6)
    selamla() {
        return `Merhaba, ben ${this.ad}!`;
    }
};

console.log(kullanici.ad);           // "Ali"
console.log(kullanici.tamAd());      // "Ali Yılmaz"
console.log(kullanici.selamla());    // "Merhaba, ben Ali!"
console.log(kullanici.adres.sehir);  // "İstanbul"
```

## 10.2 Özellik Erişimi

```javascript
let araba = {
    marka: "Toyota",
    model: "Corolla",
    yil: 2024,
    "renk kodu": "#FF0000" // Özel karakterli anahtar
};

// Nokta notasyonu (Dot notation)
console.log(araba.marka);  // "Toyota"

// Köşeli parantez notasyonu (Bracket notation)
console.log(araba["model"]);     // "Corolla"
console.log(araba["renk kodu"]); // "#FF0000"

// Dinamik anahtar erişimi
let ozellik = "yil";
console.log(araba[ozellik]); // 2024

// Özellik ekleme
araba.renk = "Beyaz";
araba["km"] = 15000;

// Özellik silme
delete araba.km;

// Özellik varlık kontrolü
console.log("marka" in araba);        // true
console.log("fiyat" in araba);        // false
console.log(araba.hasOwnProperty("model")); // true
```

## 10.3 Object Destructuring (ES6)

```javascript
let kullanici = {
    ad: "Ali",
    yas: 25,
    sehir: "İstanbul",
    email: "ali@mail.com"
};

// Temel destructuring
let { ad, yas, sehir } = kullanici;
console.log(ad);    // "Ali"
console.log(yas);   // 25

// Farklı isimle alma (rename)
let { ad: isim, yas: kacYasinda } = kullanici;
console.log(isim);        // "Ali"
console.log(kacYasinda);  // 25

// Varsayılan değer
let { ad: ad2, telefon = "Yok" } = kullanici;
console.log(telefon); // "Yok"

// İç içe destructuring
let kisi = {
    bilgi: {
        isim: "Ali",
        adres: { sehir: "İstanbul" }
    }
};
let { bilgi: { isim: kisiIsim, adres: { sehir: kisiSehir } } } = kisi;
console.log(kisiIsim);   // "Ali"
console.log(kisiSehir);  // "İstanbul"

// Rest ile kalan özellikleri alma
let { ad: ad3, ...digerBilgiler } = kullanici;
console.log(digerBilgiler); // { yas: 25, sehir: "İstanbul", email: "ali@mail.com" }
```

## 10.4 Object Metodları

```javascript
let kullanici = { ad: "Ali", yas: 25, sehir: "İstanbul" };

// Object.keys() - Anahtarları dizi olarak döner
console.log(Object.keys(kullanici));   // ["ad", "yas", "sehir"]

// Object.values() - Değerleri dizi olarak döner
console.log(Object.values(kullanici)); // ["Ali", 25, "İstanbul"]

// Object.entries() - [anahtar, değer] çiftlerini döner
console.log(Object.entries(kullanici));
// [["ad", "Ali"], ["yas", 25], ["sehir", "İstanbul"]]

// Object.fromEntries() - entries'den obje oluşturur
let girdi = [["ad", "Ali"], ["yas", 25]];
let obje = Object.fromEntries(girdi);
console.log(obje); // { ad: "Ali", yas: 25 }

// Object.assign() - Objeleri birleştirme
let varsayilan = { tema: "koyu", dil: "tr", bildirim: true };
let kullaniciAyar = { tema: "açık", fontSize: 14 };
let ayarlar = Object.assign({}, varsayilan, kullaniciAyar);
console.log(ayarlar);
// { tema: "açık", dil: "tr", bildirim: true, fontSize: 14 }

// Spread ile birleştirme (daha modern)
let ayarlar2 = { ...varsayilan, ...kullaniciAyar };

// Object.freeze() - Objeyi tamamen dondurur
let sabit = Object.freeze({ ad: "Ali", yas: 25 });
sabit.ad = "Veli"; // ❌ Hata vermez ama değiştirmez!
console.log(sabit.ad); // "Ali"

// Object.seal() - Yeni özellik eklenemez ama var olanlar değiştirilebilir
let muhurlu = Object.seal({ ad: "Ali", yas: 25 });
muhurlu.ad = "Veli";  // ✅ Değiştirilebilir
muhurlu.sehir = "İstanbul"; // ❌ Eklenmez
delete muhurlu.ad; // ❌ Silinemez

// Object.is() - Katı eşitlik (=== ile benzer ama farklılıklar var)
console.log(Object.is(NaN, NaN));   // true (=== ile false!)
console.log(Object.is(0, -0));      // false (=== ile true!)
```

## 10.5 Computed Property Names (Hesaplanmış Özellik Adları) - ES6

```javascript
let ozellik = "ad";
let deger = "Ali";

let obje = {
    [ozellik]: deger,
    [`${ozellik}Buyuk`]: deger.toUpperCase(),
    [1 + 1]: "iki"
};
console.log(obje); // { ad: "Ali", adBuyuk: "ALİ", 2: "iki" }
```

## 10.6 Shorthand Property Names (Kısa Özellik Adları) - ES6

```javascript
let ad = "Ali";
let yas = 25;
let sehir = "İstanbul";

// Eski yöntem
let kullanici1 = { ad: ad, yas: yas, sehir: sehir };

// ES6 shorthand (anahtar ve değişken adı aynıysa)
let kullanici2 = { ad, yas, sehir };
console.log(kullanici2); // { ad: "Ali", yas: 25, sehir: "İstanbul" }
```

## 10.7 this Anahtar Kelimesi

```javascript
// this, fonksiyonun çağrıldığı bağlama (context) göre değişir

// 1. Global bağlamda
console.log(this); // Tarayıcıda: window objesi

// 2. Obje metodunda
let kullanici = {
    ad: "Ali",
    selamla() {
        console.log(`Merhaba, ${this.ad}!`); // this = kullanici
    }
};
kullanici.selamla(); // "Merhaba, Ali!"

// 3. Fonksiyonda (strict mode'da undefined)
function goster() {
    "use strict";
    console.log(this); // undefined
}

// 4. Arrow function'da (lexical this - dış kapsamın this'i)
let obje = {
    ad: "Ali",
    bekle() {
        setTimeout(() => {
            console.log(this.ad); // "Ali" (arrow function dış this'i kullanır)
        }, 100);
    }
};

// 5. call, apply, bind ile this belirleme
function selamla(selam) {
    console.log(`${selam}, ${this.ad}!`);
}

let kisi = { ad: "Ali" };

selamla.call(kisi, "Merhaba");    // "Merhaba, Ali!"
selamla.apply(kisi, ["Selam"]);   // "Selam, Ali!"
let bagliFonk = selamla.bind(kisi, "Hey");
bagliFonk(); // "Hey, Ali!"
```

---

# 11. String Metodları

## 11.1 Arama Metodları

```javascript
let metin = "JavaScript çok güçlü bir dildir. JavaScript her yerde!";

// indexOf() - İlk bulunan pozisyon (-1 = bulunamadı)
console.log(metin.indexOf("JavaScript"));    // 0
console.log(metin.indexOf("JavaScript", 5)); // 32 (5. karakterden sonra ara)
console.log(metin.indexOf("Python"));         // -1

// lastIndexOf() - Sondan ilk bulunan pozisyon
console.log(metin.lastIndexOf("JavaScript")); // 32

// includes() - Var mı? (boolean) - ES6
console.log(metin.includes("güçlü"));  // true
console.log(metin.includes("zayıf"));  // false

// startsWith() / endsWith() - ES6
console.log(metin.startsWith("Java"));   // true
console.log(metin.endsWith("yerde!"));   // true

// search() - RegExp ile arama (pozisyon döner)
console.log(metin.search(/güçlü/i));  // 15

// match() - RegExp ile eşleşme (dizi döner)
console.log(metin.match(/JavaScript/g)); // ["JavaScript", "JavaScript"]

// matchAll() - Tüm eşleşmeler (iterator) - ES2020
let eslesmeleri = [...metin.matchAll(/JavaScript/g)];
console.log(eslesmeleri.length); // 2
```

## 11.2 Dönüşüm Metodları

```javascript
let metin = "  Merhaba Dünya  ";

// toUpperCase() / toLowerCase()
console.log("merhaba".toUpperCase()); // "MERHABA"
console.log("MERHABA".toLowerCase()); // "merhaba"

// trim() / trimStart() / trimEnd()
console.log(metin.trim());      // "Merhaba Dünya"
console.log(metin.trimStart()); // "Merhaba Dünya  "
console.log(metin.trimEnd());   // "  Merhaba Dünya"

// replace() / replaceAll()
let str = "elma ve elma";
console.log(str.replace("elma", "armut"));    // "armut ve elma" (sadece ilk)
console.log(str.replaceAll("elma", "armut")); // "armut ve armut" (hepsi)
console.log(str.replace(/elma/g, "armut"));   // "armut ve armut" (regex ile)

// padStart() / padEnd() - ES8
console.log("5".padStart(3, "0"));   // "005"
console.log("5".padEnd(3, "0"));     // "500"
console.log("42".padStart(5, "*"));  // "***42"

// repeat()
console.log("Ha".repeat(3));  // "HaHaHa"
console.log("=-".repeat(10)); // "=-=-=-=-=-=-=-=-=-=-"
```

## 11.3 Kesme ve Bölme Metodları

```javascript
let metin = "JavaScript Programlama";

// slice(başlangıç, bitiş) - Negatif indeks destekler
console.log(metin.slice(0, 4));    // "Java"
console.log(metin.slice(4));       // "Script Programlama"
console.log(metin.slice(-11));     // "Programlama"
console.log(metin.slice(-11, -5)); // "Progra"

// substring(başlangıç, bitiş) - Negatif indeks DESTEKLEmez
console.log(metin.substring(0, 4)); // "Java"
console.log(metin.substring(4, 0)); // "Java" (otomatik sıralanır)

// split() - String'i diziye böler
let csv = "Ali,Veli,Ayşe,Fatma";
console.log(csv.split(","));    // ["Ali", "Veli", "Ayşe", "Fatma"]
console.log(csv.split(",", 2)); // ["Ali", "Veli"] (limit)

let kelimeler = "Merhaba Dünya Nasılsın";
console.log(kelimeler.split(" ")); // ["Merhaba", "Dünya", "Nasılsın"]
console.log("Merhaba".split(""));  // ["M", "e", "r", "h", "a", "b", "a"]

// charAt() / charCodeAt() / at()
console.log(metin.charAt(0));      // "J"
console.log(metin.charCodeAt(0));  // 74 (Unicode kodu)
console.log(metin.at(-1));         // "a" (ES2022)

// concat()
let str1 = "Merhaba";
let str2 = " Dünya";
console.log(str1.concat(str2, "!")); // "Merhaba Dünya!"
// Template literal daha pratik: `${str1}${str2}!`
```

---

# 12. Array Metodları

## 12.1 Eleman Ekleme / Çıkarma

```javascript
let meyveler = ["elma", "armut"];

// push() - Sona ekler (uzunluk döner)
meyveler.push("kiraz");
console.log(meyveler); // ["elma", "armut", "kiraz"]

// pop() - Sondan çıkarır (çıkarılan elemanı döner)
let sonEleman = meyveler.pop();
console.log(sonEleman); // "kiraz"

// unshift() - Başa ekler (uzunluk döner)
meyveler.unshift("üzüm");
console.log(meyveler); // ["üzüm", "elma", "armut"]

// shift() - Baştan çıkarır (çıkarılan elemanı döner)
let ilkEleman = meyveler.shift();
console.log(ilkEleman); // "üzüm"

// splice(başlangıç, silinecekSayı, ...eklenecekler)
let sayilar = [1, 2, 3, 4, 5];

// Silme
sayilar.splice(2, 1); // İndeks 2'den 1 eleman sil
console.log(sayilar); // [1, 2, 4, 5]

// Ekleme (silinecek = 0)
sayilar.splice(2, 0, 3); // İndeks 2'ye 3 ekle
console.log(sayilar); // [1, 2, 3, 4, 5]

// Değiştirme
sayilar.splice(1, 2, 20, 30); // İndeks 1'den 2 eleman sil, yerine 20, 30 ekle
console.log(sayilar); // [1, 20, 30, 4, 5]
```

## 12.2 Arama Metodları

```javascript
let sayilar = [1, 2, 3, 4, 5, 3, 2, 1];

// indexOf() / lastIndexOf()
console.log(sayilar.indexOf(3));      // 2
console.log(sayilar.lastIndexOf(3)); // 5
console.log(sayilar.indexOf(99));    // -1

// includes() - ES7
console.log(sayilar.includes(3)); // true
console.log(sayilar.includes(99)); // false

// find() - Koşula uyan İLK elemanı döner - ES6
let kullanicilar = [
    { ad: "Ali", yas: 25 },
    { ad: "Ayşe", yas: 30 },
    { ad: "Mehmet", yas: 22 }
];
let bulunan = kullanicilar.find(k => k.yas > 24);
console.log(bulunan); // { ad: "Ali", yas: 25 }

// findIndex() - Koşula uyan İLK elemanın indeksini döner
let indeks = kullanicilar.findIndex(k => k.ad === "Ayşe");
console.log(indeks); // 1

// findLast() / findLastIndex() - ES2023
let sonBulunan = kullanicilar.findLast(k => k.yas > 24);
console.log(sonBulunan); // { ad: "Ayşe", yas: 30 }
```

## 12.3 Dönüştürme Metodları (ÇOK ÖNEMLİ!)

```javascript
// map() - Her elemanı dönüştürür, YENİ DİZİ döner
let sayilar = [1, 2, 3, 4, 5];
let kareler = sayilar.map(s => s * s);
console.log(kareler); // [1, 4, 9, 16, 25]
console.log(sayilar); // [1, 2, 3, 4, 5] (orijinal değişmez!)

let isimler = ["ali", "ayşe", "mehmet"];
let buyukHarf = isimler.map(isim => isim.charAt(0).toUpperCase() + isim.slice(1));
console.log(buyukHarf); // ["Ali", "Ayşe", "Mehmet"]

// filter() - Koşula uyan elemanları filtreler, YENİ DİZİ döner
let yaslar = [12, 25, 17, 30, 15, 22];
let yetiskinler = yaslar.filter(yas => yas >= 18);
console.log(yetiskinler); // [25, 30, 22]

// reduce() - Diziyi TEK bir değere indirger
let toplam = sayilar.reduce((accumulator, current) => accumulator + current, 0);
console.log(toplam); // 15

// reduce ile obje oluşturma
let ogrenciler = ["Ali", "Ayşe", "Ali", "Mehmet", "Ali", "Ayşe"];
let sayim = ogrenciler.reduce((acc, isim) => {
    acc[isim] = (acc[isim] || 0) + 1;
    return acc;
}, {});
console.log(sayim); // { Ali: 3, Ayşe: 2, Mehmet: 1 }

// reduce ile en büyük değer
let enBuyuk = sayilar.reduce((max, s) => s > max ? s : max, -Infinity);
console.log(enBuyuk); // 5

// every() - TÜM elemanlar koşulu sağlıyor mu?
console.log([2, 4, 6].every(n => n % 2 === 0)); // true
console.log([2, 3, 6].every(n => n % 2 === 0)); // false

// some() - EN AZ BİR eleman koşulu sağlıyor mu?
console.log([1, 3, 5].some(n => n % 2 === 0)); // false
console.log([1, 2, 5].some(n => n % 2 === 0)); // true

// flat() - İç içe dizileri düzleştirir - ES2019
console.log([1, [2, 3], [4, [5]]].flat());   // [1, 2, 3, 4, [5]]
console.log([1, [2, [3, [4]]]].flat(2));      // [1, 2, 3, [4]]
console.log([1, [2, [3, [4]]]].flat(Infinity)); // [1, 2, 3, 4]

// flatMap() - map + flat(1)
let cumleler = ["Merhaba Dünya", "JavaScript Güzel"];
let kelimeler = cumleler.flatMap(c => c.split(" "));
console.log(kelimeler); // ["Merhaba", "Dünya", "JavaScript", "Güzel"]
```

## 12.4 Sıralama Metodları

```javascript
// sort() - Diziyi yerinde sıralar (orijinal diziyi değiştirir!)
let isimler = ["Zeynep", "Ali", "Mehmet", "Ayşe"];
isimler.sort();
console.log(isimler); // ["Ali", "Ayşe", "Mehmet", "Zeynep"]

// ⚠️ DİKKAT: Sayılarda sort() string olarak sıralar!
let sayilar = [10, 1, 21, 2];
sayilar.sort();
console.log(sayilar); // [1, 10, 2, 21] (!) - Yanlış!

// Doğru sayı sıralaması:
sayilar.sort((a, b) => a - b); // Küçükten büyüğe
console.log(sayilar); // [1, 2, 10, 21]

sayilar.sort((a, b) => b - a); // Büyükten küçüğe
console.log(sayilar); // [21, 10, 2, 1]

// Türkçe sıralama
let turkceIsimler = ["Şeyma", "Çağla", "İrem", "Ömer", "Ali"];
turkceIsimler.sort((a, b) => a.localeCompare(b, "tr"));
console.log(turkceIsimler); // ["Ali", "Çağla", "İrem", "Ömer", "Şeyma"]

// reverse() - Diziyi ters çevirir
let abc = [1, 2, 3, 4, 5];
abc.reverse();
console.log(abc); // [5, 4, 3, 2, 1]

// toSorted() / toReversed() - ES2023 (orijinali DEĞİŞTİRMEZ)
let orijinal = [3, 1, 2];
let sirali = orijinal.toSorted((a, b) => a - b);
console.log(orijinal); // [3, 1, 2] (değişmedi!)
console.log(sirali);   // [1, 2, 3]
```

## 12.5 Birleştirme ve Kopyalama

```javascript
// concat() - Dizileri birleştirir (yeni dizi döner)
let a = [1, 2], b = [3, 4], c = [5, 6];
let birlesik = a.concat(b, c);
console.log(birlesik); // [1, 2, 3, 4, 5, 6]

// Spread ile birleştirme (daha modern)
let birlesik2 = [...a, ...b, ...c];

// slice() - Kesit alır (yeni dizi döner, orijinal değişmez)
let dizi = [1, 2, 3, 4, 5];
console.log(dizi.slice(1, 3));  // [2, 3]
console.log(dizi.slice(-2));    // [4, 5]
console.log(dizi.slice());      // [1, 2, 3, 4, 5] (tam kopya)

// join() - Diziyi string'e çevirir
console.log(["Ali", "Veli", "Ayşe"].join(", ")); // "Ali, Veli, Ayşe"
console.log([2026, 3, 1].join("-")); // "2026-3-1"
console.log(["M", "e", "r"].join("")); // "Mer"
```

## 12.6 Method Chaining (Metod Zincirleme)

```javascript
// Birden fazla metodu arka arkaya kullanma
let sonuc = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
    .filter(n => n % 2 === 0)    // Çift sayıları al: [2, 4, 6, 8, 10]
    .map(n => n * n)              // Karelerini al: [4, 16, 36, 64, 100]
    .reduce((t, n) => t + n, 0); // Topla: 220

console.log(sonuc); // 220

// Pratik örnek: Öğrenci notları
let ogrenciler = [
    { ad: "Ali", puan: 85 },
    { ad: "Ayşe", puan: 92 },
    { ad: "Mehmet", puan: 78 },
    { ad: "Fatma", puan: 95 },
    { ad: "Can", puan: 60 }
];

let basarililar = ogrenciler
    .filter(o => o.puan >= 80)
    .map(o => `${o.ad} (${o.puan})`)
    .join(", ");

console.log(`Başarılı öğrenciler: ${basarililar}`);
// "Başarılı öğrenciler: Ali (85), Ayşe (92), Fatma (95)"
```

---

# 13. DOM Manipülasyonu

## 13.1 DOM Nedir?

DOM (Document Object Model), HTML belgesinin JavaScript tarafından erişilebilen ağaç yapısıdır.

## 13.2 Element Seçme

```javascript
// getElementById - ID ile seçme (tek eleman)
let baslik = document.getElementById("ana-baslik");

// getElementsByClassName - Sınıf ile seçme (HTMLCollection döner)
let kartlar = document.getElementsByClassName("kart");

// getElementsByTagName - Etiket ile seçme
let paragraflar = document.getElementsByTagName("p");

// querySelector - CSS seçici ile İLK elemanı seçer ✅ ÖNERİLEN
let ilkKart = document.querySelector(".kart");
let baslik2 = document.querySelector("#ana-baslik");
let ilkLi = document.querySelector("ul > li:first-child");

// querySelectorAll - CSS seçici ile TÜM elemanları seçer (NodeList döner)
let tumKartlar = document.querySelectorAll(".kart");
let tumButonlar = document.querySelectorAll("button.btn");

// NodeList üzerinde forEach kullanılabilir
tumKartlar.forEach(kart => console.log(kart.textContent));
```

## 13.3 Element İçeriği Değiştirme

```javascript
let element = document.querySelector("#icerik");

// textContent - Sadece metin (HTML etiketleri işlenmez)
element.textContent = "Yeni metin içeriği";
console.log(element.textContent);

// innerHTML - HTML içerik (etiketler işlenir)
element.innerHTML = "<strong>Kalın</strong> ve <em>italik</em> metin";

// innerText - Görünür metin (CSS display:none olan kısımları görmez)
console.log(element.innerText);

// ⚠️ GÜVENLİK: innerHTML ile kullanıcı girdisi KULLANMAYIN (XSS riski!)
// ❌ element.innerHTML = kullaniciGirdisi; // Tehlikeli!
// ✅ element.textContent = kullaniciGirdisi; // Güvenli
```

## 13.4 Stil ve Sınıf Değiştirme

```javascript
let kutu = document.querySelector(".kutu");

// Inline stil değiştirme
kutu.style.backgroundColor = "blue";
kutu.style.color = "white";
kutu.style.padding = "20px";
kutu.style.borderRadius = "10px"; // CSS: border-radius → JS: borderRadius

// classList ile sınıf yönetimi ✅ ÖNERİLEN
kutu.classList.add("aktif");         // Sınıf ekle
kutu.classList.remove("gizli");      // Sınıf kaldır
kutu.classList.toggle("acik");       // Varsa kaldır, yoksa ekle
kutu.classList.contains("aktif");    // Sınıf var mı? (boolean)
kutu.classList.replace("eski", "yeni"); // Sınıf değiştir

// Attribute (özellik) yönetimi
let link = document.querySelector("a");
link.setAttribute("href", "https://example.com");
link.getAttribute("href");
link.removeAttribute("target");
link.hasAttribute("href"); // true/false

// Data attribute
// HTML: <div data-user-id="123" data-role="admin">
let div = document.querySelector("[data-user-id]");
console.log(div.dataset.userId); // "123"
console.log(div.dataset.role);   // "admin"
div.dataset.tema = "koyu"; // data-tema="koyu" ekler
```

## 13.5 Element Oluşturma ve Ekleme

```javascript
// Yeni element oluşturma
let yeniDiv = document.createElement("div");
yeniDiv.textContent = "Ben yeni bir div'im!";
yeniDiv.classList.add("kart");
yeniDiv.id = "yeni-kart";

// Elemente ekleme
let container = document.querySelector("#container");
container.appendChild(yeniDiv);             // Sona ekle
container.prepend(yeniDiv);                 // Başa ekle
container.insertBefore(yeniDiv, referansElement); // Önüne ekle

// insertAdjacentHTML - Belirli bir konuma HTML ekleme
container.insertAdjacentHTML("beforebegin", "<p>Öncesine</p>");
container.insertAdjacentHTML("afterbegin", "<p>İçinin başına</p>");
container.insertAdjacentHTML("beforeend", "<p>İçinin sonuna</p>");
container.insertAdjacentHTML("afterend", "<p>Sonrasına</p>");

// Element silme
let silinecek = document.querySelector("#silinecek");
silinecek.remove(); // Modern yöntem
// silinecek.parentNode.removeChild(silinecek); // Eski yöntem

// Element klonlama
let klon = yeniDiv.cloneNode(true); // true = alt elemanlarla birlikte
container.appendChild(klon);
```

## 13.6 DOM Traversal (Gezinme)

```javascript
let eleman = document.querySelector(".hedef");

// Ebeveyn
eleman.parentElement;
eleman.parentNode;
eleman.closest(".wrapper"); // En yakın eşleşen üst eleman

// Çocuklar
eleman.children;           // HTMLCollection (sadece element node)
eleman.childNodes;         // NodeList (text node dahil)
eleman.firstElementChild;
eleman.lastElementChild;
eleman.childElementCount;

// Kardeşler
eleman.nextElementSibling;
eleman.previousElementSibling;
```

---

# 14. Olaylar (Events)

## 14.1 Olay Dinleyici Ekleme

```javascript
let buton = document.querySelector("#btn");

// addEventListener ✅ ÖNERİLEN
buton.addEventListener("click", function(event) {
    console.log("Butona tıklandı!");
    console.log(event.target);  // Tıklanan element
    console.log(event.type);    // "click"
});

// Arrow function ile
buton.addEventListener("click", (e) => {
    console.log("Tıklandı!", e.target);
});

// Olay dinleyici kaldırma (isimli fonksiyon gerekli)
function tiklaHandler(e) {
    console.log("Tıklandı!");
}
buton.addEventListener("click", tiklaHandler);
buton.removeEventListener("click", tiklaHandler);

// Bir kez çalışacak olay
buton.addEventListener("click", () => {
    console.log("Sadece bir kez çalışır");
}, { once: true });
```

## 14.2 Yaygın Olay Türleri

```javascript
// Mouse olayları
element.addEventListener("click", handler);      // Tıklama
element.addEventListener("dblclick", handler);    // Çift tıklama
element.addEventListener("mouseenter", handler);  // Mouse girişi
element.addEventListener("mouseleave", handler);  // Mouse çıkışı
element.addEventListener("mousemove", handler);   // Mouse hareketi
element.addEventListener("contextmenu", handler); // Sağ tık

// Klavye olayları
document.addEventListener("keydown", (e) => {
    console.log(e.key);     // "Enter", "a", "ArrowUp"
    console.log(e.code);    // "Enter", "KeyA", "ArrowUp"
    console.log(e.ctrlKey); // Ctrl basılı mı?
    console.log(e.shiftKey);
    console.log(e.altKey);

    if (e.ctrlKey && e.key === "s") {
        e.preventDefault(); // Varsayılan davranışı engelle
        console.log("Kaydediliyor...");
    }
});

// Form olayları
form.addEventListener("submit", (e) => {
    e.preventDefault(); // Sayfanın yenilenmesini engelle
    let formData = new FormData(form);
    console.log(formData.get("isim"));
});

input.addEventListener("input", (e) => {     // Her tuşa basıldığında
    console.log(e.target.value);
});
input.addEventListener("change", (e) => {    // Değer değişip blur olunca
    console.log(e.target.value);
});
input.addEventListener("focus", handler);     // Odaklanma
input.addEventListener("blur", handler);      // Odak kaybı

// Sayfa olayları
window.addEventListener("load", handler);           // Sayfa tamamen yüklendi
window.addEventListener("DOMContentLoaded", handler); // HTML parse edildi
window.addEventListener("resize", handler);          // Pencere boyutu değişti
window.addEventListener("scroll", handler);          // Sayfa kaydırıldı
```

## 14.3 Event Delegation (Olay Delegasyonu)

```javascript
// Her elemana ayrı listener eklemek yerine üst elemana ekleyip hedefi kontrol etme
let liste = document.querySelector("#todo-list");

liste.addEventListener("click", (e) => {
    if (e.target.tagName === "LI") {
        e.target.classList.toggle("tamamlandi");
    }
    if (e.target.classList.contains("sil-btn")) {
        e.target.closest("li").remove();
    }
});

// Bu yöntemin avantajları:
// 1. Daha az bellek kullanımı
// 2. Dinamik eklenen elemanlar da otomatik çalışır
// 3. Performans artışı
```

## 14.4 Event Bubbling ve Capturing

```javascript
// Bubbling: Olay içten dışa doğru yayılır (varsayılan)
// Capturing: Olay dıştan içe doğru yayılır

// Bubbling'i durdurmak
element.addEventListener("click", (e) => {
    e.stopPropagation(); // Üst elemanlara yayılmasını engelle
});

// Capturing kullanmak (üçüncü parametre: true)
element.addEventListener("click", handler, true); // Capturing fazında çalışır

// preventDefault - Varsayılan davranışı engelleme
let link = document.querySelector("a");
link.addEventListener("click", (e) => {
    e.preventDefault(); // Linke gitmesini engelle
    console.log("Link tıklandı ama gidilmedi");
});
```

---

# 15. ES6+ Modern JavaScript

## 15.1 Destructuring (Yapısöküm) - Özet

```javascript
// Array Destructuring
let [a, b, c] = [1, 2, 3];
let [x, , z] = [1, 2, 3]; // 2'yi atla
let [ilk, ...geriKalan] = [1, 2, 3, 4];

// Object Destructuring
let { ad, yas } = { ad: "Ali", yas: 25 };
let { ad: isim } = { ad: "Ali" }; // Rename
let { ad: ad2, telefon = "Yok" } = { ad: "Ali" }; // Default

// Fonksiyon parametresinde
function kullaniciGoster({ ad, yas, sehir = "Bilinmiyor" }) {
    console.log(`${ad}, ${yas}, ${sehir}`);
}
kullaniciGoster({ ad: "Ali", yas: 25 });
```

## 15.2 Template Literals

```javascript
let ad = "Ali";
let yas = 25;

// Basit interpolasyon
console.log(`Merhaba ${ad}, ${yas} yaşındasın`);

// İfade kullanımı
console.log(`Toplam: ${10 + 20}`);
console.log(`Durum: ${yas >= 18 ? "Yetişkin" : "Çocuk"}`);

// Çok satırlı
let html = `
  <div class="kart">
    <h2>${ad}</h2>
    <p>Yaş: ${yas}</p>
  </div>
`;

// Tagged Templates
function vurgula(strings, ...values) {
    return strings.reduce((sonuc, str, i) => {
        return sonuc + str + (values[i] ? `<b>${values[i]}</b>` : "");
    }, "");
}
let mesaj = vurgula`Merhaba ${ad}, yaşın ${yas}`;
// "Merhaba <b>Ali</b>, yaşın <b>25</b>"
```

## 15.3 for...of ve Iterables

```javascript
// Array, String, Map, Set, NodeList, arguments üzerinde çalışır
for (let karakter of "Merhaba") { console.log(karakter); }
for (let eleman of [1, 2, 3]) { console.log(eleman); }
for (let [k, v] of new Map([["a", 1]])) { console.log(k, v); }
```

## 15.4 Promise - Temel

```javascript
// Promise: Asenkron işlemin gelecekteki sonucunu temsil eder
let soz = new Promise((resolve, reject) => {
    let basarili = true;
    setTimeout(() => {
        if (basarili) resolve("Veri geldi!");
        else reject("Hata oluştu!");
    }, 1000);
});

soz.then(veri => console.log(veri))      // Başarılı
   .catch(hata => console.error(hata))   // Hatalı
   .finally(() => console.log("Bitti")); // Her durumda

// Promise.all - Hepsi tamamlanınca
Promise.all([p1, p2, p3]).then(sonuclar => console.log(sonuclar));

// Promise.race - İlk tamamlanan
Promise.race([p1, p2]).then(ilk => console.log(ilk));

// Promise.allSettled - Hepsi sonuçlanınca (hata olsa bile)
Promise.allSettled([p1, p2]).then(sonuclar => console.log(sonuclar));

// Promise.any - İlk başarılı olan
Promise.any([p1, p2]).then(ilk => console.log(ilk));
```

---

# 16. Asenkron JavaScript

## 16.1 Senkron vs Asenkron

```javascript
// Senkron: Satır satır çalışır, her satır öncekini bekler
console.log("1");
console.log("2");
console.log("3");
// Çıktı: 1, 2, 3

// Asenkron: Beklemeden devam eder
console.log("1");
setTimeout(() => console.log("2"), 1000);
console.log("3");
// Çıktı: 1, 3, 2 (2 bir saniye sonra gelir)
```

## 16.2 Callback'ler

```javascript
function veriGetir(callback) {
    setTimeout(() => {
        callback({ ad: "Ali", yas: 25 });
    }, 1000);
}

veriGetir((veri) => console.log(veri));

// ⚠️ Callback Hell (Cehennem Piramidi)
getUser(userId, (user) => {
    getPosts(user.id, (posts) => {
        getComments(posts[0].id, (comments) => {
            getUser(comments[0].userId, (commenter) => {
                console.log(commenter); // 4 seviye iç içe!
            });
        });
    });
});
```

## 16.3 async/await (ES2017)

```javascript
// async fonksiyon her zaman Promise döner
async function veriGetir() {
    return "Veri geldi!";
}
veriGetir().then(v => console.log(v)); // "Veri geldi!"

// await: Promise'in sonucunu bekler (sadece async fonksiyon içinde)
async function kullanicilariGetir() {
    try {
        let response = await fetch("https://jsonplaceholder.typicode.com/users");
        let kullanicilar = await response.json();
        console.log(kullanicilar);
    } catch (hata) {
        console.error("Hata:", hata);
    } finally {
        console.log("İşlem tamamlandı");
    }
}

// Paralel async işlemler
async function parallelGetir() {
    let [users, posts] = await Promise.all([
        fetch("/api/users").then(r => r.json()),
        fetch("/api/posts").then(r => r.json())
    ]);
    console.log(users, posts);
}

// Top-level await (ES2022 - modüllerde)
// const data = await fetch("/api/data").then(r => r.json());
```

## 16.4 Event Loop

```javascript
// JavaScript tek iş parçacıklıdır (single-threaded)
// Event Loop ile asenkron işlemleri yönetir

console.log("1");                          // Call Stack
setTimeout(() => console.log("2"), 0);     // Task Queue
Promise.resolve().then(() => console.log("3")); // Microtask Queue
console.log("4");                          // Call Stack

// Çıktı: 1, 4, 3, 2
// Öncelik: Call Stack > Microtask Queue > Task Queue

// setTimeout(fn, 0) bile hemen çalışmaz!
// Çünkü callback Task Queue'ya gider ve Call Stack boşalmasını bekler
```

---

# 17. Hata Yönetimi (Error Handling)

## 17.1 try...catch...finally

```javascript
try {
    let sonuc = riskliFonksiyon();
    console.log(sonuc);
} catch (hata) {
    console.error("Hata yakalandı:", hata.message);
    console.error("Hata tipi:", hata.name);
    console.error("Stack trace:", hata.stack);
} finally {
    console.log("Bu blok HER ZAMAN çalışır");
}

// Hata fırlatma
function bolme(a, b) {
    if (b === 0) throw new Error("Sıfıra bölme hatası!");
    return a / b;
}

try {
    bolme(10, 0);
} catch (e) {
    console.error(e.message); // "Sıfıra bölme hatası!"
}
```

## 17.2 Hata Türleri

```javascript
// SyntaxError - Sözdizimi hatası
// eval("if("); // SyntaxError

// ReferenceError - Tanımsız değişken
// console.log(tanimsiz); // ReferenceError

// TypeError - Yanlış tip kullanımı
// null.property; // TypeError
// "hello"(); // TypeError

// RangeError - Geçersiz aralık
// new Array(-1); // RangeError

// Özel hata sınıfı oluşturma
class DogrulamaHatasi extends Error {
    constructor(mesaj, alan) {
        super(mesaj);
        this.name = "DogrulamaHatasi";
        this.alan = alan;
    }
}

function kayitOl(email) {
    if (!email.includes("@")) {
        throw new DogrulamaHatasi("Geçersiz email", "email");
    }
}

try {
    kayitOl("gecersiz");
} catch (e) {
    if (e instanceof DogrulamaHatasi) {
        console.log(`${e.alan}: ${e.message}`); // "email: Geçersiz email"
    }
}
```

---

# 18. JSON

```javascript
// JSON: JavaScript Object Notation - Veri alışverişi formatı

// JavaScript objesi → JSON string
let kullanici = { ad: "Ali", yas: 25, aktif: true };
let jsonStr = JSON.stringify(kullanici);
console.log(jsonStr); // '{"ad":"Ali","yas":25,"aktif":true}'

// Güzel formatlama
let guzelJson = JSON.stringify(kullanici, null, 2);

// JSON string → JavaScript objesi
let jsonMetin = '{"ad":"Ali","yas":25}';
let obje = JSON.parse(jsonMetin);
console.log(obje.ad); // "Ali"

// Derin kopya (deep clone)
let orijinal = { a: 1, b: { c: 2 } };
let kopya = JSON.parse(JSON.stringify(orijinal));
kopya.b.c = 99;
console.log(orijinal.b.c); // 2 (değişmedi!)

// structuredClone (modern yöntem)
let kopya2 = structuredClone(orijinal);
```

---

# 19. Local Storage

```javascript
// Tarayıcıda kalıcı veri saklama (5-10MB limit)

// Veri kaydetme
localStorage.setItem("tema", "koyu");
localStorage.setItem("dil", "tr");

// Obje kaydetme (JSON.stringify gerekli!)
let ayarlar = { tema: "koyu", fontSize: 14 };
localStorage.setItem("ayarlar", JSON.stringify(ayarlar));

// Veri okuma
let tema = localStorage.getItem("tema"); // "koyu"
let ayarlarObj = JSON.parse(localStorage.getItem("ayarlar"));

// Veri silme
localStorage.removeItem("tema");

// Tüm verileri silme
localStorage.clear();

// Veri var mı kontrolü
if (localStorage.getItem("tema") !== null) {
    console.log("Tema ayarı mevcut");
}

// sessionStorage - Sekme kapanınca silinir (aynı API)
sessionStorage.setItem("gecici", "veri");
```

---

# 20. Fetch API

```javascript
// Modern HTTP istek yöntemi (XMLHttpRequest yerine)

// GET isteği
async function kullanicilariGetir() {
    try {
        let response = await fetch("https://jsonplaceholder.typicode.com/users");

        if (!response.ok) {
            throw new Error(`HTTP Hata: ${response.status}`);
        }

        let kullanicilar = await response.json();
        console.log(kullanicilar);
    } catch (hata) {
        console.error("Hata:", hata);
    }
}

// POST isteği
async function kullaniciEkle(kullanici) {
    let response = await fetch("https://jsonplaceholder.typicode.com/users", {
        method: "POST",
        headers: {
            "Content-Type": "application/json"
        },
        body: JSON.stringify(kullanici)
    });
    let sonuc = await response.json();
    return sonuc;
}

// PUT isteği (güncelleme)
async function kullaniciGuncelle(id, veri) {
    let response = await fetch(`https://api.example.com/users/${id}`, {
        method: "PUT",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify(veri)
    });
    return response.json();
}

// DELETE isteği
async function kullaniciSil(id) {
    let response = await fetch(`https://api.example.com/users/${id}`, {
        method: "DELETE"
    });
    return response.ok;
}

// AbortController ile isteği iptal etme
let controller = new AbortController();
fetch(url, { signal: controller.signal })
    .then(r => r.json())
    .catch(e => {
        if (e.name === "AbortError") console.log("İstek iptal edildi");
    });

// 5 saniye sonra iptal et
setTimeout(() => controller.abort(), 5000);
```

---

# 21. Sınıflar (Classes) - ES6

```javascript
class Hayvan {
    // Constructor (yapıcı method)
    constructor(isim, tur) {
        this.isim = isim;
        this.tur = tur;
        this._yas = 0; // "private" convention (gerçekte public)
    }

    // Getter
    get yas() {
        return this._yas;
    }

    // Setter
    set yas(deger) {
        if (deger < 0) throw new Error("Yaş negatif olamaz!");
        this._yas = deger;
    }

    // Method
    sesCikar() {
        return `${this.isim} ses çıkarıyor`;
    }

    // toString
    toString() {
        return `${this.isim} (${this.tur})`;
    }

    // Static method (sınıf üzerinden çağrılır, instance'dan değil)
    static karsilastir(h1, h2) {
        return h1.yas - h2.yas;
    }
}

// Kalıtım (Inheritance)
class Kopek extends Hayvan {
    constructor(isim, cins) {
        super(isim, "Köpek"); // Üst sınıfın constructor'ını çağır
        this.cins = cins;
    }

    sesCikar() {
        return `${this.isim} havlıyor: Hav hav!`;
    }

    getir(nesne) {
        return `${this.isim} ${nesne} getirdi!`;
    }
}

let kopek = new Kopek("Buddy", "Golden");
kopek.yas = 3;
console.log(kopek.sesCikar()); // "Buddy havlıyor: Hav hav!"
console.log(kopek.getir("top")); // "Buddy top getirdi!"
console.log(kopek instanceof Kopek); // true
console.log(kopek instanceof Hayvan); // true

// Private alanlar (ES2022) - # ile
class BankaHesabi {
    #bakiye = 0; // Gerçek private alan

    constructor(sahibi) {
        this.sahibi = sahibi;
    }

    yatir(miktar) {
        if (miktar <= 0) throw new Error("Geçersiz miktar");
        this.#bakiye += miktar;
    }

    cek(miktar) {
        if (miktar > this.#bakiye) throw new Error("Yetersiz bakiye");
        this.#bakiye -= miktar;
    }

    get bakiye() {
        return this.#bakiye;
    }
}

let hesap = new BankaHesabi("Ali");
hesap.yatir(1000);
hesap.cek(300);
console.log(hesap.bakiye); // 700
// console.log(hesap.#bakiye); // ❌ SyntaxError: Private field
```

---

# 22. Modüller (Modules)

```javascript
// ES Modules (ESM) - Modern standart

// === math.js (Export) ===
// Named export
export const PI = 3.14159;
export function topla(a, b) { return a + b; }
export function cikar(a, b) { return a - b; }

// Default export (dosya başına sadece 1 tane)
export default class Hesaplama {
    static kareAl(n) { return n * n; }
}

// === app.js (Import) ===
// Named import
import { topla, cikar, PI } from './math.js';

// Default import
import Hesaplama from './math.js';

// Hepsini import
import * as Matematik from './math.js';
console.log(Matematik.topla(3, 5));
console.log(Matematik.PI);

// Rename
import { topla as toplama } from './math.js';

// HTML'de kullanım
// <script type="module" src="app.js"></script>
```

---

# 23. Regular Expressions (Regex)

```javascript
// Regex: Metin kalıplarını eşleştirmek için kullanılır

// Oluşturma
let regex1 = /merhaba/i;              // Literal (i = case-insensitive)
let regex2 = new RegExp("merhaba", "i"); // Constructor

// test() - Eşleşme var mı? (boolean)
console.log(/merhaba/i.test("Merhaba Dünya")); // true

// match() - Eşleşmeleri döner
console.log("abc123def456".match(/\d+/g)); // ["123", "456"]

// replace() ile
console.log("Merhaba Dünya".replace(/dünya/i, "JS")); // "Merhaba JS"

// Yaygın kalıplar
let emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
let telRegex = /^(\+90|0)?[0-9]{10}$/;
let urlRegex = /^https?:\/\/.+/;

console.log(emailRegex.test("ali@mail.com")); // true
console.log(telRegex.test("05551234567"));     // true

// Regex karakterleri:
// .     → Herhangi bir karakter
// \d    → Rakam [0-9]
// \w    → Kelime karakteri [a-zA-Z0-9_]
// \s    → Boşluk karakteri
// ^     → Satır başı
// $     → Satır sonu
// *     → 0 veya daha fazla
// +     → 1 veya daha fazla
// ?     → 0 veya 1
// {n}   → Tam n kez
// {n,m} → n ile m arası
// [abc] → a, b veya c
// [^abc]→ a, b, c hariç
// (x|y) → x veya y
// ()    → Grup yakalama
```

---

# 24. Map, Set, WeakMap, WeakSet

```javascript
// === MAP === (Anahtar-değer çiftleri, herhangi bir tip anahtar olabilir)
let harita = new Map();
harita.set("ad", "Ali");
harita.set(42, "sayı anahtarı");
harita.set(true, "boolean anahtarı");

console.log(harita.get("ad"));   // "Ali"
console.log(harita.size);        // 3
console.log(harita.has("ad"));   // true
harita.delete(42);

for (let [anahtar, deger] of harita) {
    console.log(`${anahtar}: ${deger}`);
}

// === SET === (Benzersiz değerler koleksiyonu)
let kume = new Set([1, 2, 3, 3, 4, 4, 5]);
console.log(kume); // Set {1, 2, 3, 4, 5} (tekrarlar kaldırıldı)

kume.add(6);
kume.delete(1);
console.log(kume.has(3)); // true
console.log(kume.size);   // 5

// Dizi tekrarlarını kaldırma
let tekrarli = [1, 2, 2, 3, 3, 3, 4];
let benzersiz = [...new Set(tekrarli)]; // [1, 2, 3, 4]

// === WEAKMAP === (Sadece obje anahtarları, garbage collection'a izin verir)
let weakMap = new WeakMap();
let obj = { id: 1 };
weakMap.set(obj, "metadata");
// obj = null olursa, weakMap'teki kayıt da silinir (GC)

// === WEAKSET === (Sadece objeler, garbage collection'a izin verir)
let weakSet = new WeakSet();
weakSet.add(obj);
```

---

# 25. Symbol ve Iterator

```javascript
// Symbol: Benzersiz tanımlayıcılar
let id = Symbol("id");
let id2 = Symbol("id");
console.log(id === id2); // false

// Well-known Symbols
class Koleksiyon {
    #items = [];

    ekle(item) { this.#items.push(item); }

    // Iterator protokolü (for...of ile kullanılabilir)
    [Symbol.iterator]() {
        let index = 0;
        let items = this.#items;
        return {
            next() {
                if (index < items.length) {
                    return { value: items[index++], done: false };
                }
                return { done: true };
            }
        };
    }
}

let kol = new Koleksiyon();
kol.ekle("a");
kol.ekle("b");
kol.ekle("c");

for (let item of kol) {
    console.log(item); // "a", "b", "c"
}
```

---

# 26. Generator Fonksiyonlar

```javascript
// function* ile tanımlanır, yield ile değer üretir
function* sayiUret() {
    yield 1;
    yield 2;
    yield 3;
}

let gen = sayiUret();
console.log(gen.next()); // { value: 1, done: false }
console.log(gen.next()); // { value: 2, done: false }
console.log(gen.next()); // { value: 3, done: false }
console.log(gen.next()); // { value: undefined, done: true }

// Sonsuz dizi
function* sonsuzSayi() {
    let i = 0;
    while (true) {
        yield i++;
    }
}

let sayac = sonsuzSayi();
console.log(sayac.next().value); // 0
console.log(sayac.next().value); // 1
console.log(sayac.next().value); // 2

// for...of ile kullanım
function* aralik(baslangic, bitis) {
    for (let i = baslangic; i <= bitis; i++) {
        yield i;
    }
}
for (let sayi of aralik(1, 5)) {
    console.log(sayi); // 1, 2, 3, 4, 5
}
```

---

# 27. Proxy ve Reflect

```javascript
// Proxy: Obje üzerindeki işlemleri engelleme ve özelleştirme
let kullanici = { ad: "Ali", yas: 25 };

let proxy = new Proxy(kullanici, {
    get(hedef, ozellik) {
        console.log(`${ozellik} okunuyor`);
        return ozellik in hedef ? hedef[ozellik] : "Özellik bulunamadı";
    },
    set(hedef, ozellik, deger) {
        if (ozellik === "yas" && typeof deger !== "number") {
            throw new TypeError("Yaş sayı olmalıdır!");
        }
        hedef[ozellik] = deger;
        return true;
    }
});

console.log(proxy.ad);    // "ad okunuyor" → "Ali"
console.log(proxy.xyz);   // "xyz okunuyor" → "Özellik bulunamadı"
proxy.yas = 26;            // ✅
// proxy.yas = "yirmi";    // ❌ TypeError

// Reflect: Proxy handler'larında kullanılan yardımcı metotlar
Reflect.get(kullanici, "ad");        // kullanici.ad
Reflect.set(kullanici, "yas", 30);   // kullanici.yas = 30
Reflect.has(kullanici, "ad");        // "ad" in kullanici
Reflect.deleteProperty(kullanici, "yas"); // delete kullanici.yas
```

---

# 28. Web API'leri

```javascript
// setTimeout / setInterval
let timer = setTimeout(() => console.log("3 sn sonra"), 3000);
clearTimeout(timer); // İptal

let interval = setInterval(() => console.log("Her 1 sn"), 1000);
clearInterval(interval); // İptal

// Date API
let simdi = new Date();
console.log(simdi.getFullYear());   // 2026
console.log(simdi.getMonth());      // 0-11 (0 = Ocak)
console.log(simdi.getDate());       // 1-31
console.log(simdi.getDay());        // 0-6 (0 = Pazar)
console.log(simdi.getHours());
console.log(simdi.toLocaleDateString("tr-TR")); // "01.03.2026"
console.log(simdi.toLocaleTimeString("tr-TR")); // "15:47:51"

// Math API
console.log(Math.PI);            // 3.14159...
console.log(Math.round(4.5));    // 5
console.log(Math.floor(4.9));    // 4
console.log(Math.ceil(4.1));     // 5
console.log(Math.trunc(4.9));    // 4
console.log(Math.abs(-5));       // 5
console.log(Math.max(1, 5, 3));  // 5
console.log(Math.min(1, 5, 3));  // 1
console.log(Math.pow(2, 10));    // 1024
console.log(Math.sqrt(16));      // 4
console.log(Math.random());      // 0-1 arası rastgele sayı

// Belirli aralıkta rastgele sayı
function rastgele(min, max) {
    return Math.floor(Math.random() * (max - min + 1)) + min;
}
console.log(rastgele(1, 100)); // 1-100 arası
```

---

# 29. Performans ve Optimizasyon

```javascript
// 1. Debounce - Belirli süre bekledikten sonra çalıştır
function debounce(fn, gecikme) {
    let timer;
    return function(...args) {
        clearTimeout(timer);
        timer = setTimeout(() => fn.apply(this, args), gecikme);
    };
}
// Kullanım: Arama kutusunda her tuşa basıldığında API çağrısı yapmamak için
let aramaYap = debounce((query) => {
    console.log("Aranıyor:", query);
}, 300);

// 2. Throttle - Belirli aralıklarla çalıştır
function throttle(fn, limit) {
    let bekliyor = false;
    return function(...args) {
        if (!bekliyor) {
            fn.apply(this, args);
            bekliyor = true;
            setTimeout(() => bekliyor = false, limit);
        }
    };
}
// Kullanım: Scroll olayında sürekli çalışmasını engellemek için
window.addEventListener("scroll", throttle(() => {
    console.log("Scroll pozisyonu:", window.scrollY);
}, 200));

// 3. Memoization - Sonuçları önbelleğe alma
function memoize(fn) {
    let cache = new Map();
    return function(...args) {
        let key = JSON.stringify(args);
        if (cache.has(key)) return cache.get(key);
        let sonuc = fn.apply(this, args);
        cache.set(key, sonuc);
        return sonuc;
    };
}

let pahaliFonk = memoize((n) => {
    console.log("Hesaplanıyor...");
    return n * n;
});
console.log(pahaliFonk(5)); // "Hesaplanıyor..." → 25
console.log(pahaliFonk(5)); // 25 (cache'den, hesaplanmadı)
```

---

# 30. Pratik Projeler ve Örnekler

## 30.1 To-Do List

```javascript
class TodoApp {
    constructor() {
        this.todos = JSON.parse(localStorage.getItem("todos")) || [];
    }

    ekle(metin) {
        this.todos.push({ id: Date.now(), metin, tamamlandi: false });
        this.kaydet();
    }

    sil(id) {
        this.todos = this.todos.filter(t => t.id !== id);
        this.kaydet();
    }

    tpigle(id) {
        let todo = this.todos.find(t => t.id === id);
        if (todo) todo.tamamlandi = !todo.tamamlandi;
        this.kaydet();
    }

    kaydet() {
        localStorage.setItem("todos", JSON.stringify(this.todos));
    }

    listele() {
        return this.todos.map(t =>
            `${t.tamamlandi ? "✅" : "⬜"} ${t.metin}`
        ).join("\n");
    }
}
```

## 30.2 Sayaç Uygulaması

```javascript
function SayacUygulamasi() {
    let deger = 0;
    const goster = document.querySelector("#deger");
    const artirBtn = document.querySelector("#artir");
    const azaltBtn = document.querySelector("#azalt");
    const sifirlaBtn = document.querySelector("#sifirla");

    function guncelle() {
        goster.textContent = deger;
        goster.style.color = deger > 0 ? "green" : deger < 0 ? "red" : "black";
    }

    artirBtn.addEventListener("click", () => { deger++; guncelle(); });
    azaltBtn.addEventListener("click", () => { deger--; guncelle(); });
    sifirlaBtn.addEventListener("click", () => { deger = 0; guncelle(); });
}
```

## 30.3 Basit Hesap Makinesi

```javascript
class HesapMakinesi {
    constructor() {
        this.sonuc = 0;
        this.gecmis = [];
    }

    hesapla(ifade) {
        try {
            // Güvenli hesaplama (eval kullanmadan)
            this.sonuc = new Function(`return ${ifade}`)();
            this.gecmis.push(`${ifade} = ${this.sonuc}`);
            return this.sonuc;
        } catch (e) {
            return "Hata: Geçersiz ifade";
        }
    }

    gecmisiGor() {
        return this.gecmis.join("\n");
    }

    temizle() {
        this.sonuc = 0;
        this.gecmis = [];
    }
}

let calc = new HesapMakinesi();
console.log(calc.hesapla("2 + 3 * 4")); // 14
console.log(calc.hesapla("(10 - 3) ** 2")); // 49
```

## 30.4 Faydalı Yardımcı Fonksiyonlar

```javascript
// 1. Rastgele renk üretici
const rastgeleRenk = () =>
    `#${Math.floor(Math.random() * 16777215).toString(16).padStart(6, "0")}`;

// 2. Benzersiz ID üretici
const benzersizId = () =>
    Date.now().toString(36) + Math.random().toString(36).substr(2);

// 3. Tarih formatlama
const tarihFormatla = (tarih) =>
    new Date(tarih).toLocaleDateString("tr-TR", {
        year: "numeric", month: "long", day: "numeric"
    });

// 4. Dizi karıştırma (Fisher-Yates)
function karistir(dizi) {
    let kopya = [...dizi];
    for (let i = kopya.length - 1; i > 0; i--) {
        let j = Math.floor(Math.random() * (i + 1));
        [kopya[i], kopya[j]] = [kopya[j], kopya[i]];
    }
    return kopya;
}

// 5. Deep clone
const deepClone = (obj) => structuredClone(obj);

// 6. Bekleme fonksiyonu
const bekle = (ms) => new Promise(resolve => setTimeout(resolve, ms));

// 7. Gruplama
function grupla(dizi, anahtar) {
    return dizi.reduce((gruplar, eleman) => {
        let grup = eleman[anahtar];
        gruplar[grup] = gruplar[grup] || [];
        gruplar[grup].push(eleman);
        return gruplar;
    }, {});
}

// 8. Pipe fonksiyonu
const pipe = (...fonksiyonlar) => (deger) =>
    fonksiyonlar.reduce((sonuc, fn) => fn(sonuc), deger);

const islemZinciri = pipe(
    x => x * 2,
    x => x + 10,
    x => x.toString()
);
console.log(islemZinciri(5)); // "20"
```

---

> 📝 **NOT:** Bu rehber JavaScript dilinin temel ve ileri seviye konularını kapsamaktadır. Düzenli pratik yaparak bu konuları pekiştiriniz. Her konuyu anladıktan sonra küçük projeler geliştirerek öğrenmenizi güçlendiriniz.

> 🎯 **ÖNERİ:** MDN Web Docs (developer.mozilla.org) JavaScript'in resmi referans kaynağıdır. Bu rehberle birlikte MDN'i de kullanınız.

---

**© 2026 - JavaScript Kapsamlı Ders Notları - Tüm hakları saklıdır.**
