  - فصل اول :clipboard:

  - قسمت اول [مفهوم-client-و-server](مفهوم-client-و-server)
  - قسمت دوم [وب-سرور-(web-server)-چیه؟](وب-سرور-(web-server)-چیه؟)
  - قسمت سوم [پایگاه-داده-(database)-چیه؟](پایگاه-داده-(database)-چیه؟)
  - قسمت چهارم [مفهوم-پروتکل-(protocol)](مفهوم-پروتکل-(protocol))
  - قسمت پنجم [آشنایی-با-پروتکل-ip-و-dns](آشنایی-با-پروتکل-ip-و-dns)
  - قسمت ششم [وب-چطور-کار-میکنه؟(how-the-web-works)](وب-چطور-کار-میکنه؟(how-the-web-works))
  - قسمت هفتم [مفهوم-پورت-(port)](مفهوم-پورت-(port))
  - قسمت هشتم [url-anatomy](url-anatomy)
    

---

فصل 7 - مفاهیم پایه وب (web core concepts)

> # مفهوم client  و server

میخوایم در مورد مفهوم کلی client , server  و هر کدوم چی هستند توضیح بدیم 
یه مثال تو دنیای وافعی بزنیم client  که بهش مشتری هم میگیم میشه سرویس گیرنده  یا ارسال کننده درخواست و اون رو یه فرد تصور کنیم و server  که میشه سرویس دهنده یا پاسخ به درخواست  که یه رستوران هست مثلا  خب این رستوران که سرور ما هست یه سری مشتری داره که بهش میگیم کلاینت این مشتریا میرن میشینن تو رستوران و درخواست میدن یه غذایی رو سرور که میشه رستوران به درخواست اونا پاسخ میده  و سرویس میده  به درخواست اون مشتریا  پس سرور یا همون رستوران به درخواست مشتریا رسیدگی میکنه و میبینه چه غذایی میخوان و بهشون سرویس میده به درخواستشون پاسخ رو ارسال میکنه  که اینجا پاسخ  میشه اون غذا 

`پس client درخواست ارسال میکنه  server یه درخواست ارسال شده از client پاسخ میده `
<div align="center">
  <img  src="./img/Client-server-model.svg.png">
</div>

<br/>
هلا توی دنیای وب client  میشه همون مرور گرهایی که ما بهاش وارد سایت های مختلف میشیم  و server میشه یه کامپیوتر قدرت مند همیشه روشن متصل به اینترنت هلا فرض کنین ما  تو مرور گرمون که میشه کلاینت سرچ میکنیم میخوایم وارد سایت گوگل بشیم وقتی ما ادرس رو میزنیم در واقع ما داریم یه درخواست میزنیم به سرور گوگل  اون کامپیوتر قدرت مند همیشه روشتن متصل به اینترنت  که گوگل روش میزبانی میشه  که بهش میگیم سرور هلا سرور میاد درخواستی که از کلاینت ارسال شده رو برسی میکنه و بهش جواب میده و اون فایل ها همه چیزی که نیاز هست تا صفحه گوگل رو ما ببینیم ارسال میکنه اون فایل هارو به سمت مرورگر ما مه کلاینت بود 
مثل اون مثال رستوران که رستوران همون سرور بود و مشتری میشد کلاینت که مشتری میاد تو رستوران و یه غذایی رو سفارش میده و رستوران متتاسب با اون درخواست اون غذایی که مشتری خواسته رو بهش میده .

---
> # وب سرور (web server) چیه؟

کفتیم که سرور میشد یه کامپیوتر همیشه روشتن قدرتمند متصل به اینترنت مثل کامپیوتر های ما رم داره spu داره و... و کلاینت میشد اون مرور گر ما که توش ادرس میزدیم و درخواست میزد به سرور و سرور پاسخ مناسب با اون درخواست رو بهش میداد اون فایلا و... هرچی که لازم هست تا اون وب سایت برای ما بالا بیاد و نمایش داده بشه پس server یک سخت افزاره یه قطعه ی  سخت افزاریه  اما web server  یک نرم افزاره  مثل فتوشاپ یا vs code اینا هم یک نرم افزار هستن که ما میاییم اینا رو رو لپ تاپ یا کامپیوترمون نصب میکنیم خب سرور هم یه کامپیوتره دیگه پس روی سرور هم نرم افزارهایی نصب میشه  ولی ما نمیاییم روی سرور فتوشاپ نصب کنیم میایم نرم افزاری روی سرور نصب میکنیم که بتونه به درخواست های client پاسخ بده یعنی درخواست هایی که از client میاد به سمت سرور رو پردازش کنه و پاسخ درست و متناسب رو به اون درخواست بده 

