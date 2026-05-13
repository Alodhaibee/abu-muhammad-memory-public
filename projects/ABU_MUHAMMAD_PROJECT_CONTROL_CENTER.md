# ControlCenter — Control Center (Public Safe)

Last updated: 2026-05-13  
Status: Active supporting tool

> **Memory file name:** هذا الملف يبقى باسم `ABU_MUHAMMAD_PROJECT_CONTROL_CENTER.md` لأسباب تاريخية للروابط؛ المحتوى يصف المشروع الحالي **ControlCenter**.

## الهوية الحالية (أسماء محايدة للأداة)
| | |
|--|--|
| **اسم المشروع / المجلد** | `ControlCenter` |
| **المسار المحلي** | `D:\MyPrograming\ControlCenter` |
| **الاسم السابق للمجلد** | `AbuMuhammadControlCenter` (أُعيدت تسميته؛ لا يُفضَّل في واجهات أو أسماء ملفات محايدة جديدة) |
| **الواجهة (عناوين نصية)** | **Control Center** — **Project Dashboard** |

## ملاحظة تهجئة (مرجع آمن)
عند الحاجة للاسم الإنجليزي للشخص، التهجئة المعتمدة: **Abu Mohammed** — وليس `AbuMuhammad` ولا `Abu Muhammad`. لأسماء الأدوات والمشاريع يُفضَّل أسماء محايدة مثل **ControlCenter**.

## الغرض
لوحة تحكم GUI محليّة (Python) لاستعراض مشاريع العمل تحت `D:\MyPrograming`، مع حالة Git، واختصارات فتح المجلد / Cursor / VS Code / PowerShell، وقراءة تقرير التدقيق، وملاحظات لكل مشروع — دون تعديل مستودعات المراقَبة من داخل الأداة (حدود آمنة كما في الذاكرة السابقة).

## ما تم توثيقه كتحسينات (ملخص عام)
- قراءة تقرير التدقيق تفضّل: `D:\MyPrograming\What_I_Have_Done\cursor.md` مع **fallback** للملف القديم: `D:\MyPrograming\What_I_Have_Done.md`.
- أزرار **Actions** مرتّبة في شبكة **3×2**.
- قائمة المشاريع عبر **`ttk.Treeview`** بدل Listbox.
- أعمدة واضحة: **Note / Git / Project**.
- اختصارات عمود Git: **OK** نظيف، **M** يوجد تغييرات، فراغ عند عدم وجود مستودع أو خطأ؛ عمود الملاحظة **N** عند وجود ملاحظة محفوظة.
- عدم تشغيل `git status` أثناء الكتابة في البحث — الاعتماد على **Git cache** في الذاكرة.
- تحديث نصوص الواجهة إلى **Control Center** / **Project Dashboard** وإزالة آثار الاسم القديم داخل مجلد المشروع.
- تحقق: `python -m py_compile main.py` نجح؛ دون إنترنت في جلسة التعديل؛ دون commit أو push من Cursor في تلك الجلسة؛ تقارير Cursor الرسمية: `D:\MyPrograming\What_I_Have_Done\cursor.md`.

## التشغيل (مرجع)
- `run.bat` / `run_debug.bat` داخل مجلد المشروع.
- ملاحظات محليّة: `data\project_notes.json`.

## Safe working rules
- لا تنشر أسرارًا أو بيانات اعتماد أو مسارات حساسة خارج هذا المستوى التلخيصي.
- الأداة للاستخدام الداخلي؛ التفاصيل التشغيلية الكاملة تبقى محليًا.

## What ChatGPT should remember
أداة مساندة لتنظيم المشاريع والوصول السريع؛ ليست جزءًا من منطق Labib الأساسي. الاسم العلني للأداة محايد: **Control Center**.

## Related safe files
- `04_ACTIVE_PROJECTS.md`
- `00_MASTER_MEMORY_INDEX.md`
- `03_TOOLS_AND_ENVIRONMENT.md`
- `projects/CODEX_SKILLS.md`

## Next-task guidance
عند التوجيه إلى Cursor، استخدم المسار **`D:\MyPrograming\ControlCenter`** وملف **`projects/ABU_MUHAMMAD_PROJECT_CONTROL_CENTER.md`** في هذه الذاكرة كمرجع عام آمن.
