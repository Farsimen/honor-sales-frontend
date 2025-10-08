# راهنمای دیپلوی فرانت‌اند روی Cloudflare Pages

## گام 1: اتصال به GitHub

1. وارد داشبورد کلادفلر شو
2. برو به **Workers & Pages**
3. کلیک **Create Application**
4. انتخاب **Pages**
5. **Connect to Git**

## گام 2: تنظیم پروژه

- **Repository:** `Farsimen/honor-sales-frontend`
- **Project name:** `honor-sales-frontend`
- **Production branch:** `main`
- **Build command:** خالی بگذار (چون static HTML است)
- **Build output directory:** خالی بگذار
- **Root directory:** خالی بگذار

## گام 3: تنظیم Worker URL

بعد از دیپلوی Worker (از پروژه honor-sales-app)، آدرس Worker را در فایل `index.html` به‌روزرسانی کن:

```javascript
const WORKER_BASE_URL = 'https://honor-sales-worker.YOUR_SUBDOMAIN.workers.dev';
```

## گام 4: دیپلوی

کلیک **Save and Deploy**

## گام 5: تنظیم Custom Domain (اختیاری)

اگر دامین شخصی داری:

1. در تنظیمات Pages
2. **Custom domains**
3. **Set up a custom domain**
4. دامین موردنظر را وارد کن

## تست نهایی

بعد از دیپلوی:
- در مرورگر به آدرس Pages برو
- فرم ثبت فروش را تست کن
- دکمه‌های مشاهده داده‌ها و دانلود CSV را آزمایش کن

## لینک‌های مهم

- Frontend: `https://honor-sales-frontend.pages.dev`
- Worker API: `https://honor-sales-worker.YOUR_SUBDOMAIN.workers.dev`
- GitHub Frontend: https://github.com/Farsimen/honor-sales-frontend
- GitHub Backend: https://github.com/Farsimen/honor-sales-app