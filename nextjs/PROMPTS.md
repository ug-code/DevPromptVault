# Modern Web Geliştirme En İyi Uygulamaları ve Standartları
*(React, Next.js, Redux, TypeScript, JavaScript, HTML, CSS ve UI Frameworkleri)*

---

## 🧭 Geliştirme Felsefesi
- Temiz, sürdürülebilir ve ölçeklenebilir kod yaz.  
- **SOLID** prensiplerini takip et.  
- Fonksiyonel ve deklaratif programlama yöntemlerini tercih et.  
- Tip güvenliği ve statik analize önem ver.  
- Komponent odaklı geliştirme yaklaşımını uygula.

---

## 💻 Kod Uygulama Kılavuzu

### Planlama Aşaması
- Adım adım planlama ile başla.  
- Uygulamadan önce detaylı pseudocode yaz.  
- Komponent mimarisini ve veri akışını belgeleyin.  
- Edge case ve hata senaryolarını düşün.

### Kod Stili
- Girintiler için tab kullan.  
- Stringlerde tek tırnak kullan (kaçış gerektiğinde çift tırnak).  
- Noktalı virgül kullanma (gerektiğinde ifadeyi ayırmak için kullan).  
- Kullanılmayan değişkenleri kaldır.  
- Anahtar kelimelerden sonra boşluk bırak.  
- Fonksiyon parantezinden önce boşluk bırak.  
- Her zaman katı eşitlik (`===`) kullan, gevşek eşitlik (`==`) kullanma.  
- İkili operatörler arasında boşluk bırak.  
- Virgülden sonra boşluk bırak.  
- `else` ifadelerini kapanış süslü parantezle aynı satırda tut.  
- Çok satırlı `if` ifadelerinde süslü parantez kullan.  
- Callback fonksiyonlardaki hata parametrelerini her zaman işle.  
- Satır uzunluğunu 80 karakter ile sınırlandır.  
- Çok satırlı obje/dizi literal’lerinde son virgül kullan.

---

## 🏷️ İsimlendirme Kuralları

### Genel Kurallar
- **PascalCase**: Komponentler, Type tanımları, Interface’ler.  
- **kebab-case**: Klasör ve dosya adları (`components/auth-wizard`, `user-profile.tsx`).  
- **camelCase**: Değişkenler, fonksiyonlar, metodlar, hook’lar, props.  
- **UPPERCASE**: Çevresel değişkenler, sabitler, global konfigürasyonlar.

### Özel İsimlendirme
- Event handler’larda `handle` ön eki: `handleClick`, `handleSubmit`.  
- Boolean değişkenlerde fiil kullan: `isLoading`, `hasError`, `canSubmit`.  
- Custom hook’larda `use` ön eki: `useAuth`, `useForm`.  
- Kısaltmalardan kaçın; yalnızca: `err`, `req`, `res`, `props`, `ref`.

---

## ⚛️ React En İyi Uygulamaları

### Komponent Mimarisi
- TypeScript interface’leri ile fonksiyonel komponentler kullan.  
- Komponentleri `function` anahtar kelimesi ile tanımla.  
- Tekrar kullanılabilir mantığı custom hook’lara taşı.  
- Kompozisyonu doğru uygula.  
- Performans için `React.memo()` kullan.  
- `useEffect` hook’larında cleanup fonksiyonlarını uygula.

### Performans Optimizasyonu
- Callback fonksiyonları `useCallback` ile memoize et.  
- Maliyetli hesaplamaları `useMemo` ile optimize et.  
- JSX içinde inline fonksiyon tanımlarından kaçın.  
- Kod bölme için dynamic import kullan.  
- Listelerde `key` prop’ları doğru uygula; index kullanmaktan kaçın.

---

## 🚀 Next.js En İyi Uygulamaları

### Temel Kavramlar
- Routing için **App Router** kullan.  
- Metadata yönetimi doğru uygula.  
- Cache stratejilerini doğru uygula.  
- Hata sınırlarını (error boundaries) uygula.

### Komponentler ve Özellikler
- Next.js built-in komponentlerini kullan:  
  - **Image**: optimize edilmiş görseller için  
  - **Link**: client-side navigation  
  - **Script**: dış script’ler için  
  - **Head**: metadata yönetimi için  
- Yüklenme durumlarını doğru uygula.  
- Doğru veri çekme yöntemlerini kullan.

### Server Components
- Varsayılan olarak Server Components kullan.  
- Veri çekme ve server state yönetimi için URL query parametrelerini kullan.  
- `'use client'` yalnızca gerektiğinde kullan:  
  - Event listener  
  - Tarayıcı API’leri  
  - State yönetimi  
  - Sadece client-side kütüphaneler

