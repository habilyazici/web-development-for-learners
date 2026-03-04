# ⚛️ REACT.JS KAPSAMLI DERS NOTLARI

> **Hazırlayan:** AI Asistan  
> **Tarih:** Mart 2026  
> **Dil:** Türkçe  
> **Seviye:** Başlangıçtan İleri Seviyeye  
> **React Sürümü:** React 18+

---

## 📑 İÇİNDEKİLER

1. [React Nedir?](#1-react-nedir)
2. [Kurulum ve Proje Oluşturma](#2-kurulum-ve-proje-olusturma)
3. [JSX (JavaScript XML)](#3-jsx-javascript-xml)
4. [Bileşenler (Components)](#4-bilesenler-components)
5. [Props (Özellikler)](#5-props-ozellikler)
6. [State (Durum Yönetimi)](#6-state-durum-yonetimi)
7. [Olaylar (Event Handling)](#7-olaylar-event-handling)
8. [Koşullu Render](#8-kosullu-render)
9. [Listeler ve Anahtarlar (Lists & Keys)](#9-listeler-ve-anahtarlar)
10. [Formlar (Forms)](#10-formlar-forms)
11. [useEffect Hook](#11-useeffect-hook)
12. [useRef Hook](#12-useref-hook)
13. [useMemo ve useCallback](#13-usememo-ve-usecallback)
14. [useReducer Hook](#14-usereducer-hook)
15. [useContext ve Context API](#15-usecontext-ve-context-api)
16. [Custom Hooks (Özel Kancalar)](#16-custom-hooks)
17. [React Router](#17-react-router)
18. [Stil Yönetimi (Styling)](#18-stil-yonetimi)
19. [API İstekleri ve Veri Çekme](#19-api-istekleri)
20. [Hata Sınırları (Error Boundaries)](#20-hata-sinirlari)
21. [React.memo ve Performans](#21-react-memo-ve-performans)
22. [Portals](#22-portals)
23. [Fragments](#23-fragments)
24. [Lazy Loading ve Suspense](#24-lazy-loading-ve-suspense)
25. [forwardRef ve useImperativeHandle](#25-forwardref-ve-useimperativehandle)
26. [State Yönetim Kütüphaneleri](#26-state-yonetim-kutuphaneleri)
27. [React ile TypeScript](#27-react-ile-typescript)
28. [Test Yazımı](#28-test-yazimi)
29. [Deployment (Yayınlama)](#29-deployment)
30. [En İyi Uygulamalar ve Kalıplar](#30-en-iyi-uygulamalar)

---

# 1. React Nedir?

## 1.1 Tanım

React, Facebook (Meta) tarafından geliştirilen, kullanıcı arayüzleri (UI) oluşturmak için kullanılan açık kaynaklı bir **JavaScript kütüphanesidir**. 2013 yılında yayınlanmıştır.

### React'in Temel Özellikleri:

- **Bileşen Tabanlı (Component-Based):** UI, yeniden kullanılabilir bileşenlerden oluşur
- **Deklaratif (Declarative):** UI'ın nasıl görünmesi gerektiğini tanımlarsınız, React güncellemeyi yapar
- **Virtual DOM:** Gerçek DOM yerine sanal bir DOM kullanır, sadece değişen kısımları günceller
- **Tek Yönlü Veri Akışı (One-Way Data Flow):** Veri üstten alta (parent → child) akar
- **JSX:** JavaScript içinde HTML benzeri sözdizimi kullanmaya izin verir
- **Hooks:** Fonksiyonel bileşenlerde state ve lifecycle yönetimi sağlar

### React Ne Zaman Kullanılır?

```
✅ Tek Sayfa Uygulamaları (SPA)
✅ Dinamik ve etkileşimli web arayüzleri
✅ Büyük ölçekli uygulamalar
✅ Mobil uygulamalar (React Native ile)
✅ Sunucu taraflı render (Next.js ile)
✅ Statik site oluşturma (Gatsby, Next.js ile)
```

## 1.2 Virtual DOM Nasıl Çalışır?

```
1. State veya props değiştiğinde React yeni bir Virtual DOM oluşturur
2. Yeni Virtual DOM ile eski Virtual DOM karşılaştırılır (Diffing)
3. Sadece farklılıklar (değişen kısımlar) tespit edilir
4. Gerçek DOM'da yalnızca değişen kısımlar güncellenir (Reconciliation)
```

```javascript
// React bunu sizin için otomatik yapar!
// Siz sadece state'i güncellersiniz:
setCount(count + 1);
// React gerisini halleder: Virtual DOM → Diff → Gerçek DOM güncelleme
```

## 1.3 React vs Diğer Framework'ler

| Özellik | React | Vue | Angular |
|---------|-------|-----|---------|
| Tür | Kütüphane | Framework | Framework |
| Öğrenme Eğrisi | Orta | Kolay | Zor |
| Dil | JSX | Template | TypeScript |
| State Yönetimi | Harici (Redux vb.) | Vuex/Pinia | Dahili (RxJS) |
| Performans | Çok İyi | Çok İyi | İyi |
| Ekosistem | Çok Geniş | Geniş | Geniş |
| Mobil | React Native | NativeScript | Ionic |
| Geliştirici | Meta | Evan You | Google |

## 1.4 React Ekosistemi

```
📦 Temel Araçlar:
├── React              → UI kütüphanesi
├── React DOM           → DOM render
├── React Native        → Mobil uygulama
├── Next.js            → SSR/SSG framework
├── Gatsby             → Statik site oluşturucu
│
📦 State Yönetimi:
├── Redux Toolkit      → Büyük uygulamalar için
├── Zustand            → Hafif state yönetimi
├── Jotai              → Atomik state
├── Recoil             → Facebook state yönetimi
│
📦 Routing:
├── React Router       → Sayfa yönlendirmesi
├── TanStack Router    → Modern router
│
📦 Veri Çekme:
├── TanStack Query     → Sunucu state yönetimi
├── SWR                → Veri çekme kancası
├── Axios              → HTTP istemcisi
│
📦 Form Yönetimi:
├── React Hook Form    → Form yönetimi
├── Formik             → Form yönetimi
├── Zod / Yup          → Validasyon
│
📦 UI Kütüphaneleri:
├── Material UI (MUI)  → Google Material Design
├── Ant Design         → Kurumsal UI
├── Chakra UI          → Erişilebilir UI
├── shadcn/ui          → Radix UI tabanlı
├── Tailwind CSS       → Utility-first CSS
│
📦 Test:
├── Jest               → Test framework
├── React Testing Lib  → Bileşen testleri
├── Vitest             → Vite tabanlı test
├── Playwright         → E2E testler
│
📦 Diğer:
├── Storybook          → Bileşen dokümantasyonu
├── Framer Motion      → Animasyonlar
└── React Helmet       → SEO / Head yönetimi
```

---

# 2. Kurulum ve Proje Oluşturma

## 2.1 Gereksinimler

```bash
# Node.js kurulu olmalı (v18+)
node --version    # v18.x.x veya üzeri
npm --version     # 9.x.x veya üzeri
```

## 2.2 Vite ile Proje Oluşturma (✅ ÖNERİLEN)

```bash
# Vite ile React projesi oluşturma
npm create vite@latest my-react-app -- --template react

# TypeScript ile
npm create vite@latest my-react-app -- --template react-ts

# Projeye gir ve bağımlılıkları yükle
cd my-react-app
npm install

# Geliştirme sunucusunu başlat
npm run dev
# → http://localhost:5173 adresinde açılır
```

## 2.3 Create React App (Eski Yöntem)

```bash
# ⚠️ CRA artık önerilmiyor, Vite tercih edin
npx create-react-app my-app
cd my-app
npm start
# → http://localhost:3000
```

## 2.4 Next.js ile Proje Oluşturma

```bash
# Next.js (SSR/SSG framework)
npx create-next-app@latest my-next-app
cd my-next-app
npm run dev
# → http://localhost:3000
```

## 2.5 Proje Yapısı (Vite)

```
my-react-app/
├── node_modules/          # Bağımlılıklar
├── public/                # Statik dosyalar
│   └── vite.svg
├── src/                   # Kaynak kodlar
│   ├── assets/            # Resimler, fontlar vb.
│   ├── components/        # Bileşenler (siz oluşturun)
│   ├── hooks/             # Özel hook'lar (siz oluşturun)
│   ├── pages/             # Sayfa bileşenleri (siz oluşturun)
│   ├── App.jsx            # Ana bileşen
│   ├── App.css            # Ana bileşen stili
│   ├── main.jsx           # Giriş noktası
│   └── index.css          # Global stiller
├── index.html             # Ana HTML dosyası
├── package.json           # Proje ayarları ve bağımlılıklar
├── vite.config.js         # Vite yapılandırması
└── .gitignore             # Git'e dahil edilmeyecek dosyalar
```

## 2.6 Giriş Noktası (main.jsx)

```jsx
// main.jsx - Uygulamanın başlangıç noktası
import React from 'react';
import ReactDOM from 'react-dom/client';
import App from './App.jsx';
import './index.css';

// React 18+ - createRoot API
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
    <React.StrictMode>
        <App />
    </React.StrictMode>
);

// ⚠️ StrictMode: Geliştirme modunda potansiyel sorunları tespit eder
// - Bileşenleri 2 kez render eder (sadece dev modda)
// - Güvenli olmayan lifecycle metodlarını uyarır
// - Production'da hiçbir etkisi yoktur
```

## 2.7 package.json Temel Komutlar

```json
{
    "scripts": {
        "dev": "vite",              // Geliştirme sunucusu
        "build": "vite build",       // Production build
        "preview": "vite preview",   // Build önizleme
        "lint": "eslint ."          // Kod kalitesi kontrolü
    }
}
```

```bash
npm run dev      # Geliştirme sunucusu başlat
npm run build    # Production için derle
npm run preview  # Derlenmiş halı önizle
```

---

# 3. JSX (JavaScript XML)

## 3.1 JSX Nedir?

JSX, JavaScript içinde HTML benzeri sözdizimi yazmanıza olanak tanıyan bir sözdizimi uzantısıdır. JSX zorunlu değildir ama React ile çalışmayı çok kolaylaştırır.

```jsx
// JSX ile (okunabilir)
const element = <h1>Merhaba Dünya!</h1>;

// JSX olmadan (karmaşık)
const element2 = React.createElement('h1', null, 'Merhaba Dünya!');

// Her ikisi de aynı sonucu üretir!
```

## 3.2 JSX Kuralları

```jsx
// 1. TEK KÖK ELEMAN GEREKLİ
// ❌ Yanlış: Birden fazla kök eleman
// return (
//     <h1>Başlık</h1>
//     <p>Paragraf</p>
// );

// ✅ Doğru: Tek kök eleman ile sarmalama
return (
    <div>
        <h1>Başlık</h1>
        <p>Paragraf</p>
    </div>
);

// ✅ Doğru: Fragment ile sarmalama (ekstra DOM elementi oluşturmaz)
return (
    <>
        <h1>Başlık</h1>
        <p>Paragraf</p>
    </>
);

// 2. className KULLANILIR (class değil!)
<div className="kart">İçerik</div>
// HTML'de: <div class="kart">

// 3. htmlFor KULLANILIR (for değil!)
<label htmlFor="email">Email:</label>
// HTML'de: <label for="email">

// 4. camelCase ÖZELLİKLER
<div tabIndex={0} onClick={handler}>
    <input autoFocus readOnly />
    <textarea defaultValue="metin" />
</div>

// 5. STYLE OBJESİ İLE YAZILIR
<div style={{ backgroundColor: 'blue', fontSize: '16px', marginTop: '20px' }}>
    Stillendirilmiş div
</div>

// 6. TÜM ETİKETLER KAPATILMALIDIR
<img src="foto.jpg" alt="Fotoğraf" />   // Self-closing
<br />                                     // Self-closing
<input type="text" />                      // Self-closing

// 7. JAVASCRIPT İFADELERİ {} İÇİNDE YAZILIR
const ad = "Ali";
const yas = 25;
return (
    <div>
        <h1>Merhaba, {ad}!</h1>
        <p>Yaşınız: {yas}</p>
        <p>Doğum yılı: {2026 - yas}</p>
        <p>Yetişkin mi: {yas >= 18 ? "Evet" : "Hayır"}</p>
        <p>Bugünün tarihi: {new Date().toLocaleDateString("tr-TR")}</p>
    </div>
);
```

## 3.3 JSX İçinde JavaScript İfadeleri

```jsx
function App() {
    const ad = "Ali";
    const meyveler = ["Elma", "Armut", "Kiraz"];
    const stil = { color: 'red', fontWeight: 'bold' };

    return (
        <div>
            {/* Yorum böyle yazılır JSX içinde */}

            {/* Değişken kullanımı */}
            <h1>Merhaba, {ad}!</h1>

            {/* Koşullu render */}
            {ad === "Ali" && <p>Hoşgeldin Ali!</p>}

            {/* Ternary */}
            <p>{ad ? `Hoşgeldin ${ad}` : "Misafir"}</p>

            {/* Dizi render */}
            <ul>
                {meyveler.map((meyve, index) => (
                    <li key={index}>{meyve}</li>
                ))}
            </ul>

            {/* Inline stil */}
            <p style={stil}>Kırmızı ve kalın metin</p>

            {/* Fonksiyon çağrısı */}
            <p>{ad.toUpperCase()}</p>
            <p>{Math.random().toFixed(2)}</p>
        </div>
    );
}
```

## 3.4 JSX İçinde KULLANILAMAYAN Yapılar

```jsx
// ❌ if/else KULLANILAMAZ (ternary veya && kullanın)
// {if (kosul) { return <p>Evet</p> }} // HATA!

// ❌ for döngüsü KULLANILAMAZ (map kullanın)
// {for (let i=0; i<5; i++) { ... }} // HATA!

// ❌ Değişken tanımlama KULLANILAMAZ
// {let x = 5} // HATA!

// ✅ Bunlar JSX dışında yapılmalı:
function App() {
    const kosul = true;
    const liste = [1, 2, 3];

    // If/else JSX dışında
    let mesaj;
    if (kosul) {
        mesaj = <p>Doğru</p>;
    } else {
        mesaj = <p>Yanlış</p>;
    }

    return (
        <div>
            {mesaj}
            {liste.map(item => <span key={item}>{item}</span>)}
        </div>
    );
}
```

---

# 4. Bileşenler (Components)

## 4.1 Bileşen Nedir?

Bileşenler, React uygulamalarının yapı taşlarıdır. Her bileşen bağımsız, yeniden kullanılabilir bir UI parçasıdır. Fonksiyonlar gibi düşünebilirsiniz: girdi alırlar (props) ve ekranda görüntülenecek React elementleri dönerler.

## 4.2 Fonksiyonel Bileşenler (✅ Modern Standart)

```jsx
// En basit bileşen
function Selamlama() {
    return <h1>Merhaba Dünya!</h1>;
}

// Arrow function ile
const Selamlama = () => {
    return <h1>Merhaba Dünya!</h1>;
};

// Tek satır ise return ve süslü parantez gerekmez
const Selamlama = () => <h1>Merhaba Dünya!</h1>;

// Props alan bileşen
function KullaniciBilgisi({ ad, yas, sehir }) {
    return (
        <div className="kullanici-kart">
            <h2>{ad}</h2>
            <p>Yaş: {yas}</p>
            <p>Şehir: {sehir}</p>
        </div>
    );
}

// Kullanımı
function App() {
    return (
        <div>
            <KullaniciBilgisi ad="Ali" yas={25} sehir="İstanbul" />
            <KullaniciBilgisi ad="Ayşe" yas={22} sehir="Ankara" />
        </div>
    );
}
```

## 4.3 Sınıf Bileşenleri (Eski Yöntem)

```jsx
// ⚠️ Artık önerilmiyor, fonksiyonel bileşen + hooks kullanın
// Ama eski kodlarda görebilirsiniz

import React, { Component } from 'react';

class Sayac extends Component {
    constructor(props) {
        super(props);
        this.state = { deger: 0 };
    }

    artir = () => {
        this.setState({ deger: this.state.deger + 1 });
    };

    render() {
        return (
            <div>
                <p>Sayaç: {this.state.deger}</p>
                <button onClick={this.artir}>Artır</button>
            </div>
        );
    }
}

// Fonksiyonel karşılığı (✅ Modern):
function Sayac() {
    const [deger, setDeger] = useState(0);

    return (
        <div>
            <p>Sayaç: {deger}</p>
            <button onClick={() => setDeger(deger + 1)}>Artır</button>
        </div>
    );
}
```

## 4.4 Bileşen Organizasyonu

```
src/
├── components/
│   ├── common/              # Ortak/paylaşılan bileşenler
│   │   ├── Button.jsx
│   │   ├── Input.jsx
│   │   ├── Modal.jsx
│   │   └── Loading.jsx
│   ├── layout/              # Layout bileşenleri
│   │   ├── Header.jsx
│   │   ├── Footer.jsx
│   │   ├── Sidebar.jsx
│   │   └── Layout.jsx
│   └── features/            # Özellik bazlı bileşenler
│       ├── auth/
│       │   ├── LoginForm.jsx
│       │   └── RegisterForm.jsx
│       └── products/
│           ├── ProductCard.jsx
│           └── ProductList.jsx
├── hooks/                    # Özel hook'lar
├── pages/                    # Sayfa bileşenleri
├── context/                  # Context dosyaları
├── services/                 # API servisleri
├── utils/                    # Yardımcı fonksiyonlar
└── constants/                # Sabit değerler
```

## 4.5 Bileşen Kompozisyonu (Composition)

```jsx
// children prop ile bileşen sarmalama
function Kart({ baslik, children }) {
    return (
        <div className="kart">
            <div className="kart-baslik">{baslik}</div>
            <div className="kart-icerik">{children}</div>
        </div>
    );
}

function SayfaDuzeni({ children }) {
    return (
        <div className="sayfa">
            <Header />
            <main>{children}</main>
            <Footer />
        </div>
    );
}

// Kullanım
function App() {
    return (
        <SayfaDuzeni>
            <Kart baslik="Hoşgeldiniz">
                <p>Bu kartın içeriğidir.</p>
                <button>Devam Et</button>
            </Kart>
        </SayfaDuzeni>
    );
}
```

---

# 5. Props (Özellikler)

## 5.1 Props Nedir?

Props (properties), üst bileşenden alt bileşene veri aktarmak için kullanılır. **Salt okunurdur** (read-only), alt bileşen props'u değiştiremez.

```jsx
// Props gönderme
<KullaniciKart
    ad="Ali"
    yas={25}
    aktif={true}
    hobiler={["kitap", "müzik"]}
    adres={{ sehir: "İstanbul", ilce: "Kadıköy" }}
    onClick={handleClick}
/>

// Props alma - Yöntem 1: props objesi
function KullaniciKart(props) {
    return (
        <div>
            <h2>{props.ad}</h2>
            <p>Yaş: {props.yas}</p>
        </div>
    );
}

// Props alma - Yöntem 2: Destructuring (✅ ÖNERİLEN)
function KullaniciKart({ ad, yas, aktif, hobiler, adres, onClick }) {
    return (
        <div onClick={onClick}>
            <h2>{ad}</h2>
            <p>Yaş: {yas}</p>
            <p>Şehir: {adres.sehir}</p>
            <p>Durum: {aktif ? "Aktif" : "Pasif"}</p>
            <ul>
                {hobiler.map((hobi, i) => (
                    <li key={i}>{hobi}</li>
                ))}
            </ul>
        </div>
    );
}
```

## 5.2 Varsayılan Props (Default Props)

```jsx
// Yöntem 1: Destructuring ile varsayılan değer (✅ ÖNERİLEN)
function Button({ metin = "Tıkla", renk = "blue", boyut = "medium", onClick }) {
    return (
        <button
            style={{ backgroundColor: renk }}
            className={`btn btn-${boyut}`}
            onClick={onClick}
        >
            {metin}
        </button>
    );
}

// Kullanım
<Button />                           // "Tıkla", blue, medium
<Button metin="Kaydet" renk="green" /> // "Kaydet", green, medium

// Yöntem 2: defaultProps (eski yöntem)
Button.defaultProps = {
    metin: "Tıkla",
    renk: "blue"
};
```

## 5.3 children Props

```jsx
// children: Bileşenin açılış ve kapanış etiketleri arasındaki içerik
function Uyari({ tur = "bilgi", children }) {
    const renkler = {
        bilgi: "#3498db",
        basari: "#2ecc71",
        uyari: "#f39c12",
        hata: "#e74c3c"
    };

    return (
        <div style={{
            padding: "15px",
            borderLeft: `4px solid ${renkler[tur]}`,
            backgroundColor: `${renkler[tur]}20`,
            borderRadius: "4px",
            margin: "10px 0"
        }}>
            {children}
        </div>
    );
}

// Kullanım
<Uyari tur="basari">
    <strong>Başarılı!</strong>
    <p>İşleminiz tamamlandı.</p>
</Uyari>

<Uyari tur="hata">
    <strong>Hata!</strong>
    <p>Bir şeyler ters gitti.</p>
</Uyari>
```

## 5.4 Prop Doğrulama (PropTypes)

```jsx
import PropTypes from 'prop-types';

function KullaniciKart({ ad, yas, email, aktif, hobiler, onClick }) {
    return (
        <div>
            <h2>{ad}</h2>
            <p>{yas} yaşında</p>
        </div>
    );
}

KullaniciKart.propTypes = {
    ad: PropTypes.string.isRequired,        // Zorunlu string
    yas: PropTypes.number,                   // Opsiyonel sayı
    email: PropTypes.string,                 // Opsiyonel string
    aktif: PropTypes.bool,                   // Boolean
    hobiler: PropTypes.arrayOf(PropTypes.string), // String dizisi
    onClick: PropTypes.func,                 // Fonksiyon
    adres: PropTypes.shape({                 // Belirli yapıda obje
        sehir: PropTypes.string,
        ilce: PropTypes.string
    }),
    durum: PropTypes.oneOf(["aktif", "pasif", "beklemede"]), // Belirli değerler
    yas2: PropTypes.oneOfType([              // Birden fazla tip
        PropTypes.string,
        PropTypes.number
    ])
};

// ⚠️ PropTypes sadece geliştirme modunda uyarı verir
// TypeScript kullanmak daha güvenli bir alternatiftir
```

## 5.5 Props Spread

```jsx
// Tüm props'ları spread ile aktarma
function SarmalButton(props) {
    return <button className="ozel-btn" {...props} />;
}

// Belirli props'ları ayırıp kalanları aktarma
function GelismisInput({ label, error, ...inputProps }) {
    return (
        <div className="form-group">
            <label>{label}</label>
            <input {...inputProps} className={error ? "hata" : ""} />
            {error && <span className="hata-mesaj">{error}</span>}
        </div>
    );
}

// Kullanım
<GelismisInput
    label="Email"
    type="email"
    placeholder="email@ornek.com"
    value={email}
    onChange={handleChange}
    error={hatalar.email}
/>
```

---

# 6. State (Durum Yönetimi)

## 6.1 useState Hook

State, bileşenin **değişebilen verisidir**. State değiştiğinde bileşen yeniden render edilir.

```jsx
import { useState } from 'react';

function Sayac() {
    // const [stateDeğeri, stateGüncelleFonksiyonu] = useState(başlangıçDeğeri);
    const [deger, setDeger] = useState(0);

    return (
        <div>
            <h2>Sayaç: {deger}</h2>
            <button onClick={() => setDeger(deger + 1)}>Artır (+)</button>
            <button onClick={() => setDeger(deger - 1)}>Azalt (-)</button>
            <button onClick={() => setDeger(0)}>Sıfırla</button>
        </div>
    );
}
```

## 6.2 Farklı Tiplerde State

```jsx
function StateOrnekleri() {
    // String state
    const [isim, setIsim] = useState("");

    // Number state
    const [sayac, setSayac] = useState(0);

    // Boolean state
    const [gorunur, setGorunur] = useState(false);

    // Array state
    const [meyveler, setMeyveler] = useState(["Elma", "Armut"]);

    // Object state
    const [kullanici, setKullanici] = useState({
        ad: "",
        email: "",
        yas: 0
    });

    return (
        <div>
            {/* String state güncelleme */}
            <input
                value={isim}
                onChange={(e) => setIsim(e.target.value)}
                placeholder="İsminiz"
            />

            {/* Boolean toggle */}
            <button onClick={() => setGorunur(!gorunur)}>
                {gorunur ? "Gizle" : "Göster"}
            </button>
            {gorunur && <p>Ben görünürüm!</p>}

            {/* Array'e eleman ekleme (spread ile) */}
            <button onClick={() => setMeyveler([...meyveler, "Kiraz"])}>
                Meyve Ekle
            </button>

            {/* Array'den eleman silme */}
            <button onClick={() => setMeyveler(meyveler.filter(m => m !== "Elma"))}>
                Elma'yı Sil
            </button>

            {/* Object güncelleme (spread ile) */}
            <input
                value={kullanici.ad}
                onChange={(e) => setKullanici({ ...kullanici, ad: e.target.value })}
                placeholder="Ad"
            />
        </div>
    );
}
```

## 6.3 State Güncelleme Kuralları

```jsx
function StateKurallari() {
    const [sayac, setSayac] = useState(0);
    const [liste, setListe] = useState([1, 2, 3]);
    const [kisi, setKisi] = useState({ ad: "Ali", yas: 25 });

    // ⚠️ KURAL 1: State'i DOĞRUDAN DEĞİŞTİRMEYİN (mutate etmeyin)
    // ❌ Yanlış:
    // sayac = sayac + 1;
    // liste.push(4);
    // kisi.ad = "Veli";

    // ✅ Doğru: setter fonksiyonunu kullanın
    const artir = () => setSayac(sayac + 1);

    // ⚠️ KURAL 2: Önceki state'e bağımlıysa FONKSIYON FORMU kullanın
    // ❌ Sorunlu (eski state'e referans):
    const ucArtir_yanlis = () => {
        setSayac(sayac + 1);
        setSayac(sayac + 1);
        setSayac(sayac + 1);
        // Sonuç: sadece 1 artar! (batch güncelleme)
    };

    // ✅ Doğru (fonksiyon formu):
    const ucArtir_dogru = () => {
        setSayac(prev => prev + 1);
        setSayac(prev => prev + 1);
        setSayac(prev => prev + 1);
        // Sonuç: 3 artar!
    };

    // ⚠️ KURAL 3: Array ve Object için YENİ referans oluşturun
    // Array işlemleri:
    const elemanEkle = () => setListe([...liste, 4]);
    const elemanSil = (i) => setListe(liste.filter((_, idx) => idx !== i));
    const elemanGuncelle = (i, yeniDeger) =>
        setListe(liste.map((item, idx) => idx === i ? yeniDeger : item));

    // Object işlemleri:
    const adGuncelle = (yeniAd) => setKisi({ ...kisi, ad: yeniAd });
    const yasArtir = () => setKisi(prev => ({ ...prev, yas: prev.yas + 1 }));

    return <div>...</div>;
}
```

## 6.4 State Kaldırma (Lifting State Up)

```jsx
// Kardeş bileşenler arasında veri paylaşımı için
// state'i ortak üst bileşene taşıyın

// Üst bileşen (state burada tutulur)
function SicaklikHesaplayici() {
    const [sicaklik, setSicaklik] = useState("");
    const [olcek, setOlcek] = useState("C");

    const celsius = olcek === "F"
        ? ((parseFloat(sicaklik) - 32) * 5/9).toFixed(2)
        : sicaklik;

    const fahrenheit = olcek === "C"
        ? ((parseFloat(sicaklik) * 9/5) + 32).toFixed(2)
        : sicaklik;

    return (
        <div>
            <SicaklikGirisi
                olcek="C"
                sicaklik={celsius}
                onChange={(deger) => { setSicaklik(deger); setOlcek("C"); }}
            />
            <SicaklikGirisi
                olcek="F"
                sicaklik={fahrenheit}
                onChange={(deger) => { setSicaklik(deger); setOlcek("F"); }}
            />
        </div>
    );
}

// Alt bileşen (state'i props olarak alır)
function SicaklikGirisi({ olcek, sicaklik, onChange }) {
    return (
        <fieldset>
            <legend>{olcek === "C" ? "Celsius" : "Fahrenheit"}</legend>
            <input
                value={sicaklik}
                onChange={(e) => onChange(e.target.value)}
            />
        </fieldset>
    );
}
```

---

# 7. Olaylar (Event Handling)

## 7.1 Olay Yönetimi Temelleri

```jsx
function OlayOrnekleri() {

    // Click olayı
    const tiklandi = () => {
        console.log("Butona tıklandı!");
    };

    // Parametre ile
    const selamla = (isim) => {
        alert(`Merhaba, ${isim}!`);
    };

    // Event objesi ile
    const inputDegisti = (event) => {
        console.log("Yeni değer:", event.target.value);
    };

    return (
        <div>
            {/* Fonksiyon referansı (✅ doğru) */}
            <button onClick={tiklandi}>Tıkla</button>

            {/* ❌ Yanlış: Fonksiyonu hemen çağırır! */}
            {/* <button onClick={tiklandi()}>Tıkla</button> */}

            {/* Parametre gönderme (arrow function ile) */}
            <button onClick={() => selamla("Ali")}>Selamla</button>

            {/* Event objesi */}
            <input onChange={inputDegisti} placeholder="Yazın..." />

            {/* Inline arrow function */}
            <button onClick={(e) => {
                e.preventDefault();
                console.log("Tıklandı", e.target);
            }}>
                Alt Satır İşlem
            </button>
        </div>
    );
}
```

## 7.2 Yaygın Olaylar

```jsx
function YayginOlaylar() {
    return (
        <div>
            {/* Mouse Olayları */}
            <div
                onClick={() => console.log("Tıklandı")}
                onDoubleClick={() => console.log("Çift tıklandı")}
                onMouseEnter={() => console.log("Mouse girdi")}
                onMouseLeave={() => console.log("Mouse çıktı")}
                onContextMenu={(e) => { e.preventDefault(); console.log("Sağ tık"); }}
            >
                Mouse Olayları
            </div>

            {/* Klavye Olayları */}
            <input
                onKeyDown={(e) => {
                    if (e.key === "Enter") console.log("Enter basıldı");
                    if (e.ctrlKey && e.key === "s") {
                        e.preventDefault();
                        console.log("Ctrl+S basıldı");
                    }
                }}
                onKeyUp={(e) => console.log("Tuş bırakıldı:", e.key)}
            />

            {/* Form Olayları */}
            <form onSubmit={(e) => {
                e.preventDefault(); // Sayfa yenilenmesini engelle!
                console.log("Form gönderildi");
            }}>
                <input
                    onChange={(e) => console.log(e.target.value)}
                    onFocus={() => console.log("Odaklandı")}
                    onBlur={() => console.log("Odak kaybetti")}
                />
                <button type="submit">Gönder</button>
            </form>

            {/* Scroll */}
            <div onScroll={(e) => console.log(e.target.scrollTop)}>
                Kaydırılabilir içerik
            </div>
        </div>
    );
}
```

## 7.3 Sentetik Olaylar (Synthetic Events)

```jsx
// React kendi olay sistemini kullanır (SyntheticEvent)
// Tüm tarayıcılarda tutarlı çalışır

function SentetikOlay() {
    const handleClick = (event) => {
        // SyntheticEvent özellikleri
        console.log(event.type);           // "click"
        console.log(event.target);          // Tıklanan element
        console.log(event.currentTarget);   // Handler'ın bağlı olduğu element
        console.log(event.clientX, event.clientY); // Mouse pozisyonu
        console.log(event.ctrlKey);         // Ctrl basılı mı?

        event.preventDefault();   // Varsayılan davranışı engelle
        event.stopPropagation();  // Üst elemanlara yayılmayı engelle

        // Gerçek DOM olayına erişim
        console.log(event.nativeEvent);
    };

    return <button onClick={handleClick}>Tıkla</button>;
}
```

---

# 8. Koşullu Render

```jsx
function KosulluRender({ girisYapildi, yukleniyor, hata, kullanici }) {

    // 1. if/else ile (return öncesinde)
    if (yukleniyor) return <p>Yükleniyor...</p>;
    if (hata) return <p>Hata: {hata}</p>;
    if (!girisYapildi) return <GirisFormu />;

    // 2. Ternary operatör (JSX içinde)
    return (
        <div>
            {girisYapildi
                ? <p>Hoşgeldin, {kullanici.ad}!</p>
                : <p>Lütfen giriş yapın.</p>
            }

            {/* 3. && operatörü (sadece true ise render) */}
            {kullanici.admin && <button>Yönetim Paneli</button>}

            {/* ⚠️ DİKKAT: sayı 0 ile && kullanımı */}
            {/* ❌ {mesajSayisi && <span>{mesajSayisi}</span>} */}
            {/* mesajSayisi 0 ise ekranda "0" görünür! */}
            {/* ✅ {mesajSayisi > 0 && <span>{mesajSayisi}</span>} */}

            {/* 4. IIFE ile karmaşık koşullar */}
            {(() => {
                switch (kullanici.rol) {
                    case "admin": return <AdminPanel />;
                    case "editor": return <EditorPanel />;
                    default: return <KullaniciPanel />;
                }
            })()}

            {/* 5. Obje lookup ile */}
            {
                {
                    admin: <AdminPanel />,
                    editor: <EditorPanel />,
                    user: <KullaniciPanel />
                }[kullanici.rol]
            }
        </div>
    );
}

// 6. Ayrı bileşen ile
function DurumMesaji({ durum }) {
    const mesajlar = {
        basarili: { renk: "green", metin: "✅ Başarılı!" },
        hata: { renk: "red", metin: "❌ Hata oluştu!" },
        uyari: { renk: "orange", metin: "⚠️ Dikkat!" }
    };

    const bilgi = mesajlar[durum];
    if (!bilgi) return null; // Hiçbir şey render etme

    return <p style={{ color: bilgi.renk }}>{bilgi.metin}</p>;
}
```

---

# 9. Listeler ve Anahtarlar (Lists & Keys)

```jsx
function ListeOrnekleri() {
    const meyveler = ["Elma", "Armut", "Kiraz", "Üzüm"];

    const kullanicilar = [
        { id: 1, ad: "Ali", yas: 25 },
        { id: 2, ad: "Ayşe", yas: 22 },
        { id: 3, ad: "Mehmet", yas: 28 }
    ];

    return (
        <div>
            {/* Basit liste */}
            <ul>
                {meyveler.map((meyve, index) => (
                    <li key={index}>{meyve}</li>
                ))}
            </ul>

            {/* Obje listesi (benzersiz id kullanın!) */}
            <div>
                {kullanicilar.map((kullanici) => (
                    <div key={kullanici.id} className="kart">
                        <h3>{kullanici.ad}</h3>
                        <p>Yaş: {kullanici.yas}</p>
                    </div>
                ))}
            </div>
        </div>
    );
}

// ⚠️ KEY KURALLARI:
// 1. key benzersiz olmalı (kardeşler arasında)
// 2. key değişmemeli (stabil olmalı)
// 3. ❌ index'i key olarak kullanmaktan KAÇININ (sıralama değişirse sorun çıkar)
// 4. ✅ Veritabanı ID'si veya benzersiz bir değer kullanın
// 5. key bir prop değildir, bileşen içinden erişilemez
```

---

# 10. Formlar (Forms)

## 10.1 Controlled Components (Kontrollü Bileşenler)

```jsx
import { useState } from 'react';

function KayitFormu() {
    const [formData, setFormData] = useState({
        ad: "",
        email: "",
        sifre: "",
        cinsiyet: "",
        sehir: "istanbul",
        kabul: false,
        mesaj: ""
    });

    const [hatalar, setHatalar] = useState({});

    const handleChange = (e) => {
        const { name, value, type, checked } = e.target;
        setFormData(prev => ({
            ...prev,
            [name]: type === "checkbox" ? checked : value
        }));
    };

    const validate = () => {
        const yeniHatalar = {};
        if (!formData.ad.trim()) yeniHatalar.ad = "Ad zorunludur";
        if (!formData.email.includes("@")) yeniHatalar.email = "Geçersiz email";
        if (formData.sifre.length < 6) yeniHatalar.sifre = "En az 6 karakter";
        if (!formData.kabul) yeniHatalar.kabul = "Kabul etmelisiniz";
        setHatalar(yeniHatalar);
        return Object.keys(yeniHatalar).length === 0;
    };

    const handleSubmit = (e) => {
        e.preventDefault();
        if (validate()) {
            console.log("Form gönderildi:", formData);
        }
    };

    return (
        <form onSubmit={handleSubmit}>
            {/* Text Input */}
            <div>
                <label htmlFor="ad">Ad:</label>
                <input
                    id="ad"
                    name="ad"
                    type="text"
                    value={formData.ad}
                    onChange={handleChange}
                />
                {hatalar.ad && <span className="hata">{hatalar.ad}</span>}
            </div>

            {/* Email Input */}
            <div>
                <label htmlFor="email">Email:</label>
                <input
                    id="email"
                    name="email"
                    type="email"
                    value={formData.email}
                    onChange={handleChange}
                />
                {hatalar.email && <span className="hata">{hatalar.email}</span>}
            </div>

            {/* Password Input */}
            <div>
                <label htmlFor="sifre">Şifre:</label>
                <input
                    id="sifre"
                    name="sifre"
                    type="password"
                    value={formData.sifre}
                    onChange={handleChange}
                />
                {hatalar.sifre && <span className="hata">{hatalar.sifre}</span>}
            </div>

            {/* Radio Buttons */}
            <div>
                <label>
                    <input type="radio" name="cinsiyet" value="erkek"
                        checked={formData.cinsiyet === "erkek"}
                        onChange={handleChange} /> Erkek
                </label>
                <label>
                    <input type="radio" name="cinsiyet" value="kadin"
                        checked={formData.cinsiyet === "kadin"}
                        onChange={handleChange} /> Kadın
                </label>
            </div>

            {/* Select */}
            <div>
                <label htmlFor="sehir">Şehir:</label>
                <select id="sehir" name="sehir" value={formData.sehir} onChange={handleChange}>
                    <option value="istanbul">İstanbul</option>
                    <option value="ankara">Ankara</option>
                    <option value="izmir">İzmir</option>
                </select>
            </div>

            {/* Textarea */}
            <div>
                <label htmlFor="mesaj">Mesaj:</label>
                <textarea id="mesaj" name="mesaj" value={formData.mesaj}
                    onChange={handleChange} rows={4} />
            </div>

            {/* Checkbox */}
            <div>
                <label>
                    <input type="checkbox" name="kabul"
                        checked={formData.kabul}
                        onChange={handleChange} />
                    Koşulları kabul ediyorum
                </label>
                {hatalar.kabul && <span className="hata">{hatalar.kabul}</span>}
            </div>

            <button type="submit">Kayıt Ol</button>
        </form>
    );
}
```

---

# 11. useEffect Hook

## 11.1 useEffect Nedir?

useEffect, bileşenlerde **yan etki** (side effect) işlemlerini yönetmek için kullanılır. Veri çekme, abonelik oluşturma, DOM manipülasyonu gibi işlemler yan etkidir.

```jsx
import { useState, useEffect } from 'react';

function Ornek() {
    const [sayac, setSayac] = useState(0);

    // Her render'dan SONRA çalışır
    useEffect(() => {
        document.title = `${sayac} kez tıklandı`;
    });

    return <button onClick={() => setSayac(sayac + 1)}>Tıkla: {sayac}</button>;
}
```

## 11.2 Bağımlılık Dizisi (Dependency Array)

```jsx
function UseEffectOrnekleri() {
    const [sayac, setSayac] = useState(0);
    const [isim, setIsim] = useState("");

    // 1. Bağımlılık dizisi YOK → HER render'da çalışır
    useEffect(() => {
        console.log("Her render'da çalışır");
    });

    // 2. Boş bağımlılık dizisi [] → SADECE İLK render'da çalışır (mount)
    useEffect(() => {
        console.log("Sadece bir kez çalışır (componentDidMount)");
        // API çağrıları, event listener ekleme vb.
    }, []);

    // 3. Bağımlılıklı → Belirtilen değerler DEĞİŞTİĞİNDE çalışır
    useEffect(() => {
        console.log(`Sayaç değişti: ${sayac}`);
        document.title = `Sayaç: ${sayac}`;
    }, [sayac]); // Sadece sayac değiştiğinde çalışır

    // 4. Birden fazla bağımlılık
    useEffect(() => {
        console.log(`Sayaç: ${sayac}, İsim: ${isim}`);
    }, [sayac, isim]); // İkisinden biri değiştiğinde çalışır

    return (
        <div>
            <p>Sayaç: {sayac}</p>
            <button onClick={() => setSayac(s => s + 1)}>Artır</button>
            <input value={isim} onChange={e => setIsim(e.target.value)} />
        </div>
    );
}
```

## 11.3 Cleanup (Temizlik) Fonksiyonu

```jsx
function ZamanGosterici() {
    const [saat, setSaat] = useState(new Date());

    useEffect(() => {
        // Effect: Interval başlat
        const intervalId = setInterval(() => {
            setSaat(new Date());
        }, 1000);

        // Cleanup: Bileşen unmount olduğunda veya effect yeniden çalışmadan önce
        return () => {
            clearInterval(intervalId); // Bellek sızıntısını önle!
        };
    }, []); // Boş dizi: sadece mount/unmount'ta çalışır

    return <p>Saat: {saat.toLocaleTimeString("tr-TR")}</p>;
}

// Event listener örneği
function PencereBoyutu() {
    const [boyut, setBoyut] = useState({
        genislik: window.innerWidth,
        yukseklik: window.innerHeight
    });

    useEffect(() => {
        const handleResize = () => {
            setBoyut({
                genislik: window.innerWidth,
                yukseklik: window.innerHeight
            });
        };

        window.addEventListener("resize", handleResize);

        return () => {
            window.removeEventListener("resize", handleResize); // Temizlik!
        };
    }, []);

    return <p>Pencere: {boyut.genislik} x {boyut.yukseklik}</p>;
}
```

## 11.4 Veri Çekme (Data Fetching)

```jsx
function KullaniciListesi() {
    const [kullanicilar, setKullanicilar] = useState([]);
    const [yukleniyor, setYukleniyor] = useState(true);
    const [hata, setHata] = useState(null);

    useEffect(() => {
        const veriGetir = async () => {
            try {
                setYukleniyor(true);
                const response = await fetch("https://jsonplaceholder.typicode.com/users");

                if (!response.ok) throw new Error(`HTTP Hata: ${response.status}`);

                const data = await response.json();
                setKullanicilar(data);
            } catch (err) {
                setHata(err.message);
            } finally {
                setYukleniyor(false);
            }
        };

        veriGetir();
    }, []); // Sadece mount'ta çalışır

    if (yukleniyor) return <p>Yükleniyor...</p>;
    if (hata) return <p>Hata: {hata}</p>;

    return (
        <ul>
            {kullanicilar.map(k => (
                <li key={k.id}>{k.name} - {k.email}</li>
            ))}
        </ul>
    );
}

// Abort Controller ile iptal edilebilir fetch
function AramaKutusu() {
    const [query, setQuery] = useState("");
    const [sonuclar, setSonuclar] = useState([]);

    useEffect(() => {
        if (!query.trim()) { setSonuclar([]); return; }

        const controller = new AbortController();

        const ara = async () => {
            try {
                const res = await fetch(`/api/search?q=${query}`, {
                    signal: controller.signal
                });
                const data = await res.json();
                setSonuclar(data);
            } catch (err) {
                if (err.name !== "AbortError") console.error(err);
            }
        };

        const timer = setTimeout(ara, 300); // Debounce

        return () => {
            clearTimeout(timer);
            controller.abort(); // Önceki isteği iptal et
        };
    }, [query]);

    return (
        <div>
            <input value={query} onChange={e => setQuery(e.target.value)} placeholder="Ara..." />
            <ul>{sonuclar.map(s => <li key={s.id}>{s.title}</li>)}</ul>
        </div>
    );
}
```

## 11.5 useEffect Yaygın Hatalar

```jsx
// ❌ HATA 1: Sonsuz döngü
useEffect(() => {
    setDeger(deger + 1); // State değişir → useEffect tekrar çalışır → sonsuz!
}); // Bağımlılık dizisi yok!

// ✅ Çözüm: Bağımlılık dizisi ekle
useEffect(() => {
    setDeger(deger + 1);
}, []); // Sadece mount'ta çalışır

// ❌ HATA 2: useEffect'te async fonksiyon
useEffect(async () => { // ❌ useEffect callback async olamaz!
    const data = await fetch("/api/data");
}, []);

// ✅ Çözüm: İç fonksiyon kullan
useEffect(() => {
    const fetchData = async () => {
        const data = await fetch("/api/data");
    };
    fetchData();
}, []);

// ❌ HATA 3: Obje/Array bağımlılık
const options = { url: "/api" }; // Her render'da yeni referans!
useEffect(() => {
    fetch(options.url);
}, [options]); // Her render'da çalışır (referans değişiyor)!

// ✅ Çözüm: useMemo veya primitif bağımlılık kullan
const url = "/api";
useEffect(() => {
    fetch(url);
}, [url]); // String karşılaştırma, sorunsuz
```

---

# 12. useRef Hook

```jsx
import { useRef, useState, useEffect } from 'react';

function UseRefOrnekleri() {
    // 1. DOM elemanına erişim
    const inputRef = useRef(null);

    const odaklan = () => {
        inputRef.current.focus();   // DOM elemanına doğrudan erişim
        inputRef.current.value = ""; // Değer temizleme
    };

    // 2. Önceki değeri saklama (render tetiklemez!)
    const [sayac, setSayac] = useState(0);
    const oncekiRef = useRef(0);

    useEffect(() => {
        oncekiRef.current = sayac;
    }, [sayac]);

    // 3. Interval/Timeout ID saklama
    const intervalRef = useRef(null);

    const baslat = () => {
        intervalRef.current = setInterval(() => {
            setSayac(s => s + 1);
        }, 1000);
    };

    const durdur = () => {
        clearInterval(intervalRef.current);
    };

    // 4. Render sayısını takip etme
    const renderSayisi = useRef(0);
    renderSayisi.current++;

    return (
        <div>
            <input ref={inputRef} placeholder="Odaklanmak için butona tıklayın" />
            <button onClick={odaklan}>Odaklan</button>

            <p>Sayaç: {sayac} (Önceki: {oncekiRef.current})</p>
            <button onClick={baslat}>Başlat</button>
            <button onClick={durdur}>Durdur</button>

            <p>Bu bileşen {renderSayisi.current} kez render edildi.</p>
        </div>
    );
}

// ⚠️ useRef vs useState:
// useRef: Değer değiştiğinde render TETIKLEMEZ, .current ile erişilir
// useState: Değer değiştiğinde render TETIKLER, setter ile güncellenir
```

---

# 13. useMemo ve useCallback

## 13.1 useMemo - Hesaplama Sonucunu Önbelleğe Alma

```jsx
import { useState, useMemo } from 'react';

function PahalıHesaplama() {
    const [sayilar, setSayilar] = useState([1, 2, 3, 4, 5]);
    const [tema, setTema] = useState("açık");

    // ❌ Her render'da yeniden hesaplanır (tema değişse bile!)
    // const toplam = sayilar.reduce((acc, n) => acc + n, 0);

    // ✅ Sadece sayilar değiştiğinde yeniden hesaplanır
    const toplam = useMemo(() => {
        console.log("Toplam hesaplanıyor...");
        return sayilar.reduce((acc, n) => acc + n, 0);
    }, [sayilar]);

    // useMemo ile obje referansı koruma
    const stil = useMemo(() => ({
        backgroundColor: tema === "koyu" ? "#333" : "#fff",
        color: tema === "koyu" ? "#fff" : "#333"
    }), [tema]);

    return (
        <div style={stil}>
            <p>Toplam: {toplam}</p>
            <button onClick={() => setTema(t => t === "açık" ? "koyu" : "açık")}>
                Tema Değiştir
            </button>
        </div>
    );
}
```

## 13.2 useCallback - Fonksiyon Referansını Önbelleğe Alma

```jsx
import { useState, useCallback } from 'react';

function UstBilesen() {
    const [sayac, setSayac] = useState(0);
    const [metin, setMetin] = useState("");

    // ❌ Her render'da yeni fonksiyon oluşur
    // const artir = () => setSayac(s => s + 1);

    // ✅ Fonksiyon referansı korunur (memo'lu alt bileşenler için önemli)
    const artir = useCallback(() => {
        setSayac(s => s + 1);
    }, []); // Bağımlılık yok, fonksiyon asla yeniden oluşturulmaz

    const sil = useCallback((id) => {
        setSayac(s => s - 1);
    }, []);

    return (
        <div>
            <input value={metin} onChange={e => setMetin(e.target.value)} />
            <SayacButonu onClick={artir} label="Artır" />
            <p>Sayaç: {sayac}</p>
        </div>
    );
}

// React.memo ile sarmalanmış alt bileşen
const SayacButonu = React.memo(({ onClick, label }) => {
    console.log(`${label} butonu render edildi`);
    return <button onClick={onClick}>{label}</button>;
});
```

## 13.3 Ne Zaman Kullanmalı?

```
useMemo kullan:
✅ Pahalı hesaplamalar (büyük dizi işlemleri, karmaşık Math)
✅ Referans eşitliği gereken objeler/diziler (useEffect bağımlılığı)
✅ React.memo ile kullanılan alt bileşenlere geçirilen objeler

useCallback kullan:
✅ React.memo ile sarmalanmış alt bileşenlere geçirilen fonksiyonlar
✅ useEffect bağımlılık dizisindeki fonksiyonlar
✅ Custom hook'lardan dönen fonksiyonlar

❌ KULLANMAYIN:
❌ Basit hesaplamalar (a + b gibi)
❌ Primitive değerler (string, number)
❌ Her yerde gereksiz kullanım (erken optimizasyon)
```

---

# 14. useReducer Hook

```jsx
import { useReducer } from 'react';

// Reducer: Mevcut state ve action alıp yeni state döner
function todoReducer(state, action) {
    switch (action.type) {
        case "EKLE":
            return [...state, {
                id: Date.now(),
                metin: action.payload,
                tamamlandi: false
            }];

        case "SIL":
            return state.filter(todo => todo.id !== action.payload);

        case "TOGGLE":
            return state.map(todo =>
                todo.id === action.payload
                    ? { ...todo, tamamlandi: !todo.tamamlandi }
                    : todo
            );

        case "TEMIZLE":
            return [];

        default:
            return state;
    }
}

function TodoApp() {
    const [todos, dispatch] = useReducer(todoReducer, []);
    const [girdi, setGirdi] = useState("");

    const ekle = () => {
        if (!girdi.trim()) return;
        dispatch({ type: "EKLE", payload: girdi });
        setGirdi("");
    };

    return (
        <div>
            <input value={girdi} onChange={e => setGirdi(e.target.value)}
                onKeyDown={e => e.key === "Enter" && ekle()} />
            <button onClick={ekle}>Ekle</button>
            <button onClick={() => dispatch({ type: "TEMIZLE" })}>Temizle</button>

            <ul>
                {todos.map(todo => (
                    <li key={todo.id}
                        style={{ textDecoration: todo.tamamlandi ? "line-through" : "none" }}>
                        <span onClick={() => dispatch({ type: "TOGGLE", payload: todo.id })}>
                            {todo.metin}
                        </span>
                        <button onClick={() => dispatch({ type: "SIL", payload: todo.id })}>
                            🗑️
                        </button>
                    </li>
                ))}
            </ul>
        </div>
    );
}

// useReducer vs useState:
// useState → Basit state (sayaç, toggle, tek değer)
// useReducer → Karmaşık state (birden fazla alt değer, ilişkili güncellemeler)
```

---

# 15. useContext ve Context API

## 15.1 Context Nedir?

Context, prop drilling (props'ları birçok seviye aşağı geçirme) sorununu çözer. Global state paylaşımı sağlar.

```jsx
import { createContext, useContext, useState } from 'react';

// 1. Context oluştur
const TemaContext = createContext();

// 2. Provider oluştur
function TemaProvider({ children }) {
    const [tema, setTema] = useState("açık");

    const temaToggle = () => {
        setTema(prev => prev === "açık" ? "koyu" : "açık");
    };

    return (
        <TemaContext.Provider value={{ tema, temaToggle }}>
            {children}
        </TemaContext.Provider>
    );
}

// 3. Custom hook ile kullanımı kolaylaştır
function useTema() {
    const context = useContext(TemaContext);
    if (!context) {
        throw new Error("useTema, TemaProvider içinde kullanılmalıdır!");
    }
    return context;
}

// 4. Bileşenlerde kullan
function Header() {
    const { tema, temaToggle } = useTema();
    return (
        <header style={{ background: tema === "koyu" ? "#333" : "#fff" }}>
            <h1>Uygulama</h1>
            <button onClick={temaToggle}>
                {tema === "koyu" ? "☀️ Açık" : "🌙 Koyu"} Tema
            </button>
        </header>
    );
}

function Icerik() {
    const { tema } = useTema();
    return (
        <main style={{
            background: tema === "koyu" ? "#222" : "#f5f5f5",
            color: tema === "koyu" ? "#fff" : "#333"
        }}>
            <p>İçerik burada</p>
        </main>
    );
}

// 5. App'i Provider ile sar
function App() {
    return (
        <TemaProvider>
            <Header />
            <Icerik />
        </TemaProvider>
    );
}
```

## 15.2 Çoklu Context Birleştirme

```jsx
// Birden fazla context'i tek provider'da birleştirme
function AppProviders({ children }) {
    return (
        <TemaProvider>
            <AuthProvider>
                <DilProvider>
                    {children}
                </DilProvider>
            </AuthProvider>
        </TemaProvider>
    );
}

function App() {
    return (
        <AppProviders>
            <Router />
        </AppProviders>
    );
}
```

---

# 16. Custom Hooks (Özel Kancalar)

Custom hook'lar, bileşenler arası state mantığını paylaşmak için kullanılır. `use` ile başlamalıdır.

```jsx
// 1. useLocalStorage - Local Storage ile senkronize state
function useLocalStorage(anahtar, varsayilan) {
    const [deger, setDeger] = useState(() => {
        try {
            const kayitli = localStorage.getItem(anahtar);
            return kayitli ? JSON.parse(kayitli) : varsayilan;
        } catch {
            return varsayilan;
        }
    });

    useEffect(() => {
        localStorage.setItem(anahtar, JSON.stringify(deger));
    }, [anahtar, deger]);

    return [deger, setDeger];
}
// Kullanım: const [tema, setTema] = useLocalStorage("tema", "açık");

// 2. useFetch - Veri çekme hook'u
function useFetch(url) {
    const [data, setData] = useState(null);
    const [loading, setLoading] = useState(true);
    const [error, setError] = useState(null);

    useEffect(() => {
        const controller = new AbortController();

        const fetchData = async () => {
            try {
                setLoading(true);
                const res = await fetch(url, { signal: controller.signal });
                if (!res.ok) throw new Error(`HTTP ${res.status}`);
                const json = await res.json();
                setData(json);
                setError(null);
            } catch (err) {
                if (err.name !== "AbortError") setError(err.message);
            } finally {
                setLoading(false);
            }
        };

        fetchData();
        return () => controller.abort();
    }, [url]);

    return { data, loading, error };
}
// Kullanım:
// const { data, loading, error } = useFetch("/api/users");

// 3. useDebounce
function useDebounce(deger, gecikme = 500) {
    const [debouncedDeger, setDebouncedDeger] = useState(deger);

    useEffect(() => {
        const timer = setTimeout(() => setDebouncedDeger(deger), gecikme);
        return () => clearTimeout(timer);
    }, [deger, gecikme]);

    return debouncedDeger;
}
// Kullanım:
// const [arama, setArama] = useState("");
// const debouncedArama = useDebounce(arama, 300);

// 4. useToggle
function useToggle(ilkDeger = false) {
    const [deger, setDeger] = useState(ilkDeger);
    const toggle = useCallback(() => setDeger(v => !v), []);
    return [deger, toggle];
}
// Kullanım: const [gorunur, toggleGorunur] = useToggle(false);

// 5. useWindowSize
function useWindowSize() {
    const [size, setSize] = useState({
        width: window.innerWidth,
        height: window.innerHeight
    });

    useEffect(() => {
        const handler = () => setSize({
            width: window.innerWidth,
            height: window.innerHeight
        });
        window.addEventListener("resize", handler);
        return () => window.removeEventListener("resize", handler);
    }, []);

    return size;
}
// Kullanım: const { width, height } = useWindowSize();

// 6. useOnClickOutside
function useOnClickOutside(ref, handler) {
    useEffect(() => {
        const listener = (e) => {
            if (!ref.current || ref.current.contains(e.target)) return;
            handler(e);
        };
        document.addEventListener("mousedown", listener);
        return () => document.removeEventListener("mousedown", listener);
    }, [ref, handler]);
}
// Kullanım:
// const menuRef = useRef();
// useOnClickOutside(menuRef, () => setMenuAcik(false));
```

---

# 17. React Router

```bash
# Kurulum
npm install react-router-dom
```

```jsx
import { BrowserRouter, Routes, Route, Link, NavLink,
         useNavigate, useParams, useSearchParams, Outlet,
         Navigate } from 'react-router-dom';

// Ana Router yapısı
function App() {
    return (
        <BrowserRouter>
            <nav>
                <Link to="/">Ana Sayfa</Link>
                <Link to="/hakkinda">Hakkında</Link>
                <NavLink to="/iletisim"
                    className={({ isActive }) => isActive ? "aktif" : ""}>
                    İletişim
                </NavLink>
            </nav>

            <Routes>
                <Route path="/" element={<AnaSayfa />} />
                <Route path="/hakkinda" element={<Hakkinda />} />
                <Route path="/iletisim" element={<Iletisim />} />

                {/* Dinamik parametre */}
                <Route path="/kullanici/:id" element={<KullaniciDetay />} />

                {/* Nested (iç içe) route */}
                <Route path="/panel" element={<PanelLayout />}>
                    <Route index element={<PanelAnaSayfa />} />
                    <Route path="ayarlar" element={<Ayarlar />} />
                    <Route path="profil" element={<Profil />} />
                </Route>

                {/* Korumalı route */}
                <Route path="/gizli" element={
                    <KorumaliRoute>
                        <GizliSayfa />
                    </KorumaliRoute>
                } />

                {/* Yönlendirme */}
                <Route path="/eski-sayfa" element={<Navigate to="/yeni-sayfa" replace />} />

                {/* 404 Sayfası */}
                <Route path="*" element={<Sayfa404 />} />
            </Routes>
        </BrowserRouter>
    );
}

// Dinamik parametre kullanımı
function KullaniciDetay() {
    const { id } = useParams();
    return <h1>Kullanıcı ID: {id}</h1>;
}

// Programatik yönlendirme
function GirisFormu() {
    const navigate = useNavigate();

    const girisYap = () => {
        // Giriş işlemi...
        navigate("/panel");           // Yönlendir
        // navigate(-1);              // Geri git
        // navigate("/panel", { replace: true }); // Geçmişi değiştir
    };

    return <button onClick={girisYap}>Giriş Yap</button>;
}

// Nested route layout
function PanelLayout() {
    return (
        <div className="panel">
            <aside>
                <Link to="/panel">Ana Sayfa</Link>
                <Link to="/panel/ayarlar">Ayarlar</Link>
                <Link to="/panel/profil">Profil</Link>
            </aside>
            <main>
                <Outlet /> {/* Alt route'lar burada render edilir */}
            </main>
        </div>
    );
}

// Korumalı route
function KorumaliRoute({ children }) {
    const { kullanici } = useAuth(); // Custom auth hook
    if (!kullanici) return <Navigate to="/giris" replace />;
    return children;
}

// Query parametreleri
function AramaSayfasi() {
    const [searchParams, setSearchParams] = useSearchParams();
    const query = searchParams.get("q") || "";

    return (
        <input
            value={query}
            onChange={e => setSearchParams({ q: e.target.value })}
            placeholder="Ara..."
        />
    );
}
```

---

# 18. Stil Yönetimi (Styling)

```jsx
// 1. Inline Styles
function InlineStil() {
    const stil = {
        backgroundColor: '#3498db',
        color: 'white',
        padding: '10px 20px',
        borderRadius: '8px',
        border: 'none',
        cursor: 'pointer',
        fontSize: '16px'
    };
    return <button style={stil}>Stillendirilmiş Buton</button>;
}

// 2. CSS Dosyası
// Button.css
// .btn { padding: 10px 20px; border-radius: 8px; }
// .btn-primary { background: #3498db; color: white; }

import './Button.css';
function CssButton() {
    return <button className="btn btn-primary">CSS Buton</button>;
}

// 3. CSS Modules (✅ Önerilen - scoped CSS)
// Button.module.css
// .button { padding: 10px 20px; }
// .primary { background: blue; }

import styles from './Button.module.css';
function ModuleButton() {
    return (
        <button className={`${styles.button} ${styles.primary}`}>
            Module Buton
        </button>
    );
}

// 4. Koşullu sınıf ekleme
function KosulluSinif({ aktif, disabled }) {
    const siniflar = [
        "btn",
        aktif && "btn-aktif",
        disabled && "btn-disabled"
    ].filter(Boolean).join(" ");

    return <button className={siniflar}>Koşullu Buton</button>;
}

// 5. clsx veya classnames kütüphanesi ile
// npm install clsx
import clsx from 'clsx';
function ClsxButton({ aktif, boyut }) {
    return (
        <button className={clsx("btn", {
            "btn-aktif": aktif,
            "btn-buyuk": boyut === "lg",
            "btn-kucuk": boyut === "sm"
        })}>
            clsx Buton
        </button>
    );
}
```

---

# 19. API İstekleri ve Veri Çekme

```jsx
// Kapsamlı API servisi
const API_BASE = "https://jsonplaceholder.typicode.com";

const apiServisi = {
    async getir(endpoint) {
        const res = await fetch(`${API_BASE}${endpoint}`);
        if (!res.ok) throw new Error(`HTTP ${res.status}`);
        return res.json();
    },

    async gonder(endpoint, veri) {
        const res = await fetch(`${API_BASE}${endpoint}`, {
            method: "POST",
            headers: { "Content-Type": "application/json" },
            body: JSON.stringify(veri)
        });
        return res.json();
    },

    async guncelle(endpoint, veri) {
        const res = await fetch(`${API_BASE}${endpoint}`, {
            method: "PUT",
            headers: { "Content-Type": "application/json" },
            body: JSON.stringify(veri)
        });
        return res.json();
    },

    async sil(endpoint) {
        const res = await fetch(`${API_BASE}${endpoint}`, { method: "DELETE" });
        return res.ok;
    }
};

// Kullanım
function GonderiListesi() {
    const [posts, setPosts] = useState([]);
    const [loading, setLoading] = useState(true);

    useEffect(() => {
        apiServisi.getir("/posts?_limit=10")
            .then(setPosts)
            .catch(console.error)
            .finally(() => setLoading(false));
    }, []);

    const yeniGonderi = async () => {
        const sonuc = await apiServisi.gonder("/posts", {
            title: "Yeni Gönderi",
            body: "İçerik"
        });
        setPosts(prev => [sonuc, ...prev]);
    };

    if (loading) return <p>Yükleniyor...</p>;

    return (
        <div>
            <button onClick={yeniGonderi}>Yeni Gönderi Ekle</button>
            {posts.map(post => (
                <article key={post.id}>
                    <h3>{post.title}</h3>
                    <p>{post.body}</p>
                </article>
            ))}
        </div>
    );
}
```

---

# 20. Hata Sınırları (Error Boundaries)

```jsx
import { Component } from 'react';

// Error Boundary SADECE class component olarak yazılabilir
class HataSiniri extends Component {
    constructor(props) {
        super(props);
        this.state = { hataVar: false, hata: null };
    }

    static getDerivedStateFromError(error) {
        return { hataVar: true, hata: error };
    }

    componentDidCatch(error, errorInfo) {
        console.error("Hata yakalandı:", error, errorInfo);
        // Hata raporlama servisine gönder (Sentry vb.)
    }

    render() {
        if (this.state.hataVar) {
            return this.props.fallback || (
                <div style={{ padding: 20, textAlign: "center" }}>
                    <h2>😞 Bir şeyler ters gitti</h2>
                    <p>{this.state.hata?.message}</p>
                    <button onClick={() => this.setState({ hataVar: false })}>
                        Tekrar Dene
                    </button>
                </div>
            );
        }
        return this.props.children;
    }
}

// Kullanım
function App() {
    return (
        <HataSiniri fallback={<p>Uygulama hatası!</p>}>
            <Header />
            <HataSiniri fallback={<p>İçerik yüklenemedi</p>}>
                <Icerik />
            </HataSiniri>
            <Footer />
        </HataSiniri>
    );
}

// ⚠️ Error Boundary YAKALAMAZ:
// - Olay yöneticilerindeki hatalar (try/catch kullanın)
// - Asenkron kodlar (setTimeout, fetch vb.)
// - Sunucu taraflı render hataları
// - Error Boundary kendisindeki hatalar
```

---

# 21. React.memo ve Performans

```jsx
import React, { useState, memo } from 'react';

// React.memo: Props değişmediği sürece bileşeni yeniden render ETMEZ
const PahaliBilesen = memo(function PahaliBilesen({ veri, onClick }) {
    console.log("PahaliBilesen render edildi");
    return (
        <div>
            {veri.map(item => <p key={item.id}>{item.ad}</p>)}
            <button onClick={onClick}>Tıkla</button>
        </div>
    );
});

// Özel karşılaştırma fonksiyonu
const KartBilesen = memo(
    function KartBilesen({ kullanici }) {
        return <div>{kullanici.ad} - {kullanici.yas}</div>;
    },
    (prevProps, nextProps) => {
        // true dönerse: render ETME (props aynı)
        // false dönerse: render ET (props farklı)
        return prevProps.kullanici.id === nextProps.kullanici.id;
    }
);

// Performans İpuçları:
// 1. State'i mümkün olduğunca ALT bileşenlere taşıyın
// 2. Gereksiz re-render'ları React DevTools Profiler ile tespit edin
// 3. Büyük listelerde react-window veya react-virtuoso kullanın
// 4. Ağır hesaplamalarda useMemo kullanın
// 5. Event handler'ları useCallback ile sarmalayın
// 6. children prop'u kullanarak render optimizasyonu yapın
```

---

# 22. Portals

```jsx
import { createPortal } from 'react-dom';

// Portal: Bileşeni DOM hiyerarşisi dışında farklı bir yere render eder
// Modal, tooltip, dropdown gibi UI elemanları için idealdir

function Modal({ acik, onKapat, children }) {
    if (!acik) return null;

    return createPortal(
        <div className="modal-overlay" onClick={onKapat}>
            <div className="modal-icerik" onClick={e => e.stopPropagation()}>
                <button className="modal-kapat" onClick={onKapat}>✕</button>
                {children}
            </div>
        </div>,
        document.getElementById("modal-root") // index.html'de <div id="modal-root"></div>
    );
}

// Kullanım
function App() {
    const [modalAcik, setModalAcik] = useState(false);

    return (
        <div>
            <button onClick={() => setModalAcik(true)}>Modal Aç</button>
            <Modal acik={modalAcik} onKapat={() => setModalAcik(false)}>
                <h2>Modal Başlığı</h2>
                <p>Modal içeriği burada.</p>
            </Modal>
        </div>
    );
}
```

---

# 23. Fragments

```jsx
import { Fragment } from 'react';

function FragmentOrnekleri() {
    const kullanicilar = [
        { id: 1, ad: "Ali", email: "ali@mail.com" },
        { id: 2, ad: "Ayşe", email: "ayse@mail.com" }
    ];

    return (
        <table>
            <tbody>
                {kullanicilar.map(k => (
                    // Fragment ile key kullanımı (kısa sözdizimi <> ile key kullanılamaz)
                    <Fragment key={k.id}>
                        <tr>
                            <td>{k.ad}</td>
                            <td>{k.email}</td>
                        </tr>
                    </Fragment>
                ))}
            </tbody>
        </table>
    );
}

// Kısa sözdizimi (key gerekmediğinde)
function Baslik() {
    return (
        <>
            <h1>Ana Başlık</h1>
            <p>Alt başlık metni</p>
        </>
    );
}
```

---

# 24. Lazy Loading ve Suspense

```jsx
import { lazy, Suspense, useState } from 'react';

// Lazy loading: Bileşeni ihtiyaç duyulduğunda yükler (code splitting)
const AgirBilesen = lazy(() => import('./AgirBilesen'));
const YonetimPaneli = lazy(() => import('./pages/YonetimPaneli'));

function App() {
    const [goster, setGoster] = useState(false);

    return (
        <div>
            <button onClick={() => setGoster(true)}>Ağır Bileşeni Yükle</button>

            {/* Suspense: Lazy bileşen yüklenirken fallback gösterir */}
            <Suspense fallback={<div>Yükleniyor...</div>}>
                {goster && <AgirBilesen />}
            </Suspense>

            {/* Route bazlı code splitting */}
            <Suspense fallback={<YukleniyorSpinner />}>
                <Routes>
                    <Route path="/" element={<AnaSayfa />} />
                    <Route path="/panel" element={<YonetimPaneli />} />
                </Routes>
            </Suspense>
        </div>
    );
}

function YukleniyorSpinner() {
    return (
        <div style={{ display: "flex", justifyContent: "center", padding: 40 }}>
            <div className="spinner"></div>
            <p>Sayfa yükleniyor...</p>
        </div>
    );
}
```

---

# 25. forwardRef ve useImperativeHandle

```jsx
import { forwardRef, useRef, useImperativeHandle } from 'react';

// forwardRef: Ref'i alt bileşene iletmek için
const OzelInput = forwardRef(function OzelInput({ label, ...props }, ref) {
    return (
        <div className="form-group">
            <label>{label}</label>
            <input ref={ref} {...props} />
        </div>
    );
});

// useImperativeHandle: Alt bileşenden üst bileşene özel API açmak için
const VideoPlayer = forwardRef(function VideoPlayer({ src }, ref) {
    const videoRef = useRef();

    useImperativeHandle(ref, () => ({
        oynat: () => videoRef.current.play(),
        durdur: () => videoRef.current.pause(),
        ses: (deger) => { videoRef.current.volume = deger; }
    }));

    return <video ref={videoRef} src={src} />;
});

// Kullanım
function App() {
    const inputRef = useRef();
    const videoRef = useRef();

    return (
        <div>
            <OzelInput ref={inputRef} label="Ad" />
            <button onClick={() => inputRef.current.focus()}>Odaklan</button>

            <VideoPlayer ref={videoRef} src="/video.mp4" />
            <button onClick={() => videoRef.current.oynat()}>▶️ Oynat</button>
            <button onClick={() => videoRef.current.durdur()}>⏸️ Durdur</button>
        </div>
    );
}
```

---

# 26. State Yönetim Kütüphaneleri

## 26.1 Zustand (Hafif ve Basit)

```bash
npm install zustand
```

```jsx
import { create } from 'zustand';

// Store oluşturma
const useStore = create((set, get) => ({
    sayac: 0,
    kullanici: null,
    todos: [],

    artir: () => set(state => ({ sayac: state.sayac + 1 })),
    azalt: () => set(state => ({ sayac: state.sayac - 1 })),
    sifirla: () => set({ sayac: 0 }),

    girisYap: (kullanici) => set({ kullanici }),
    cikisYap: () => set({ kullanici: null }),

    todoEkle: (metin) => set(state => ({
        todos: [...state.todos, { id: Date.now(), metin, bitti: false }]
    })),
    todoSil: (id) => set(state => ({
        todos: state.todos.filter(t => t.id !== id)
    }))
}));

// Bileşende kullanım
function Sayac() {
    const { sayac, artir, azalt } = useStore();
    return (
        <div>
            <p>{sayac}</p>
            <button onClick={artir}>+</button>
            <button onClick={azalt}>-</button>
        </div>
    );
}

// Seçici (selector) ile performans optimizasyonu
function SadeceSayac() {
    const sayac = useStore(state => state.sayac); // Sadece sayac değiştiğinde render
    return <p>{sayac}</p>;
}
```

## 26.2 Redux Toolkit (Büyük Uygulamalar)

```bash
npm install @reduxjs/toolkit react-redux
```

```jsx
import { configureStore, createSlice } from '@reduxjs/toolkit';
import { Provider, useSelector, useDispatch } from 'react-redux';

// Slice oluşturma
const sayacSlice = createSlice({
    name: 'sayac',
    initialState: { deger: 0 },
    reducers: {
        artir: (state) => { state.deger += 1; },
        azalt: (state) => { state.deger -= 1; },
        mikdarArtir: (state, action) => { state.deger += action.payload; }
    }
});

export const { artir, azalt, mikdarArtir } = sayacSlice.actions;

// Store oluşturma
const store = configureStore({
    reducer: {
        sayac: sayacSlice.reducer
    }
});

// Provider ile sarmalama
function App() {
    return (
        <Provider store={store}>
            <SayacBilesen />
        </Provider>
    );
}

// Bileşende kullanım
function SayacBilesen() {
    const deger = useSelector(state => state.sayac.deger);
    const dispatch = useDispatch();

    return (
        <div>
            <p>{deger}</p>
            <button onClick={() => dispatch(artir())}>+</button>
            <button onClick={() => dispatch(azalt())}>-</button>
            <button onClick={() => dispatch(mikdarArtir(5))}>+5</button>
        </div>
    );
}
```

---

# 27. React ile TypeScript

```tsx
// Temel bileşen tipleri
interface KullaniciProps {
    ad: string;
    yas: number;
    email?: string;              // Opsiyonel
    aktif: boolean;
    hobiler: string[];
    rol: "admin" | "user" | "editor"; // Union type
    onClick: () => void;         // Fonksiyon
    onChange: (deger: string) => void;
    children: React.ReactNode;    // JSX içerik
    stil?: React.CSSProperties;  // Stil objesi
}

function KullaniciKart({ ad, yas, email = "Yok", onClick, children }: KullaniciProps) {
    return (
        <div onClick={onClick}>
            <h2>{ad}</h2>
            <p>Yaş: {yas}</p>
            <p>Email: {email}</p>
            {children}
        </div>
    );
}

// useState ile tip
const [sayac, setSayac] = useState<number>(0);
const [isim, setIsim] = useState<string>("");
const [kullanici, setKullanici] = useState<Kullanici | null>(null);
const [items, setItems] = useState<Item[]>([]);

// useRef ile tip
const inputRef = useRef<HTMLInputElement>(null);
const divRef = useRef<HTMLDivElement>(null);

// Event tipleri
const handleChange = (e: React.ChangeEvent<HTMLInputElement>) => {
    setIsim(e.target.value);
};
const handleSubmit = (e: React.FormEvent<HTMLFormElement>) => {
    e.preventDefault();
};
const handleClick = (e: React.MouseEvent<HTMLButtonElement>) => {
    console.log(e.clientX);
};

// Generic bileşen
interface ListeProps<T> {
    items: T[];
    renderItem: (item: T) => React.ReactNode;
}

function Liste<T>({ items, renderItem }: ListeProps<T>) {
    return <ul>{items.map((item, i) => <li key={i}>{renderItem(item)}</li>)}</ul>;
}

// Kullanım
<Liste
    items={["Ali", "Ayşe"]}
    renderItem={(isim) => <span>{isim}</span>}
/>
```

---

# 28. Test Yazımı

```bash
# Kurulum (Vite projelerinde)
npm install -D vitest @testing-library/react @testing-library/jest-dom jsdom
```

```jsx
// Button.test.jsx
import { render, screen, fireEvent } from '@testing-library/react';
import { describe, it, expect, vi } from 'vitest';
import Button from './Button';

describe('Button Bileşeni', () => {
    it('metni doğru render eder', () => {
        render(<Button>Tıkla Beni</Button>);
        expect(screen.getByText('Tıkla Beni')).toBeInTheDocument();
    });

    it('tıklandığında onClick çağrılır', () => {
        const handleClick = vi.fn(); // Mock fonksiyon
        render(<Button onClick={handleClick}>Tıkla</Button>);
        fireEvent.click(screen.getByText('Tıkla'));
        expect(handleClick).toHaveBeenCalledTimes(1);
    });

    it('disabled olduğunda tıklanamaz', () => {
        const handleClick = vi.fn();
        render(<Button onClick={handleClick} disabled>Tıkla</Button>);
        fireEvent.click(screen.getByText('Tıkla'));
        expect(handleClick).not.toHaveBeenCalled();
    });
});

// Custom Hook testi
import { renderHook, act } from '@testing-library/react';
import useCounter from './useCounter';

describe('useCounter Hook', () => {
    it('başlangıç değeri ile başlar', () => {
        const { result } = renderHook(() => useCounter(10));
        expect(result.current.deger).toBe(10);
    });

    it('artır fonksiyonu çalışır', () => {
        const { result } = renderHook(() => useCounter(0));
        act(() => { result.current.artir(); });
        expect(result.current.deger).toBe(1);
    });
});
```

---

# 29. Deployment (Yayınlama)

```bash
# 1. Production build oluşturma
npm run build
# → dist/ klasörü oluşur

# 2. Build'i test etme
npm run preview

# 3. Vercel ile yayınlama (en kolay yöntem)
npm install -g vercel
vercel
# veya GitHub'a push edin, Vercel otomatik deploy eder

# 4. Netlify ile yayınlama
npm install -g netlify-cli
netlify deploy --prod --dir=dist

# 5. GitHub Pages
# vite.config.js'e base ekleyin:
# export default defineConfig({ base: '/repo-adi/' })
npm run build
# dist/ klasörünü gh-pages branch'ına push edin

# 6. Firebase Hosting
npm install -g firebase-tools
firebase init hosting
npm run build
firebase deploy
```

---

# 30. En İyi Uygulamalar ve Kalıplar

## 30.1 Bileşen Tasarım İlkeleri

```jsx
// 1. Tek Sorumluluk (Single Responsibility)
// ❌ Kötü: Her şeyi yapan dev bileşen
function HerSeyBilesen() {
    // Veri çekme, form yönetimi, render, stil... hepsi burada
}

// ✅ İyi: Her bileşen tek bir iş yapar
function KullaniciListesi() { /* Sadece listeyi render eder */ }
function KullaniciFormu() { /* Sadece formu yönetir */ }
function KullaniciKart({ kullanici }) { /* Sadece kartı render eder */ }

// 2. Container/Presentational Pattern
// Container: Mantık ve veri (akıllı bileşen)
function KullaniciContainer() {
    const { data, loading } = useFetch("/api/users");
    if (loading) return <Spinner />;
    return <KullaniciListesi kullanicilar={data} />;
}

// Presentational: Sadece görüntü (aptal bileşen)
function KullaniciListesi({ kullanicilar }) {
    return (
        <ul>
            {kullanicilar.map(k => <li key={k.id}>{k.ad}</li>)}
        </ul>
    );
}

// 3. Composition over Inheritance
// ❌ Kalıtım kullanmayın
// ✅ Composition (bileşen birleştirme) kullanın
function SayfaDuzeni({ baslik, sidebar, children }) {
    return (
        <div className="sayfa">
            <header>{baslik}</header>
            <div className="icerik">
                <aside>{sidebar}</aside>
                <main>{children}</main>
            </div>
        </div>
    );
}
```

## 30.2 Hook Kuralları

```jsx
// ⚠️ Hook'lar SADECE:
// 1. Fonksiyonel bileşenlerin EN ÜST SEVİYESİNDE çağrılmalı
// 2. Custom hook'ların EN ÜST SEVİYESİNDE çağrılmalı

// ❌ YANLIŞ KULLANIMLAR:
function Hatali() {
    // ❌ Koşul içinde hook
    if (kosul) {
        const [deger, setDeger] = useState(0);
    }

    // ❌ Döngü içinde hook
    for (let i = 0; i < 5; i++) {
        useEffect(() => {});
    }

    // ❌ İç içe fonksiyon içinde hook
    function icFonksiyon() {
        const ref = useRef();
    }

    // ❌ return'dan sonra hook
    if (hata) return <p>Hata</p>;
    const [veri, setVeri] = useState(null); // ❌ return'dan sonra!
}

// ✅ DOĞRU KULLANIM:
function Dogru() {
    const [deger, setDeger] = useState(0);
    const [veri, setVeri] = useState(null);
    const ref = useRef(null);

    useEffect(() => {
        // Yan etki burada
    }, []);

    if (hata) return <p>Hata</p>;

    return <div>{deger}</div>;
}
```

## 30.3 Dosya ve Klasör İsimlendirme

```
Bileşenler:     PascalCase  → Button.jsx, UserCard.jsx
Hook'lar:       camelCase   → useAuth.js, useFetch.js
Yardımcılar:    camelCase   → formatDate.js, validateEmail.js
Sabitler:       UPPER_CASE  → API_URL, MAX_ITEMS
Stiller:        kebab-case  → user-card.module.css
Test dosyaları: .test.jsx   → Button.test.jsx
```

## 30.4 Sık Kullanılan Kalıplar

```jsx
// 1. Render Props Pattern
function MouseTracker({ render }) {
    const [pozisyon, setPozisyon] = useState({ x: 0, y: 0 });

    useEffect(() => {
        const handler = (e) => setPozisyon({ x: e.clientX, y: e.clientY });
        window.addEventListener("mousemove", handler);
        return () => window.removeEventListener("mousemove", handler);
    }, []);

    return render(pozisyon);
}

// Kullanım
<MouseTracker render={({ x, y }) => (
    <p>Mouse: {x}, {y}</p>
)} />

// 2. Compound Components Pattern
function Tabs({ children, defaultIndex = 0 }) {
    const [activeIndex, setActiveIndex] = useState(defaultIndex);
    return (
        <TabsContext.Provider value={{ activeIndex, setActiveIndex }}>
            {children}
        </TabsContext.Provider>
    );
}
Tabs.List = function TabList({ children }) { /* ... */ };
Tabs.Tab = function Tab({ index, children }) { /* ... */ };
Tabs.Panels = function TabPanels({ children }) { /* ... */ };
Tabs.Panel = function TabPanel({ index, children }) { /* ... */ };

// Kullanım
<Tabs>
    <Tabs.List>
        <Tabs.Tab index={0}>Profil</Tabs.Tab>
        <Tabs.Tab index={1}>Ayarlar</Tabs.Tab>
    </Tabs.List>
    <Tabs.Panels>
        <Tabs.Panel index={0}><ProfilSayfasi /></Tabs.Panel>
        <Tabs.Panel index={1}><AyarlarSayfasi /></Tabs.Panel>
    </Tabs.Panels>
</Tabs>

// 3. HOC (Higher-Order Component) Pattern
function withAuth(WrappedComponent) {
    return function AuthenticatedComponent(props) {
        const { kullanici } = useAuth();
        if (!kullanici) return <Navigate to="/giris" />;
        return <WrappedComponent {...props} kullanici={kullanici} />;
    };
}
const KorumaliSayfa = withAuth(GizliSayfa);
```

## 30.5 Performans Kontrol Listesi

```
✅ React.memo ile gereksiz render'ları önle
✅ useCallback ile event handler referanslarını koru
✅ useMemo ile pahalı hesaplamaları önbelleğe al
✅ Büyük listelerde sanallaştırma (virtualization) kullan
✅ Lazy loading ile code splitting yap
✅ useEffect cleanup fonksiyonlarını unutma
✅ Key olarak benzersiz ID kullan (index kullanma)
✅ State'i mümkün olduğunca lokal tut
✅ Context'i küçük parçalara böl
✅ React DevTools Profiler ile performansı ölç
```

---

> 📝 **NOT:** Bu rehber React 18+ sürümünü kapsamaktadır. React ekosistemi sürekli gelişmektedir; güncel bilgi için [React resmi dokümantasyonu](https://react.dev) adresini takip edin.

> 🎯 **ÖNERİ:** React öğrenirken küçük projeler yaparak ilerleyin: Todo App → Hava Durumu App → E-ticaret → Sosyal Medya klonu

---

**© 2026 - React.js Kapsamlı Ders Notları - Tüm hakları saklıdır.**
