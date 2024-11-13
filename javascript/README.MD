1. What are the different data types present in javascript?

JavaScript'da quyidagi ma'lumot turlari mavjud:

1. **Number** – Raqamlar (butun sonlar va o'nli sonlar).
   - Misol: `let age = 25;`

2. **String** – Matnli qiymatlar (qavslar ichida yozilgan harf va raqamlar).
   - Misol: `let name = "Ali";`

3. **Boolean** – Ikki qiymatli mantiqiy qiymatlar (`true` yoki `false`).
   - Misol: `let isActive = true;`

4. **Object** – Ob'ektlar, bu bir yoki bir nechta qiymatlarni saqlash uchun ishlatiladi (kalit-qiymat juftliklari).
   - Misol: `let person = { name: "Ali", age: 25 };`

5. **Array** – Ro'yxatlar yoki massivlar, bir nechta qiymatlarni saqlash uchun ishlatiladi.
   - Misol: `let numbers = [1, 2, 3, 4];`

6. **Null** – Bo'sh yoki aniqlanmagan qiymat.
   - Misol: `let data = null;`

7. **Undefined** – O'zgaruvchiga qiymat berilmagan holda qoldirilgan qiymat.
   - Misol: `let city;`

8. **Symbol** – Unikal va o'zgarmas qiymatlarni yaratish uchun ishlatiladi.
   - Misol: `let sym = Symbol("id");`

9. **BigInt** – Katta sonlarni ifodalash uchun ishlatiladi (JavaScriptning raqamlar diapazoni cheklangan, BigInt esa bundan kattaroq sonlarni ishlatish imkonini beradi).
   - Misol: `let bigNumber = 1234567890123456789012345678901234567890n;`

Bu JavaScript'dagi asosiy ma'lumot turlari.

2. Explain Hoisting in javascript.

**Hoisting** — bu JavaScript'da kodni ishlatishdan oldin o'zgaruvchilar va funksiyalarni avtomatik ravishda yuqoriga ko'tarish (yoki "ko'chirish") hodisasidir. Boshqacha aytganda, JavaScript kodni bajarishda o'zgaruvchilar va funksiyalarni deklaratsiya qilishni (ya'ni, e'lon qilishni) dastur ishlashidan oldin bajaradi.

### Hoisting qanday ishlaydi?

1. **O'zgaruvchilar (var, let, const):**
   - **`var`** o'zgaruvchilari uchun hoisting ishlaydi, ya'ni ular e'lon qilinishidan oldin ishlatilsa ham, `undefined` bo'lib qoladi.
   - **`let`** va **`const`** o'zgaruvchilari hoisting qilinsa ham, ular o'zgaruvchi e'lon qilinmagan "temir zonada" (temporal dead zone, TDZ) qoladi, va ular bilan ishlashda xato beradi.

   Misollar:
   ```javascript
   console.log(a); // undefined (hoisting)
   var a = 5;

   console.log(b); // ReferenceError: Cannot access 'b' before initialization
   let b = 10;

   console.log(c); // ReferenceError: Cannot access 'c' before initialization
   const c = 15;
   ```

2. **Funksiyalar:**
   - **Funksiyalarni deklaratsiya qilish** hoisting qilinganida butun funksiya tanasi yuqoriga ko'tariladi, shuning uchun ularni e'lon qilishdan oldin chaqirish mumkin.
   
   Misol:
   ```javascript
   sayHello(); // "Hello!"
   
   function sayHello() {
       console.log("Hello!");
   }
   ```

3. **Funksiyalarni ifodalash (Function Expressions):**
   - Agar funktsiya ifodalangan bo'lsa (ya'ni, funksiya o'zgaruvchiga berilgan bo'lsa), u holda hoisting ishlamaydi. Bu holatda, o'zgaruvchi deklaratsiyasi va funksiya tayinlash bir vaqtning o'zida amalga oshiriladi, shuning uchun funksiyani e'lon qilishdan oldin chaqirish xato beradi.

   Misol:
   ```javascript
   greet(); // TypeError: greet is not a function

   var greet = function() {
       console.log("Hello!");
   };
   ```

### Xulosa:
- **Hoisting** — bu JavaScript'dagi o'zgaruvchilar va funksiyalarni e'lon qilishni avtomatik ravishda yuqoriga ko'tarish hodisasidir.
- `var` o'zgaruvchilari hoisting qilinadi va `undefined` bo'lib qoladi.
- `let` va `const` o'zgaruvchilari hoisting qilinadi, lekin ular "temporal dead zone"da qoladi va ularni e'lon qilmasdan ishlatish xatoga olib keladi.
- Funksiya deklaratsiyalari hoisting qilinadi va kodni yuqoridan pastga qarab bajarish imkonini beradi, ammo funksiyalarning ifodasi hoisting qilinmaydi.

Hoisting'ni tushunish JavaScript'dagi kodingizni qanday ishlashini aniqroq tushunishga yordam beradi.

3. Why do we use the word “debugger” in javascript?

