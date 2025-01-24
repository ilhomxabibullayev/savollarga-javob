1. Explain TypeScript and its use?
(TypeScript va uning ishlatilishini tushuntiring?)

TypeScript - bu Microsoft tomonidan ishlab chiqilgan va qo'llab-quvvatlanadigan ochiq kodli dasturlash tili bo'lib, u JavaScript-ning statik tarzda yozilgan super to'plami sifatida ishlaydi. JavaScript-ni turdagi izohlar va interfeyslar bilan kengaytirish orqali u ishlab chiquvchilarga xatoliklarni ish vaqtida emas, balki kompilyatsiya jarayonida aniqlash imkonini beradi va shu bilan xavfsizroq va samaraliroq kodni ta'minlaydi.

TypeScript shuningdek, katta hajmli dasturlarni ishlab chiqishga imkon beradi, bu nomlar maydoni, dekorativlar va mavhum sinflar kabi xususiyatlarga ega. Uning eng muhim kuchli tomonlaridan biri bu JavaScript ekotizimlari va Angular, React yoki Vue.js kabi zamonaviy ramkalar bilan uzluksiz integratsiya bo'lib, uni barqaror va mustahkam veb-ilovalarni yaratmoqchi bo'lgan har qanday dasturchi uchun bebaho vositaga aylantiradi.

2. Can you tell the names of some of the built-in types in TypeScript?
(TypeScript-dagi ba'zi o'rnatilgan turlarning nomlarini ayta olasizmi?)

TypeScript-da xavfsizroq va aniqroq kodni ta'minlash uchun ishlab chiquvchilar uchun bir nechta o'rnatilgan turlar mavjud. Eng keng tarqalgan o'rnatilgan turlardan ba'zilari:

har qanday: qiymatning har qanday turini ifodalaydi va o'zgaruvchiga bir nechta turlarni saqlashga imkon beradi.

mantiqiy: to'g'ri yoki noto'g'ri bo'lishi mumkin bo'lgan mantiqiy qiymatni ifodalaydi.

raqam: butun sonlar va suzuvchi nuqtali raqamlarni o'z ichiga olgan har qanday raqamli qiymatni ifodalaydi.

string: odatda matnli ma'lumotlarni saqlash uchun ishlatiladigan belgilar ketma-ketligini ifodalaydi.

null: o'zgaruvchiga ataylab tayinlangan qiymat yo'qligini bildiradi.

aniqlanmagan: hali qiymat tayinlanmagan o'zgaruvchini ifodalaydi.

void: odatda qiymat qaytarmaydigan funksiyalar uchun qaytarish turi sifatida ishlatiladigan turning etishmasligini ifodalaydi.

3. Give an example of generics in TypeScript?
(TypeScript-dagi generiklarga misol keltiring?)

TypeScript-dagi generiklar tip xavfsizligini buzmasdan qayta foydalanish mumkin bo'lgan va moslashuvchan komponentlarni yaratishga imkon beradi. Ular sizga har xil turlar bilan ishlay oladigan funksiyalar, sinflar yoki interfeyslarni yaratishga imkon beradi va shu bilan birga statik yozishning afzalliklarini ta'minlaydi. TypeScript funksiyasida generiklardan foydalanishga misol:

4. Tell me about Modules in TypeScript.
(TypeScript-dagi modullar haqida gapirib bering.)

TypeScript-dagi modullar kodni tartibga solish va inkapsulyatsiya qilish usulini taqdim etadi, bu esa katta ilovalarni ishlab chiqish, saqlash va sinovdan o'tkazishni osonlashtiradi. Ular sizning kodingizni alohida fayllarga bo'lish imkonini beradi, bunda har bir fayl ma'lum funktsiyalar to'plamiga yoki bitta mas'uliyatga qaratilgan. Modullar bog'liqliklarni boshqarish va turli nomlar bo'shliqlari va import/eksport yordamida nomlash ziddiyatlarining oldini olish uchun mo'ljallangan.

TypeScript-da modullarning ikkita asosiy turi mavjud:

Tashqi modullar: "Fayl modullari" deb ham ataladi, ular har bir manba fayli uchun bitta moduldir. Yangi TypeScript faylini yaratganingizda va import va eksport kalit so'zlari bilan ishlaganingizda, siz avtomatik ravishda tashqi modul yaratasiz. Bu eng ko'p ishlatiladigan TypeScript modullari.

Atrof muhit modullari: Ular uchinchi tomon kutubxonalari yoki mavjud global o'zgaruvchilar uchun turdagi ma'lumotlarni taqdim etish uchun ishlatiladi. Ular odatda .d.ts fayli yordamida e'lon qilinadi va kutubxona ishlab chiquvchilari tomonidan taqdim etilishi yoki hamjamiyat tomonidan yaratilishi mumkin. Deklaratsiya moduli sintaksisi muhit modulini aniqlash uchun ishlatiladi.

