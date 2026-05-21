# Youtube_TextExtractor — مستخرج نص YouTube (Telegram)

Last updated: 2026-05-21  
Status: **Active — local workstation + remote Linux host (deployed)**  
Public-safe: نعم (لا أسرار، لا توكنات، لا محتوى `.env`)

## الموقع

- **محلي (تطوير/مرجع):** `D:\MyPrograming\Youtube_TextExtractor` — **uv**, `pyproject.toml`
- **بعيد (تشغيل):** `/home/0hani0/Programing/Telgram` — تفاصيل SSH والمضيف في _KnowledgeWiki الخاص (لا تُنشر tokens هنا)

## الحكم

- بوت Telegram: رابط YouTube → نص/ترجمة → ملف **`.txt`** (اسم الملف من عنوان الفيديو).
- **لا** Supabase و**لا** MySQL و**لا** تخزين قاعدة بيانات و**لا** مطالبة حفظ (أُزيلت من النسخة النشطة على الخادم، 2026-05-21).
- **محلي:** إعدادات عبر **`.env`** — لا ترفع إلى Git أو الذاكرة العامة.
- **بعيد:** أسرار في **`config.py`** — **محفوظة دون استبدال**؛ لم يُنسخ `.env` أو توكن المحلي إلى الخادم.

## التقنية (ملخص عام)

| بيئة | Runtime |
|------|---------|
| Local Windows | **uv** + youtube-transcript-api 1.2.x + yt-dlp |
| Remote Linux | **venv + pip** (uv غير متوفر على الخادم حاليًا — عمدًا لتجنب كسر PM2) |

المنطق: youtube-transcript-api (متوافق 1.2.x) ثم yt-dlp fallback.

## تشغيل بعيد (ملخص عام — بدون أسرار)

| Item | Public-safe note |
|------|------------------|
| Process manager | **PM2** — process name `telgram-bot` |
| Active entry | `youtube_transcript_bot.py` |
| Legacy file | `youtubeToText.py` — موجود كأرشيف، **ليس** العملية النشطة |
| Restart | `pm2 restart telgram-bot` |
| Logs | `pm2 logs telgram-bot` (على الخادم) |

## تشغيل ذاتي على Windows (محلي فقط)

- **يدوي:** `scripts\run_bot.bat`
- **عند logon:** `wscript.exe //B` → `run_bot_hidden.vbs` (بدون نافذة سوداء عالقة)
- انظر _KnowledgeWiki skill `python-windows-autostart` للتفاصيل المحلية

## قرار لاحق (خاص)

مراجعة ما إذا كان بوت **الخادم** يحتاج تقييد `USER_ID` / `ALLOWED_TELEGRAM_USER_IDS` — التفاصيل في _KnowledgeWiki و`What_I_Have_Done\cursor.md` (بدون قيم).

## مصدر قديم (غير معتمد)

مجلد Downloads على Windows — **ليست** النسخة الرسمية. المسارات المعتمدة أعلاه.

## للوكلاء

1. اقرأ **`AGENTS_PROTOCOL.md`** ثم **`00_MASTER_MEMORY_INDEX.md`** ثم **هذا الملف**.
2. تفاصيل SSH والمسارات الكاملة: _KnowledgeWiki `projects/youtube-text-extractor.md` (خاص).
3. **لا** تطلب نشر توكن Telegram أو قيم `.env` في الذاكرة العامة.
