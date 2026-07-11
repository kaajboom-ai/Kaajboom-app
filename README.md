# راهنمای راه‌اندازی کامل کاج‌بوم (از صفر، روی حساب جدید)

## مرحلهٔ ۱: ساخت پروژهٔ رایگان Firebase

۱. با فیلترشکن روشن برو به **console.firebase.google.com** و با جیمیلت وارد شو
۲. «Add project» → یک اسم بده (مثلاً kajboom) → Google Analytics را خاموش کن → Create project
۳. از منوی سمت چپ دنبال **Firestore** بگرد (زیر Build یا Databases & Storage) → **Create database**
۴. اگر گزینهٔ Edition آمد، **Standard** را انتخاب کن؛ یک Location نزدیک انتخاب کن (مثلاً eur3)
۵. توی Security Rules گزینهٔ **Start in test mode** را بزن → Enable
۶. برگرد به Project Overview → آیکون چرخ‌دنده ⚙️ کنارش → **Project settings** → پایین صفحه بخش **«Your apps»** → آیکون `</>` (وب) را بزن
۷. یک اسم بده → **Register app** (تیک Firebase Hosting را نزن)
۸. کدی که نشان می‌دهد را کامل کپی کن — مقادیر `apiKey`, `authDomain`, `projectId`, `storageBucket`, `messagingSenderId`, `appId` را لازم داری

## مرحلهٔ ۲: جای‌گذاری تنظیمات در فایل

۱. فایل `index.html` (که پیوست شده) را باز کن
۲. نزدیک بالای فایل دنبال `const firebaseConfig = {` بگرد
۳. مقادیر `"PASTE_HERE"` را با مقادیر واقعی که از Firebase کپی کردی جایگزین کن

## مرحلهٔ ۳: ساخت مخزن روی گیت‌هاب

۱. برو به **github.com** و با همین حساب جدید وارد شو
۲. علامت `+` بالای صفحه → **New repository**
۳. یک اسم بده (مثلاً `kajboom-app`) → گزینهٔ **Public** را انتخاب کن → **Create repository**
۴. از منوی «Add file» → **Upload files** → همهٔ فایل‌ها (`index.html`, `manifest.json`, `sw.js`, پوشهٔ `icons`) را بکش و رها کن → **Commit changes**
۵. از همان «Add file» → **Create new file** → اسمش را دقیقاً `.nojekyll` بگذار (نقطهٔ اولش یادت نرود) → خالی بگذار → Commit
   (این فایل لازم است وگرنه گیت‌هاب کد را با پردازش Jekyll خراب می‌کند)

## مرحلهٔ ۴: فعال‌سازی آدرس اینترنتی (GitHub Pages)

۱. توی مخزن، برو به تب **Settings** → از منوی چپ **Pages**
۲. زیر «Build and deployment»: Source = **Deploy from a branch**، Branch = **main**، فولدر = **/ (root)** → **Save**
۳. چند دقیقه صبر کن، بعد آدرس آماده می‌شود:
```
https://یوزرنیمت.github.io/kajboom-app/
```
۴. برای تست، همیشه اول توی یک پنجرهٔ **Incognito** بازش کن

## نکات خیلی مهم که قبلاً بهشان برخوردیم

- **فیلترشکن باید همیشه روشن باشد** (هم روی گوشی، هم روی لپ‌تاپ) چون Firebase یک سرویس گوگل است
- بعد از هر تغییر در فایل‌ها، اگر سایت آپدیت نشد، یک‌بار روی گوشی/لپ‌تاپ: تنظیمات مرورگر → Site settings → آدرس سایت → **Clear & reset**
- اگر خطای «Deployment failed» دیدی، فقط دوباره امتحان کن یا Re-run بزن — معمولاً موقتی است

## نصب به‌عنوان اپ روی گوشی

بعد از باز شدن سایت، از منوی Chrome گزینهٔ **«Add to Home Screen»** را بزن — یک آیکون مثل اپ روی گوشی می‌نشیند.

## هوش مصنوعی (اختیاری — برای تب‌های رویدادها/توسعهٔ فردی حذف شده، نیازی نیست)

فعلاً این ویژگی از اپ برداشته شده و رویدادها/کتاب‌ها کاملاً دستی ثبت می‌شوند.
