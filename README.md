# عُقدة سحب — sa1

حزمة **جاهزة ومجهّزة بالكامل** لهذا المزوّد: **vercel**.
العُقدة تسرّع السحب التلقائي عبر موازاة العمل مع السيرفر الأصلي
— **بدون** تخزين أي بيانات قاعدة هنا.

- رابط اللوحة: `https://tv-api.verx1.xyz/0000`
- التوكن: `nd_ضع-توكن-العقدة-هنا`
- نطاق العمل: كل المواقع

## النشر على Vercel (طريقتان)

### الطريقة ١ — رفع المشروع كامل (لن يسل عن Python أو Web)

الحزمة هذه **Node.js فقط** — كل الملفات الأساسية في الجذر
(`package.json` + `api/cron.js`)، فلا يوجد مشروع Python ثانٍ يربك Vercel.

1. ادخل https://vercel.com/new ← **Import Git Repository** (أو من داخل المجلد `npx vercel`).
2. لو سألك Vercel عن النوع: اختر **Other** (لا Python).
   Framework Preset: **Other** · Build Command: فارغ · Output Directory: فارغ.
3. من **Settings → Environment Variables** أضف:
   - `NODE_PANEL_URL` = `https://tv-api.verx1.xyz/0000`
   - `NODE_TOKEN` = `nd_ضع-توكن-العقدة-هنا`
   - `NODE_NAME` = `sa1`
4. Deploy. الكرون كل دقيقة تلقائيا (مضبوط في `vercel.json`).

### الطريقة ٢ — سطر الأوامر

```bash
npm i -g vercel
vercel
vercel --prod
```

## التأكد من الاتصال

بعد النشر افتح رابط العُقدة — يجب أن يظهر: `{"ok":true,"node":"sa1"}`

بعدها ارجع للوحة ← «عُقد السحب» واضغط **فحص الاتصال**. لما تصير خضراء يبدأ التوزيع تلقائيا.
