پرسش ها
1) پوشه‌ی.git  یک دایرکتوری مخفی است که در هر مخزن (repository) گیت ایجاد می‌شود و شامل تمام اطلاعات مربوط به پروژه و تاریخچه‌ی تغییرات آن است. اطلاعاتی که در این پوشه ذخیره می‌شود شامل موارد زیر است:
    1.	تاریخچه‌ی کامیت‌ها تمامی تغییرات و نسخه‌های مختلف فایل‌ها ذخیره می‌شود.
    2.	برنچ‌ها و تگ‌ها اطلاعات مربوط به برنچ‌ها (branches) و تگ‌ها (tags) پروژه.
    3.	متادیتا اطلاعات مربوط به تنظیمات مخزن، شامل پیکربندی‌ها و اطلاعات مربوط به ریموت‌ها (remotes).
    4.	ایندکس(Index) فایل‌هایی که برای کامیت بعدی آماده شده‌اند.
    5.	اشیاء (Objects)محتوای فایل‌ها و تغییرات آنها که به صورت باینری ذخیره می‌شود.
    برای ایجاد یک پوشه‌ی .git، کافیست به دایرکتوری پروژه بروید و دستور زیر را اجرا کنید:
    git init
    این دستور یک مخزن جدید گیت ایجاد می‌کند و پوشه‌ی .git را در دایرکتوری فعلی ایجاد می‌نماید.


3) 
    1. git fetch
    •	عملکرد: این دستور به شما اجازه می‌دهد تا تغییرات جدید از مخزن ریموت را به مخزن محلی خود دانلود کنید، بدون اینکه این تغییرات را به برنچ فعلی شما ادغام کند.
    •	استفاده: به‌خصوص زمانی که می‌خواهید ببینید چه تغییراتی در مخزن ریموت وجود دارد، بدون اینکه تغییرات جدید را بلافاصله در کد خود اعمال کنید.
    •	نتیجه: اطلاعات جدید در مورد برنچ‌های ریموت به محلی شما دانلود می‌شود، اما هیچ کدی تغییر نمی‌کند.
    2. git pull
    •	عملکرد: این دستور ترکیبی از fetch و merge است. ابتدا تغییرات جدید را از مخزن ریموت دانلود می‌کند (مانند fetch) و سپس آن تغییرات را به برنچ فعلی شما ادغام می‌کند.
    •	استفاده: زمانی که می‌خواهید آخرین تغییرات ریموت را به طور مستقیم به کد محلی خود اضافه کنید.
    •	نتیجه: برنچ فعلی شما به‌روز می‌شود و تغییرات جدید به آن ادغام می‌شود.
    3. git merge
    •	عملکرد: این دستور برای ادغام دو برنچ مختلف استفاده می‌شود. تغییرات یک برنچ (مانند برنچ ریموت) به برنچ فعلی ادغام می‌شود.
    •	استفاده: زمانی که می‌خواهید تغییرات یک برنچ را به برنچ دیگر (مانند ادغام یک ویژگی جدید به برنچ اصلی) اضافه کنید.
    •	نتیجه: یک کامیت جدید ایجاد می‌شود که نمایانگر ادغام دو برنچ است. این کامیت می‌تواند شامل ترکیبی از تغییرات دو برنچ باشد.
    4. git rebase
    •	عملکرد: این دستور برای ادغام تغییرات از یک برنچ به برنچ دیگر با تغییر تاریخچه استفاده می‌شود. در واقع، rebase تغییرات یک برنچ را بر اساس برنچ دیگری قرار می‌دهد.
    •	استفاده: برای حفظ تاریخچه‌ای تمیز و خطی از تغییرات، به‌خصوص در پروژه‌هایی که همکاری زیادی دارند.
    •	نتیجه: تاریخچه‌ی کامیت‌ها تغییر می‌کند و به‌جای ایجاد یک کامیت جدید برای ادغام، کامیت‌های جدید به‌طور مستقیم بر اساس برنچ مورد نظر قرار می‌گیرند.
    5. git cherry-pick
    •	عملکرد: این دستور به شما اجازه می‌دهد تا یک یا چند کامیت خاص را از یک برنچ به برنچ دیگر منتقل کنید.
    •	استفاده: زمانی که می‌خواهید یک تغییر خاص (کامیت) را بدون ادغام کامل برنچ، به برنچ فعلی اضافه کنید.
    •	نتیجه: کامیت‌های انتخابی به برنچ فعلی شما افزوده می‌شوند و این کامیت‌ها به عنوان کامیت‌های جدید در برنچ فعلی نمایش داده می‌شوند.
    خلاصه:
    •	fetch: دانلود تغییرات بدون ادغام.
    •	pull: دانلود و ادغام تغییرات.
    •	merge: ادغام دو برنچ با ایجاد یک کامیت جدید.
    •	rebase: ادغام با تغییر تاریخچه برای یک نمای خطی.
    •	cherry-pick: انتقال کامیت‌های خاص به برنچ دیگر.

