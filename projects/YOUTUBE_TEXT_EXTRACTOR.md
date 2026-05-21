# Youtube_TextExtractor — مستخرج نص YouTube (Telegram)

Last updated: 2026-05-21  
Status: **Active / local-only / PASS (revived & cleaned)**  
Public-safe: نعم (لا أسرار، لا توكنات، لا محتوى `.env`)

## الموقع

- **المسار المعتمد:** `D:\MyPrograming\Youtube_TextExtractor`
- **النوع:** أداة Python محلية صغيرة — بوت Telegram يستقبل رابط YouTube ويرسل نص/ترجمة كملف `.txt` (اسم الملف من عنوان الفيديو حسب الإعدادات).

## الحكم

- **محلي فقط** في هذه المرحلة — **لا** نشر على سيرفر و**لا** IP أو بنية استضافة في الذاكرة العامة.
- **لا** Supabase و**لا** MySQL و**لا** تخزين قاعدة بيانات للنصوص.
- الإعدادات عبر **`.env` محلي** فقط (من قالب `.env.example`) — **لا** ترفع `.env` إلى Git أو الذاكرة العامة.

## التقنية (ملخص عام)

- **Python** + **uv** (`pyproject.toml`, `uv.lock`)
- **youtube-transcript-api** (تدفق متوافق مع 1.2.x)
- **yt-dlp** كاحتياطي للترجمات
- **لا** أسرار في هذا الملف

## مصدر قديم (غير معتمد للتشغيل)

نسخة عمل سابقة في مجلد Downloads — **ليست** المسار الرسمي بعد الآن. استخدم المسار تحت `D:\MyPrograming` فقط.

## تشغيل ذاتي على Windows (ملخص عام)

- **يدوي:** `scripts\run_bot.bat` (قد تظهر نافذة CMD).
- **عند logon:** مهمة `Youtube_TextExtractor_Bot` تشغّل `wscript.exe //B` → `scripts\run_bot_hidden.vbs` — **بدون** نافذة سوداء عالقة.
- **لا** تستخدم `cmd.exe` أو `run_bot.bat` مباشرة في Scheduled Task للتشغيل الذاتي (نمط قديم يُستبدل).
- السجلات: `logs\bot_autostart.log` محليًا — لا تُنشر.

## للوكلاء

1. اقرأ **`AGENTS_PROTOCOL.md`** ثم **`00_MASTER_MEMORY_INDEX.md`** ثم **هذا الملف**.
2. للتفاصيل التشغيلية الكاملة: `_KnowledgeWiki` محليًا (`projects/youtube-text-extractor.md`, skill `python-windows-autostart.md`) أو ملخص تدقيق في `D:\MyPrograming\What_I_Have_Done\cursor.md`.
3. **لا** تطلب من أبو محمد نشر توكن Telegram أو قيم `.env` هنا.