`پس فهمیدیم که web server یه نرم افزاره که روی سرور نصب میشه `
هلا چند تا نرم افزار وب سرور معروف داریم : Apache , Nginx , IIs , Litespeed
یه بار دیگه تاکیید میکنیم که وظیفه وب سرور که روی سرور نصب میشه پردازش و پاسخ دادن به درخواست های کلاینت است . سرور فقط یه کامپیوتر قدرتمند .... است که سخت افزاره و روش وب سرور هایی که نام بردیم نصب میشن.
گفتیم که client ارسال کننده درخواست است به اون درخواستی که کلاینت میفرسته سمت سرور request  میگیم  و به پاسخی که سرور میفرسته به سمت کلاینت بهش میگیم response 


<div align="center">
  <img  src="./img/request-response.PNG">
</div>

---

> # پایگاه داده (database) چیه؟

Database
میخوایم درمورد مفهوم Database یا پایگاه داده یاد بگیریم معدل فارسی Database میشه پایگاه داده یا بانک اطلاعاتی  یه نکته سعی کنیم که بیشتر رو خیلی تمرکز نکنیم رو معادل های فارسی ترجیع بدیم که به همون انگلیسیش عادت کنیم و همون انگلیسیشو یاد بگیریم این رو سعنی میکنم یه روتین شخصی خودم قرار بدم 

هلا دیتابیس چیه ؟ دیتابیس یه محلی هست برای ذخیره کردن و نگهداری از اطلاعات محل که اون دیتا اون اطلاعات نگهداری و ذخیره میشن 

🟢محلی برای ذخیره  کردن و نگهداری از اطلاعات

🟢مجموعه ای از اطلاعات که بصورت منظم دسته بندی شده اند

همونطور که مثلا کتابخانه محلی برای ذخیره کردن و نگهداری کتاب هاست و یا گلخانه محلی برای ذخیره و نگهداری گل های است 
دیتا بیس بصورت منظم مرتب و دسته بندی میشن صحبت از نظم و دسته بندی هست یعنی اطلاعات وب سایت ما توی دسته هایی که بهم مرتبت هستن و جدا از هم  تو دسته های مختلف نگهداری میشن 


فرض کنین ما یه وب سایت فروشگاهی میخوایم بزنیم وب سایت ما یه سری کاربر user داره کاربرای ما یه سری اطلاعاتی دارن مثل اینکه ما موقع ثبت نام ازشون نام و... میگیریم که اینا میتونن بیان تو یه دسته یا این کاربرا میتونن بیان و کامنت بزارن زیر محصولات و ما میاییم کل کانتا رو تو یه دسته بندی قرار میدیم  توی سایتمون ما قطعا یه سری محصولاتی داریم سایت فروشکاهی داریم دیگه خب محصولاتی هم داریم که اون اطلاعات مربوط به محصولات رو هم میزاریم تو یه دست بندی که قیمتش چنده ایا موجودی داره یا نه و...  و توسایتمون ممکنه مقالاتی داشته باشیم فرضن درمورد این محصولات مقاله ای هم بنویسم  مثلا موبایل هستن هالا ممکنه یه سری مقالات درمورد تکنولوژی های روز موبایل و... بنویسیم  و منتشر کنیم 


<div align="center">
  <img  src="./img/databaseModel.PNG">
</div>

`پس فهمیدیم که دیتا بیس چیزی نیست جز یک محلی که تمامی اطلاعات سایت ما داخل اون ذخیره و نگهداری میشن  و بصورت منظم و دسته بندی شده`