---

## 📝 TypeScript Uygulaması
- Strict mode’u aktif et.  
- Komponent props, state ve Redux state yapısı için net interface’ler tanımla.  
- Olası `undefined` veya `null` değerler için type guard kullan.  
- Fonksiyon, action ve slice’larda generics kullan.  
- TypeScript utility tiplerini (Partial, Pick, Omit) kullan.  
- Nesne yapıları için `interface` tercih et, özellikle extend gerekiyorsa.  
- Var olan tiplerden dinamik varyasyonlar oluşturmak için mapped types kullan.

---

## 🎨 UI ve Stil

### Komponent Kütüphaneleri
- **Shadcn UI** ile tutarlı ve erişilebilir komponentler oluştur.  
- **Radix UI** primitives ile özelleştirilebilir ve erişilebilir UI uygula.  
- Modüler ve tekrar kullanılabilir komponentler için kompozisyon desenlerini uygula.

### Stil Kuralları
- **Tailwind CSS** kullan.  
- Utility-first ve sürdürülebilir stil için Tailwind uygula.  
- Mobil-first responsive tasarım uygula.  
- Koyu mod desteği için CSS değişkenleri veya Tailwind dark mode kullan.  
- Renk kontrast oranları erişilebilirlik standartlarına uygun olmalı.  
- Tutarlı spacing değerleri kullan.  
- Tema renkleri ve spacing için CSS değişkenleri tanımla.

---

## 🔄 Durum Yönetimi (State Management)

### Local State
- Component-level state için `useState`.  
- Karmaşık state için `useReducer`.  
- Paylaşılan state için `useContext`.  
- State’in doğru initialize edildiğinden emin ol.

### Global State
- **Redux Toolkit** kullan.  
- `createSlice` ile state, reducer ve action’ları birlikte tanımla.  
- `createReducer` ve `createAction` yalnızca gerekirse kullan.  
- Nested veri yapılarından kaçın; state’i normalize et.  
- State erişimi için selector kullan.  
- Büyük slice’lar yerine feature bazlı ayır.

---

## ⚠️ Hata Yönetimi ve Validasyon

### Form Validasyonu
- **Zod** ile schema validation yap.  
- Hatalı girişlerde doğru mesajları göster.  
- Formlar için React Hook Form gibi kütüphaneler kullan.

### Error Boundaries
- React component tree’sinde hataları yakalamak için error boundaries kullan.  
- Hataları Sentry gibi servislerde logla.  
- Kullanıcı dostu fallback UI göster.

---

## 🧪 Test

### Unit Test
- Fonksiyon ve komponentleri doğrulamak için kapsamlı test yaz.  
- Jest ve React Testing Library kullan.  
- Arrange-Act-Assert pattern’ini uygula.  
- Dış bağımlılıkları mock’la.

### Integration Test
- Kullanıcı akışlarına odaklan.  
- Test ortamını setup/teardown ile izole et.  
- Snapshot testlerini ölçülü kullan.  
- RTL araçları ile okunabilir test yaz.

---

## ♿ Erişilebilirlik (a11y)
- Semantic HTML kullan.  
- Doğru ARIA attributelarını uygula.  
- Klavye navigasyonunu destekle.  
- Focus sırasını ve görünürlüğü yönet.  
- Erişilebilir renk kontrastları sağla.  
- Mantıklı heading hiyerarşisi kullan.  
- Tüm interaktif elementler erişilebilir olmalı.  
- Hatalarda açık ve erişilebilir geri bildirim ver.

---

## 🔒 Güvenlik
- Kullanıcı girdilerini sanitize et, XSS önle.  
- HTML içeriğini sanitize etmek için **DOMPurify** kullan.  
- Doğru authentication yöntemlerini uygula.

---

## 🌐 Uluslararasılaştırma (i18n)
- **next-i18next** ile çeviri yönet.  
- Doğru locale detection uygula.  
- Sayı ve tarih formatlarını doğru kullan.  
- RTL desteğini uygula.  
- Para birimi formatlamalarını doğru uygula.

---

## 📚 Dokümantasyon
- JSDoc kullan.  
- Tüm public fonksiyon, sınıf, metod ve interface’leri dokümante et.  
- Örnekler ekle.  
- Tam cümle, doğru noktalama kullan.  
- Açık ve öz açıklamalar yaz.  
- Markdown, code block, link, heading ve listeleri doğru kullan.
