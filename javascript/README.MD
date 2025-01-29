1. Javascriptda qanday ma'lumotlar turlari mavjud?

JavaScript o'zgaruvchisining turini bilish uchun typeof operatoridan foydalanishimiz mumkin.

1 Primitiv tiplar

String - u bir qator belgilarni ifodalaydi va tirnoq bilan yoziladi. Satr bitta yoki ikkita tirnoq yordamida ifodalanishi mumkin.

Raqam - Bu raqamni ifodalaydi va o'nli yoki o'nli kasrlarsiz yozilishi mumkin.

BigInt - Ushbu ma'lumotlar turi Raqamli ma'lumotlar turi chegarasidan yuqori bo'lgan raqamlarni saqlash uchun ishlatiladi. U katta butun sonlarni saqlashi mumkin va butun son harfiga “n” qoʻshish orqali ifodalanadi.

Mantiqiy - Bu mantiqiy ob'ektni ifodalaydi va faqat ikkita qiymatga ega bo'lishi mumkin: rost yoki noto'g'ri. Booleanlar odatda shartli sinov uchun ishlatiladi.

Aniqlanmagan - o'zgaruvchi e'lon qilingan, lekin tayinlanmagan bo'lsa, u undefined qiymatiga ega va uning turi ham aniqlanmagan.

Null - u mavjud bo'lmagan yoki noto'g'ri qiymatni ifodalaydi.

Symbol - Bu javascriptning ES6 versiyasida kiritilgan yangi ma'lumotlar turi. U anonim va noyob qiymatni saqlash uchun ishlatiladi.

2 Primitiv bo'lmagan turlar

Primitiv ma'lumotlar turlari faqat bitta qiymatni saqlashi mumkin. Bir nechta va murakkab qiymatlarni saqlash uchun primitiv bo'lmagan ma'lumotlar turlari qo'llaniladi.

Ob'ekt - ma'lumotlar to'plamini saqlash uchun ishlatiladi.

2. Javascriptda Hoistingni tushuntiring.

Yuk ko'tarish JavaScript-ning standart xatti-harakati bo'lib, unda barcha o'zgaruvchilar va funksiya deklaratsiyasi tepaga ko'chiriladi.

Bu shuni anglatadiki, o'zgaruvchilar va funktsiyalar qayerda e'lon qilinganidan qat'i nazar, ular qamrovning yuqori qismiga ko'chiriladi. Qamrov ham mahalliy, ham global bo'lishi mumkin.

3. Nima uchun javascriptda “debugger” so‘zini ishlatamiz?

Kodni disk raskadrovka qilish uchun brauzer uchun tuzatuvchi faollashtirilgan bo'lishi kerak. O'rnatilgan tuzatuvchilarni yoqish va o'chirish mumkin, bu esa foydalanuvchidan nosozliklar haqida xabar berishni talab qiladi. Kodning qolgan qismi disk raskadrovka paytida keyingi qatorga o'tishdan oldin bajarilishini to'xtatishi kerak.

4. “ == “ va “ === “ operatorlari orasidagi farq.

Ikkalasi ham taqqoslash operatorlari. Ikkala operator o'rtasidagi farq shundaki, "==" qiymatlarni solishtirish uchun ishlatiladi, " ===" esa ikkala qiymat va turlarni solishtirish uchun ishlatiladi.

5. Javascriptdagi var va let kalit so'zlari orasidagi farq.

Ba'zi farqlar 

1 Eng boshidan JavaScript dasturlashda "var" kalit so'zi ishlatilgan bo'lsa, "let" kalit so'zi 2015 yilda qo'shilgan.

2 "Var" kalit so'zi funksiya doirasiga ega. Funktsiyaning istalgan joyida var yordamida ko'rsatilgan o'zgaruvchiga kirish mumkin, lekin "let" da "let" kalit so'zi bilan e'lon qilingan o'zgaruvchining doirasi u e'lon qilingan blok bilan cheklangan. Block Scope bilan boshlaylik.

