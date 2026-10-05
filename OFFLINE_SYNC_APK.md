# مساعد الأستاذ — Offline + Cloud Sync + Android

هذه النسخة تحافظ على محتوى التطبيق ووظائفه، وتستخدم التخزين المحلي كطبقة أولى مع مزامنة BodoWorkspace إلى حساب Base44 عند توفر الإنترنت.

- Base44 App ID: `6abe7886e3abdf46e56cb091`
- Android package: `com.bodo.teacherassistant`
- App name: `مساعد الأستاذ`
- Local workspace key: `bodo-workspace-v2:<user-id>`
- Cloud entity: `BodoWorkspace`

## Build APK

```bash
npm install
npm run build
npx cap add android
npx cap sync android
npx cap open android
```

ثم في Android Studio: Build > Build APK(s).

> لا يمكن تضمين مجلد `android` الناتج من Capacitor هنا دون تنزيل حزم npm/Gradle؛ يجب تنفيذ أوامر البناء في بيئة متصلة بالإنترنت.