JavaScript'da **`debugger`** kalit so'zi dasturchilarga kodni xatolarni aniqlash (ya'ni, *debugging*) va tuzatish uchun yordam beradi. Bu xususiyat, kodni bajarish jarayonini to'xtatib, brauzerning *developer tools* (dasturchi asboblari) yoki konsolida xatolarni aniqlash va kodni qadam-baqadam tekshirish imkonini beradi.

### **`debugger`** ni qanday ishlatish mumkin?
- **`debugger`** kalit so'zi kodda ma'lum bir nuqtada bajarilishini to'xtatadi. Dastur to'xtab, brauzerning Developer Tools (F12 yoki Ctrl+Shift+I) oynasida **Console** yoki **Sources** panelida xatolarni tekshirish va kodni tahlil qilish imkonini beradi.

### Misol:
```javascript
function add(a, b) {
    debugger; // Bu yerda bajarish to'xtaydi
    return a + b;
}

let result = add(5, 7); // Bu yerda "debugger" chaqiriladi
console.log(result);
```

Yuqoridagi kodda, **`debugger`** ishlatilgan joyda dastur to'xtaydi va siz developer tools orqali kodni qadam-baqadam bajarishingiz mumkin.

### **`debugger`** ning foydalari:
1. **Koddagi xatolarni aniqlash:**
   - Kod to'xtatilgan joyda dasturchi o'zgaruvchilarning qiymatini tekshirishi, funksiyalarni chaqirish jarayonini ko'rishi mumkin.
   
2. **Kodni qadam-baqadam bajarish:**
   - Kodni to'liq bajarilishini kutmasdan, har bir qadamni ko'rib chiqish va xatolikni aniqlash osonlashadi.
   
3. **Brauzer asboblari bilan integratsiya:** 
   - Brauzerning developer tools'lari orqali, masalan, Google Chrome, Firefox yoki Safari kabi brauzerlarda **Sources** panelida kodni turli nuqtalarda tekshirishingiz mumkin.

### **`debugger`** ning ishlash tartibi:
1. Kod bajarilganda, **`debugger`** joylashgan nuqtada to'xtaydi.
2. Dasturchi Developer Tools orqali o'zgaruvchilarni va kodning holatini tekshirishi mumkin.
3. Kodni davom ettirish yoki bir qadam oldinga borish imkoniyatlari mavjud.

### **Eslatma:**
- **`debugger`** faqat *developer* yoki dasturchilar uchun mo'ljallangan vositadir. Kodni yakuniy foydalanuvchiga yuborishdan oldin, odatda, **`debugger`** koddan olib tashlanadi, chunki bu foydalanuvchi tajribasini to'xtatishi yoki noto'g'ri ishlashiga olib kelishi mumkin.

### Xulosa:
**`debugger`** — bu JavaScript'dagi xatolarni aniqlash va tuzatishda yordam beradigan vosita bo'lib, kodni to'xtatib, o'zgaruvchilarni tekshirish va qadam-baqadam bajarishni osonlashtiradi. Bu, ayniqsa, murakkab dasturlarni ishlab chiqishda juda foydalidir.

4. Difference between “ == “ and “ === “ operators.

JavaScript'da **`==`** va **`===`** operatorlari o'xshash bo'lsa ham, ular orasida muhim farqlar mavjud. Quyida bu operatorlar o'rtasidagi farqlarni tushuntirib o'taman:

### 1. **`==` (Loose Equality) Operator:**
**`==`** operatori *bo'sh qiymatlarni* yoki *turlarni* solishtirishda avtomatik ravishda turni **avtomatik tarzda o'zgartiradi**. Bu shuni anglatadiki, **`==`** operatori solishtirilayotgan qiymatlar turini (data type) hisobga olmaydi va agar kerak bo'lsa, ular turini bir xil qilish uchun konversiya qiladi.

#### Misol:
```javascript
console.log(5 == '5');   // true
console.log(true == 1);   // true
console.log(null == undefined);  // true
```

- **`5 == '5'`**: Bu yerda **`5`** raqami va **`'5'`** matni turli xil turlarga ega, lekin **`==`** operatori ularni teng deb hisoblaydi, chunki u turni avtomatik ravishda tenglashtiradi (string `'5'` ni number `5` ga o'zgartiradi).
- **`true == 1`**: **`true`** boolean qiymati va **`1`** raqami teng deb hisoblanadi, chunki boolean qiymatlarni raqamga o'zgartirganimizda **`true`** ning qiymati `1` ga teng bo'ladi.
- **`null == undefined`**: Bu ikki qiymat ham bir xil deb hisoblanadi, chunki ular `null` va `undefined` sifatida javob beradi.

### 2. **`===` (Strict Equality) Operator:**
**`===`** operatori *kattaroq* va *qattiq* solishtirishni amalga oshiradi. U solishtirilayotgan qiymatlarning nafaqat qiymatini, balki turini ham taqqoslaydi. Ya'ni, **`===`** operatori qiymat va tur o'rtasidagi tenglikni aniq tekshiradi.

#### Misol:
```javascript
console.log(5 === '5');   // false
console.log(true === 1);   // false
console.log(null === undefined);  // false
```

- **`5 === '5'`**: Bu yerda **`5`** (raqam) va **`'5'`** (string) turlari turlicha, shuning uchun **`===`** operatori ular teng emas deb hisoblaydi.
- **`true === 1`**: **`true`** boolean qiymati va **`1`** raqami turli turlarga ega bo'lgani uchun ular teng emas.
- **`null === undefined`**: **`null`** va **`undefined`** ham turli qiymatlar, shuning uchun ular teng emas.

### Asosiy Farqlar:
| **Xususiyat**            | **`==` (Loose Equality)** | **`===` (Strict Equality)** |
|--------------------------|----------------------------|-----------------------------|
| **Turlarni solishtirish** | Turlarni avtomatik ravishda moslashtiradi (type coercion) | Turlarni ham, qiymatlarni ham qat'iyan solishtiradi |
| **Tenglikni tekshirish**  | Taqsimlangan qiymatlarni tenglashtiradi | Qattiq tenglikni tekshiradi (qiymat va tur) |
| **Natija**               | Avtomatik tur konversiyasi bilan tenglikni tekshiradi | Faqat qiymatlar va turlar teng bo'lsa, `true` qaytaradi |

### Xulosa:
- Agar siz qiymatlar va turlarni qat'iy ravishda solishtirmoqchi bo'lsangiz, **`===`** operatoridan foydalaning.
- Agar siz qiymatlar tengligini turlarni o'zgartirishga ruxsat berib solishtirishni istasangiz, **`==`** operatorini ishlating. Biroq, bu ko'pincha kutilmagan natijalarga olib kelishi mumkin, shuning uchun **`===`** ni afzal ko'rish tavsiya etiladi, chunki u yanada aniq va xavfsiz hisoblanadi.

5. Difference between var and let keyword in javascript.

JavaScript'da **`var`** va **`let`** kalit so'zlari o'zgaruvchilarni e'lon qilishda ishlatiladi, lekin ular o'rtasida muhim farqlar mavjud. Quyida **`var`** va **`let`** o'rtasidagi farqlarni tushuntirib beraman.

### 1. **`var` (ES5 va undan avvalgi versiyalari):**
**`var`** o'zgaruvchisini e'lon qilishda foydalanilgan. Bu eski JavaScript versiyalarida ishlatilgan va ba'zi muammolarga olib kelishi mumkin.

#### Asosiy xususiyatlar:
- **Blok darajasidagi ko'lam** (block scope): **`var`** o'zgaruvchisi **funktsiya darajasida** (function scope) ishlaydi, ya'ni faqat o'zini e'lon qilgan funksiya ichida mavjud bo'ladi. Agar **`var`** blok (masalan, `if` yoki `for` tsikli) ichida e'lon qilingan bo'lsa, u blokdan tashqarida ham mavjud bo'ladi.
- **Hoisting**: **`var`** o'zgaruvchilari **hoisting** (ko'tarish) jarayonida e'lon qilishdan oldin ham ishlatilishi mumkin, lekin qiymatlari `undefined` bo'ladi.

#### Misol:
```javascript
if (true) {
    var x = 10;
}
console.log(x); // 10 (blokdan tashqarida ham mavjud)
```

- Yuqoridagi misolda, **`x`** o'zgaruvchisi **`if`** blokidan tashqarida ham mavjud, chunki **`var`** o'zgaruvchisi **funktsiya darajasida** ko'lamga ega bo'ladi, blok darajasida emas.

### 2. **`let` (ES6 va undan keyingi versiyalari):**
**`let`** o'zgaruvchisini **ES6** (ECMAScript 2015) bilan tanishtirildi va **`var`** o'rnini bosishga mo'ljallangan. **`let`** o'zgaruvchilarini deklaratsiya qilishda yanada aniqroq va xavfsizroq usul hisoblanadi.

#### Asosiy xususiyatlar:
- **Blok darajasidagi ko'lam** (block scope): **`let`** o'zgaruvchisi **blok darajasida** ishlaydi. Ya'ni, agar o'zgaruvchi **`let`** bilan blok ichida e'lon qilinsa, u faqat shu blok ichida mavjud bo'ladi va blokdan tashqarida ko'rinmaydi.
- **Hoisting**: **`let`** o'zgaruvchilari ham hoisting qilinadi, lekin ular **temporal dead zone (TDZ)** ga kiradi, ya'ni o'zgaruvchi e'lon qilinmaguncha uni ishlatish xatoga olib keladi.

#### Misol:
```javascript
if (true) {
    let y = 20;
    console.log(y); // 20
}
console.log(y); // ReferenceError: y is not defined
```

- Yuqoridagi misolda, **`y`** o'zgaruvchisi **`if`** blokidan tashqarida mavjud emas, chunki **`let`** o'zgaruvchisi faqat blok ichida mavjud bo'ladi.

### 3. **Hoisting (ko'tarish) farqi:**
- **`var`** o'zgaruvchisi hoisting qilinadi, lekin uning qiymati **`undefined`** bo'ladi. Kodni yuqoriga ko'tarishda **`var`** o'zgaruvchisi e'lon qilinadi, lekin qiymati tayinlanmaguncha u `undefined` bo'ladi.
  
  Misol:
  ```javascript
  console.log(a); // undefined
  var a = 5;
  console.log(a); // 5
  ```

- **`let`** o'zgaruvchisi ham hoisting qilinadi, lekin **`let`** o'zgaruvchilari **temporal dead zone** ga tushadi, shuning uchun e'lon qilinishidan oldin ishlatilsa, **ReferenceError** xatosi yuzaga keladi.
  
  Misol:
  ```javascript
  console.log(b); // ReferenceError: Cannot access 'b' before initialization
  let b = 10;
  ```

### 4. **Takroran e'lon qilish:**
- **`var`** bilan e'lon qilingan o'zgaruvchi takroran e'lon qilinishi mumkin va yangi qiymat beriladi. Bu kutilmagan natijalarga olib kelishi mumkin.
  
  Misol:
  ```javascript
  var c = 30;
  var c = 40;
  console.log(c); // 40
  ```

- **`let`** bilan e'lon qilingan o'zgaruvchi takroran e'lon qilinsa, **SyntaxError** xatosi yuzaga keladi.
  
  Misol:
  ```javascript
  let d = 50;
  let d = 60; // SyntaxError: Identifier 'd' has already been declared
  ```

### 5. **`var` va `let` ko'lami (Scope):**
- **`var`** o'zgaruvchilari **funktsiya darajasida** ko'lamga ega, bu esa o'zgaruvchini butun funktsiyada ishlatish imkonini beradi, hatto uning blok ichida e'lon qilinmagan bo'lsa ham.
- **`let`** o'zgaruvchilari **blok darajasida** ko'lamga ega, ya'ni ular faqat e'lon qilingan blok ichida mavjud bo'ladi.

### Xulosa:
| Xususiyat                     | **`var`**                               | **`let`**                             |
|-------------------------------|-----------------------------------------|--------------------------------------|
| **Ko'lam (Scope)**             | Funktsiya darajasi (function scope)     | Blok darajasi (block scope)         |
| **Hoisting**                   | Ha, lekin qiymati `undefined` bo'ladi  | Ha, lekin Temporal Dead Zone (TDZ)   |
| **Takroran e'lon qilish**      | Mavjud, yangi qiymat tayinlanadi       | Takroran e'lon qilishga ruxsat berilmaydi |
| **Xatoliklar**                 | Kutilmagan natijalar (masalan, blokdan tashqarida mavjud bo'lish) | Kutilmagan natijalar yo'q, aniqroq |

**`let`** yangi JavaScript versiyalarida **`var`** o'rnini bosgan va kodni aniqroq, xavfsizroq va tushunarliroq qilishga yordam beradi. Shuning uchun, ko'pincha **`let`** o'zgaruvchilari afzal ko'riladi.

6. Explain Implicit Type Coercion in javascript.

**Implicit Type Coercion** (yoki *avtomatik tur konversiyasi*) — bu JavaScript'da bir qiymatni boshqa turga o'zgartirish jarayonidir, va bu o'zgarish avtomatik ravishda sodir bo'ladi. Ya'ni, JavaScript turli turlarni bir-biriga solishtirayotganda yoki ularga amallar bajarayotganda, kerak bo'lsa, bir turdagi qiymatni avtomatik ravishda boshqa turga o'zgartiradi.

### Implicit Type Coercion qanday ishlaydi?
JavaScript ba'zi operatsiyalarni bajarishda turlarni moslashtirish uchun **implicit type coercion** (avtomatik tur konversiyasi)dan foydalanadi. Bu jarayon JavaScript tomonidan avtomatik ravishda amalga oshiriladi va dasturchi tomonidan hech qanday alohida kod yozishni talab qilmaydi.

### Misollar orqali tushuntirish:

1. **Raqam va string o'rtasidagi qo'shish:**
   Agar bir tomonda string va boshqa tomonda raqam bo'lsa, JavaScript raqamni stringga o'zgartirib, ularni qo'shadi.

   Misol:
   ```javascript
   let result = 5 + '10';
   console.log(result); // "510" (raqam 5 va string '10' birlashib, stringga aylanadi)
   ```

   Bu yerda, raqam **`5`** avtomatik ravishda **`'5'`** stringga aylantirildi, so'ngra ikkita string birlashdi va **`"510"`** natija chiqdi.

2. **String va boolean o'rtasida qo'shish:**
   Agar string va boolean qiymatlari qo'shilsa, boolean qiymati stringga aylantiriladi va qo'shish amalga oshiriladi.

   Misol:
   ```javascript
   let result = 'Hello' + true;
   console.log(result); // "Hellotrue" (boolean true stringga aylantirilib qo'shildi)
   ```

   Bu holatda, **`true`** boolean qiymati **`'true'`** stringga aylantirilib, `Hello` bilan birlashtirildi.

3. **Raqam va boolean o'rtasida qo'shish:**
   Agar raqam va boolean qiymatlari qo'shilsa, boolean qiymati raqamga aylantiriladi: **`true`** -> **1** va **`false`** -> **0**.

   Misol:
   ```javascript
   let result = 5 + true;
   console.log(result); // 6 (true 1 ga o'zgartirildi, so'ng 5 + 1 = 6)
   ```

   Bu yerda **`true`** boolean qiymati **1** ga aylantirildi, shuning uchun natija **`5 + 1 = 6`** bo'ldi.

4. **Agar `undefined` va boshqa turdagi qiymatlar qo'shilsa:**
   **`undefined`** qiymati qo'shish amali bilan ishlatilganda, u **`NaN`** (Not a Number) qiymatini qaytaradi.

   Misol:
   ```javascript
   let result = undefined + 5;
   console.log(result); // NaN (undefined raqamga o'zgartirilganda NaN hosil bo'ladi)
   ```

   Bu holatda, **`undefined`** qiymati raqamga aylantirilganda **`NaN`** hosil bo'ladi, chunki **`undefined`** raqamga o'zgartirilganda hech qanday mantiqiy qiymatga ega emas.

5. **String va null o'rtasidagi qo'shish:**
   **`null`** qiymati qo'shilsa, u **`0`** raqamiga o'zgartiriladi va keyin qo'shish amalga oshiriladi.

   Misol:
   ```javascript
   let result = null + 5;
   console.log(result); // 5 (null 0 ga aylantiriladi, so'ng 0 + 5 = 5)
   ```

   Bu holatda, **`null`** qiymati **`0`** ga aylantirildi, va natija **`5`** bo'ldi.

### **Implicit Type Coercion holatlari:**

1. **Arifmetik amallar:**
   Agar arifmetik amallar, masalan, qo'shish yoki ko'paytirish amalga oshirilsa, JavaScript avtomatik ravishda tur konversiyasini bajaradi.
   - Qo'shish amali (`+`) **string bilan raqamni** birlashtiradi (stringga aylantiradi).
   - Boshqa arifmetik amallar (masalan, ayirish, ko'paytirish) **string, boolean yoki null** qiymatlarini raqamga aylantiradi.

   Misol:
   ```javascript
   let a = '10';
   let b = 5;
   console.log(a - b);  // 5 (string '10' raqamga aylantirilib, 10 - 5 = 5)
   ```

2. **Qo'shish amali (`+`) bilan string birlashtirish:**
   Agar biri string bo'lsa va boshqa biri raqam, boolean, null yoki undefined bo'lsa, ular stringga aylantiriladi va birlashtiriladi.

   Misol:
   ```javascript
   let result = 'Value is ' + 10;
   console.log(result); // "Value is 10"
   ```

### Xulosa:
**Implicit Type Coercion** — bu JavaScript'dagi avtomatik tur konversiyasi jarayonidir, ya'ni turli turlarni bir-biriga solishtirayotganda yoki amallarni bajarishda JavaScript o'zini avtomatik ravishda moslashtiradi. Bu xususiyat ba'zan kutmagan natijalarga olib kelishi mumkin, shuning uchun dasturchilar kodni yozishda turlarni aniq tushunib, ehtiyotkorlik bilan ishlashlari kerak.

7. Is javascript a statically typed or a dynamically typed language?

JavaScript **dinamik tarzda tiplangan** (dynamically typed) dasturlash tilidir. Bu shuni anglatadiki, JavaScript'da o'zgaruvchining turi dastur bajarilayotganda aniqlanadi va o'zgaruvchilarga turli xil turlardagi qiymatlar berilishi mumkin. O'zgaruvchilarni e'lon qilishda ularning turini aniq belgilash talab qilinmaydi, va ular bajarilish vaqtida o'zgarishi mumkin.

### Dinamik tipli tilning xususiyatlari:
1. **O'zgaruvchi turini aniqlash talab qilinmaydi:**
   JavaScript'da o'zgaruvchining turini deklaratsiya qilishda ko'rsatish shart emas. O'zgaruvchi turini JavaScript avtomatik ravishda aniqlaydi.
   
   Misol:
   ```javascript
   let x = 5;        // x - number
   x = "Hello";      // x - string
   x = true;         // x - boolean
   ```

   Bu yerda, **`x`** o'zgaruvchisi dastlab **raqam** sifatida e'lon qilinadi, keyin esa **matn (string)** va **boolean** turiga o'zgaradi. JavaScript avtomatik ravishda turni moslashtiradi.

2. **Tur konversiyasi (type coercion):**
   JavaScript turli turlardagi qiymatlar bilan ishlaganda ularni avtomatik ravishda o'zgartiradi (bu **implicit type coercion** deb ataladi), va bu holatni dasturchi nazorat qilmaydi.

   Misol:
   ```javascript
   let a = 10;       // number
   let b = "5";      // string
   let result = a + b; // "105" (number 10 va string "5" birlashtirildi)
   ```

   Bu yerda **`a`** raqam, **`b`** esa string turida, ammo ularning qo'shilishi natijasida **`"105"`** string hosil bo'ladi. JavaScript avtomatik ravishda **`a`** raqamini stringga aylantirib, ularni birlashtiradi.

3. **Tur aniqlanishi bajarilish vaqtida:**
   JavaScriptda o'zgaruvchilarni e'lon qilganingizda ular uchun aniq tur ko'rsatilmaydi va tur dastur bajarilishi vaqtida aniqlanadi. Bu **dinamik** tiplash degan ma'noni anglatadi.

   Misol:
   ```javascript
   let z = "Hello";
   z = 100;  // z endi number turida
   ```

   **`z`** o'zgaruvchisi dastlab string bo'lib boshlanadi, keyin esa raqamga o'zgartiriladi. JavaScript uning turini dinamik ravishda o'zgartiradi.

### Statik va Dinamik tiplarni taqqoslash:
| **Xususiyat**               | **Statik Tiplangan Tillar**      | **Dinamik Tiplangan Tillar**  |
|-----------------------------|----------------------------------|-------------------------------|
| **Tipni aniqlash**          | Kompilyatsiya vaqtida (oldindan) | Dastur bajarilish vaqtida     |
| **Tiplarni o'zgartirish**   | Emas, faqat aniq tipdagi qiymatlar ishlatiladi | Ha, o'zgaruvchilar turini bajarilish vaqtida o'zgartirish mumkin |
| **Kompilyatsiya xatoliklari**| Tezda aniqlanadi (kompilyatsiya vaqtida) | Ba'zan bajarilish vaqtida yuzaga kelishi mumkin |
| **Misollar**                | Java, C, C++                    | JavaScript, Python, Ruby      |

### Xulosa:
JavaScript **dinamik tarzda tiplangan** dasturlash tilidir. Bu shuni anglatadiki, o'zgaruvchilar dastur bajarilayotganda turini o'zgartirishi mumkin, va ularning turini deklaratsiya qilish talab qilinmaydi. Bu esa dasturchiga kodni yozishda ko'proq erkinlik beradi, ammo ba'zan kutilmagan xatolarga olib kelishi mumkin, chunki tur aniqlanishi bajarilish vaqtida amalga oshiriladi.

8. What is NaN property in JavaScript?

**NaN** (Not a Number) — bu JavaScript'da **raqam bo'lmagan qiymat**ni ifodalovchi maxsus qiymatdir. **NaN** qiymati, odatda, raqamli amallar bajarilganda, ammo natija aniqlanmagan yoki mantiqan noto'g'ri bo'lgan hollarda qaytariladi.

### **NaN ning Xususiyatlari:**

1. **NaN — bu maxsus qiymatdir:**
   **NaN** qiymati odatiy raqam sifatida ishlamaydi. U **raqam turlaridan** biri bo'lib, lekin uning o'zi **raqam emas**. Bu qiymatni hisoblash yoki taqqoslash amallari yordamida aniqlash mumkin.

2. **NaN bilan solishtirish:**
   JavaScript'da **NaN** qiymati bilan **`NaN`** ning o'zi teng emas deb hisoblanadi. Bu juda muhim xususiyatdir, chunki **NaN** o'zi bilan solishtirilganda ham **false** qaytaradi.

   Misol:
   ```javascript
   let a = NaN;
   console.log(a === NaN);  // false
   console.log(isNaN(a));   // true
   ```

   Bu yerda **`a === NaN`** false bo'ladi, chunki **NaN** o'zi bilan teng emas, lekin **`isNaN(a)`** true qaytaradi, chunki **`a`** NaN ekanligini tekshiradi.

3. **NaN ni yaratish:**
   **NaN** qiymati odatda **raqamli amallar** yoki **mantiqan noto'g'ri hisoblashlar** natijasida hosil bo'ladi. Masalan, nolga bo'lish, nomutanosib raqamli qiymatlar yoki noto'g'ri arifmetik amallar.

   Misol:
   ```javascript
   let x = 0 / 0;      // NaN (nolga bo'lish)
   let y = Math.sqrt(-1);  // NaN (manfiy sonning kvadrat ildizi)
   let z = "hello" * 2;  // NaN ("hello" ni raqamga ko'paytirish)
   console.log(x);  // NaN
   console.log(y);  // NaN
   console.log(z);  // NaN
   ```

   - **`0 / 0`**: Nolga bo'lish har doim **NaN** ga olib keladi.
   - **`Math.sqrt(-1)`**: Manfiy sonning kvadrat ildizi **NaN** hosil qiladi.
   - **`"hello" * 2`**: Stringni raqamga ko'paytirish mumkin emas, shuning uchun **NaN** qaytadi.

4. **NaN ni tekshirish:**
   JavaScript'da **NaN** ni tekshirish uchun **`isNaN()`** funksiyasi ishlatiladi. Bu funksiya, agar qiymat **NaN** bo'lsa, **true** qaytaradi.

   Misol:
   ```javascript
   let value = NaN;
   if (isNaN(value)) {
       console.log("Bu NaN!");
   }
   ```

   Agar **`value`** **NaN** bo'lsa, **`isNaN()`** funksiyasi **true** qaytaradi va ekranga **"Bu NaN!"** chiqariladi.

5. **NaN va arifmetik amallar:**
   **NaN** qiymati boshqa raqamli qiymatlar bilan arifmetik amallar bajarilganda ham natija sifatida chiqishi mumkin.

   Misol:
   ```javascript
   let a = 5 + NaN;   // NaN
   let b = NaN * 10;  // NaN
   console.log(a);    // NaN
   console.log(b);    // NaN
   ```

   Agar **NaN** bilan boshqa raqamlar qo'shilsa yoki ko'paytirilsa, natija har doim **NaN** bo'ladi.

### **NaN ning Xulosa:**
- **NaN** — bu JavaScript'da "raqam bo'lmagan" yoki **not a number** degan ma'noni bildiradi. Bu qiymat arifmetik yoki mantiqan xato bo'lgan holatlarda hosil bo'ladi.
- **NaN** bilan solishtirishda ehtiyot bo'lish kerak, chunki **NaN** o'zi bilan teng emas (`NaN === NaN` false bo'ladi).
- **`isNaN()`** funksiyasi yordamida **NaN** qiymatini aniqlash mumkin.

### **Xulosa:**
**NaN** qiymati JavaScript'da noto'g'ri yoki mantiqan aniqlanmagan raqamli qiymatlarni ifodalaydi. U bilan ishlashda ehtiyotkorlik kerak, chunki u boshqa turdagi qiymatlar bilan solishtirilganda kutishdan tashqari natijalar beradi.

9. Explain passed by value and passed by reference.

JavaScript’da **"passed by value"** va **"passed by reference"** kontseptsiyalari, o'zgaruvchilarni funksiyalarga qanday uzatish usulini tushunishga yordam beradi. Bu ikkita tamoyil o'rtasidagi farqlarni tushunish juda muhim, chunki ular o'zgaruvchilarni o'zgartirishda qanday natijalar kutishimizni belgilaydi.

### 1. **Passed by Value (Qiymat bilan uzatish):**
**Passed by value** (qiymat bilan uzatish) — bu o'zgaruvchining **qiymatini** funksiyaga uzatish jarayonidir. Bu usulda, o'zgaruvchining asl qiymati funksiyaga uzatiladi, ammo funksiyada uning o'zgarishi asl o'zgaruvchiga ta'sir qilmaydi.

JavaScript'da **primitiv turlar** (string, number, boolean, null, undefined, symbol va bigint) **passed by value** usulida uzatiladi. Bu shuni anglatadiki, o'zgaruvchi funksiyaga uzatilganida uning **nusxasi** uzatiladi.

#### Misol:
```javascript
function changeValue(a) {
    a = 10;  // a qiymatini 10 ga o'zgartiramiz
}

let x = 5;
changeValue(x);
console.log(x);  // 5
```

Bu yerda:
- **`x`** o'zgaruvchisi **5** qiymatiga ega va **`changeValue(x)`** funksiyasiga uzatiladi.
- Funksiya ichida **`a`** o'zgaruvchisi **10** ga o'zgartiriladi, lekin bu **`x`** ning asl qiymatiga ta'sir qilmaydi.
- **`x`** ning qiymati **5** bo'lib qoladi, chunki **passed by value** usulida o'zgaruvchining faqat **nusxasi** uzatiladi, asli emas.

### 2. **Passed by Reference (Manba bilan uzatish):**
**Passed by reference** (manba bilan uzatish) — bu o'zgaruvchining **manbasini** (yoki **xotirada joylashgan joyini**) funksiyaga uzatish jarayonidir. Bu usulda, o'zgaruvchining asl manbasi uzatiladi, shuning uchun funksiyada o'zgaruvchiga qo'shilgan o'zgartirishlar asl o'zgaruvchiga ta'sir qiladi.

JavaScript'da **obyektlar** (masalan, arrays, functions, objects va boshqalar) **passed by reference** usulida uzatiladi. Bu shuni anglatadiki, agar siz obyektni funksiyaga uzatsangiz, asl obyektni emas, balki uning manbasini uzatasiz.

#### Misol:
```javascript
function changeObject(obj) {
    obj.name = "Alice";  // Obyektning ichidagi qiymatni o'zgartiramiz
}

let person = { name: "John", age: 25 };
changeObject(person);
console.log(person.name);  // "Alice"
```

Bu yerda:
- **`person`** obyektining manbasi **`changeObject(person)`** funksiyasiga uzatiladi.
- Funksiya ichida **`obj.name = "Alice"`** bilan obyektning **name** xususiyati **"Alice"** ga o'zgartiriladi.
- **`person.name`** qiymati funksiyadan keyin **"Alice"** bo'ladi, chunki biz obyektning manbasini uzatganmiz va funksiyada o'zgarish asl obyektga ta'sir qilgan.

### Passed by Value va Passed by Reference o'rtasidagi farqlar:

| **Xususiyat**                   | **Passed by Value**                    | **Passed by Reference**              |
|----------------------------------|----------------------------------------|--------------------------------------|
| **Turlar**                       | Primitiv turlar (number, string, boolean, null, undefined, symbol, bigint) | Ob'ektlar (arrays, functions, objects) |
| **Uzatilgan qiymat**             | O'zgaruvchining **nusxasi** uzatiladi  | O'zgaruvchining **manbasi** uzatiladi |
| **O'zgarishlar ta'siri**         | Funksiyada o'zgartirishlar asl o'zgaruvchiga ta'sir qilmaydi | Funksiyada o'zgartirishlar asl o'zgaruvchiga ta'sir qiladi |
| **Misol**                        | `let a = 5; changeValue(a);` → `a` o'zgarmaydi | `let obj = {}; changeValue(obj);` → `obj` o'zgaradi |

### Xulosa:
- **Passed by value** (qiymat bilan uzatish) — bu o'zgaruvchining **nusxasi** funksiyaga uzatiladi. Primitiv turlar (masalan, raqamlar yoki matn) bu usulda uzatiladi, va funksiyada amalga oshirilgan o'zgarishlar asl o'zgaruvchiga ta'sir qilmaydi.
- **Passed by reference** (manba bilan uzatish) — bu o'zgaruvchining **manbasi** funksiyaga uzatiladi. Obyektlar (masalan, massivlar yoki obyektlar) bu usulda uzatiladi, va funksiyada amalga oshirilgan o'zgarishlar asl o'zgaruvchiga ta'sir qiladi.

JavaScriptda, **primitiv turlar** uchun qiymat uzatiladi (passed by value), **obyektlar** uchun esa manba uzatiladi (passed by reference).

10. What is an Immediately Invoked Function in JavaScript?

**Immediately Invoked Function Expression (IIFE)** (darhol chaqiriladigan funksiya ifodasi) — bu JavaScript'da o'zini o'zi darhol chaqiradigan funksiya bo'lib, u **funktsiya ifodasi** sifatida yaratiladi va darhol bajariladi. IIFE, odatda, funksiyani tezda ishga tushirish va ko'pincha global o'zgaruvchilardan yoki ob'ektlardan izolyatsiya qilish uchun ishlatiladi.

### IIFE qanday ishlaydi?
IIFE asosan ikkita asosiy qismdan iborat:
1. **Funksiya ifodasi**: Bu yerda funksiyaning o'zi biror o'zgaruvchiga tayinlanmagan va **funksiya ifodasi** sifatida yaratiladi.
2. **Darhol chaqirish**: Funksiya o'zi yaratilgan zahoti darhol chaqiriladi. Buning uchun funksiyaning oxirida `()` operatori ishlatiladi.

### IIFE ning sintaksisi:
```javascript
(function() {
    // Funksiya tanasi
})();
```

Yuqoridagi kodda:
- **`(function() {...})`** — bu funksiya ifodasi.
- **`()`** — bu funksiya ifodasini darhol chaqirish uchun ishlatiladi.

### Misol:
```javascript
(function() {
    console.log("Bu IIFE funksiyasi!");
})();
```

Bu kodni ishlatganda:
- Funksiya o'zini o'zi chaqiradi va konsolga **"Bu IIFE funksiyasi!"** xabarini chiqaradi.
- Funksiya darhol bajariladi va uning o'zgaruvchilari va funksiyasi global doirada mavjud bo'lmaydi.

### IIFE ning ishlatilish sabablari:

1. **Global o'zgaruvchilardan himoya qilish**:
   JavaScriptda global o'zgaruvchilarning o'zgarishi va nom to'qnashuvi masalalari mavjud. IIFE yordamida lokal o'zgaruvchilar yaratish orqali bu muammolardan qochish mumkin.

   Misol:
   ```javascript
   (function() {
       let x = 10;
       console.log(x);  // 10
   })();

   // x globalda mavjud emas
   console.log(x);  // x not defined (x topilmadi)
   ```

   Bu misolda, **`x`** faqat IIFE ichida mavjud va uning qiymati funksiyadan tashqarida mavjud emas.

2. **Kodni modullar sifatida tashkil qilish**:
   IIFE, modulli dasturlashda ham foydalidir. IIFE yordamida funktsiyalar va o'zgaruvchilarni lokal qilib, ularni global doiradan ajratib qo'yish mumkin. Bu boshqa kod bilan to'qnashmaslikka yordam beradi.

   Misol:
   ```javascript
   let counter = (function() {
       let count = 0;
       return {
           increment: function() {
               count++;
               return count;
           },
           decrement: function() {
               count--;
               return count;
           }
       };
   })();

   console.log(counter.increment());  // 1
   console.log(counter.increment());  // 2
   console.log(counter.decrement());  // 1
   ```

   Bu misolda:
   - **`counter`** IIFE yordamida yaratilgan va bu ob'ekt orqali lokal **`count`** o'zgaruvchisi boshqarilmoqda.
   - **`increment`** va **`decrement`** metodlari **`count`** o'zgaruvchisini yangilaydi va uni globalda ko'rsatmaysiz.

3. **Kodning izolyatsiyasi**:
   IIFE yordamida kodni bir vaqtning o'zida izolyatsiya qilish va uning o'zgaruvchilarini boshqa koddan ajratib olish mumkin. Bu, ayniqsa, katta dasturlarda juda foydalidir.

4. **JavaScript Closure** bilan ishlash:
   IIFE ko'pincha **closure** (yopiq funksiyalar) bilan birgalikda ishlatiladi, bu esa funksiyalarning yopilish (lexical) muhiti orqali qiymatlarni uzatishga imkon beradi.

### IIFE o'zgaruvchilari va funksiya:
IIFE ichida e'lon qilingan o'zgaruvchilar faqatgina o'sha funksiya ichida mavjud bo'ladi va ular global doiraga ta'sir qilmaydi. Bu JavaScript dasturlarida yaxshi tartibni saqlashga yordam beradi.

Misol:
```javascript
(function() {
    var localVar = "Men faqat bu funksiya ichidaman!";
    console.log(localVar);  // "Men faqat bu funksiya ichidaman!"
})();

console.log(localVar);  // ReferenceError: localVar is not defined
```

Yuqoridagi misolda:
- **`localVar`** faqatgina IIFE ichida mavjud va tashqarida uning mavjud emasligi uchun xatolik (ReferenceError) yuzaga keladi.

### Xulosa:
**Immediately Invoked Function Expression (IIFE)** JavaScript'da funksiyani darhol chaqirish uchun ishlatiladigan sintaksisdir. IIFE yordamida:
- O'zgaruvchilar va funksiyalarni lokal qilib, global doirada ifodalangan nomlar bilan to'qnashuvni oldini olish mumkin.
- Kodingizni izolyatsiya qilib, modulli ishlashni ta'minlash mumkin.
- IIFE, ayniqsa, **closure** va lokal o'zgaruvchilar bilan ishlashda foydalidir.

IIFE dasturlashda ko'pincha zamonaviy JavaScript kodlarida ishlatiladi, chunki u kodning izolyatsiyasi va tartibini ta'minlaydi.

11. What do you mean by strict mode in javascript and characteristics of javascript strict-mode?

**Strict mode** (qat'iy rejim) — bu JavaScript'da kodni bajarishning qat'iyroq va xavfsizroq usulidir. **Strict mode**ni faollashtirish orqali ba'zi noxush xatoliklar va kamchiliklarni oldini olish mumkin. **Strict mode** kodni yanada aniq va ishonchli qilishga yordam beradi, chunki u ba'zi potentsial xatoliklarni va noto'g'ri kod yozishni oldini oladi.

### **Strict Mode nima?**
**Strict mode** JavaScript tilining yangi qoidalarini qo'llaydi, ya'ni bu rejimda ba'zi sintaksis va semantik xatoliklar ko'rsatiladi. Bu rejimda ba'zi eski va noxush xususiyatlar ishlatilmaydi yoki ular xatoliklarni keltirib chiqaradi. **Strict mode** yordamida kodni yanada to'g'ri va xavfsizroq yozish mumkin.

### **Strict Mode ni qanday faollashtirish mumkin?**
**Strict mode**ni faollashtirish uchun, funksiyaning boshida yoki global doirada `use strict;` deb yozish kerak.

#### 1. **Funksiya darajasida**:
```javascript
function myFunction() {
    "use strict";
    // strict mode'da kod
}
```

#### 2. **Global darajada**:
```javascript
"use strict";
// Global scope'da strict mode
```

Agar global doirada **`"use strict";`** ni yozsangiz, butun fayl strict mode’da ishlaydi.

### **Strict Mode xususiyatlari va xatti-harakatlari:**

1. **Ixtiyoriy yoki rezervlangan so'zlarni ishlatishga yo'l qo'ymaydi**:
   JavaScript'da ba'zi so'zlar kelajakdagi versiyalar uchun ajratilgan (masalan, **`let`, `class`, `yield`**). Strict mode bu so'zlarni o'zgaruvchi nomi sifatida ishlatishga ruxsat bermaydi.

   Misol:
   ```javascript
   "use strict";
   let let = 5;  // SyntaxError: Unexpected strict mode reserved word
   ```

2. **`this` ning qiymati o'zgaradi**:
   Oddiy rejimda funksiyalarga chaqirishda **`this`** global ob'ektga (brauzerda **`window`** ga) kiradi. Ammo strict mode'da **`this`** `undefined` bo'ladi, agar u funksiya sifatida chaqirilsa.

   Misol:
   ```javascript
   "use strict";
   function showThis() {
       console.log(this);  // undefined
   }
   showThis();
   ```

3. **Global o'zgaruvchilarning avtomatik e'lon qilinishini oldini olish**:
   Oddiy rejimda, agar o'zgaruvchi e'lon qilinmasa, JavaScript avtomatik ravishda uni global o'zgaruvchi sifatida qabul qiladi. Strict mode’da esa bunday o'zgaruvchilarni e'lon qilmasdan ishlatish xatolikni keltirib chiqaradi.

   Misol:
   ```javascript
   "use strict";
   x = 10;  // ReferenceError: x is not defined
   ```

4. **O'zgaruvchilarni ikki marta e'lon qilishni oldini olish**:
   Strict mode'da bir xil o'zgaruvchini ikki marta e'lon qilish (masalan, `let` yoki `const` bilan) xatolikni keltirib chiqaradi.

   Misol:
   ```javascript
   "use strict";
   let a = 5;
   let a = 10;  // SyntaxError: Identifier 'a' has already been declared
   ```

5. **O'zgaruvchilarni yozishda `with` so'zidan foydalanish taqiqlanadi**:
   `with` operatori strict mode’da ishlatilmaydi. Bu operator kodni noaniq qilib, ishlashni qiyinlashtiradi, shuning uchun strict mode’da bu taqiqlanadi.

   Misol:
   ```javascript
   "use strict";
   with (Math) {  // SyntaxError: Strict mode code may not include a with statement
       let x = cos(2);
   }
   ```

6. **Delete operatorining cheklanishi**:
   Strict mode’da siz o'zgaruvchilar, funksiyalar, yoki ob'ekt xususiyatlarini `delete` operatori bilan o'chira olmaysiz.

   Misol:
   ```javascript
   "use strict";
   let obj = { prop: 42 };
   delete obj.prop;  // This is allowed

   delete obj;  // SyntaxError: Delete of an unqualified identifier in strict mode
   ```

7. **Eval va arguments nomlari**:
   Strict mode’da **`eval`** va **`arguments`** maxsus so'zlari aniq ishlatiladi va ular o'zgaruvchi yoki parametr nomi sifatida ishlatilishi mumkin emas. Bu, kodning yaxlitligini saqlashga yordam beradi.

   Misol:
   ```javascript
   "use strict";
   let eval = 5;  // SyntaxError: Unexpected eval or arguments in strict mode
   ```

### **Strict Mode foydalari:**

1. **Xatoliklarni erta aniqlash**: Strict mode’da ko'plab sintaktik va semantik xatoliklar tezda aniqlanadi. Bu dasturlashda xatoliklarni tezroq topishga yordam beradi.

2. **Yaxshi xavfsizlik**: Strict mode'da ba'zi noxush xatti-harakatlar (masalan, `with` operatori, global o'zgaruvchilarni avtomatik e'lon qilish va boshqalar) taqiqlanadi, bu dastur xavfsizligini oshiradi.

3. **Kodni izolyatsiya qilish**: Strict mode yordamida funksiyalar va kod bloklarining xatti-harakatlarini qat'iyroq qilish mumkin, bu esa kodni boshqarishni va optimallashtirishni osonlashtiradi.

4. **Kodni optimallashtirish**: JavaScript dvigatellari, **strict mode**ni faollashtirganda, kodni yanada samarali bajarishi mumkin, chunki ko'plab noxush va ishlatilmaydigan sintaksislar va xatti-harakatlarni hisobga olishning hojati yo'q.

### **Xulosa:**
**Strict mode** JavaScript'ni xavfsizroq va aniqroq qilish uchun ishlatiladigan rejimdir. U sintaktik va semantik xatoliklarni erta aniqlashga yordam beradi, global o'zgaruvchilarni noto'g'ri ishlatishdan himoya qiladi va ba'zi xavfli amallarni (masalan, `with` yoki `eval` ishlatish) taqiqlaydi. Strict mode, ayniqsa, katta va murakkab dasturlarda kodning yaxlitligi va to'g'riligini ta'minlashda foydalidir.

12. Explain Higher Order Functions in javascript.

**Higher-order function** (yuqori tartibli funksiya) — bu JavaScript'da **funksiya** bo'lib, u **boshqa bir funksiyani argument sifatida qabul qilishi** yoki **funksiya sifatida natija qaytarishi** mumkin. Higher-order functions (HOF) funksiyalarni boshqa funksiyalar bilan ishlatishning qulay va kuchli usulini taqdim etadi.

### Higher-order function nima?

Agar biror funksiya quyidagi ikki xususiyatdan birini bajaradigan bo'lsa, u **higher-order function** hisoblanadi:
1. **Boshqa funksiyani argument sifatida qabul qilishi**.
2. **Funksiya sifatida natija qaytarishi**.

JavaScript’dagi ko'plab o'rnatilgan metodlar, masalan, **`map()`, `filter()`, `reduce()`** kabi metodlar, yuqori tartibli funksiyalar hisoblanadi.

### Higher-order functions ishlashining oddiy misoli:

```javascript
function greet(name) {
    return "Salom, " + name;
}

function processUserInput(callback) {
    var userName = "Ali";
    console.log(callback(userName));  // Callback funksiyasini chaqirish
}

processUserInput(greet);  // Higher-order function'ga 'greet' funksiyasini uzatish
```

Bu yerda:
- **`processUserInput`** — bu **higher-order function**, chunki u **`greet`** funksiyasini argument sifatida qabul qilmoqda.
- **`greet`** esa oddiy funksiya bo'lib, uni **`processUserInput`** ga uzatib, chaqirganimizda foydalanuvchi nomini ko'rsatadi.

### Higher-order function'lar qanday ishlaydi?
1. **Funksiyalarni argument sifatida qabul qilish**:
   Funksiya boshqa funksiya sifatida boshqa funksiya chaqirishni talab qiladi. Bu ko'pincha **callback functions** deb ataladi, ya'ni chaqirilishi kerak bo'lgan funktsiyalar.

   Misol:
   ```javascript
   function add(a, b) {
       return a + b;
   }

   function operation(x, y, callback) {
       return callback(x, y);  // Callback funksiyasini chaqirish
   }

   console.log(operation(5, 3, add));  // 8
   ```

   Bu yerda **`add`** funksiyasi **`operation`** funksiyasiga uzatilgan. **`operation`** esa bu funksiyani chaqiradi va natijani qaytaradi.

2. **Funksiya sifatida natija qaytarish**:
   Higher-order function boshqa funksiya qaytarishi mumkin. Buning uchun birinchi funksiya ichida ikkinchi funksiya yaratiladi va qaytariladi.

   Misol:
   ```javascript
   function multiply(x) {
       return function(y) {
           return x * y;
       };
   }

   const multiplyBy2 = multiply(2);  // `multiply` funksiyasi natija sifatida funksiya qaytaradi
   console.log(multiplyBy2(5));  // 10
   ```

   Bu yerda:
   - **`multiply`** — bu higher-order function, chunki u boshqa funksiyani qaytaradi.
   - **`multiplyBy2`** esa qaytarilgan funksiya bo'lib, 2 ga ko'paytirish amali bajaradi.

### Higher-order functions misollarini ko'rib chiqaylik:

1. **`map()` funksiyasi**:
   **`map()`** funksiyasi massivdagi har bir elementga funksiya qo'llaydi va yangi massiv qaytaradi. Bu yuqori tartibli funksiya bo'lib, unda callback funksiyasi argument sifatida uzatiladi.

   Misol:
   ```javascript
   let numbers = [1, 2, 3, 4];
   let squaredNumbers = numbers.map(function(num) {
       return num * num;
   });
   console.log(squaredNumbers);  // [1, 4, 9, 16]
   ```

   Bu yerda **`map()`** funksiyasi **callback funksiyasini** (ya'ni **`function(num) { return num * num; }`**) argument sifatida qabul qiladi.

2. **`filter()` funksiyasi**:
   **`filter()`** funksiyasi massivdagi shartga javob beradigan elementlarni ajratib oladi va yangi massiv qaytaradi.

   Misol:
   ```javascript
   let numbers = [1, 2, 3, 4, 5, 6];
   let evenNumbers = numbers.filter(function(num) {
       return num % 2 === 0;
   });
   console.log(evenNumbers);  // [2, 4, 6]
   ```

   Bu yerda **`filter()`** funksiyasi **callback funksiyasini** (ya'ni **`function(num) { return num % 2 === 0; }`**) argument sifatida qabul qiladi.

3. **`reduce()` funksiyasi**:
   **`reduce()`** funksiyasi massivni yakuniy bitta qiymatga qisqartiradi (masalan, yig'indi yoki mahsulot).

   Misol:
   ```javascript
   let numbers = [1, 2, 3, 4];
   let sum = numbers.reduce(function(acc, num) {
       return acc + num;
   }, 0);
   console.log(sum);  // 10
   ```

   Bu yerda **`reduce()`** funksiyasi **callback funksiyasini** (ya'ni **`function(acc, num) { return acc + num; }`**) argument sifatida qabul qiladi. Bu funksiya massivning har bir elementini yig'indiga qo'shadi.

### Higher-order function'larning afzalliklari:
1. **Yaxshi modullik**:
   Higher-order function'lar yordamida funksiyalarni modulli tarzda yozish mumkin, bu esa kodni yanada toza va qayta ishlatishga qulay qiladi.

2. **Callback funktsiyalar**:
   Bu usul ko'pincha asinxron operatsiyalar bilan ishlashda, masalan, **callback** funksiyalarni ishlatishda foydalidir. Bu funksiyalar kodni asinxron tarzda bajarishga yordam beradi (masalan, **`setTimeout()`, `setInterval()`, `fetch()`**).

3. **Yaxshi o'qilishi va tushunilishi**:
   Higher-order function'lar yordamida kodni qisqaroq va o'qilishi osonroq qilish mumkin. Bu, ayniqsa, katta va murakkab dasturlarni yaratishda juda foydalidir.

### Xulosa:
**Higher-order functions** — bu JavaScript'da funksiyalarni boshqa funksiyalar bilan ishlatishga imkon beruvchi kuchli konseptdir. Bu funksiyalarni **argument sifatida qabul qilish** yoki **funksiya sifatida natija qaytarish** orqali dastur kodini modular va qayta ishlatishga imkon beradi. Higher-order function'lar ko'plab foydali metodlar, masalan, **`map()`**, **`filter()`**, va **`reduce()`** kabi funksiyalarni o'z ichiga oladi va ular JavaScript'da kodni aniq, qisqa va samarali yozishga yordam beradi.

13. Explain “this” keyword.

**`this`** kalit so'zi JavaScriptda **hozirgi kontekstdagi ob'ektni** ifodalaydi. Ya'ni, **`this`** o'ziga xos tarzda funksiyalarga va kodning bajarilish joyiga qarab turlicha qiymatga ega bo'lishi mumkin. Bu JavaScript'da muhim tushuncha, chunki **`this`** orqali biz obyektning xususiyatlariga yoki metodlariga murojaat qilishimiz mumkin.

### **`this` ni tushunish:**

**`this`** kalit so'zi **dinamik** tarzda o'zgaradi va funksiyaning qanday chaqirilishiga bog'liq. **`this`** ning qiymati **funksiya chaqirilgan joyga** yoki **kontekstga** qarab o'zgaradi.

### **`this` ning qiymati qanday aniqlanadi?**
`this` ning qiymati quyidagi omillarga qarab belgilanadi:
1. **Global kontekstda (yoki oddiy kodda)**: 
   - Agar **`this`** globalda ishlatilsa (ya'ni, funksiya ichida emas, balki tashqi kodda), unda **`this`** **global ob'ektga** (brauzerda **`window`** ob'ektiga) teng bo'ladi.

   ```javascript
   console.log(this);  // Brauzerda: window (global ob'ekt)
   ```

2. **Funksiya ichida**:
   - Agar **`this`** funktsiya ichida ishlatilsa, u **funksiya qanday chaqirilishiga** qarab turlicha qiymat oladi.

   a) **Oddiy funksiya chaqirig'ida**:
      - Globalda chaqirilgan funksiya ichida **`this`** global ob'ektga (`window`) ishora qiladi (brauzerda).
      - Agar **strict mode** (`"use strict"`) ishlatilsa, **`this`** **`undefined`** bo'ladi.

      Misol:
      ```javascript
      function showThis() {
          console.log(this);  // Brauzerda: window
      }
      showThis();
      ```

   b) **Metod ichida** (obyektga tegishli metod):
      - Agar **`this`** obyekt metodida ishlatilsa, unda **`this`** shu obyektga ishora qiladi.

      Misol:
      ```javascript
      const person = {
          name: "Ali",
          greet: function() {
              console.log(this.name);  // "Ali"
          }
      };
      person.greet();  // this person obyektiga ishora qiladi
      ```

3. **Arrow function (yoki стрелка funksiyalari) bilan ishlash**:
   - **Arrow function**larda **`this`** o'zgaradi. **Arrow function** o'zining **`this`** qiymatini funksiya chaqirilgan kontekstdan oladi, ya'ni ular **lexical scoping** (leksik muhit) qoidasiga amal qiladi. **Arrow function** ichida **`this`** hech qachon o'zgarmaydi, u faqat funksiyaning atrofidagi muhitdan olingan **`this`** qiymatini oladi.

   Misol:
   ```javascript
   const person = {
       name: "Ali",
       greet: () => {
           console.log(this.name);  // undefined (this arrow function ichida ishlatilsa global ob'ektga ishora qiladi)
       }
   };
   person.greet();
   ```

   Bu yerda **`this`** **arrow function** ichida ishlatilganligi sababli, u global ob'ektni bildiradi va **`this.name`** undefined bo'ladi, chunki globalda **`name`** o'zgaruvchisi mavjud emas.

4. **`this` ni `call()`, `apply()`, va `bind()` metodlari orqali o'zgartirish**:
   - JavaScript’da **`this`** qiymatini chaqirishda **`call()`**, **`apply()`**, va **`bind()`** metodlari yordamida aniq bir qiymatga belgilash mumkin. Bu metodlar funksiyaning **`this`** qiymatini explicit (aniq) belgilash imkonini beradi.

   a) **`call()` va `apply()`** metodlari:
   - Bu metodlar yordamida funksiya chaqirilganda **`this`** ob'ektini aniq belgilash mumkin. **`call()`** va **`apply()`** metodlari farqi shundaki, **`call()`** metodida argumentlar virgulli tarzda beriladi, **`apply()`** metodida esa argumentlar massiv sifatida beriladi.

   Misol:
   ```javascript
   function greet() {
       console.log("Salom, " + this.name);
   }

   const person = { name: "Ali" };
   greet.call(person);  // "Salom, Ali"
   greet.apply(person);  // "Salom, Ali"
   ```

   b) **`bind()`** metodi:
   - **`bind()`** metodi funksiya yaratadi va unga yangi **`this`** qiymatini bog'laydi, lekin uni darhol chaqirmaydi. Funksiya keyincha chaqirilganda, u belgilangan **`this`** qiymatini ishlatadi.

   Misol:
   ```javascript
   function greet() {
       console.log("Salom, " + this.name);
   }

   const person = { name: "Ali" };
   const greetPerson = greet.bind(person);
   greetPerson();  // "Salom, Ali"
   ```

### **`this` ning xususiyatlari va ishlash usullari:**
1. **Globalda yoki funksiya ichida (`this` global ob'ektni bildiradi)**:
   - Global doirada yoki oddiy funksiyalar ichida **`this`** global ob'ektga (`window` yoki `global`) ishora qiladi.
   - **Strict mode** da **`this`** **`undefined`** bo'ladi.

2. **Metodlar ichida (`this` obyektni bildiradi)**:
   - Agar **`this`** obyekt metodida ishlatilsa, u metodni chaqirgan obyektni bildiradi.

3. **Arrow functions**:
   - **Arrow functions** leksik tarzda **`this`** ni o'z atrofidagi kontekstdan oladi va uni hech qachon o'zgartirmaydi. Arrow functions **`this`** ni funksiyani chaqirish vaqtida emas, balki uning e'lon qilinishi vaqtida oladi.

4. **`call()`, `apply()`, va `bind()` metodlari**:
   - Bu metodlar yordamida funksiya chaqirilganda **`this`** qiymatini aniq belgilash mumkin.

### Xulosa:
**`this`** JavaScript'da dinamik tarzda o'zgaradigan kalit so'zdur, u funksiya chaqirilganda o'zining qiymatini belgilaydi. **`this`** ning qiymati **global kontekst**, **obyekt metodlari**, **arrow function** yoki **`call()`, `apply()`, `bind()`** metodlari orqali o'zgarishi mumkin. JavaScriptda **`this`** ni to'g'ri tushunish va ishlatish, kodning ishlashini va muammolarni hal qilishni osonlashtiradi.

14. What do you mean by Self Invoking Functions?

**Self-Invoking Functions** (o'z-o'zini chaqiruvchi funksiyalar) — bu JavaScript'da **funksiya** bo'lib, uni e'lon qilgan zahoti darhol chaqiriladi. Boshqacha qilib aytganda, bu funksiya **bajarilishini o'z-o'zidan boshlaydi** va uni chaqirish uchun qo'shimcha `()` belgilari kerak bo'lmaydi.

Self-invoking funksiyalar **IIFE** (Immediately Invoked Function Expression) deb ataladi, ya'ni **darhol chaqiriladigan funksiya ifodasi**. Bu turdagi funksiyalarni ishlatishning asosiy maqsadi, **global doiraga aralashmasdan** lokal muhitda kodni bajarishdir. IIFE yordamida, masalan, **o'zgaruvchilarni** faqat funksiya ichida ishlatish va global doiraga chiqarmaslik mumkin.

### **Self-Invoking Function qanday ishlaydi?**

Self-invoking function, funktsiya ifodasini e'lon qilish bilan birga darhol chaqiriladigan funksiyadir. Bu, asosan, **funksiya ifodasi** (function expression) bo'lishi kerak, ya'ni funksiyaning **e'lon qilinishi** va **chaqirilishi** bir joyda bo'ladi.

IIFE quyidagi sintaksisda yoziladi:
```javascript
(function() {
    // Kodlar bu yerda bajariladi
})();
```

Bu yerda:
- **`()`** — funktsiyani chaqirish uchun ishlatilgan qavslar.
- **`function()`** — funktsiyaning e'lon qilinishi.
- Funktsiya o'z-o'zini chaqiradi, chunki u darhol **`()`** orqali chaqiriladi.

### **Self-Invoking Functionning misoli:**

```javascript
(function() {
    console.log("Bu funksiyaning o'z-o'zini chaqirishi");
})();
```

Bu kodda:
- **`function() {...}`** — bu funksiyaning o'zi.
- **`()`** — funktsiyaning darhol chaqirilishini bildiradi.
- Natijada, funksiyaning ichidagi kod darhol ishlaydi va **"Bu funksiyaning o'z-o'zini chaqirishi"** deb konsolga chiqariladi.

### **Self-Invoking Functionning asosiy xususiyatlari:**

1. **Global doiraga ta'sir qilmaydi**:
   - IIFE yordamida funksiya ichidagi o'zgaruvchilar faqat lokal doirada qoladi va global doiraga kirib ketmaydi. Bu, xususan, o'zgaruvchilar nomlarining **kollisionini** (ya'ni, bir xil nomdagi o'zgaruvchilarning bir-biriga to'g'ri kelishini) oldini oladi.

   Misol:
   ```javascript
   (function() {
       var a = 5;
       console.log(a);  // 5
   })();

   console.log(a);  // ReferenceError: a is not defined
   ```

   Bu yerda:
   - **`a`** o'zgaruvchisi faqat funksiya ichida mavjud va global doirada mavjud emas.

2. **Modullar yaratish**:
   - Self-invoking funksiyalarni modullarni yaratishda ishlatish mumkin, chunki ular kodni **izolyatsiya** qilishga yordam beradi. Modullarni yaratishda o'zgaruvchilarni global doiradan ajratib olish juda foydalidir.

   Misol:
   ```javascript
   var counter = (function() {
       var count = 0;  // Lokal o'zgaruvchi
       return {
           increment: function() {
               count++;
               console.log(count);
           },
           decrement: function() {
               count--;
               console.log(count);
           }
       };
   })();

   counter.increment();  // 1
   counter.increment();  // 2
   counter.decrement();  // 1
   ```

   Bu yerda:
   - **`count`** o'zgaruvchisi faqat IIFE ichida mavjud bo'lib, **`counter.increment()`** va **`counter.decrement()`** metodlari yordamida unga murojaat qilinadi. Bu modullarning global doiraga ta'siri yo'q.

3. **Kapsulyatsiya (Encapsulation)**:
   - Self-invoking funksiyalar yordamida kodni kapsulyatsiya qilish mumkin. Bu, o'zgaruvchilarning va funksiyalarning faqat kerakli qismda ishlatilishini ta'minlaydi.

4. **Asinxron ishlash**:
   - IIFE yordamida asinxron kodlarni ham yaratish mumkin, masalan, ma'lumotlarni serverdan olish yoki vaqtinchalik hisoblashlarni bajarish.

### **Self-Invoking Function uchun sintaksis:**

Self-invoking funksiyalarni yozishning eng keng tarqalgan sintaksisi quyidagicha:

1. **Oddiy funksiya ifodasi:**
   ```javascript
   (function() {
       // Kod
   })();
   ```

2. **Arrow function (стрелка funktsiya) bilan:**
   ```javascript
   (() => {
       // Kod
   })();
   ```

### **Self-Invoking Functionning afzalliklari:**

1. **Global doirada tozalash**:
   - O'zgaruvchilarni va funksiyalarni faqat lokal doirada ishlatish orqali global doirani tozalash va boshqarishni osonlashtiradi.

2. **Kodning izolyatsiyasi**:
   - Self-invoking funksiyalar kodni izolyatsiya qilishga yordam beradi, shuningdek, **modul** va **kapsulyatsiya** kabi dasturlash amallarini osonlashtiradi.

3. **Lokal xotira**:
   - Self-invoking funksiyalar yordamida yaratgan o'zgaruvchilar va funksiyalar faqat o'zlarining muhitida mavjud bo'ladi, bu esa ular o'rtasida to'g'ridan-to'g'ri bog'lanishning oldini oladi.

### **Xulosa:**

**Self-Invoking Functions** yoki **IIFE** (Immediately Invoked Function Expression) — bu darhol o'z-o'zini chaqiruvchi funksiyalar bo'lib, ular JavaScript'da kodni modular va xavfsiz yozishga yordam beradi. IIFE yordamida global doiraga ta'sir qilmasdan lokal xotira yaratish mumkin. Bu, ayniqsa, katta loyihalarda o'zgaruvchilar nomlari va funktsiyalarni boshqarishda foydalidir.

15. Explain call(), apply() and, bind() methods.

**`call()`**, **`apply()`**, va **`bind()`** metodlari JavaScript'da **`this`** qiymatini aniq belgilash va funksiya chaqirishda ishlatiladigan metodlardir. Bu metodlar bir xil maqsadda ishlaydi — funksiyaning **`this`** qiymatini o'zgartirish va uni aniqlash. Ammo, ular ishlash jihatdan bir-biridan farq qiladi.

### **1. `call()` metodi:**

**`call()`** metodi yordamida funksiyani chaqirganingizda, unga **`this`** qiymatini va parametrlarni uzatishingiz mumkin. **`call()`** metodi parametrlarini **virgullab** uzatadi.

Sintaksis:
```javascript
functionName.call(thisValue, arg1, arg2, ...);
```

- **`thisValue`** — bu **`this`** ning qiymati bo'lib, funksiyaning ichida ishlatiladi.
- **`arg1, arg2, ...`** — bu funksiya uchun uzatilgan argumentlar.

#### **Misol:**

```javascript
function greet() {
    console.log("Salom, " + this.name);
}

const person = { name: "Ali" };

greet.call(person);  // Salom, Ali
```

Bu yerda **`call()`** yordamida **`greet`** funksiyasini **`person`** obyektiga bog'lab chaqirdik. Demak, **`this`** endi **`person`** obyektiga ishora qiladi.

### **2. `apply()` metodi:**

**`apply()`** metodi **`call()`** metodiga juda o'xshash bo'lib, faqatgina parametrlarni uzatish usuli bilan farqlanadi. **`apply()`** metodi barcha argumentlarni **massiv** sifatida uzatadi.

Sintaksis:
```javascript
functionName.apply(thisValue, [arg1, arg2, ...]);
```

- **`thisValue`** — bu **`this`** ning qiymati bo'lib, funksiyaning ichida ishlatiladi.
- **`[arg1, arg2, ...]`** — bu funksiya uchun uzatilgan argumentlar massiv sifatida beriladi.

#### **Misol:**

```javascript
function greet(greeting) {
    console.log(greeting + ", " + this.name);
}

const person = { name: "Ali" };

greet.apply(person, ["Assalom"]);  // Assalom, Ali
```

Bu yerda **`apply()`** metodi yordamida **`greet`** funksiyasini **`person`** obyektiga bog'lab chaqirdik va **greeting** argumentini massiv sifatida uzatdik.

### **3. `bind()` metodi:**

**`bind()`** metodi, **`call()`** va **`apply()`** metodlaridan farqli o'laroq, funksiyani darhol chaqirmaydi. **`bind()`** metodi **yangi funksiyani** yaratadi va unga yangi **`this`** qiymatini bog'laydi. Bu metod faqat yangi funksiya qaytaradi va funksiyani keyin chaqirish kerak bo'ladi.

Sintaksis:
```javascript
let newFunction = functionName.bind(thisValue, arg1, arg2, ...);
```

- **`thisValue`** — bu **`this`** ning qiymati bo'lib, yangi yaratilgan funksiyaning ichida ishlatiladi.
- **`arg1, arg2, ...`** — bu yangi funksiyaga uzatilgan argumentlar.

#### **Misol:**

```javascript
function greet(greeting) {
    console.log(greeting + ", " + this.name);
}

const person = { name: "Ali" };

let greetPerson = greet.bind(person, "Salom");
greetPerson();  // Salom, Ali
```

Bu yerda **`bind()`** metodi orqali **`greet`** funksiyasini **`person`** obyektiga bog'ladik va yangi funksiyani (ya'ni **`greetPerson`**) yaratdik. Endi **`greetPerson()`** chaqirilganda, **`this`** **`person`** obyektiga ishora qiladi va `"Salom, Ali"` natijasi chiqadi.

### **`call()`, `apply()`, va `bind()` o'rtasidagi farqlar:**

| Xususiyat        | `call()`                         | `apply()`                        | `bind()`                        |
|------------------|----------------------------------|----------------------------------|---------------------------------|
| **Argumentlar**   | Virgullab uzatish                | Massiv sifatida uzatish          | Virgullab uzatish, keyincha chaqirish |
| **Natija**        | Funksiyani darhol chaqiradi      | Funksiyani darhol chaqiradi      | Yangi funksiyani qaytaradi     |
| **Qo'llanilish**  | Yangi funksiyani darhol chaqiradi | Yangi funksiyani darhol chaqiradi | Yangi funksiyani yaratib, keyin chaqiradi |
| **Misol**         | `greet.call(person, "Salom")`    | `greet.apply(person, ["Salom"])` | `let greetPerson = greet.bind(person, "Salom"); greetPerson();` |

### **Qaysi vaziyatda qaysi metodni ishlatish kerak?**

1. **`call()`**:
   - Agar sizga funksiyani darhol chaqirib, uni aniq **`this`** bilan bog'lash va funksiyaning argumentlarini individual tarzda uzatish kerak bo'lsa, **`call()`** metodidan foydalaning.
   
   Misol:
   ```javascript
   myFunction.call(myObj, arg1, arg2);
   ```

2. **`apply()`**:
   - Agar sizga funksiyani darhol chaqirib, argumentlarni **massiv** sifatida uzatish kerak bo'lsa, **`apply()`** metodidan foydalaning.
   
   Misol:
   ```javascript
   myFunction.apply(myObj, [arg1, arg2]);
   ```

3. **`bind()`**:
   - Agar sizga yangi funksiya yaratish kerak bo'lsa, ya'ni **`this`** qiymatini aniq belgilash va bu funksiya keyinchalik chaqirilishini xohlasangiz, **`bind()`** metodidan foydalaning.
   
   Misol:
   ```javascript
   let newFunc = myFunction.bind(myObj, arg1);
   newFunc();
   ```

### **Xulosa:**

- **`call()`** va **`apply()`** metodlari funksiyani darhol chaqirishga yordam beradi va ularda **`this`** qiymatini aniqlash mumkin. Farqi shundaki, **`call()`** argumentlarni individual tarzda uzatadi, **`apply()`** esa massiv sifatida.
- **`bind()`** metodi esa yangi funksiyani qaytaradi va **`this`** ni aniq belgilab, uni keyin chaqirish imkonini beradi.

Ushbu metodlar yordamida siz **`this`** ning qiymatini aniq belgilashingiz va funksiyani kerakli kontekstdan ishlatishingiz mumkin.

16. What is the difference between exec () and test () methods in javascript?

**`exec()`** va **`test()`** metodlari JavaScriptda **RegExp (regular expressions)** bilan ishlashda qo'llaniladi. Ikkala metod ham bir xil **RegExp** ob'ekti bilan ishlaydi, lekin ularning ishlash usullari va natijalari turlicha.

### **1. `exec()` metodi:**

**`exec()`** metodi **RegExp** ob'ekti bilan ishlatiladigan va **string**ni tekshiruvchi metoddir. Bu metod **RegExp** shabloniga mos keluvchi birinchi moslikni qidiradi va agar topilsa, **array** (massiv) formatida natija qaytaradi. Agar moslik topilmasa, **null** qaytariladi.

**Sintaksis**:
```javascript
regexp.exec(string);
```

- **`regexp`** — bu **RegExp** ob'ekti.
- **`string`** — bu tekshiriladigan **string** (matn).

#### **Qaytariladigan natija**:
- Agar moslik topilsa, **`exec()`** metodi birinchi moslikni va qo'shimcha ma'lumotlarni o'z ichiga olgan massivni qaytaradi.
- Agar moslik topilmasa, **`exec()`** metodi **null** qaytaradi.

#### **Misol:**
```javascript
const regex = /a(b)c/;
const str = "abc";
const result = regex.exec(str);

console.log(result);  // ["abc", "b"] (massiv: to'liq moslik va guruhlar)
```

Bu yerda:
- **`result[0]`** — bu to'liq moslik: `"abc"`.
- **`result[1]`** — bu birinchi guruh: `"b"`.

Agar moslik topilmasa:
```javascript
const regex = /d+/;
const str = "abc";
const result = regex.exec(str);

console.log(result);  // null
```
**`null`** natijasi qaytadi, chunki `"abc"`da **`d`** harfi mavjud emas.

### **2. `test()` metodi:**

**`test()`** metodi **RegExp** ob'ekti bilan ishlatiladigan va **boolean** (haqiqat/soxta) qiymatni qaytaradigan metoddir. Bu metod shablon matnga mos keladimi-yo'qmi degan savolga javob beradi: agar moslik topilsa, **true**; aks holda, **false** qaytaradi.

**Sintaksis**:
```javascript
regexp.test(string);
```

- **`regexp`** — bu **RegExp** ob'ekti.
- **`string`** — bu tekshiriladigan **string** (matn).

#### **Qaytariladigan natija**:
- Agar **RegExp** ob'ekti matnga mos kelsa, **`test()`** metodi **true** qaytaradi.
- Agar moslik topilmasa, **`test()`** metodi **false** qaytaradi.

#### **Misol:**
```javascript
const regex = /a(b)c/;
const str = "abc";
const result = regex.test(str);

console.log(result);  // true (matn mos keldi)
```

Agar moslik topilmasa:
```javascript
const regex = /d+/;
const str = "abc";
const result = regex.test(str);

console.log(result);  // false (matn mos kelmadi)
```

### **Asosiy Farqlar:**

| Xususiyat           | **`exec()`**                                    | **`test()`**                                  |
|---------------------|-------------------------------------------------|------------------------------------------------|
| **Natija**          | Agar moslik topilsa, massiv (array) qaytaradi; agar topilmasa, **null** qaytaradi. | **true** (agar moslik topilsa) yoki **false** (agar topilmasa) qaytaradi. |
| **Qo'llanishi**     | Matndan moslikni yoki guruhlarni olish uchun ishlatiladi. | Faqat moslikning mavjudligini tekshirish uchun ishlatiladi. |
| **Maqsad**          | Moslikni topib, guruhlar va to'liq moslikni olish uchun ishlatiladi. | Faqatgina moslik bor-yo'qligini tekshirish uchun ishlatiladi. |
| **Chiqish turi**    | Massiv (agar moslik topilsa) yoki **null** (agar moslik topilmasa). | **true** yoki **false**. |

### **Misollarni ko'rib chiqish:**

#### 1. **`exec()` misoli:**

```javascript
const regex = /(\d+)/;
const str = "There are 123 apples";

const result = regex.exec(str);
console.log(result);  // ["123", "123"]
```
- Bu yerda **`exec()`** metodi matndan raqamni topadi va **["123", "123"]** natijani qaytaradi. Birinchi element to'liq moslikni bildiradi, ikkinchi element esa guruhni bildiradi (ya'ni, **`(\d+)`** guruh).

#### 2. **`test()` misoli:**

```javascript
const regex = /(\d+)/;
const str = "There are 123 apples";

const result = regex.test(str);
console.log(result);  // true
```
- Bu yerda **`test()`** metodi faqat **true** qaytaradi, chunki matnda raqam mavjud.

### **Xulosa:**
- **`exec()`** metodi yordamida **RegExp** shabloni bilan mos keluvchi to'liq moslik va guruhlar haqida batafsil ma'lumot olish mumkin.
- **`test()`** metodi esa **boolean** qiymatini qaytarib, faqat moslikning mavjudligini tekshiradi. 

Agar sizga moslikni aniqlab, qo'shimcha ma'lumot kerak bo'lsa, **`exec()`** metodidan foydalaning. Agar faqat moslik bor-yo'qligini tekshirishingiz kerak bo'lsa, **`test()`** metodini ishlatishingiz mumkin.

17. What is currying in JavaScript?

**Currying** JavaScript'da funksional dasturlashda ishlatiladigan kontseptlardan biridir. **Currying** — bu bir nechta argumentlarni olish o'rniga, faqat bitta argumentni olish orqali funksiyani qadam-baqadam chaqirish usulidir. Ya'ni, bir nechta argumentlar bo'yicha ishlovchi funksiyani bir nechta kichik funksiyalarga ajratish. Har bir yangi chaqirilgan funksiya o'zining argumentini olishadi va oxirgi funksiya esa natijani qaytaradi.

### **Curryingning asosiy tushunchasi:**
Currying birinchi funksiyadan keyin boshqa funksiyalarni qaytarish orqali, har bir chaqiruvda faqat birta argumentni olishni nazarda tutadi. Bu usul orqali kodni yanada qayta ishlatiladigan, aniq va o'qilishi oson qilish mumkin.

### **Currying misoli:**

Quyidagi kodda **currying** usulida yozilgan funksiyani ko'rib chiqamiz:

```javascript
function add(a) {
    return function(b) {
        return a + b;
    };
}

const add5 = add(5); // `a` ni 5 ga tenglab yangi funksiya yaratdik
console.log(add5(3)); // 5 + 3 = 8
console.log(add5(10)); // 5 + 10 = 15
```

Bu yerda:
- **`add(a)`** funksiyasi birinchi argumentni qabul qiladi (masalan, 5).
- Keyin, bu funksiya boshqa bir funksiya (ya'ni, `function(b)`)ni qaytaradi, u ikkinchi argumentni qabul qiladi va natijani qaytaradi.

Shunday qilib, **`add(5)`** chaqirilganda, **`add5`** nomli yangi funksiya hosil bo'ladi, u faqat **b** argumentini kutadi. Keyin **`add5(3)`** yoki **`add5(10)`** chaqirilganda, birinchi argument (ya'ni 5) va ikkinchi argument (masalan, 3 yoki 10) yig'indisi hisoblanadi.

### **Currying misoli:**

Quyida yanada murakkab misol keltiraman:

```javascript
function multiply(a) {
    return function(b) {
        return function(c) {
            return a * b * c;
        };
    };
}

console.log(multiply(2)(3)(4));  // 2 * 3 * 4 = 24
```

Bu yerda:
- **`multiply(a)`** birinchi argumentni (masalan, `2`) qabul qiladi va yana bir funksiya qaytaradi.
- Bu funksiya esa **`b`** ni qabul qiladi va yana bir funksiya qaytaradi.
- Oxirgi funksiya esa **`c`** ni qabul qilib, barcha uchta argumentni ko'paytirib natijani qaytaradi.

### **Curryingni qanday amalga oshirish mumkin?**

JavaScriptda **currying**ni amalga oshirish uchun, odatda, **funksiya** ichida **ichki funksiya** yaratilib, har bir chaqirilganida yana bir argument olinadi. Misol uchun:

```javascript
function curryingExample(a) {
    return function(b) {
        return function(c) {
            return a + b + c;
        };
    };
}
```

Bu yerda har bir yangi chaqirilgan funksiya o'zining argumentini qabul qiladi va oxirgi natijani hisoblab chiqaradi.

### **Yordamchi funksiya bilan currying:**

JavaScriptda curryingni ko'pincha yordamchi funksiyalar yordamida amalga oshirishingiz mumkin. Quyidagi misolda curryingni o'zlashtirish uchun **`currying`** yordamchi funksiyasi yozilgan:

```javascript
function currying(fn) {
    return function(a) {
        return function(b) {
            return fn(a, b);
        };
    };
}

const add = (a, b) => a + b;

const curriedAdd = currying(add);
console.log(curriedAdd(2)(3));  // 5
```

Bu yerda:
- **`currying()`** yordamchi funksiyasi **`add`** funksiyasini currying usulida yozadi.
- Keyin **`curriedAdd(2)(3)`** chaqirilganda, avval 2, keyin esa 3 argumenti olinadi va yig'indisi (5) qaytariladi.

### **Curryingning afzalliklari:**
1. **Qayta ishlatish imkoniyati**:
   - Currying yordamida funksiya va uning qismlarini qayta ishlatish osonlashadi. Ya'ni, bitta funktsiyani bir nechta usullar bilan ishlatish mumkin.
   
2. **Kodning modulli bo'lishi**:
   - Currying kodni kichik va modularga bo'lishga yordam beradi, bu esa uni o'qish va tushunishni osonlashtiradi.

3. **Optimallashtirish**:
   - Curryingning yordamida kodni optimallashtirish mumkin. Misol uchun, ba'zi bir parametrlar uchun funksiyani oldindan sozlab qo'yib, keyin uni boshqa joylarda chaqirish mumkin.

4. **Qayta ishlatish va parametrlarni kechiktirish**:
   - Currying orqali parametrlarni kechiktirib uzatish mumkin, bu esa yanada moslashuvchan va qulay kod yozishni ta'minlaydi.

### **Xulosa:**
**Currying** — bu funksiyani bir necha qadamda chaqirish va har safar birta argumentni uzatish orqali bajarish usuli. Bu yondashuv kodni yanada modul, qayta ishlatiladigan va optimallashtirilgan qilishga yordam beradi. Currying JavaScriptda ko'plab funksional dasturlash usullaridan biridir va undan murakkab hisoblashlar yoki parametrlar uzatilganda foydalanish mumkin.

18. What are some advantages of using External JavaScript?

**Tashqi JavaScript** (External JavaScript) dan foydalanish bir qancha afzalliklar beradi. Tashqi JavaScript — bu JavaScript kodini alohida faylga joylashtirish va uni HTML fayliga `<script>` tegidan foydalanib ulash orqali ishlashni anglatadi. Bu usul bir nechta afzalliklarni taqdim etadi, quyida ularning ba'zilarini ko'rib chiqamiz:

### **1. Kodni qayta ishlatish va modularlik:**

Tashqi JavaScript fayllarini ishlatish orqali bir xil JavaScript kodini bir nechta HTML sahifalarida qayta ishlatish mumkin. Bu, xususan, katta web dasturlarda juda qulaydir.

- **Modularlik**: Tashqi fayllar kodni ajratishga yordam beradi, bu esa dasturning tuzilishini aniq va tushunarli qiladi.
- **Qayta ishlatish**: Agar bir xil JavaScript kodi bir nechta sahifalarda ishlatilishi kerak bo'lsa, uni alohida faylga ajratib, har bir sahifada qayta-qayta yozmasdan ishlatishingiz mumkin.

#### Misol:
```html
<!-- index.html -->
<script src="scripts.js"></script>
```
Bu yerda **`scripts.js`** faylini bir nechta sahifada ishlatish mumkin, faqat bitta faylni yaratib, barcha sahifalarda ulash kerak.

### **2. Sahifaning yuklanish tezligini oshirish:**

Tashqi JavaScript fayllarini ishlatish sahifaning yuklanishini tezlashtirishi mumkin. Sababi, tashqi JavaScript faylini brauzer keshiga saqlab qo'yadi, va keyingi safar sahifa ochilganda, JavaScript fayli yana yuklanmasdan to'g'ridan-to'g'ri keshdan olinadi.

- **Brauzer keshidan foydalanish**: Agar JavaScript faylini tashqi qilib ajratgan bo'lsangiz, foydalanuvchining brauzeri bu faylni saqlab qo'yadi va keyingi tashriflarda qayta yuklanmasdan ishlatiladi. Bu sahifani tezroq yuklash imkonini beradi.
- **Sahifa yuklanishini optimallashtirish**: Sahifa ichida JavaScript kodini to'g'ridan-to'g'ri yozish o'rniga, tashqi faylni chaqirish sahifaning ko'rsatilish vaqtini qisqartiradi, chunki bu fayl faqat bir marta yuklanadi.

### **3. Kodingizni boshqarish osonlashadi:**

JavaScript kodini tashqi faylga ajratish orqali, uni boshqarish va yangilash osonlashadi. Har bir sahifa uchun alohida JavaScript fayllari yaratib, kodni tartibga solish mumkin. Bu, ayniqsa, jamoa bilan ishlaganda, turli funksiyalarni bir joyga jamlashda juda foydalidir.

- **Kodni yaxshiroq tashkil etish**: Tashqi fayllar yordamida kodni yaxshi tashkil qilish mumkin. Masalan, alohida faylni faqat sahifa animatsiyalari uchun yoki formalar uchun ajratish mumkin.
- **Kodni boshqarish osonlashadi**: JavaScript kodini tashqi faylga ajratish orqali, kodni tahrirlash va yangilash osonlashadi, chunki barcha JavaScript kodlari bitta joyda bo'ladi.

### **4. Sahifaning HTML va JavaScript kodlarini ajratish:**

Tashqi JavaScript fayllari HTML faylidan alohida bo'lib, kodni yaxshiroq ajratishga yordam beradi. Bu, ayniqsa, kodni o'qish va tushunishni osonlashtiradi. HTML va JavaScript kodlarini ajratish, dasturchilar uchun ishlashni yanada qulayroq qiladi.

- **Qisqargan HTML fayllar**: JavaScript kodini HTML faylidan ajratib tashlash HTML kodini soddalashtiradi va uni o'qish osonlashadi.
- **Sodda tuzilma**: JavaScript va HTMLni alohida saqlash, dasturchilarga kodni yanada yaxshi boshqarish imkoniyatini beradi.

### **5. Katta loyihalar uchun qulaylik:**

Katta web loyihalarida JavaScriptni tashqi faylga joylashtirish zarur. Bu turdagi loyihalar ko'pincha bir nechta sahifalar, komponentlar va kutubxonalarni o'z ichiga oladi. Tashqi JavaScript fayllari bu turdagi loyihalarni tartibli va samarali boshqarish imkonini beradi.

- **Katta loyihalarda qulay**: Agar siz katta loyiha ustida ishlayotgan bo'lsangiz, barcha JavaScript kodlarini bitta faylga jamlab, ularni modullarga ajratishingiz mumkin. Bu loyihaning o'zgarishlarini kuzatishni va yangi funksiyalarni qo'shishni osonlashtiradi.
- **Kompaniya yoki jamoa ishlari uchun mos**: Bir nechta dasturchilar bir vaqtda turli fayllar ustida ishlashlari mumkin, va tashqi fayllar yordamida barcha kodni boshqarish ancha osonlashadi.

### **6. SEO uchun foydali:**

JavaScript kodini tashqi faylga ajratish sahifa manbasini toza va samarali saqlashga yordam beradi, bu esa qidiruv tizimlari optimallashtirish (SEO) uchun foydali bo'lishi mumkin. Qidiruv tizimlari JavaScript kodini o'qishga qiynalishi mumkin, ammo tashqi faylga joylashtirilgan kod sahifa manbasini tozalashga yordam beradi.

- **Sahifaning toza manbasi**: Sahifadagi JavaScriptni tashqi faylga ajratish HTML manbasini toza va samarali qiladi, bu esa qidiruv tizimlari uchun optimallashtirilgan sahifa yaratishga yordam beradi.

### **Xulosa:**

**Tashqi JavaScript**dan foydalanish bir qancha foydali jihatlarga ega:
1. **Modularlik** va **qayta ishlatish** imkonini yaratadi.
2. Sahifani **tezroq yuklash** va **brauzer keshidan** foydalanishga yordam beradi.
3. Kodingizni boshqarish osonlashadi va **HTML va JavaScript kodlarini ajratadi**.
4. **Katta loyihalar** uchun qulaylik yaratadi.
5. **SEO** uchun foydali bo'lishi mumkin.

Bu afzalliklar JavaScriptni tashqi faylga joylashtirishni web rivojlantirishda tavsiya etilgan usulga aylantiradi.

19. Explain Scope and Scope Chain in javascript.

**Scope** va **Scope Chain** JavaScriptda muhim tushunchalardir, chunki ular kodning qaysi qismlarida o'zgaruvchilar va funksiyalar mavjudligini aniqlaydi. Bu tushunchalar JavaScriptda o'zgaruvchilarni boshqarish va ularni qayerda ishlatish mumkinligini tushunishga yordam beradi. Keling, har birini batafsil ko'rib chiqaylik.

### **1. Scope (Kapsam)**

**Scope** — bu o'zgaruvchilar, funksiyalar, va obyektlarning mavjud bo'ladigan hududi yoki doirasini bildiradi. JavaScriptda o'zgaruvchilar va funksiyalarni qanday va qayerda ishlatishingiz mumkinligi, shu doira (scope) orqali belgilab qo'yiladi.

- **Global Scope** (Global doira): Agar o'zgaruvchi yoki funksiya global doirada e'lon qilingan bo'lsa, uni dasturdagi har qanday joyda ishlatish mumkin.
- **Local Scope** (Mahalliy doira): Agar o'zgaruvchi yoki funksiya ma'lum bir funksiyada e'lon qilingan bo'lsa, u faqat shu funksiya ichida mavjud bo'ladi.
- **Block Scope** (Blok doira): **`let`** va **`const`** kabi o'zgaruvchilarni blok ichida e'lon qilsangiz, ular faqat shu blokda mavjud bo'ladi.

#### **Misollar:**

**Global Scope**:
```javascript
let globalVar = "This is a global variable";

function exampleFunction() {
    console.log(globalVar); // globalVar global doiradagi o'zgaruvchi
}

exampleFunction(); // "This is a global variable"
```

**Local Scope** (Mahalliy doira):
```javascript
function localScopeExample() {
    let localVar = "This is a local variable";
    console.log(localVar); // Bu yerda localVar ishlatilishi mumkin
}

localScopeExample();
console.log(localVar); // Xatolik: localVar faqat function ichida mavjud
```

**Block Scope** (Blok doira):
```javascript
if (true) {
    let blockVar = "This is a block-scoped variable";
    console.log(blockVar); // "This is a block-scoped variable"
}
console.log(blockVar); // Xatolik: blockVar faqat if blokida mavjud
```

### **2. Scope Chain (Kapsam zanjiri)**

**Scope Chain** — bu JavaScriptda o'zgaruvchilarni qayerdan va qanday qilib izlash jarayonidir. Har bir funksiya va blok o'zining doirasiga ega, ammo o'zgaruvchi topilmaganda, JavaScript yuqoriga qarab o'zgaruvchilarni qidiradi. O'zgaruvchini topish jarayoni davomida bir nechta doira (scope) zanjirni tashkil qiladi — bu zanjirni **Scope Chain** deb atashadi.

Agar o'zgaruvchi bir doirada topilmasa, JavaScript uni tashqaridagi doiradan izlashni davom ettiradi, bu jarayon **scope chain** deb ataladi.

#### **Misol:**
```javascript
let a = "Global scope";

function outerFunction() {
    let b = "Outer function scope";

    function innerFunction() {
        let c = "Inner function scope";
        console.log(a); // "Global scope" - a global doiradan olinadi
        console.log(b); // "Outer function scope" - b outerFunction'dan olinadi
        console.log(c); // "Inner function scope" - c local doiradan olinadi
    }

    innerFunction();
}

outerFunction();
```

- **`a`** global scope'dan olinadi, chunki u global doiraga e'lon qilingan.
- **`b`** `outerFunction` scope'dan olinadi, chunki `b` faqat shu funksiya ichida mavjud.
- **`c`** `innerFunction` scope'dan olinadi, chunki `c` faqat ichki funksiya ichida mavjud.

JavaScriptda **scope chain** odatda quyidagicha ishlaydi:
1. Birinchi navbatda, o'zgaruvchini hozirgi doirada (ya'ni, funksiyada yoki blokda) qidiradi.
2. Agar o'zgaruvchi mavjud bo'lmasa, JavaScript tashqaridagi (yuqoridagi) doiraga qaraydi va shu tarzda zanjir davom etadi, to global doiraga yetgunga qadar.

### **3. Lexical Scope (Leksik Kapsam)**

JavaScriptda **lexical scope** tushunchasi, ya'ni "leksik doira", funksiyalar kodda yozilgan joyiga qarab aniqlanadi. Bu, ya'ni, funksiyaning qayerda e'lon qilinganligi uning qanday doirada ishlashini belgilaydi.

#### **Misol:**
```javascript
function outer() {
    let outerVar = "I am in the outer function";
    
    function inner() {
        console.log(outerVar); // outerVar outer() funktsiyasidan olinadi
    }
    
    return inner;
}

const innerFunc = outer();
innerFunc(); // "I am in the outer function"
```

Bu misolda, **`inner`** funksiyasi **`outer`** funksiyasidan tashqarida chaqiriladi, lekin u **`outerVar`** o'zgaruvchisini ko'rib chiqadi. Bu **lexical scope** (leksik doira)ning namunasidir, chunki **`inner`** funksiyasi **`outer`** funksiyasining doirasida e'lon qilingan va uning ichidagi o'zgaruvchilarni ko'rishi mumkin.

### **4. Global Scope va Local Scope o'rtasidagi farq**

- **Global Scope**: Dasturda bir marta e'lon qilingan o'zgaruvchilar har joydan ko'rinadi.
- **Local Scope**: O'zgaruvchilar faqat ularni e'lon qilgan joyda, masalan, funksiyaning ichida mavjud bo'ladi. Funksiya tashqarisida bu o'zgaruvchiga murojaat qilish mumkin emas.

### **Xulosa:**
- **Scope** — bu o'zgaruvchilar va funksiyalar qayerda mavjud bo'lsa, ularning qaysi doirada ishlashini belgilovchi hududdir.
- **Scope Chain** — bu o'zgaruvchilarni topish jarayoni bo'lib, agar o'zgaruvchi hozirgi doiradan topilmasa, JavaScript yuqori doiraga qarab uni qidiradi.
- **Lexical Scope** esa funksiyaning o'z doirasiga va kodning yozilgan joyiga qarab aniqlanadi.

Ushbu tushunchalar JavaScriptda kodni aniq va samarali yozishda juda muhim ahamiyatga ega, chunki ular o'zgaruvchilarni boshqarish va kodni optimallashtirishda yordam beradi.

20. Explain Closures in JavaScript.

### **Closures (Yopilishlar) JavaScriptda**

**Closure** (yopilish) JavaScriptda juda muhim va kuchli tushuncha bo'lib, u funksiya ichida e'lon qilingan o'zgaruvchilarga murojaat qilish imkonini beradi, hatto funksiya chaqirilgandan keyin ham. **Closure** — bu funksiya va uning yaratilgan muhitining (lexical environment) kombinatsiyasidir. Boshqacha aytganda, **closure** — bu funksiya o'zining tashqi funksiyasi yoki doirasidagi o'zgaruvchilarga kirish imkoniyatini saqlab qolgan funksiya.

### **Closures qanday ishlaydi?**

JavaScriptda, funksiyalar **lexical scope** (leksik doira)ga ega, ya'ni funksiyaning doirasi uning kod yozilgan joyiga qarab belgilanadi. **Closure** esa, bu funksiyaning o'zgaruvchilariga tashqaridan ham murojaat qilish imkonini beradi, hatto funksiya chaqirilgandan keyin ham.

### **Closures ni misol bilan tushuntirish**

Misol keltiraylik, bu orqali **closure** qanday ishlashini tushunishga yordam beradi:

```javascript
function outerFunction() {
    let outerVar = "I am from the outer function"; // Tashqi o'zgaruvchi

    function innerFunction() {  // Ichki funksiya
        console.log(outerVar);  // InnerFunction tashqi o'zgaruvchiga murojaat qiladi
    }

    return innerFunction; // innerFunction ni qaytaradi
}

const closureFunc = outerFunction();  // outerFunction chaqiriladi va innerFunction qaytadi
closureFunc();  // "I am from the outer function"
```

**Qanday ishladi?**
1. **`outerFunction`** chaqirilganda, uning ichida **`outerVar`** o'zgaruvchisi va **`innerFunction`** funksiyasi yaratiladi.
2. **`outerFunction`** `innerFunction` ni qaytaradi, ya'ni ichki funksiya tashqariga chiqadi.
3. **`closureFunc`** orqali **`innerFunction`** chaqiriladi.
4. Garchi **`outerFunction`** bajarilganidan keyin **`outerVar`** mavjud bo'lmasa ham, **`innerFunction`** hali ham unga kirish imkoniyatiga ega. Bu **closure** — ichki funksiya tashqi funksiyaning o'zgaruvchilariga murojaat qilishi mumkin.

### **Closure qanday ishlaydi?**

- **Closure** yaratilganida, ichki funksiya o'zining tashqi funksiyasining **lexical environment** (leksik muhiti)ni saqlab qoladi. Bu **lexical environment** — bu tashqi funksiya doirasidagi barcha o'zgaruvchilar va ular bilan bog'liq ma'lumotlarni o'z ichiga oladi.
- **Closure** ichki funksiyaga tashqi o'zgaruvchilarga murojaat qilish imkonini beradi, hatto tashqi funksiya chaqirilganidan keyin ham.

### **Misol: Closure va counter (Hisoblagich)**

Quyidagi misolda **closure**ni hisoblagich (counter) yaratish uchun qanday ishlatish mumkinligini ko'rsatib beraman:

```javascript
function createCounter() {
    let count = 0;  // `count` - tashqi o'zgaruvchi

    return function() {
        count++;  // `count` ni oshiradi
        console.log(count);  // `count` ni chiqaradi
    };
}

const counter = createCounter();  // createCounter chaqiriladi
counter();  // 1
counter();  // 2
counter();  // 3
```

**Qanday ishlaydi?**
1. **`createCounter`** funksiyasi chaqirilganda, **`count`** o'zgaruvchisi `0` ga teng bo'ladi.
2. **`createCounter`** ichida **`return`** orqali **`count`** o'zgaruvchisiga murojaat qiluvchi funksiya qaytariladi. Bu funksiya **closure** bo'lib, **`count`** o'zgaruvchisiga kirish imkoniyatini saqlaydi.
3. Har safar **`counter()`** chaqirilganda, **`count`** o'zgaruvchisi oshadi va yangi qiymat qaytariladi, chunki **`counter`** funksiyasi **`createCounter`** funksiyasining leksik doirasini saqlaydi.

### **Closurening afzalliklari**

1. **Ma'lumotni yashirish (Encapsulation):**
   - **Closure** yordamida o'zgaruvchilarni tashqi doiralardan yashirish mumkin. Boshqacha aytganda, ba'zi o'zgaruvchilarni faqat ichki funksiyalarda ishlatish imkoniyati bo'ladi, bu esa ma'lumotlarni tashqi o'zgarishlardan himoya qiladi.
   
   Misol:
   ```javascript
   function secret() {
       let secretValue = "This is secret!";
       return function() {
           console.log(secretValue);  // secretValue faqat ichki funksiya orqali ko'rsatiladi
       };
   }

   const getSecret = secret();
   getSecret();  // "This is secret!"
   // console.log(secretValue);  // Xatolik: secretValue define qilinmagan
   ```

2. **Qayta ishlatish va o'zgaruvchilarni saqlash:**
   - **Closure** yordamida funksiyaning holatini saqlash mumkin. Bu, masalan, hisoblagichlar yoki boshqa holatlarni kuzatish uchun juda foydali bo'ladi.
   
   Misol:
   ```javascript
   function createAdder(x) {
       return function(y) {
           return x + y;
       };
   }

   const add5 = createAdder(5);
   console.log(add5(3));  // 8
   console.log(add5(10)); // 15
   ```

3. **Yopish orqali o'zgaruvchilarni saqlash (Private data):**
   - **Closure** yordamida private o'zgaruvchilarni yaratish va ularni tashqi dunyodan yashirish mumkin.

### **Closurening muammolari:**

1. **Xotira (Memory) muammolari:**
   - **Closure** o'zining tashqi doirasidagi o'zgaruvchilarni saqlab qoladi, bu esa xotira iste'moliga olib kelishi mumkin. Agar ko'p miqdorda closure yaratilsangiz, ularning saqlab qolgan ma'lumotlari xotirangizni to'ldirishi mumkin.
   
2. **Noaniq o'zgaruvchilarni boshqarish:**
   - Agar closure noto'g'ri ishlatilsa, unda o'zgaruvchilarni boshqarish va ularni qayerda va qanday ishlatayotganini aniqlash qiyin bo'lishi mumkin.

### **Xulosa:**

- **Closure** — bu funksiya va uning yaratilgan leksik muhiti (lexical environment) kombinatsiyasidir.
- **Closure** yordamida tashqi funksiyaning o'zgaruvchilariga ichki funksiya orqali murojaat qilish mumkin.
- Bu JavaScriptda **ma'lumotni yashirish**, **holatni saqlash** va **qayta ishlatish** kabi ko'plab qulayliklarni taqdim etadi.