3 ECMAScript 2015 da let va const ko'tariladi, lekin ishga tushirilmaydi. O'zgaruvchini e'lon qilishdan oldin blokdagi o'zgaruvchiga havola qilish ReferenceErrorga olib keladi, chunki o'zgaruvchi blok boshlanganidan to deklaratsiyaga ishlov berilgunga qadar "vaqtinchalik o'lik zonada" bo'ladi.

6. Javascriptda Implicit Type Coercionni tushuntiring.

JavaScript-da yashirin turdagi majburlash - bu qiymatni bir ma'lumot turidan ikkinchisiga avtomatik ravishda o'zgartirish. Bu ifodaning operandlari har xil turdagi ma'lumotlarga ega bo'lganda sodir bo'ladi.

7. Javascript statik yoki dinamik terilgan tilmi?

JavaScript dinamik ravishda terilgan tildir. Dinamik tarzda terilgan tilda, o'zgaruvchining turi kompilyatsiya vaqtida tekshiriladigan statik tarzda yozilgan tildan farqli o'laroq, o'zgaruvchining turi ish vaqtida tekshiriladi.

Javascript erkin (dinamik) terilgan til bo'lgani uchun JSdagi o'zgaruvchilar hech qanday tur bilan bog'lanmaydi. O'zgaruvchi har qanday turdagi ma'lumotlarning qiymatini ushlab turishi mumkin.

8. JavaScript-da NaN xossasi nima?

NaN xususiyati "Raqam emas" qiymatini ifodalaydi. Bu qonuniy raqam bo'lmagan qiymatni bildiradi.

typeof of NaN raqamni qaytaradi .

Qiymat NaN ekanligini tekshirish uchun isNaN() funksiyasidan foydalanamiz,

9. Qiymat bo'yicha o'tgan va mos yozuvlar bo'yicha o'tganlarni tushuntiring.

JavaScript-da ibtidoiy ma'lumotlar turlari qiymat bo'yicha, noaniq ma'lumotlar turlari esa mos yozuvlar bo'yicha uzatiladi.

10. JavaScript-da darhol chaqiriladigan funksiya nima?

Darhol chaqiriladigan funktsiya (IIFE deb nomlanadi va IIFY deb talaffuz qilinadi) bu aniqlangandan so'ng darhol ishlaydigan funksiya.

11. Javascriptdagi qat'iy rejim va javascriptning qat'iy rejimi deganda nimani tushunasiz?

ECMAScript 5 da JavaScript Strict Mode deb nomlanuvchi yangi xususiyat “qattiq” operatsion muhitda kod yoki funksiya yozish imkonini beradi. Ko'pgina hollarda, bu til xatolarga yo'l qo'yishda "ayniqsa og'ir emas". "Qat'iy rejimda" esa barcha xatolar, shu jumladan jim xatolar ham tashlanadi. Natijada, disk raskadrovka ancha soddalashadi. Shunday qilib, dasturchining xato qilish ehtimoli kamayadi.

Javascriptdagi qat'iy rejimning xususiyatlari

1 Ikki nusxadagi argumentlar ishlab chiquvchilar tomonidan ruxsat etilmaydi.

2 Qattiq rejimda siz JavaScript kalit soʻzidan parametr yoki funksiya nomi sifatida foydalana olmaysiz.

3 "Use strict" kalit so'zi skript boshida qat'iy rejimni aniqlash uchun ishlatiladi. Qattiq rejim barcha brauzerlar tomonidan qo'llab-quvvatlanadi.

4 Muhandislarga "Qat'iy rejim"da global o'zgaruvchilar yaratishga ruxsat berilmaydi.

12. Javascriptda oliy tartibli funksiyalarni tushuntiring.

Boshqa funktsiyalarda yoki ularni argument sifatida qabul qilish yoki ularni qaytarish orqali ishlaydigan funksiyalar yuqori tartibli funktsiyalar deb ataladi. Yuqori darajadagi funktsiyalar javascriptda birinchi darajali fuqarolar

