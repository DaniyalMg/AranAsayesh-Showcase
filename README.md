<div dir="rtl" style="text-align: right; line-height: 1.8;">

# 💳 AranAsayesh | پلتفرم کارت‌های تخفیف سازمانی

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue?style=for-the-badge&logo=python)](https://www.python.org/)
[![Django](https://img.shields.io/badge/Django-4.x-green?style=for-the-badge&logo=django)](https://www.djangoproject.com/)
[![DRF](https://img.shields.io/badge/DRF-REST%20API-orange?style=for-the-badge&logo=django)](https://www.django-rest-framework.org/)
[![PostgreSQL](https://img.shields.io/badge/Database-PostgreSQL-lightgrey?style=for-the-badge&logo=postgresql)](https://www.postgresql.org/)

<div dir="rtl" style="text-align: right; line-height: 1.6;">
<strong>AranAsayesh</strong> یک سیستم مقیاس‌پذیر و امن برای مدیریت چرخه عمر کارت‌های تخفیف (<span dir="ltr">Gift Cards & Vouchers</span>) در محیط‌های B2B است. این API به مجموعه‌های تجاری (مانند پاساژها، برندها و سازمان‌ها) اجازه می‌دهد تا سیستم‌های وفاداری مشتریان خود را به صورت دیجیتالی و خودکار مدیریت کنند.
</div>
> ⚠️ **توجه:** کدهای منبع به دلیل محرمانه بودن پروژه اصلی، در اینجا موجود نیستند. این مخزن شامل مستندات فنی، معماری و دموهای وب‌سایت است.

---

## 🚀 اهداف و ویژگی‌های کلیدی

این پروژه با تمرکز بر **دقت مالی**، **امنیت بالا** و **تجربه توسعه‌دهنده (DX)** طراحی شده است:

### 🏢 مدیریت سازمانی (B2B Focus)
*   **چند سازمانی (Multi-Tenancy):** هر سازمان (Organization) داده‌ها، کاربران و کارت‌های اختصاصی خود را دارد و داده‌ها کاملاً ایزوله هستند.
*   **صدور انبوه کارت (Bulk Issuance):** امکان تولید هزاران کد تخفیف منحصر‌به‌فرد در یک عملیات واحد با استفاده از الگوریتم‌های بهینه.
*   **مدیریت سطوح دسترسی (RBAC):** تعریف نقش‌های مختلف برای کاربران سازمان (مدیر کل، کارمند فروش، پشتیبان) با دسترسی‌های متفاوت.

### 💰 هسته مالی و تراکنش‌ها
*   **تراکنش‌های اتمیک (Atomic Transactions):** اطمینان از اینکه عملیات کسر موجودی و ثبت تراکنش، یا هر دو انجام می‌شوند یا هیچ‌کدام (ACID Compliance).
*   **جلوگیری از Double Spending:** مکانیزم‌های Locking برای جلوگیری از استفاده همزمان از یک کارت تخفیف توسط چند کاربر.
*   **گزارش‌گیری لحظه‌ای:** آمار مصرف کارت‌ها، نرخ تبدیل و درآمد حاصل از فروش کارت‌ها.

### 🔐 امنیت و استانداردها
*   **احراز هویت JWT:** پیاده‌سازی کامل JSON Web Tokens (Access & Refresh) برای مدیریت نشست‌های کاربری بدون نیاز به State در سرور.
*   **Rate Limiting:** محدود کردن تعداد درخواست‌ها برای جلوگیری از حملات Brute Force و DDoS.
*   **Validation پیشرفته:** استفاده از DRF Serializers برای اعتبارسنجی دقیق تمام ورودی‌ها و جلوگیری از خطاهای امنیتی.

---

## 🛠️ تکنولوژی‌ها و معماری فنی

این پروژه بر اساس اصول **Clean Architecture** و با استفاده از الگوهای طراحی مدرن ساخته شده است:

| لایه | تکنولوژی | توضیحات فنی |
| :--- | :--- | :--- |
| **Core** | Python 3.10+, Django 4.x | هسته اصلی اپلیکیشن وب |
| **API** | Django REST Framework (DRF) | پیاده‌سازی RESTful APIs با پشتیبانی از Pagination و Filtering |
| **Auth** | `djangorestframework-simplejwt` | مدیریت توکن‌های JWT با قابلیت Refresh Token |
| **Database** | PostgreSQL | استفاده از قابلیت‌های پیشرفته SQL برای روابط پیچیده |
| **Async** | Celery + Redis | پردازش وظایف پس‌زمینه (مثل ارسال ایمیل‌های انبوه یا تولید کدها) |
| **Docs** | DRF YASG / drf-spectacular | مستندسازی خودکار APIها با Swagger UI |

---