هلا یه سوال ممکنه پیش بیاد چرا ما بیاد اطلاعات رو بصورت دسته بندی و منظم انجام بدیم چه الزامی به اینکار هست؟؟
یه مثال بزنیم فرض کنین ما یه کتاب خانه داریم که تو این کتاب خانه هیج نظمی نیست و کل کتاب ها همه شون بهم ریخته هستن این چند هزار کتاب هلا یه نفر میخواد بیاد یه کتاب از شما درخواست کنه پیدا کردن اون کتاب چقدر سخته وقتی مظم و دسته بندی وجود نداره معلوم نیست کتابای تاریخی و فلسفی کجان و... توی سایت هم اینطوریه اگه ما دسته بندی نکنیم اطلاعات سایت رو کارمون خیلی بد میشه پس دقیقن کاری که دیتا بیس میکنه مثل دسته بندی قفسه کتاب خانه هست تو کتابخانه مییایم دسته بندی میکنیم که مثلا این قفسه برای کتاب های تاریخیه این برای فلسفیه این برای ... هست و اینطوری خیلی راحتر میتونیم مدیریت کنیم کتاب هاییی که میخوایم 
توی سایت هم اطلاعات کاربرای سایت همه میان دسته بندی میشن


جدول اطلاعات کاربران
| آدی      |نام |  جنسیت |تاریخ تولد |    یوزرنیم |   پسورد |
| ----------- | ----------- | -----------| ----------- | ----------- | ----------- |
| 1   |  میلاد       |  مذکر          |   75/11/2          |     miladb20        |    miladavbs         |
| 2   | الهه           |   مونث          |      ...       |       ...       |      ...      |
| 3   | مهران          |   مذکر          |     ...        |      ...       |     ...        |


اطلاعات کامت ها هم به همین صورت جدا بصورت دسته یندی و منظم

جدول اطلاعات کامنت ها

| آیدی      | یوزر آدی | کامنت      | تاریخ ثبت |
| ----------- | ----------- | ----------- | ----------- |
| 1      | 1       |      متن...       |      1403/02/12       |
| 2   | 1        |    متن ...         |     ...        |
| 3   | 5        |    متن ...         |     ...        |


مشخص هست دقیق که کاربری با این ایدی تو این تاریخ چه کامنتی رو ثبت کرده 
هلا دوباره برای مقالات و ... هم جدول هایی داریم مثل این 
---

> # مفهوم پروتکل (protocol)



میخوایم با مفهوم protocol | پروتکل  اشنا شیم خب با یه مثال خیلی ساده شروع کنیم اگه خاطرتون باشه تو دوران کرونا خیلی کلمه پروتکل های بهداشتی رو میشنیدیم هلا این پروتکل های بهداشتی چی بودن؟ 

پروتکل های بهداشتی :
🟢استفاده از ماسک
🟢رعایت فاصله مناسب
🟢دست ندادن
🟢و...

`مجموعه ای از قوانین و مقررات برای برقراری برای ارتباط بین انسان ها`

پس پروتوکل چیزی نیست جر یه سری قوانین و چهارچوب ها هالا توی دنیای وب 
`مجموعه ای از قوانین برای برقراری بین دو کامپیوتر`

هلا این دوتا کامپیوتر که گفتیم لزومن دقیقن دوتا کامپیوتر نیستن ممکنه یه لپ تاپ با یه سرور مثلا یه تبلت با یه سرور همونطور که گفتیم ما که نقش کلاینت رو داریم تو مرورگر ادرس یه وب سایتی رو میزنیم از کلاینت به سرور اون سایت یه reqest میره و سرور متناسب با اون request  براش یه response یا پاسخ رو به client میفرسته که این رویداد تحت قوانین و مقراراتی تحت یه چهارچوبی ارسال و دریافت میشه که بهش میگیم protocol که تو وب http یا https است انواع مختلف پروتکل ها رو داریم که با چند تا معروفشون اشنا میشیم



<div align="center">
  <img  src="./img/protocols.png">
</div>

---


> # آشنایی با پروتکل ip و dns