13. “Bu” kalit so‘zini tushuntiring.

“This” kalit so‘zi funksiya xossasi bo‘lgan obyektga ishora qiladi.

“This” kalit so‘zining qiymati har doim funksiyani chaqirayotgan obyektga bog‘liq bo‘ladi.

14. O'z-o'zini chaqiruvchi funksiyalar deganda nimani tushunasiz?

So'ralmagan holda, o'z-o'zini chaqiruvchi ifoda avtomatik ravishda chaqiriladi (boshlanadi). Agar funktsiya ifodasidan keyin () bo'lsa, u avtomatik ravishda bajariladi. Funktsiya deklaratsiyasini o'zi chaqirib bo'lmaydi.

Odatda, biz funktsiyani e'lon qilamiz va uni chaqiramiz, biroq, funksiya tasvirlanganda avtomatik ravishda ishga tushirish uchun anonim funktsiyalardan foydalanish mumkin va qayta chaqirilmaydi. Va bu turdagi funktsiyalar uchun hech qanday nom yo'q.

15. Call(), apply() va, bind() usullarini tushuntiring.

1 qo'ng'iroq ():

Bu javascriptda oldindan belgilangan usul.

Bu usul ega ob'ektini ko'rsatish orqali usulni (funktsiyani) chaqiradi.

call() usuli ob'ektga boshqa ob'ektning usulidan (funktsiyasidan) foydalanishga imkon beradi.

apply()

Qo'llash usuli call() usuliga o'xshaydi. Faqatgina farq shundaki,

call() usuli argumentlarni alohida oladi, application() usuli esa argumentlarni massiv sifatida oladi.

2 bog‘lash():

Ushbu usul yangi funktsiyani qaytaradi, bu erda "bu" kalit so'zining qiymati parametr sifatida taqdim etilgan egasi ob'ektiga bog'lanadi.

16. Javascriptdagi exec () va test () usullarining farqi nimada?

test () va exec () javascriptda ishlatiladigan RegExp ifoda usullaridir.

Biz exec () dan ma'lum bir naqsh uchun satrni qidiramiz va agar u topsa, to'g'ridan-to'g'ri naqshni qaytaradi; aks holda, u "bo'sh" natijani qaytaradi.

Muayyan naqsh uchun satrni topish uchun test () dan foydalanamiz . Berilgan matnni topishda u mantiqiy qiymatni "true" qaytaradi, aks holda "noto'g'ri" qiymatini qaytaradi

17. JavaScript-da karriing nima?

Currying - bu n argumentlar funksiyasini bir yoki bir nechta argumentlarning n funksiyasiga aylantirishning ilg'or usuli.

18. Tashqi JavaScript dan foydalanishning qanday afzalliklari bor?

Tashqi JavaScript bu kengaytmali alohida faylda yozilgan JavaScript kodi (skript). 

Tashqi javascriptning ba'zi afzalliklari

1 Bu veb-dizaynerlar va ishlab chiquvchilarga HTML va JavaScript fayllari ustida hamkorlik qilish imkonini beradi.

2 Biz kodni qayta ishlatishimiz mumkin.

3 Tashqi javascriptda kodni o'qish oson.

19. Scope va Scope Chainni javascriptda tushuntiring.

JSdagi qamrov o'zgaruvchilar va funktsiyalarning kodning turli qismlarida foydalanish imkoniyatini aniqlaydi.

Umuman olganda, qamrov bizga kodning ma'lum bir qismida qanday o'zgaruvchilar va funktsiyalarga kirishimiz yoki kira olmasligimiz haqida ma'lumot beradi.

JSda uch xil doiralar mavjud:

Global qamrov

Mahalliy yoki funksiya doirasi

Blok doirasi

