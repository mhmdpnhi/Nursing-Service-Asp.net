<div align="center">
  <img src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/dotnet/dotnet.png" width="100" alt=".NET Logo" />
  <h1>سامانه مدیریت خدمات پرستاری</h1>
  <p><strong>Nursing Service Management System</strong></p>
  <p>
    <a href="https://nursing-service-aspnet-production.up.railway.app/">
      <img src="https://img.shields.io/badge/Live Demo-0d9488?style=for-the-badge&logo=vercel" alt="Live Demo" />
    </a>
  </p>
</div>

---

## 📌 معرفی پروژه
پروژه **پرستار سلامت (Nursing Service System)** یک پلتفرم جامع برای مدیریت خدمات پرستاری، مراقبت در منزل، اعزام پزشک و خدمات توانبخشی است. این سامانه با هدف تسهیل ارتباط بین بیماران، پرستاران مجرب، سوپروایزرها و تیم پشتیبانی طراحی شده است تا خدماتی ایمن و استاندارد را ارائه دهد. 

این سیستم بستری مناسب برای ثبت درخواست نیرو، مدیریت شیفت‌ها و نظارت همه‌جانبه بر کیفیت خدمات درمانی در منزل فراهم می‌آورد.

---

## 🏗️ معماری (Architecture)
این پروژه بر پایه **معماری پیاز (Onion Architecture)** یا **معماری تمیز (Clean Architecture)** توسعه یافته است تا قابلیت نگهداری، مقیاس‌پذیری و تست‌پذیری بالایی داشته باشد. 

لایه‌های اصلی سیستم عبارتند از:
- **Core / Domain:** شامل موجودیت‌های اصلی (Entities) و Interfaceهای پایه‌ای (مانند مدل‌های بیمار، پرستار، خدمات و درخواست‌ها).
- **Application:** شامل منطق تجاری (Business Logic)، سرویس‌ها و تفکیک لایه‌های Command/Query.
- **Infrastructure:** ابزارهای زیرساختی نظیر سرویس پیامک و ارتباط با سرویس‌های خارجی.
- **Persistence:** پیاده‌سازی و مدیریت دیتابیس با استفاده از Entity Framework Core.
- **Presentation (Endpoints):** لایه دسترسی کاربر شامل رابط کاربری تحت وب (ASP.NET Core MVC) و وب‌سرویس‌ها (Web API).

---

## 💻 تکنولوژی‌های استفاده شده (Tech Stack)
این پروژه از مدرن‌ترین تکنولوژی‌های اکوسیستم مایکروسافت بهره می‌برد:
- **Framework:** .NET 9
- **Web UI:** ASP.NET Core MVC & Razor Pages
- **API:** ASP.NET Core Web API
- **ORM:** Entity Framework Core
- **Database:** SQL Server
- **Front-end:** HTML5, CSS3, Bootstrap 5 (RTL), jQuery, SweetAlert2
- **Architecture Patterns:** Clean Architecture, Repository Pattern, Dependency Injection

---

## 🚀 نقشه راه و توسعه آینده (Roadmap)
این پروژه **به صورت فعال در دست توسعه است** و در نسخه‌های آینده با هدف ارتقای پرفورمنس و امنیت، فیچرهای پیشرفته زیر به آن اضافه خواهند شد:
- [ ] ⚡ **پیاده‌سازی Redis** جهت Caching و بهبود چشمگیر سرعت پاسخ‌دهی.
- [ ] 📨 **استفاده از RabbitMQ** برای مدیریت صف پیام‌ها و پردازش‌های ناهمگام (Asynchronous Processing).
- [ ] 🔐 **مهاجرت به احراز هویت JWT (JSON Web Tokens)** جهت امنیت بالاتر و ایجاد بستری مناسب برای اپلیکیشن موبایل.
- [ ] 🧪 **افزودن Integration Tests** برای تضمین پایداری و صحت عملکرد کل سیستم قبل از استقرار.

---

## ⚙️ راهنمای اجرا (How to Run)
برای اجرای پروژه روی سیستم لوکال خود، مراحل زیر را طی کنید:
1. ابتدا مخزن را Clone کنید.
2. اطمینان حاصل کنید که **SDK .NET 9.0** روی سیستم شما نصب شده است.
3. فایل `appsettings.json` در پروژه `Endpoint_WebApp` (یا پروژه API) را باز کرده و در صورت نیاز Connection String دیتابیس خود را تنظیم نمایید.
4. پروژه `Endpoint_WebApp.csproj` را به عنوان پروژه پیش‌فرض تنظیم و اجرا کنید (Run).