توی قسمت قبل با مفهوم protocol آشنا شدیم  گفتیم که پروتکل چیزی نیست جز مجموعه ای از قوانین ومقررات  و چهارچوب ها که دوتا کامپیوتر برای برقراری ارتباط باهم دیگه ازش استفاده میکنند دوتا از پروتکل هایی که داشتیم ip , dns بود که تو این قسمت برسیش میکنیم چون بهم دیگه ربط هم دارن و باهم مرتبط هستند 

(ip) internet prorocol 
هر دستگاه متصل به اینترنت یه ip مخصوص داره میتونیم آی پی رو به شماره ملی تشبیه کنیم 
یعنی فقط اون ip مخصوص اون دستگاه اینترنتی هست دقیقن مثل شماره ملی هر شخص شما نمیتونین دونفر رو پیدا کنین که شماره ملی مثل هم داشته باشن دقیق  

🟢google.com    142.251.46.206
🟢w3schools.com    13.248.240.135
🟢aparat.com    185.147.178.11

هر دامنه یه ip مختص به خودشو داره در واقع هر سایت رو یه سرور هست دیگه و اون سرور هم چیزی نیست جز یه کامپیوتر قدرت مند همیشه روشن همیشه متصل به اینترنت هست دیگه  اینجام گفتیم که هر دستگاه متصل به اینترنت یه ای پی داره پس اون سرور هم که متصل به اینترنت هست یه ای پی داره 
هلا مثلا سرور google.com   ای پی اون اینه 142.251.46.206 یعنی اگه ما بجای google.com  بیاییم شماره ip  اون سایت گوکل رو داخل مرورگر مون وارد کنیم وارد خود وب سایت گوگل میشه 

`پس متوجه شدیم که هر وب ساتی یه ip منحصر به فرد داره  و این  ip  از چهار بخش تشکیل شده  که از 0 تا 255 میتونه باشه  و توسط نقطه از هم دیگه جدا میشن `

البته دو نوع ای پی داریم یک ای پی ورژن 4 که همینه که توضیح دادیم و یکی ورژن 6 که نیاز نیست درموردش اینجا توضیح بدیم اگه خواستین میتونین درموردش مطلالعه کینن ولی کلیت مفهوم ip اینه 

خب هلا بریم سراغ Dns

Domain Name System <- DNS
پروتکلی که وضیفه تبدیل نام دامنه به ip و بلعکس رو برعهده داره 
🟢google.com  ->    142.251.46.206
🟢aparat.com   ->   185.147.178.11

dns  یه دونه دیگه از پروتکل های مهم  وب است  که بخواییم به فارسی ترجمش کنیم میشه سیستم نام دامنه ولی دنبال معنی فارسیش نریم چون ممکنه یکم بهاش برنخوره با کارش و معنی اصلیشو ازدست میده 
وضیفش تبدیل نام دامنه یا domain به ip و برعکس تبدیل ip به domain رو بعهده داره 

ما به آدرس سایت میگیم Domain یا دامنه 
چون زدن اون ip رو هر بار که بخواییم بزنیم سخته  با استفاده از پروتکل DNS  وقتی ما نام دامنه رو میزنیم اون خودش تبدیل به ip  میکنه و تو سمت سرور هم برعکس انجام میده برای سرور 
مثل دفترجه تلفن هست شما اگه بخوایید شماره هر کسی مثلا 1000 تا مخاطب دارین بجای اینکه شماره هر شخص رو دونه دونه حفظ کنین یا بنویسن رو برگه اسمش رو ذخیره میکنین رو هر بار که رو اسمش بزنین شماره رو میگیره براتون تلفنتون و اینکار خیلی راحت تره به این DNS دفترجه تلفن اسنترنت هم میگن به این اسم  هم معروفه

| Domain      | Ip Address |
| ----------- | ----------- |
| google.com      | 142.251.46.206       |
| w3schools.com   | 13.248.240.135       |
| aparat.com   | 185.147.178.11          |

بخاطر سپردن و وارد کردن نام دامنه سایت خیلی راحت تره تا ای پی ادرسش رو حفظ کنیم.

