What is javascript?

JavaScript — bu interaktiv veb-saytlar va veb-ilovalar yaratish uchun ishlatiladigan yuqori darajadagi dasturlash tili. U asosan brauzerda ishlaydi, lekin server tomonda ham ishlatilishi mumkin (masalan, Node.js orqali). JavaScript yordamida veb-sahifalarda dinamik o'zgarishlar, foydalanuvchi bilan interaktiv aloqalar, ma'lumotlar yuborish va olish (AJAX), animatsiyalar yaratish va boshqa ko'plab funksiyalarni amalga oshirish mumkin.

1. What are the different data types present in javascript?

JavaScript'da mavjud bo'lgan turli xil ma'lumot turlari (data types) quyidagilar:

Primitive (Oddiy) ma'lumot turlari:

String: Matn (masalan, "Salom" yoki 'Hello')

Number: Sonlar (masalan, 10, 3.14, -7)

BigInt: Katta sonlar (masalan, 100n, 12345678901234567890n)

Boolean: Mantiqiy qiymatlar (masalan, true yoki false)

undefined: Aniqlanmagan qiymat, o'zgaruvchi yaratilib, unga qiymat berilmaganida bo'ladi.

null: Hech qanday qiymat yo'qligi (null) ni ifodalaydi.

Symbol: Yagona va o'zgarmas qiymat, odatda ob'ektlar uchun noyob kalit sifatida ishlatiladi.

Object: Kengaytirilgan ma'lumot turi, o'zgaruvchilarni, funksiyalarni va boshqa murakkab tuzilmalarni o'z ichiga oladi.

Kompozit (Murakkab) ma'lumot turlari:

Object: Ma'lumotlar to'plami yoki tuzilmasi (masalan, { name: "Ali", age: 25 })

Array: Elementlar ro'yxati (masalan, [1, 2, 3, 4])

Function: JavaScript funksiyalari ham ob'ektlar sifatida qaraladi (masalan, function greet() { ... }).

3. Why do we use the word “debugger” in javascript?

JavaScript’da debugger so'zi asosan dasturdagi xatoliklarni topish va tuzatish (debugging) jarayonini osonlashtirish uchun ishlatiladi. debugger — bu JavaScriptda maxsus bir buyruq bo'lib, uning yordamida kodni to'xtatib, uni qadam-vaqadam tahlil qilish imkonini beradi.

4. Difference between “ == “ and “ === “ operators.

JavaScript'da == va === operatorlari o'xshash ko'rinishga ega bo'lsa-da, ular orasida katta farq bor.

== operatori qiymatlarni solishtirishda faqat qiymatlarni solishtiradi. Agar turlar bir xil bo'lmasa, ularni bir-biriga o'zgartiradi (type coercion), ya'ni turlari farq qilsa, ular avtomatik ravishda bir xil turga aylantiriladi va so'ngra solishtiriladi.

=== operatori qiymatni va turini ham solishtiradi. Agar ikki operand turli xil turlarga ega bo'lsa, u holda ular teng deb hisoblanmaydi. Ya'ni, === operatori avtomatik tur o'zgartirishni amalga oshirmaydi.

5. Difference between var and let keyword in javascript.

JavaScript'da var va let kalit so'zlari o'zgaruvchilarni e'lon qilish uchun ishlatiladi, lekin ularning orasida bir nechta muhim farqlar mavjud. Quyida bu farqlarni batafsil tushuntiraman:

1. var (Eski usul)

Doirasi (Scope): var o'zgaruvchisi funksiya doirasida (function scope) yoki, agar globalda e'lon qilingan bo'lsa, global doirada mavjud bo'ladi. Agar var o'zgaruvchisi blok (masalan, if yoki for siklida) ichida e'lon qilinsa, u blokning tashqarisida ham mavjud bo'ladi (bu hozirgi zamon JavaScript uchun noxush xulosa).

Hoisting: var o'zgaruvchisi hoisting (ko'tarish) xususiyatiga ega, ya'ni uning e'lon qilinishi kodda uning joyidan yuqoriga ko'tariladi. Biroq, qiymat hoisting bo'lmaydi, ya'ni qiymatni ulashdan oldin undefined bo'ladi.

2. let (Yangi usul)

Doirasi (Scope): let o'zgaruvchisi blok doirasida (block scope) mavjud bo'ladi, ya'ni u faqat o'z e'lon qilingan blok ichida ishlaydi. Agar let o'zgaruvchisi if, for yoki boshqa blok ichida e'lon qilinsa, u faqat shu blokda mavjud bo'ladi.

Hoisting: let o'zgaruvchisi hoisting xususiyatiga ega, lekin vardan farqli o'laroq, uning qiymati undefined sifatida ko'tarilmaydi. let o'zgaruvchisi faqat e'lon qilingan joydan keyin ishlatilishi mumkin.

