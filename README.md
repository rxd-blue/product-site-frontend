# منتجات - موقع تفاعلي مع بوت

هذا المشروع يتكون من جزئين:
1. واجهة أمامية (Frontend) تعرض المنتجات
2. سيرفر خلفي (Backend) يدير الفلاتر

## 🚀 نشر المشروع

### 1. نشر الواجهة الأمامية على GitHub Pages

1. قم بإنشاء مستودع جديد على GitHub
2. ارفع ملف `index.html` إلى المستودع
3. فعّل GitHub Pages من إعدادات المستودع
4. قم بتحديث رابط السيرفر في ملف `index.html` بالرابط الجديد من Render

### 2. نشر السيرفر على Render

1. قم بإنشاء حساب على [Render.com](https://render.com)
2. اختر "New Web Service"
3. اربط حساب GitHub الخاص بك
4. اختر المستودع الذي يحتوي على ملفات السيرفر
5. اضبط الإعدادات التالية:
   - Build Command: `npm install`
   - Start Command: `npm start`
   - Environment: Node

### 3. تحديث رابط السيرفر

بعد نشر السيرفر على Render، قم بتحديث الرابط في ملف `index.html`:

```javascript
const res = await fetch('https://YOUR-RENDER-URL.onrender.com/api/filter');
```

## 🧪 اختبار النظام

يمكنك اختبار النظام باستخدام curl:

```bash
curl -X POST https://YOUR-RENDER-URL.onrender.com/api/filter \
  -H "Content-Type: application/json" \
  -d '{"category": "تليفونات", "brand": "سامسونج"}'
```

## 📝 ملاحظات

- تأكد من تفعيل CORS في السيرفر
- تأكد من تحديث رابط السيرفر في الواجهة الأمامية
- يمكنك إضافة المزيد من المنتجات في ملف `index.html` 