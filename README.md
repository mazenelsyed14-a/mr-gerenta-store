# 👑 متجر mr.gerenta الفاخر (MR. GERENTA STORE)
متجر إلكتروني متكامل للساعات الأصلية والعطور الفاخرة مع لوحة تحكم خاصة بالمالك، سلة مشتريات تفاعلية، وربط كامل مع واتساب لإتمام الطلبات بضغطة زر. جاهز للنشر السحابي المجاني 24/7 على **Render** أو **Vercel**.

---

## 📁 هيكل المشروع (Project Structure)

```text
mr-gerenta-store/
│── backend/
│   ├── server.js          # خادم Express وواجهات الـ API
│   ├── auth.js            # إعدادات المصادقة وحماية لوحة المالك
│   ├── package.json       # تبعيات ومكتبات الباك إند
│   ├── products.json      # قاعدة بيانات المنتجات (JSON)
│   └── upload/            # مجلد حفظ صور المنتجات المرفوعة
│
│── frontend/
│   ├── index.html         # الواجهة الرئيسية للمتجر (العرض + السلة + واتساب)
│   ├── product.css        # التنسيقات الفاخرة لواجهة المتجر (Dark Luxury Theme)
│   ├── admin.html         # لوحة تحكم المالك (تسجيل الدخول + إضافة وحذف المنتجات)
│   └── admin.css          # تنسيقات لوحة التحكم
│
├── package.json           # ملف الحزم الرئيسي للنشر السحابي (Root)
├── render.yaml            # ملف إعدادات النشر التلقائي على Render
├── vercel.json            # إعدادات النشر على Vercel
├── .gitignore             # تجاهل الملفات المؤقتة و node_modules
├── start.bat              # تشغيل محلي بضغطة زر
└── README.md              # دليل الاستخدام والنشر أونلاين
```

---

## 🌐 دليل رفع المتجر أونلاين مجاناً (Deployment Guide)

المنصة الأنسب والأسهل لهذا المشروع هي **[Render.com](https://render.com)** لأنها تدعم تشغيل خوادم Node.js بالكامل مع ملفات الرفع والجلسات مجاناً وبدون الحاجة لإبقاء جهازك أو أي أداة قيد التشغيل.

### 🌟 الخطوة الأولى: رفع المشروع على GitHub
1. اذهب لموقع **[GitHub.com](https://github.com)** وأنشئ حساباً إن لم يكن لديك.
2. اضغط على **New Repository** وأعطه اسماً مثل: `mr-gerenta-store`، واجعله **Public** أو **Private**.
3. ارفع ملفات المجلد `mr-gerenta-store` (احرص على رفع الملفات والمجلدات `backend` و `frontend` و `package.json` و `render.yaml` - وتجنب رفع مجلد `node_modules`).

---

### 🌟 الخطوة الثانية: الربط والنشر على Render (في دقيقتين)
1. افتح موقع **[Render.com](https://render.com)** وسجل الدخول بحساب GitHub الخاص بك.
2. اضغط على زر **New +** ثم اختر **Web Service**.
3. اختر مستودع المشروع `mr-gerenta-store` من قائمة GitHub ثم اضغط **Connect**.
4. اضبط الإعدادات التالية (أو سيتعرف عليها تلقائياً من ملف `render.yaml`):
   - **Name:** `mr-gerenta-store`
   - **Runtime:** `Node`
   - **Build Command:** `npm install && cd backend && npm install`
   - **Start Command:** `node backend/server.js`
   - **Instance Type:** `Free`
5. اضغط على **Create Web Service** في أسفل الصفحة.

🎉 **مبروك!** خلال دقيقة واحدة سيعطيك Render رابطاً دائماً مثل:  
`https://mr-gerenta-store.onrender.com`  
يعمل من أي متصفح ومن أي موبايل طوال الـ 24 ساعة بدون الحاجة لتشغيل جهازك!

- 🌐 رابط المتجر للعملاء: `https://your-app.onrender.com/`
- 👑 رابط لوحة الإدارة للمالك: `https://your-app.onrender.com/admin` (أو `/admin.html`)

---

## 🔑 بيانات تسجيل دخول المالك (Admin Credentials)

- **اسم المستخدم:** `mazen elsyed5060`
- **كلمة المرور:** `Mazen 3safra2523`

> 💡 *يمكنك تعديل اسم المستخدم وكلمة المرور من داخل ملف `backend/auth.js` أو عبر المتغيرات البيئية (Environment Variables) في Render.*

---

## 💻 طريقة التشغيل محلياً على جهازك (Local Run)

إذا أردت تجربة المتجر أو التعديل عليه على جهازك:
1. اضغط مرتين على ملف `start.bat`.
2. أو من التيرمينال:
   ```bash
   cd backend
   npm install
   node server.js
   ```
3. افتح المتصفح على: `http://localhost:3000`
