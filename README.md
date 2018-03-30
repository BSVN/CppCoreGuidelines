<p align="center">
بسم الله الرحمن الرحیم



[![C++ Core Guidelines](cpp_core_guidelines_logo_text.png)](http://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines)

>"Within C++ is a smaller, simpler, safer language struggling to get out."
>-- <cite>Bjarne Stroustrup</cite>

<div dir="rtl">

[رهنمودهای بنیادین سی پلاس پلاس](CppCoreGuidelines-Persian.md) با تلاش بزرگان این زبان از جمله سازنده اصلی تولید و نگهداری می گردد و در اینجا ما یک نسخه کوچک تر شده و فارسی از آن را ارایه می کینم که برای شرکت های که با این زبان کار می کنند ان شا الله مفید واقع شود

## شروع کنید

دو مستند وجود دارد یکی نسخه مرجع که در [CppCoreGuidelines](CppCoreGuidelines.md) قابل خواندن است و نسخه‌ای است که بر اساس آن مستند فارسی توسعه داده شده است، نسخه دوم نسخه فارسی می‌باشد که در [رهنمود‌های بنیادین سی پلاس پلاس](CppCoreGuidelines-Persian.md)  قابل خواندن است و آخرین نکات تایید شده برای رعایت شدن در شرکت‌ها در آن آمده است

[یک نسخه مناسب برای مرورگر](http://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines) به زبان انگلیسی نیز وجود دارد که به صورت دستی بروزرسانی می‌گردد و معمولا از آخرین تغییرات عقب تر است

این مستند ان‌شا‌الله به طور مدام در [مخزن مرجع بروزرسانی](https://github.com/isocpp/CppCoreGuidelines) می‌گردد و به تبع آن ان‌شا‌الله در اینجا نیز تغییرات به صورت دوره‌ای بروزرسانی می‌گردد و بعد از بررسی‌های لازم مستند یک نسخه جدید از مستند با افزایش شماره نسخه منتشر می‌گردد. برای دیدن انتشار‌های فعلی مستند می‌تواند به [بخش انتشار‌ها](https://github.com/BSVN/CppCoreGuidelines/releases) مراجعه کنید.

بسیاری از رهنمود‌ها از کتابخانه پشتیبانی رهنمود[1] استفاده می‌کنند. یک پیاده‌سازی اصلی از این کتابخانه در [GSL: Guideline Support Library](https://github.com/Microsoft/GSL) قابل دسترسی می‌باشد.

## پیش ضمینه و حوزه

این رهنمود‌ها به توسعه دهندگان کمک می‌کند که بتوانند از سی پلاس پلاس جدید کارا تر استفاده کنند. منظور از جدید نگارش‌های ۱۱ و ۱۴ و ۱۷ از این زبان می‌باشد.

رهنمود‌های مطرح شده در این مستند بیشتر ناظر بر مسایل و موضوعات بالادستی می‌باشند مانند واسط‌های برنامه نویسانه، مدیریت منابع، مدیریت حافظه و همروندی. قوانین گفته شده در مستند تاثیراتی بر معماری و طراحی کتابخانه‌ها و برنامه‌ها خواهند داشت و باعث خواهند شد که کتابخانه‌های گویا تر، بدون نشت حافظه و دارای خطاهای منطقی کمتری ایجاد گردد. و تمام این نکات با پایین ترین هزینه و در نتیجه با کارایی بسیار بال ان‌شا‌اللها قابل حصول خواهد بود.

این مستند فعلا توجه کمتری به مسایل سطح پایین تر مانند نام‌گذاری و یا قالب بندی کد دارد ولی هر مساله‌ای به توسعه دهنده برای بهتر کد زدن کمک کند شامل حوزه این سند می‌شود.

مجموعه قوانین اولیه بیشتر ناظر بر ایمنی در جنبه‌های متفاوت در عین سادگی هستند. همچنین قوانین سعی شده است بسیار سخت و سفت بیان بشوند و بعدا با اضافه کردن تبصره‌ها برای نیازمندی‌های متفاوت شرکت‌ها و پروژه‌ها بهتر تطبیق پیدا کنند. همچنین تعداد قوانین هنوز بسیار کم است و بسیاری از جنبه‌ها را پوشش نداده است که ان‌شا‌الله باید به مرور زمان بیشتر و جامع تر گردد.

بسیاری از قوانین ممکن است که با تجربیات شما و نحوه کاری شما تا به امروز همخوانی نداشته باشد، این یک امر طبیعی است و در واقع اگر این قوانین هیچ تغییری در سبک کد زدن شما و سبک کد نوشته شده در پروژه ایجاد نمی‌کرد، نشان از عدم کارکرد این قوانین بود. البته ما علاقمند هستیم که تجربیات شما و نظرات شما را در مورد اجرای این قوانین و اثراتی که می‌گذارد جویا شویم، و از شما خواهش می‌کنم که در قالب Issue ما را از پیشنهادات و انتقادات خود مطلع سازید.
همچنین هرگونه مثال جدید و بهتری برای طرز استفاده قوانین و یا ارزیابی از فایده‌مندی هر کدام از قوانین بسیار خوشحال کننده و مایه مباهات است.

بعضی از قوانین ممکن است بنظر بعضی از افراد بدیهی بنظر برسد. ولی لازم به ذکر است که چون این قوانین برای افرادی با تجربه‌های متفاوت و دانش متفاوت از زبان و برنامه‌نویسی نگاشته شده است این امر اجتناب ناپذیر است.

اکثر قوانین سعی شده است که به نحوی طراحی گردند که با هزینه معقولی توسط ابزار‌های تحلیل کد قابل بررسی باشند، و از ابزار‌های تحلیل کد انتظار می‌رود که هر قانونی که زیر پا گذاشته شد به آن قانون اشاره کند. به همین منظور این انتظار که در وهله اول تمامی قوانین توسط توسعه دهندگان از حفظ گردد وجود ندارد و باید با کد زدن و تمرین ان‌شا‌الله این اتفاق بیفتد.

این قوانین باید به صورت تدریجی به کد‌های منبع قدیمی عرضه گردند و این کد‌ها را با قوانین سازگار ساخت. ولی کد‌های جدید باید بر مبنای این قوانین نوشته شوند و در این کد‌ها تخطی از این قوانین مشاهده نگردد. همچنین بهتر می‌باشد که ابزار‌های ساخت کد و همگردان‌ها از این قوانین به نحوی پشتیبانی کنند.

## مشارکت و مجوز

از هرگونه نظر و پیشنهاد به منظور بهبود سند فارسی و انگلیسی بسیار استقبال می‌گردد، فقط نکته لازم به ذکر این است که با توجه به توسعه نسخه مرجع در محل دیگر که در بالا گفته شده است نکات و پیشنهادات مربوط به سند مرجع را در آن مکان بیان بفرمایید و نکات و پیشنهادات و حتی توسعه سند فارسی را در همین پروژه دنبال کنید.

برای توضیحات بیشتر می‌توانید به نحوه [مشارکت](./CONTRIBUTING.md)  و [مجوز](./LICENSE) مراجعه کنید.

[1]: GSL: Guideline Support Library
