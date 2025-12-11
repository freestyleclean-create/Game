Football Mobile Pro - README

هذه الحزمة تحتوي على مشروع ويب قابل للتشغيل داخل متصفح (HTML + Phaser 3).
اخترت لك ستايل 'PES'، وضعت عدة ملاعب (صور placeholder) ولاعب، وأصوات placeholder بما في ذلك ملف تعليق باسم 'commentator_essam_shawaly_placeholder.mp3'.

محتويات الحزمة:
- index.html
- assets/
   - images/ (stadium_*.png, player_front.png)
   - sounds/ (kick.wav, crowd_loop.wav, commentator_essam_shawaly_placeholder.mp3)

ملاحظة هامة عن تعليق 'عصام الشوالي':
- لا أستطيع إنشاء أو توليد صوت يقلّد شخصية حية مشهورة دون إذن صريح؛ هذا قد ينتهك حقوق الشخصية وسياسات الاستخدام. لذا وضعت ملف placeholder باسم الملف المطلوب.
- الخيارات المتاحة:
  1) تزودني بتسجيلات صوتية مرخّصة من عصام الشوالي أو إذن خطي منه لاستخدام صوته، وسأركّبها.
  2) أستخدم تعليقًا بديلًا مُركّبًا (TTS) بصوت عربي عامّ (لا يقلّد شخص معين). سأرفق خطوات لاستخدام TTS في الملف.
  3) تستخدم مُعلّق حرّ (مثلاً معلق عام أو صديقك يسجل) وتزودني بالملفات.

خطوات لتحويل المشروع إلى APK (Capacitor) — ملخّص:
1) ثبت Node.js وnpm وAndroid Studio.
2) في مجلّد المشروع شغّل:
   npm init -y
   npm install @capacitor/core @capacitor/cli
3) أنشئ ملف بسيط ونسخ محتويات index.html داخل مجلد 'www'.
4) npx cap init football-pro com.example.football
   npx cap add android
   npx cap copy android
5) افتح المشروع في Android Studio: npx cap open android
6) Build -> Generate Signed Bundle / APK

ملف 'build_apk_steps.txt' داخل الحزمة يحتوي خطوات مفصّلة أكثر.

إذا تريد، أقدر:
- أركّب تعليق TTS بديل (صوت عربي عام) مباشرة وأضعه مكان الـ placeholder.
- أجهّز مشروع Capacitor جاهز (www folder, package.json) مع سكريبتات build، لكن لا أستطيع بناء APK فعليًا هنا؛ تحتاج Android Studio على جهازك أو أقدّم ملف تعليمات مفصّلة.

أخبرني أي خيار تفضّل بخصوص التعليق، وهل تريد أجهّز مشروع Capacitor كامل (حاجيات البناء في المجلد)؟