Global qamrov: Global nomlar maydonida e'lon qilingan o'zgaruvchilar yoki funktsiyalar global qamrovga ega, ya'ni global miqyosga ega bo'lgan barcha o'zgaruvchilar va funktsiyalarga kodning istalgan joyidan kirish mumkin.

Funktsiya doirasi: Funktsiya ichida e'lon qilingan har qanday o'zgaruvchilar yoki funktsiyalar mahalliy/funktsiya doirasiga ega, ya'ni funktsiya ichida e'lon qilingan barcha o'zgaruvchilar va funktsiyalarga funktsiyadan tashqarida emas, balki uning ichidan kirish mumkin.

Blok doirasi: Blok doirasi let va const yordamida e'lon qilingan o'zgaruvchilar bilan bog'liq. var bilan e'lon qilingan o'zgaruvchilar blok doirasiga ega emas. Blok doirasi bizga { } blokida e'lon qilingan har qanday o'zgaruvchiga faqat shu blok ichida kirish mumkinligini va undan tashqarida kirish mumkin emasligini aytadi.

Scope Chain: JavaScript mexanizmi o'zgaruvchilarni topish uchun Scope-dan ham foydalanadi. Keling, buni misol yordamida tushunaylik:

20. JavaScript-dagi yopilishlarni tushuntiring.

Yopish - bu funksiyaning tashqi doirasida e'lon qilingan o'zgaruvchilar va funktsiyalarni eslab qolish qobiliyati.

Funktsiyaning o'zgaruvchini bajarilgandan keyin ham qo'shimcha ma'lumot olish uchun saqlash qobiliyati Yopish deb ataladi.

21. Javascriptning ba'zi afzalliklarini aytib o'ting.

Javascriptning afzalliklari juda ko'p. Ulardan ba'zilari 

1 Javascript mijoz tomonidan ham, server tomonida ham bajariladi. 
Siz o'rganishingiz va foydalanishingiz mumkin bo'lgan turli xil Frontend Frameworklar mavjud. Biroq, agar siz JavaScript-ni backendda ishlatmoqchi bo'lsangiz, NodeJS-ni o'rganishingiz kerak bo'ladi. Hozirda bu backendda ishlatilishi mumkin bo'lgan yagona JavaScript ramkasidir.

2 Javascript o'rganish uchun oddiy tildir.

3 Javascript tufayli veb-sahifalar endi ko'proq funksionallikka ega.

4 Yakuniy foydalanuvchi uchun Javascript juda tez.

22. Ob'ekt prototiplari nima?

Barcha javascript obyektlari prototipdan xossalarni meros qilib oladi. Masalan,

Sana obyektlari Date prototipidan xossalarni meros qilib oladi

Matematik obyektlar Math prototipidan xossalarni meros qilib oladi

Massiv obyektlari Array prototipidan xossalarni meros qilib oladi.

Zanjirning tepasida Object.prototype joylashgan. Har bir prototip Object.prototype dan xossa va usullarni meros qilib oladi.

Prototip - bu ob'ektning rejasi. Prototip, hozirgi ob'ektda xususiyatlar va usullar mavjud bo'lmasa ham, ob'ektda xususiyatlar va usullardan foydalanishga imkon beradi.

23. Qayta qo'ng'iroqlar nima?

Qayta qo'ng'iroq - bu boshqa funktsiya bajarilgandan keyin bajariladigan funktsiya. JavaScript-da funksiyalar birinchi darajali fuqarolar sifatida ko'rib chiqiladi, ular boshqa funktsiyaning argumenti sifatida ishlatilishi mumkin, boshqa funktsiya tomonidan qaytarilishi mumkin va ob'ektning mulki sifatida ishlatilishi mumkin.

Boshqa funktsiyaga argument sifatida ishlatiladigan funksiyalar qayta qo'ng'iroq qilish funktsiyalari deb ataladi.

24. Javascriptda qanday xatolar turlari mavjud?

Javascriptda ikki xil xatolik mavjud.

