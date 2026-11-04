# LAVENDER | لافندر

منصة عربية تربط تجار الأزياء النسائية بالمسوّقين.

## التقنية
- React + TypeScript + Vite
- Supabase Auth وPostgres وStorage
- واجهة عربية RTL متجاوبة

## الإعداد
1. انسخ `.env.example` إلى `.env.local`.
2. ضع رابط مشروع Supabase ومفتاح publishable أو anon في متغيرات البيئة.
3. نفّذ `npm install` ثم `npm run dev`.
4. تحقق من بناء الإنتاج عبر `npm run build`.

لا تضع مفتاح service_role أو secret في الواجهة أو في أي متغير يبدأ بـ `VITE_`.

## قاعدة البيانات
يستخدم المشروع الجداول الموجودة: profiles, categories, products, product_images, product_variants, marketer_favorites, orders, order_items. إنشاء ملف المسوّق يتم بواسطة trigger قاعدة البيانات، وتُرسل بيانات التسجيل كـ auth user metadata؛ وتظل صلاحية الحساب pending حتى موافقة المدير.