let — bu zamonaviy va xavfsiz usul, var esa eski va ko'proq kutilmagan xulq-atvorlarga olib kelishi mumkin. Shuning uchun, let o'zgaruvchilarini e'lon qilishda let ishlatish yaxshiroqdir.

6. Explain Implicit Type Coercion in javascript.

Implicit Type Coercion (yoki Avtomatik tur o'zgartirish) — bu JavaScriptning xususiyatidir, ya'ni JavaScript avtomatik ravishda bir turdagi qiymatni boshqa turdagi qiymatga o'zgartiradi. Bu o'zgarishlar dastur bajarilishi davomida amalga oshadi, va foydalanuvchi buni bevosita ko'rmaydi.

Implicit Type Coercion — JavaScriptning qulay xususiyatlaridan biri bo'lsa-da, uni ehtiyotkorlik bilan ishlatish kerak. Kutilmagan turdagi o'zgartirishlar va xatoliklarni oldini olish uchun, imkon qadar === operatorini va aniq tur o'zgartirishni (explicit coercion) ishlatish tavsiya etiladi.

7. Is javascript a statically typed or a dynamically typed language?

JavaScript — dinamik tiplash (dynamically typed) dasturlash tili. Bu shuni anglatadiki, JavaScript'da o'zgaruvchilarni e'lon qilishda ular uchun aniq tur belgilanishi shart emas. O'zgaruvchining turi dastur bajarilayotgan paytda avtomatik ravishda aniqlanadi va o'zgartirilishi mumkin.

JavaScript — dinamik tiplash (dynamically typed) tili. Bu uning foydalanuvchilarga kodni tezroq yozish va sinovdan o'tkazishda osonlik yaratadi, lekin shu bilan birga turlarni boshqarishdan kelib chiqadigan xatoliklar ehtimolini ham oshiradi.

Statik tiplash tili o'zgaruvchilarni turini oldindan belgilashni talab qiladi, bu esa kodni optimallashtirish va xatoliklarni kamaytirishda yordam beradi.

Shu bilan birga, TypeScript (JavaScriptning tip bilan ishlaydigan ustuvor versiyasi) JavaScriptga tiplarni qo'shish imkoniyatini beradi, bu esa JavaScriptdagi dinamik tiplashni statik tiplashga o'zgartirishga imkon beradi.

9. Explain passed by value and passed by reference.

JavaScript'da "passed by value" (qiymat bo'yicha uzatish) va "passed by reference" (manzil bo'yicha uzatish) konseptlari juda muhim, chunki ular qanday qilib o'zgaruvchilar funktsiyalarga uzatilishini tushunishga yordam beradi.

Passed by value (qiymat bo'yicha uzatish) — bu primitive turlarda ishlatiladi, va ular funktsiyaga uzatilganida faqat qiymatning nusxasi uzatiladi.

Passed by reference (manzil bo'yicha uzatish) — bu obyektlar va massivlar uchun amal qiladi, va ular funktsiyaga uzatilganda, asl manzilga havola uzatiladi, shuning uchun o'zgarishlar asl ma'lumotga ta'sir qiladi.

10. What is an Immediately Invoked Function in JavaScript?

Immediately Invoked Function Expression (IIFE) — bu JavaScript'da funksiyaning o'zini darhol chaqiradigan ifodasi. IIFE yordamida funksiya e'lon qilinadi va darhol bajariladi. Bu usul asosan o'zgaruvchilarni lokal doirada (local scope) saqlash va global doiraga kirmaslik uchun ishlatiladi.

IIFE yordamida siz funksiya e'lon qilishingiz va uni darhol bajarishingiz mumkin.

Bu metod global o'zgaruvchilarni ifloslanishini oldini olish va kapsulalash maqsadida juda foydalidir.

IIFE asosan JavaScript modullarini yaratishda yoki o'zgaruvchilarni maxfiy saqlashda ishlatiladi.

11. What do you mean by strict mode in javascript and characteristics of javascript strict-mode?

Strict mode (qattiq rejim) — bu JavaScriptning maxsus rejimi bo'lib, u kodni yanada qat'iy va xavfsiz qilish uchun ishlatiladi. Strict mode dasturga kiritilganda, ba'zi eski va noto'g'ri xulq-atvorlarni man etadi va xatoliklarni aniqlashni osonlashtiradi.

Strict mode — bu JavaScript kodining xatoliklarni kamaytirish va xavfsizroq bajarilishini ta'minlash uchun ishlatiladigan maxsus rejimdir.

U ba'zi noto'g'ri xulq-atvorlarni man qiladi va kodingizni to'g'ri va xavfsizroq ishlashini ta'minlaydi.

Agar siz JavaScriptni aniqroq va xavfsizroq ishlatishni xohlasangiz, strict mode’dan foydalanish tavsiya etiladi.

12. Explain Higher Order Functions in javascript.

Higher-Order Functions (yuqori darajali funksiyalar) — bu JavaScriptdagi juda muhim va kuchli kontseptlardan biri bo'lib, ularning asosiy xususiyati shundaki, ular boshqa funksiyalarni argument sifatida qabul qilishlari yoki funksiya qaytarishlari mumkin.

Higher-Order Functions — bu funksiyalar bo'lib, ular boshqa funksiyalarni argument sifatida qabul qilishlari yoki funksiya sifatida qaytarishlari mumkin.

Bu kontsept JavaScriptni yanada qudratli va moslashuvchan qilishga yordam beradi, chunki funksiyalarni boshqarish, o'zgartirish va turli xil vazifalarni bajarish imkonini beradi.

map(), filter(), reduce(), forEach() kabi metodlar yuqori darajali funksiyalar sifatida ishlaydi va JavaScriptdagi massivlar bilan ishlashni osonlashtiradi.

13. Explain “this” keyword.

JavaScript'da this kalit so'zi — bu juda muhim tushuncha bo'lib, u hozirgi kontekstdagi yoki hozirgi funksiyada ishlatiladigan obyektni anglatadi. Asosan, this o'zgaruvchisi, funktsiya chaqirilayotgan joyga va qanday chaqirilishiga qarab farq qiladi. U ko'pincha funksiya yoki metodlarning kontekstini aniqlashda ishlatiladi.

this — bu JavaScriptdagi kontekstni anglatadigan kalit so'zdir va u chaqirilgan joyga qarab har xil qiymatlarni olishadi.

Global doirada this global obyektga ishora qiladi (window yoki global).

Funktsiyada this global obyektga ishora qiladi, lekin strict modeda undefined bo'ladi.

Obyekt metodlarida this metodni chaqirgan obyektga ishora qiladi.

Arrow functionsda this tashqi kontekstdan olinadi.

call(), apply(), bind() metodlari yordamida thisni qo'lda o'zgartirish mumkin.

this kalit so'zi JavaScriptning eng muhim tushunchalaridan biri bo'lib, uning qanday ishlashini to'liq tushunish dasturchilar uchun juda muhimdir.

14. What do you mean by Self Invoking Functions?

Self-Invoking Functions (o'z-o'zini chaqiradigan funksiyalar) — bu JavaScript'da funksiyaning o'zini darhol chaqiradigan xususiyatga ega bo'lgan funksiya turi. Bu funksiyalar, e'lon qilingandan so'ng, darhol bajariladi va hech qanday tashqi chaqiriqni kutmaydi.

Self-Invoking Functions (IIFE) — bu funksiya turidagi kod bo'lib, o'zini darhol chaqiradi.

Ularning asosiy foydasi — global doiradagi o'zgaruvchilarni ifloslanishini oldini olish, kodni kapsulalash va natijalarni darhol olish imkoniyatini yaratishdir.

IIFE JavaScriptda modul yaratish, maxfiy o'zgaruvchilar bilan ishlash va bir martalik kodni bajarish uchun juda qulay vosita hisoblanadi.

15. Explain call(), apply() and, bind() methods.

JavaScript'da call(), apply() va bind() metodlari — bu this kalit so'zining qiymatini o'zgartirish uchun ishlatiladi. Ushbu metodlar, biror funksiyaning this qiymatini aniq bir obyektga bog'lash imkoniyatini beradi va bu metodlar turli holatlarda, ayniqsa, yuqori darajali funksiyalarni ishlatishda juda foydalidir.

call(), apply() va bind() metodlari JavaScriptda this kalit so'zining qiymatini boshqarish uchun ishlatiladi.

call() va apply() metodlari funksiya darhol chaqiriladi, faqat argumentlarni uzatish usuli farq qiladi.

bind() metodida esa funksiya darhol chaqirilmaydi, balki yangi funksiya qaytariladi va this qiymati belgilangan obyektga bog'lanadi.

Ushbu metodlarni o'rganish, JavaScript kodini yanada moslashuvchan va samarali yozishga yordam beradi.

16. What is the difference between exec () and test () methods in javascript?

JavaScript'da exec() va test() metodlari RegExp (regular expressions) bilan ishlash uchun ishlatiladi. Ular o'xshash maqsadni ko'zlashadi, ya'ni matnni tekshirish yoki ma'lumot olish uchun ishlatiladi, ammo ularning ishlash usuli va qaytaradigan natijalari bir-biridan farq qiladi.

test() metodi boolean natija qaytaradi, ya'ni regulyar ifoda matnga mos keladimi yoki yo'qligini tekshiradi.

exec() metodi esa, agar moslik bo'lsa, mos kelgan qismni va qo'shimcha ma'lumotlarni (masalan, indeks) qaytaradi. Agar moslik bo'lmasa, null qaytaradi.

test() oddiy tekshirishlar uchun qulay, exec() esa mosliklarni olish va qo'shimcha ma'lumotlarni (masalan, indeks) olish uchun qulaydir.

17. What is currying in JavaScript?

Currying (kurrin qilish) — bu JavaScriptda funktsiyani bir nechta qadamlar orqali chaqirishga imkon beradigan texnikadir. Boshqacha aytganda, currying bir nechta argumentlarni qabul qiluvchi funksiyani, bir vaqtning o'zida faqat bitta argument qabul qiladigan funksiyalarga aylantirish jarayonidir. Har bir chaqiruvda faqat bitta argument uzatiladi va oxirgi natijaga erishish uchun barcha argumentlar to'planadi.

Currying — bu funksiyani bir nechta kichik funktsiyalarga bo'lish texnikasi bo'lib, har bir funksiya faqat bitta argumentni qabul qiladi.

Bu texnika modullik, qayta foydalanish, va kodning qisqarishini ta'minlaydi.

Currying funksiyalarni ancha samarali va o'qilishi oson qiladi, ayniqsa murakkab hisoblashlar va parametrlar bilan ishlashda.

18. What are some advantages of using External JavaScript?

Tashqi JavaScript (External JavaScript) — bu JavaScript kodini HTML faylidan alohida tashqi faylda saqlash va uni HTML faylga ulash usulidir. Tashqi JavaScript fayllari .js kengaytmasiga ega bo'ladi va HTML faylga script tegidan foydalanib ulanishi mumkin.

Tashqi JavaScript foydalangan holda, kodni yaxshiroq tashkil etish, qayta ishlatish, optimallashtirish va o'qish imkoniyatlarini oshirish mumkin. Bu yondashuv saytning ishlash tezligini yaxshilaydi, kodni boshqarishni soddalashtiradi va jamoaviy ishni qulaylashtiradi. U ko'plab zamonaviy veb-saytlar va ilovalarda keng qo'llaniladi.

19. Explain Scope and Scope Chain in javascript.

Scope (kengaytma) va Scope Chain (kengaytma zanjiri) — JavaScriptda o'zgaruvchilar va funksiyalarning ko'rinish yoki qamrovini boshqaradigan muhim tushunchalardir. Bu tushunchalar dasturchilar uchun JavaScriptning qanday ishlashini, o'zgaruvchilarning qayerda mavjudligini va ular qanday ko'rinishi mumkinligini tushunish uchun juda muhimdir.

Scope — bu o'zgaruvchilar va funksiyalar mavjud bo'lgan hudud.

Global scope — barcha joylarda ko'rinadigan o'zgaruvchilarni o'z ichiga oladi.

Local scope — faqat ma'lum bir blok yoki funksiyada ko'rinadigan o'zgaruvchilarni o'z ichiga oladi.

Scope Chain — o'zgaruvchilarni izlash jarayoni bo'lib, ichki funksiyalar tashqi funksiyalar yoki global scopedagi o'zgaruvchilarga murojaat qiladi.

Lexical scoping — o'zgaruvchilarni izlash jarayoni kod yozilgan joyga asoslanadi.

Closures — funksiyalar orqali tashqi o'zgaruvchilarni saqlash va ularni keyinchalik ishlatish imkonini beradi.

JavaScriptda scope va scope chain konseptlarini tushunish, dasturda o'zgaruvchilarni to'g'ri boshqarish va xatolardan qochish uchun juda muhimdir.

20. Explain Closures in JavaScript.

Closure (Yopishma) — bu JavaScriptdagi kuchli va muhim tushunchalardan biridir. Closure — bu ichki funksiya (nested function) tashqi funksiyaning o'zgaruvchilariga kirish huquqiga ega bo'lgan funksiya. Boshqacha qilib aytganda, closure — bu ichki funksiyaning o'zgaruvchilariga tashqi funktsiyaning o'zgaruvchilariga murojaat qilish imkoniyatini beradigan mexanizm.

Closure asosan JavaScriptning lexical scoping (leksikal kengaytma) printsipiga asoslanadi, ya'ni o'zgaruvchilarning qayerda aniqlanganiga qarab ular qaysi scope'da ko'rinishini belgilaydi.

Closures JavaScriptda juda muhim tushuncha bo'lib, bu funksiya ichida boshqa bir funksiyaning o'zgaruvchilariga kirish imkonini beruvchi mexanizmni anglatadi. Closure yordamida private o'zgaruvchilar yaratish, xotira boshqaruvi va asinxron dasturlashda samarali ishlash mumkin. Bu tushuncha nafaqat oddiy, balki murakkab JavaScript ilovalarida ham keng qo'llaniladi.