5. Why can TypeScript be chosen over JavaScript?
(Nima uchun TypeScript-ni JavaScript-dan tanlash mumkin?)

TypeScript JavaScript-ga nisbatan bir qancha afzalliklarni taqdim etadi, bu esa uni keng miqyosli va texnik xizmat ko'rsatish mumkin bo'lgan ilovalar yaratishga intilayotgan ko'plab ishlab chiquvchilar uchun afzalroq tanlov qiladi. TypeScript-ning eng ko'zga ko'ringan afzalliklaridan biri bu xatolarni osongina topishga yordam beradigan boy muhitni ta'minlovchi vositalar va IDElar. Boshqa ba'zi afzalliklar quyidagilardan iborat:

Kengaytirilgan avtomatik toʻldirish va IntelliSense: TypeScript Visual Studio Code kabi muharrirlar bilan yaxshiroq integratsiyalashuv orqali yaxshilangan avtomatik toʻldirish, kod navigatsiyasi va refaktoring imkoniyatlarini taʼminlaydi, bu esa ishlab chiqish jarayonini tezroq va samaraliroq qiladi.

Keng miqyosdagi ilovalarni qo'llab-quvvatlash: TypeScript-dagi sinflar, interfeyslar, generiklar va nomlar bo'shliqlari kabi xususiyatlar modulli kodni loyihalashni osonlashtiradi va uni katta va murakkab ilovalar uchun juda mos keladi.

Yaxshilangan kodni o'qish imkoniyati: TypeScript-ning turdagi izohlari va ilg'or OOP xususiyatlari kodlar bazalariga aniqlik kiritadi va boshqa ishlab chiquvchilar tomonidan yozilgan kodni tushunish, disk raskadrovka va saqlashni osonlashtiradi.

Qattiq null tekshiruvlari: TypeScript qat'iy null tekshiruvlarini amalga oshiradi, bu kompilyatsiya paytida nol yoki noaniq qiymatlarni ushlashga yordam beradi, etishmayotgan yoki mavjud bo'lmagan ma'lumotlar bilan bog'liq ish vaqti xatolarini kamaytiradi.

6. Do TypeScript files need compilation?
(TypeScript fayllarini kompilyatsiya qilish kerakmi?)

Ha, TypeScript brauzerlar tomonidan talqin qilinishi mumkin emas. TypeScript-ni JavaScript-ga aylantirish uchun kompilyatsiya qilish kerak. Va kompilyatsiya qilish uchun sizga TypeScript kompilyatori kerak. TypeScript JavaScript-ning barcha xususiyatlari va funksiyalariga ega, ba'zi qo'shimcha funktsiyalar mavjud. Bu ishlab chiquvchilar tajribasini yaxshilaydi, turdagi taxalluslar, mavhum sinflar, kortejlar, generiklar va boshqalar kabi xususiyatlarni taqdim etadi va ishlab chiquvchilarga o'z loyihalariga turdagi xavfsizlikni qo'shish imkonini beradi.

7. List some benefits of TypeScript?
(TypeScript ning ba'zi afzalliklarini sanab o'ting?)

TypeScript ishlab chiqish jarayonini yaxshilaydigan, kod sifatini yaxshilaydigan va hamkorlikni soddalashtiradigan bir qancha afzalliklarni taklif etadi. Ushbu imtiyozlardan ba'zilari:

Statik yozish: TypeScript JavaScript-ga statik yozishni qo'shadi, bu esa ishlash vaqti o'rniga kompilyatsiya vaqtida turga bog'liq xatolarni ushlaydi. Bu ishlab chiquvchilarga muammolarni ishlab chiqish jarayonining boshida aniqlash va tuzatish, xatolarni kamaytirish va umumiy kod sifatini yaxshilash imkonini beradi.

Kodning barqarorligi: TypeScript-ning statik turlari, interfeyslari va boshqa OOP xususiyatlari kodni yaxshiroq o'qish va saqlab turishga yordam beradi, bu esa ishlab chiquvchilarga umumiy kod bazalarini tushunish va ishlashni osonlashtiradi.

Yaxshiroq asboblar va muharrirni qo'llab-quvvatlash: TypeScript mashhur IDElar bilan mukammal integratsiyani ta'minlaydi, natijada rivojlangan avtoto'ldirish, kod navigatsiyasi va refaktoring vositalari. Bu rivojlanish tajribasini yaxshilaydi va samaradorlikni oshiradi.

Keng miqyosli ilovalarni qo'llab-quvvatlash: TypeScript-ning generiklar, nomlar maydoni va modullar kabi xususiyatlari modulli va kengaytiriladigan kodni yaratishga yordam beradi va bu uni katta va murakkab ilovalar uchun ideal tanlovga aylantiradi.