1 Sintaksis xatosi : Sintaksis xatolar - bu dasturning umuman bajarilmasligiga yoki yarim yo'lda ishlashni to'xtatishiga olib keladigan koddagi xatolar yoki imlo muammolari. Odatda xato xabarlari ham taqdim etiladi.

2 Mantiqiy xato : Sintaksis to'g'ri bo'lsa, lekin mantiq yoki dastur noto'g'ri bo'lsa, mulohaza yuritish xatolari yuzaga keladi. Bu holda dastur muammosiz ishlaydi. Biroq, chiqish natijalari noto'g'ri. Ba'zan ularni sintaktik muammolardan ko'ra tuzatish qiyinroq, chunki bu ilovalar mantiqiy nosozliklar uchun xato signallarini ko'rsatmaydi.

25. Memoizatsiya nima?

Memoizatsiya - bu keshlash shakli bo'lib, unda funktsiyaning qaytish qiymati uning parametrlari asosida keshlanadi. Agar ushbu funktsiyaning parametri o'zgartirilmasa, funktsiyaning keshlangan versiyasi qaytariladi.

26. Dasturlash tilida rekursiya nima?

Rekursiya - bu natijaga kelgunga qadar funktsiyaning o'zini qayta-qayta chaqirishi orqali operatsiyani takrorlash usuli.

27. Javascriptda konstruktor funksiyasidan qanday foydalaniladi?

Konstruktor funktsiyalari javascriptda ob'ektlar yaratish uchun ishlatiladi.

Konstruktor funksiyalaridan qachon foydalanamiz?

Agar biz o'xshash xususiyat va usullarga ega bo'lgan bir nechta ob'ektlarni yaratmoqchi bo'lsak, konstruktor funktsiyalaridan foydalaniladi.

28. DOM nima?

DOM hujjat ob'ekt modeli degan ma'noni anglatadi. DOM - bu HTML va XML hujjatlari uchun dasturlash interfeysi.

Brauzer HTML hujjatni ko'rsatishga harakat qilganda, u HTML hujjati asosida DOM deb nomlangan ob'ektni yaratadi. Ushbu DOM-dan foydalanib, biz HTML hujjatidagi turli elementlarni manipulyatsiya qilishimiz yoki o'zgartirishimiz mumkin.

29. Muayyan indeksdan belgini olish uchun qaysi usuldan foydalaniladi?

JavaScript qatorining charAt() funksiyasi berilgan indeksda char elementini topadi. Indeks raqami 0 dan boshlanadi va n-1 gacha davom etadi, Bu erda n - satr uzunligi. Indeks qiymati musbat, undan yuqori yoki satr uzunligi bilan bir xil bo'lishi kerak.

30. BOM deganda nimani tushunasiz?

Brauzer ob'ekt modeli BOM sifatida tanilgan. Bu foydalanuvchilarga brauzer bilan muloqot qilish imkonini beradi. Brauzerning boshlang'ich obyekti oynadir. Natijada, siz oynaning barcha funktsiyalarini to'g'ridan-to'g'ri yoki oynaga havola qilish orqali chaqirishingiz mumkin. Hujjat, tarix, ekran, navigator, joylashuv va boshqa atributlar oyna obyektida mavjud.

31. Mijoz tomoni va server tomoni JavaScript-ning farqi nimada?

Mijoz tomoni JavaScript ikki qismdan iborat, asosiy til va brauzerda JavaScript-ni bajarish uchun oldindan belgilangan ob'ektlar. Mijoz uchun JavaScript avtomatik ravishda HTML sahifalariga kiritiladi. Ishlash vaqtida brauzer ushbu skriptni tushunadi.

Server tomonidagi JavaScript, mijoz so'rovlariga javoban serverda JavaScript kodini bajarishni o'z ichiga oladi. U ushbu so'rovlarni ko'rib chiqadi va mijozga tegishli javobni etkazib beradi, bu brauzerda keyingi bajarilishi uchun mijoz tomonidagi JavaScript-ni o'z ichiga olishi mumkin.

