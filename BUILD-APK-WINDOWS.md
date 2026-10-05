# مساعد الأستاذ — بناء APK على Windows 10

## 1) تثبيت الحزم
داخل مجلد المشروع:

```bat
npm install
```

## 2) بناء نسخة الويب

```bat
npm run build
```

## 3) إضافة Android (مرة واحدة فقط)

```bat
npx cap add android
```

إذا ظهرت رسالة أن مجلد `android` موجود أصلًا، لا تعاود تنفيذ هذا الأمر.

## 4) مزامنة Android

```bat
npx cap sync android
```

## 5) فتح Android Studio

```bat
npx cap open android
```

ثم من Android Studio:

**Build → Build APK(s)**

ملف APK الناتج عادة داخل:

`android\app\build\outputs\apk\debug\app-debug.apk`

## ملاحظات
- لا تستخدم `npm audit fix --force` أثناء تجهيز هذه النسخة.
- App ID الخاص بـ Base44 موجود في `.env.local`.
- التطبيق يحفظ محليًا أولًا، ثم يزامن مع Base44 عند توفر الإنترنت.