---

> # وب چطور کار میکنه؟(how the web works)

میخوایم برسی کنیم که دقیقن از لحضه ای که ما ادرس یک وب سایتی رو وارد میکنیم داخل مرورگر مون چه اتفاقاتی میفته و یه جورایی هم مرور کنیم چیزایی که تا الان یاد گرفتیم .

فرض کنین ما داخل مرورگر ادرس google.com رو وارد میکنیم اینجا مرور گر میشه client پس باید یه درسخاست بفرستیم به سرور google.com اما قبلش باید Ip گوگل رو پیدا کنیم اگه خاطرتون باشه گفتیم DNS کارش چیه ؟ تبدیل Domain سابت به Ip و برعکث 

<div align="center">
  <img  src="./img/webWork.PNG">
</div>

DNS Server Server Ip گوگل رو به ما میده  هلا که Ip گوگل رو داریم  هلا یه درخواست از سمت مرورگر ارسال میشه به سمت سرور اون سایت هلا اینجا ممکنه که نیاز باشه
یه سری اطلاعات هم از سرور گرفته بشه اگه نیاز به اینکار باشه یه ارتباطی هم بین سرور و دیتا بیس صورت میگیره و چیزهایی که لازم هست رو سرور از دیتابیس میگیره  و در نهایت سرور response یا پاسخی که باید آماده کنه رو اماده میکنه و میفرسته به سمت client و سایت روی مرور گر ما نمایش داده میشه هلا اون پاسخ یه response که میگیم همون فایل های html , css , js  ممکنه عکس باشه یا... بستگی داره چه سایتی درخواست زدیم و کدوم صفحه هست و اون صفحه چه اطلاعاتی داره این میشه ساروکار کلی وب البته که جزیات بیشتری داره که ما واردش نشدیم و بخش های اصلیشو توضیح دادیم .

---

> # مفهوم پورت (port)

کلمه port به معنی  درگاه یا در هست. روی سرور نرم افزارهای مختلفی نصبه سرور چی بود؟ سرور یه کامپیوتر قدرت مند همیشه روشن متصل به انترنت هست خب این یه کامپیوتره دیگه مثل بقیه کامپیوترهای خودمون نرم افزار های مختلفی روش نصبه 
<div align="center">
  <img  src="./img/port-1.PNG">
</div>

نرم افزارهایی که مدیریت میکنن درخواست هایی که به سمت سرور ارسال میشه مثل web server ها که انواع شو داریم  دیگه چه چیزهای نصب هست روی سرور مثل نرم افزارهای Database management نرم افزار هایی که وضیفه دارن دیتابیس رو مدیریت کنند و دیگه مثل زبان برنامه نویسی مثلا وقتی ما میخوایم روی یه سرور کد js اجرا کنیم باید روی اون سرور node نصب باشه دقیقن مثل کامپیوتر خودمون که اومدیم نودجی اس رو نصب کردیم و هلا نرم افزار های دیگه .

هلا وقتی یه درخواستی میاد به سمت سرور سرور از جا باید بفهمه که اون درخواست رو باید کدوم نرم افزار مدیریت کنه؟ درخواستو باید بده به webserver یا databaseManagement یا... چطور اینو متوجه میشه؟ از روی port یا درگاه یه مثال هم میرنیم برای فهم بیشتر
فرض کنین شما به یه بانک مراجعه میکنین توی اون بانک باجه های مختلفی وجود داره که هر کدومش مختص به یه کاری هستن

<div align="center">
  <img  src="./img/port-2.PNG">
</div>
مثلا اون باجه که بالاش نوشته وام مخصوص اینه که اگه شما میخواید وام بگیرین باید به اون مراجعه کنین و... هلا ما میتونیم پورت رو به همینا تشبیه کنیم هلا ` پورت یه عدد هست` توی باجه های بانکی بالاش اسم باجه هست مثلا وام یا افتتاح حساب و... اما مال پورت یه عدد هست یعنی به هر پورت یه عدد نسبت داده میشه `شماره پورت ها میتونه بین 0 تا 6535 پس تا الان فهمیدیم که port یه درگاه هست یه در هست که اطلاعات از این درها وارد و خارج میشن` 