JavaScript ekotizimining mosligi: TypeScript JavaScript kutubxonalari, ramkalari va vositalari bilan toʻliq mos keladi, bu esa mavjud ishlab chiqish ish oqimlariga uzluksiz integratsiyalashish imkonini beradi.

8. In TypeScript, can we call the base class constructor from the child class ?
(TypeScript-da biz asosiy sinf konstruktorini bolalar sinfidan chaqira olamizmi?)

Ha, TypeScript-da siz asosiy sinf konstruktorini bolalar sinfidan chaqirishingiz mumkin. Asosiy sinfni kengaytiradigan bolalar sinfini yaratganingizda, ota-sinf konstruktorini chaqirish uchun bolalar sinfi konstruktoridagi super() funksiyasidan foydalanishingiz mumkin.

9. What is the difference between TypeScript and a statically typed language?
(TypeScript va statik terilgan til o'rtasidagi farq nima?)

TypeScript ixtiyoriy ravishda statik tarzda yoziladi, ya'ni siz kompilyatorga o'zgaruvchining turini e'tiborsiz qoldirishni aytishingiz mumkin. Biz har qanday ma'lumotlar turidan foydalangan holda o'zgaruvchiga har qanday turdagi qiymatlarni belgilashimiz mumkin. Kompilyatsiya paytida TypeScript hech qanday xato tekshiruvini amalga oshirmaydi.

10. Is string interpolation possible in TypeScript?
(TypeScript-da string interpolatsiyasi mumkinmi?)

Ha, TypeScript-da satr interpolyatsiyasi mumkin va u shablon literallari yoki shablon satrlari sifatida ham tanilgan. Bu sizga bitta yoki qoʻsh tirnoq oʻrniga teskari belgilar (`) yordamida iboralarni satr harflari ichiga joylashtirish imkonini beradi. Oʻzgaruvchi yoki ifodani satrga kiritish uchun ${expression} sintaksisidan foydalaning. Bu xususiyat qatorlarni birlashtirishga murojaat qilmasdan, yanada o'qiladigan va ixcham satrlarni yaratishni osonlashtiradi.

11. How do the extensions .ts and .tsx differ in TypeScript?
(.ts va .tsx kengaytmalari TypeScript da qanday farq qiladi?)

12. Differentiate between Classes and Interfaces in TypeScript?
(TypeScript-dagi sinflar va interfeyslarni farqlay olasizmi?)

13. Explain the Interface in TypeScript?
(TypeScript-dagi interfeysni tushuntirib bering?)

TypeScript-da interfeys - bu ob'ekt yoki sinfning shakli, tuzilishi va shartnomasini uning haqiqiy funksionalligini amalga oshirmasdan aniqlash imkonini beruvchi asosiy tushuncha. Interfeyslar ob'ektga ega bo'lishi kerak bo'lgan xususiyatlar va ularning tegishli turlarini belgilash orqali maxsus turlarni aniqlash imkonini beradi va interfeysni amalga oshiradigan sinf ushbu spetsifikatsiyalarga rioya qilishi kerak. Interfeyslar, shuningdek, muayyan parametrlar va qaytish turlarini aniqlash uchun funktsiyalar bilan ishlatilishi mumkin.

Interfeyslar ixtiyoriy xususiyatlarga, faqat o'qishga mo'ljallangan xususiyatlarga va usul imzolariga ega bo'lishi mumkin, shuningdek, bir nechta interfeyslarni kengaytirish va amalga oshirishni qo'llab-quvvatlaydi.

14. Explain Decorators in TypeScript.
(TypeScript-da dekorativlarni tushuntiring.)

TypeScript-dagi dekorativlar metadata qo'shish yoki sinflar, usullar, xususiyatlar yoki parametrlarning xatti-harakatlarini o'zgartirish uchun ishlatiladigan deklarativ sintaksisning maxsus turidir. Ular har bir maqsadli elementni qo'lda o'zgartirmasdan kodingizning bir nechta qismlarida qayta foydalanish mumkin bo'lgan mantiq yoki xatti-harakatni qo'llashning qulay usulini ta'minlaydi. Dekoratorlar maqsadli elementni (masalan, sinf yoki xususiyat) argument sifatida qabul qiladigan va uning o'zgartirilgan versiyasini qaytaradigan yoki unda muayyan harakatlarni bajaradigan yuqori darajadagi funktsiyalar yordamida qurilgan.

15. When should you use interfaces or classes in TypeScript?
(TypeScript-da interfeys yoki sinflardan qachon foydalanish kerak?)

TypeScript-da interfeyslar ham, sinflar ham maxsus turlar va tuzilmalarni aniqlash uchun ishlatiladi. Biroq, siz o'zingizning maxsus talablaringiz asosida interfeyslar va sinflarni tanlashingiz kerak:

