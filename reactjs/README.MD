1. What is React?
(React nima?)

React (yoki ReactJS) — bu ochiq manba kodli front-end JavaScript kutubxonasi bo'lib, u asosan bitta sahifa ilovalarini yaratish uchun ishlatiladi. React foydalanuvchi interfeyslarini yaratish uchun ishlatiladi, va bu komponentlar asosida deklarativ yondashuvni qo'llaydi.

Reactni Facebook’da ishlovchi dasturchi Jordan Walke yaratgan. React birinchi marta 2011 yilda Facebook News Feed'ida, 2012 yilda esa Instagram’da ishlatilgan.

2. What is the history behind React evolution?
(React evolyutsiyasining tarixi qanday?)

ReactJS tarixi 2010 yilda XHP yaratishdan boshlangan. XHP — bu PHP kengaytmasi bo'lib, til sintaksisini shunday yaxshilaydi-ki, XML hujjat parchalarini haqiqiy PHP ifodalari sifatida ishlatish mumkin bo'ladi. Asosiy maqsadi esa maxsus va qayta ishlatiladigan HTML elementlarini yaratishda ishlatilgan.

Ushbu kengaytmaning asosiy printsipi front-end kodini tushunishni osonlashtirish va cross-site scripting (XSS) hujumlaridan himoya qilishga yordam berish edi. Loyihaning muvaffaqiyati foydalanuvchi tomonidan kiritilgan zararli tarkibni tozalashda namoyon bo'ldi.

Lekin XHP bilan boshqa bir muammo yuzaga keldi: dinamik veb-ilovalar serverga ko'plab so'rovlar yuborishni talab qiladi, va XHP bu muammoni hal qilmagan. Shuningdek, dasturdagi kichik o'zgarishlar uchun butun foydalanuvchi interfeysi qayta render qilinardi. Keyin, Jordan tomonidan XHP'dan ilhomlanib React ning dastlabki prototipi FaxJ deb nomlangan. Nihoyat, bir oz vaqt o'tgach, React JavaScript dunyosiga yangi kutubxona sifatida taqdim etildi.

3. What are the major features of React?
(Reactning asosiy xususiyatlari qanday?)

Reactning asosiy xususiyatlari quyidagilardan iborat:

- JSX sintaksisini ishlatadi, bu JS sintaksis kengaytmasi bo'lib, dasturchilarga JS kodida HTML yozish imkonini beradi.
- Real DOM o'rniga Virtual DOMni ishlatadi, chunki Real DOM bilan ishlash qimmatga tushadi.
- Server tomoni renderingini qo'llab-quvvatlaydi, bu esa Qidiruv tizimlari optimallashtirish (SEO) uchun foydalidir.
- Bir yo'nalishda yoki unidirectional ma'lumot oqimi (data flow) yoki ma'lumot bog'lanishini (data binding) ta'minlaydi.
- Foydalanuvchi interfeysini yaratishda qayta ishlatiladigan va birlashtiriladigan UI komponentlaridan foydalanadi.

4. What is JSX?
(JSX nima?)

JSX — bu JavaScript XML deb ataladi va ECMAScript uchun XML-ga o'xshash sintaksis kengaytmasidir. Aslida, bu faqat React.createElement(type, props, ...children) funksiyasi uchun sintaktik shakarlikni taqdim etadi, bu esa bizga JavaScriptning ifodali qulayligi bilan HTMLga o'xshash shablon sintaksisini taqdim etadi.

5. What is the difference between Element and Component?
(Element va komponent o'rtasidagi farq nima?)

Element — bu ekranda ko'rinishi kerak bo'lgan narsani DOM tugunlari yoki boshqa komponentlar nuqtai nazaridan tasvirlaydigan oddiy ob'ekt. Elementlar o'z prop'larida boshqa Elementlarni o'z ichiga olishi mumkin. React elementini yaratish arzon. Bir marta element yaratilgandan so'ng, u o'zgartirilishi mumkin emas.

6. How to create components in React?
(React-da komponentlarni qanday yaratish mumkin?)

Komponentlar Reactda foydalanuvchi interfeyslarini (UI) yaratish uchun qurilish bloklari hisoblanadi. Komponentni yaratishning ikkita mumkin bo'lgan usuli mavjud.

Funktsiya komponentlari: Bu komponent yaratishning eng oddiy usuli. Bular rekvizit ob'ektini yagona va yagona parametr sifatida qabul qiladigan va natijani ko'rsatish uchun React elementlarini qaytaradigan sof JavaScript funktsiyalari:

Sinf komponentlari: Siz komponentni aniqlash uchun ES6 sinfidan ham foydalanishingiz mumkin. Yuqoridagi funktsiya komponenti sinf komponenti sifatida yozilishi mumkin:

7. When to use a Class Component over a Function Component?
(Sinf komponentidan funksiya komponentidan qachon foydalanish kerak?)

Hooks (ya'ni React 16.8 dan keyin) qo'shilgandan so'ng, har doim React'dagi Class komponentlari o'rniga Function komponentlarini ishlatish tavsiya etiladi. Chunki siz faqat funksiya komponentida mavjud bo'lgan sinf komponentida mavjud bo'lgan holat, hayot aylanish usullari va boshqa xususiyatlardan foydalanishingiz mumkin.

8. What are Pure Components?
(Sof komponentlar nima?)

Sof komponentlar - bu bir xil holat va rekvizitlar uchun bir xil natijani beruvchi komponentlar. Funktsiya komponentlarida siz ushbu sof komponentlarga komponentni o'rab olish uchun xotirada saqlangan React.memo() API orqali erishishingiz mumkin. Bu API oldingi rekvizitlar va yangi rekvizitlarni sayoz taqqoslash yordamida solishtirish orqali keraksiz qayta ishlashni oldini oladi. Shunday qilib, u ishlashni optimallashtirish uchun foydali bo'ladi.

Shu bilan birga, u avvalgi holatni joriy holat bilan solishtirmaydi, chunki funktsiya komponentining o'zi bir xil holatni qayta o'rnatganingizda sukut bo'yicha keraksiz ko'rsatishni oldini oladi.

9. What is state in React?
(Reactdagi state nima?)

Komponentning holati - komponentning ishlash muddati davomida o'zgarishi mumkin bo'lgan ba'zi ma'lumotlarni saqlaydigan ob'ekt. Muhim nuqta shundaki, har doim holat ob'ekti o'zgarganda, komponent qayta ko'rsatiladi. Har doim bizning davlatimizni iloji boricha sodda qilish va statistik komponentlar sonini kamaytirish tavsiya etiladi.

Xabar holatiga ega User komponentining misolini olaylik. Bu yerda User komponentiga holat qoʻshish uchun useState kancasidan foydalanilgan va uni yangilash uchun joriy holat va funksiyaga ega massivni qaytaradi.

10. What are props in React?
(React-da props nima?)

Props komponentlarga kirish hisoblanadi. Ular HTML-teg atributlariga o'xshash yaratishda komponentlarga uzatiladigan qiymatlar to'plamini o'z ichiga olgan yagona qiymatlar yoki ob'ektlardir. Bu erda ma'lumotlar asosiy komponentdan pastki komponentga uzatiladi.

11. What is the difference between state and props?
(State va props o'rtasidagi farq nima?)

Reactda holat ham, rekvizit ham oddiy JavaScript obyektlari bo‘lib, komponent ma’lumotlarini boshqarish uchun ishlatiladi, lekin ular turli usullarda qo‘llaniladi va har xil xususiyatlarga ega.

Shtat ob'ekti komponentning o'zi tomonidan boshqariladi va uni setter (sinf komponentlari uchun setState()) funksiyasi yordamida yangilash mumkin. Rekvizitlardan farqli o'laroq, holat komponent tomonidan o'zgartirilishi mumkin va komponentning ichki holatini boshqarish uchun ishlatiladi. ya'ni holat komponent xotirasi vazifasini bajaradi. Bundan tashqari, holatdagi o'zgarishlar komponent va uning bolalarini qayta ko'rsatishga olib keladi. Komponentlar faqat davlatdan foydalanish bilan qayta foydalanish mumkin emas.

Boshqa tomondan, rekvizitlar (“xususiyatlar”ning qisqartmasi) komponentga uning asosiy komponenti tomonidan uzatiladi va faqat o‘qish uchun mo‘ljallangan, ya’ni ularni o‘z komponentining o‘zi o‘zgartirib bo‘lmaydi. ya'ni rekvizitlar funksiya uchun argument vazifasini bajaradi. Shuningdek, rekvizitlar komponentning harakatini sozlash va komponentlar o'rtasida ma'lumotlarni uzatish uchun ishlatilishi mumkin. Komponentlar rekvizitlardan foydalanish bilan qayta foydalanish mumkin bo'ladi.

12. What is the difference between HTML and React event handling?
(HTML va React hodisalarini boshqarish o'rtasidagi farq nima?)

1 HTMLda hodisa nomi odatda konventsiya sifatida kichik harflar bilan ifodalanadi:

2 HTMLda standart xatti-harakatni oldini olish uchun false ni qaytarishingiz mumkin:

3 HTMLda siz funktsiyani () qo'shish orqali chaqirishingiz kerak, reaksiyada esa funktsiya nomi bilan () qo'shmasligingiz kerak. (masalan, birinchi nuqtada "activateLasers" funksiyasiga qarang)

13. What are synthetic events in React?
(Reactdagi sintetik hodisalar nima?)

SyntheticEvent - bu brauzerning mahalliy hodisasi atrofidagi o'zaro faoliyat brauzer. Uning APIsi brauzerning mahalliy hodisasi bilan bir xil, jumladan stopPropagation() va preventDefault(), hodisalar barcha brauzerlarda bir xil ishlaydi. Mahalliy voqealarga to'g'ridan-to'g'ri sintetik voqealardan mahalliyEvent atributidan foydalangan holda kirish mumkin.

14. What are inline conditional expressions?
(Inline shartli ifodalar nima?)

Ifodalarni shartli ko'rsatish uchun JS da mavjud bo'lgan if yoki uchlik ifodalardan foydalanishingiz mumkin. Ushbu yondashuvlardan tashqari, JSX-ga har qanday iboralarni jingalak qavslar ichiga o'rash va keyin JS mantiqiy operatori && orqali joylashtirishingiz mumkin.

15. What is "key" prop and what is the benefit of using it in arrays of elements?
("Kalit" prop nima va uni elementlar massivlarida ishlatishning foydasi nimada?)

Kalit - bu ma'lumotlarni ko'rsatish uchun massivlar ustida xaritalashda qo'shishingiz kerak bo'lgan maxsus atribut. Kalit tayanch Reactga qaysi elementlar o‘zgargan, qo‘shilgan yoki o‘chirilganligini aniqlashga yordam beradi.

16. Virtual DOM nima?

Virtual DOM (VDOM) Real DOM ning xotiradagi tasviridir . UI ko'rinishi xotirada saqlanadi va "haqiqiy" DOM ​​bilan sinxronlashtiriladi. Bu chaqirilayotgan render funktsiyasi va elementlarning ekranda ko'rsatilishi o'rtasida sodir bo'ladigan bosqich. Bu butun jarayon yarashuv deb ataladi .

17. Virtual DOM qanday ishlaydi?

Virtual DOM uchta oddiy bosqichda ishlaydi.

Har qanday asosiy ma'lumotlar o'zgarganda, butun UI Virtual DOM ko'rinishida qayta ko'rsatiladi.

Keyin oldingi DOM vakili va yangisi o'rtasidagi farq hisoblab chiqiladi.

Hisob-kitoblar amalga oshirilgandan so'ng, haqiqiy DOM faqat haqiqatda o'zgargan narsalar bilan yangilanadi.

18. Shadow DOM va Virtual DOM o'rtasidagi farq nima?

Shadow DOM brauzer texnologiyasi bo'lib, asosan veb-komponentlardagi o'zgaruvchilar va CSS-ni aniqlash uchun mo'ljallangan . Virtual DOM - bu JavaScript-dagi kutubxonalar tomonidan brauzer API-lari ustida amalga oshirilgan kontseptsiya.

19. React Fiber nima?

Elyaf - bu yangi yarashtiruvchi vosita yoki React v16 da asosiy algoritmni qayta tiklash. React Fiber-ning maqsadi - animatsiya, tartib, imo-ishoralar, ishni to'xtatib turish, to'xtatish yoki qayta ishlatish va har xil turdagi yangilanishlarga ustuvorlik berish kabi sohalarga mosligini oshirish; va yangi parallellik primitivlari.

20. React Fiber-ning asosiy maqsadi nima?

React Fiber -ning maqsadi animatsiya, tartib va ​​imo-ishoralar kabi sohalarga mosligini oshirishdir. Uning sarlavhali xususiyati - bosqichma-bosqich ko'rsatish : ko'rsatish ishini bo'laklarga bo'lish va uni bir nechta ramkalarga tarqatish qobiliyati.

hujjatlardan

Uning asosiy maqsadlari quyidagilardan iborat:

Uzluksiz ishni bo'laklarga bo'lish qobiliyati.

Amaldagi ishlarni ustuvorlashtirish, qayta asoslash va qayta ishlatish qobiliyati.

React-da tartibni qo'llab-quvvatlash uchun ota-onalar va bolalar o'rtasida oldinga va orqaga kelish qobiliyati.

render() dan bir nechta elementlarni qaytarish imkoniyati.
Xato chegaralarini yaxshiroq qo'llab-quvvatlash.

