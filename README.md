MVP وب‌اپ موبایل-فرست با پشتیبانی چند زبانه
هدف پروژه
ایجاد پلتفرم آموزشی زبان با تمرکز بر zh_HSK (HSK1 تا HSK4) همراه با زبان‌های انگلیسی و روسی، که به صورت وب‌اپ موبایل-فرست (PWA) طراحی می‌شود و امکان تبدیل به اپ موبایل بومی را در آینده دارد.

ویژگی‌های کلیدی

فرانت‌اند موبایل-اول با رویکرد PWA
بک‌اند FastAPI روی SQLite (قابل ارتقا به PostgreSQL)
محتوای zh_hsk1-4 و vocabهای EN/RU
حمایت از سه زبان رابط: EN, ZH, RU با نمایش توضیحات به فارسی
تولید صوتی خودکار برای واژگان با گویش‌های male/female در EN/RU/ZH
تمرین‌ها و کوییزهای کوتاه پس از هر درس
مخزن گیت-هاب با CI ساده و مستندات
ساختار پروژه

backend/
main.py
models.py
database.py
/content/
zh_hsk1.json
zh_hsk2.json
zh_hsk3.json
zh_hsk4.json
en_vocab.json
ru_vocab.json
/audio/
zh_hsk1_001.mp3 ... (تولیدشده با generate_tts.py)
/api/
content_endpoints.py
user_endpoints.py
quiz_endpoints.py
/tools/
generate_tts.py
content_loader.py
frontend/
src/
App.jsx
index.css
components/
Header.jsx
LanguageSelector.jsx
Lesson.jsx
Quiz.jsx
Progress.jsx
services/
api.js
hooks/
useContent.js
useQuiz.js
/assets/audio/
zh_hsk1_001.mp3 ...
docs/
INSTALL.md
API_REFERENCE.md
CONTENT_SCHEMA.md
DEPLOYMENT.md
scripts/
build_all.sh
run_all.sh
.github/
workflows