میخوایم مفهوم پورت هم وارد شبکه وب کنیم که چطوریه چیکارا میکنه برای درک بیشتر وقتی که ما ادرس یک وبسایتی رو وارد میکنیم توی مرورگر چه اتفاقی میفته و مفهوم پورت رو هم واردش کنیم 

<div align="center">
  <img  src="./img/port-3.PNG">
</div>

port 443 , 80 مخصوص به webServer هستن
گفتیم که پورت یه عدد هست مثل باجه های بانکی هلا دوتا پورت داریم پورت های بیشفرض 80 و 443 این دوتا عدد این دوتا پورت مخصوص درگاه webserver هستن یعنی اگه درخواستی بیاد  به این پورت 80 یا 443  رو اینا باشه وب سروری که روی سرور ما نصب هست وضیفه داره که به اون درخواست پاسخ بده 

ما وقتی توی مرورگر google.com رو وارد میکنیم درواقع اینطوریه google.com:443 بعد ادرس دامنه یه دونقطه قرار میگیره و بعد هم شماره پورت اما مرورگر خودش بصورت پیشفرض اینو تشخیص میده و نیاز نیست ما بیاییم این :443  رو بنویسیم اما چیزی که درواقع اتفاق میفته اینه که بهمراه https پورتی که اخر ادرس هست و میزاره خود مرورگر 443 هست .

خب یه باردیگه مرور کنیم ما ادرس google.com رو وارد میکنیم یه درخواست میره سمت DNS سرور و ای پی گوگل رو میگیره و یه reqest  از cleint  میره سمت سرور وب سایت گوگل هلا از روی این پورت 443  میفهمه که باید این درخواست رو webServer مدیریت کنه `پس از روی شماره پورت میفهمیم که کدوم نرم افزار باید این درخواست رو مدیریت کنه`  دقیفن مثلا باجه های بانک طرف از روی اسم باجه میفهمه که باید برای درخواست خودش به کردوم باجه مراجعه کنه. درخواست هایی هم که به سرور ارسال میشن سرور از روی شماره پورتشون میفهمه که باید کدوم نرم افزاری که روی سرور نصب هست توسط کدوم باید مدیریت بشن

اگه ما خودمون هم تو مرورگر سرچ کنیم https://www.google.com:443 باز هم سایت گوگل باز میشه چه بنویسم چه ننویسیم ولی درکل خود مرورگر خودش تشخیص میده و مینویسه اخر ادرس

مثلا پورت 3306 مربوط به نرم افزار mySql دیتابیس هست  یا پورت 20 و 21 مربوط به ftp هست ftpچیه یه پروتوکل هست برای انتفال فایل بین کلاینت و سرور  
اگه protocol ادرسمون http باشه پورت اون میشه 80 و اگه https باشه میشه 443
---

> # url anatomy
url چیه؟ ما به یه آدرس اینترنتی میگیم url
همون چیزی که ما تو اینترنت مینویسیم و دنبالش هستیم بهش میگیم url کلمه anatomy هم بهش میگیم کالبدشکافی تشریح و تجزیه هست میخوایم بصورت کلی ببینیم یه ادرس اینترنتی از چه بخش هایی تشکیل شده البته اینو بگیم درحد اطلاعات فعلیمون داریم یه ادرس اینترنتی بخش هاشو برسی میکنیم بصور کلی هست نه با تمام جزییات 


<div align="center">
  <img  src="./img/urlAnatomy.PNG">
</div>
برای اطلاعات بیشتر و جزییات بیشتر میتونیم تو مرورگر اینا رو سرچ کنیم part of url یا anatomy url که عکسها و مقالاتشونو میتونیم بیشتر بخونیم یه نکته ممکنه تو سایت های مختلف اسم هایی دیگه ای هم رو این بخش هایی که داخل عکس بود بزارن  مثلا به اون protol بگن scheme البته اونا خیلی با جزییات بیشتر توضیح دادن بخش های مختلف یه url رو .
---
