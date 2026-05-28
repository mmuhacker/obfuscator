<div align="center">

**🔐 Python Obfuscator**

**أداة تشويش وحماية كود بايثون**


```
  ██████╗ ██████╗ ███████╗██╗   ██╗███████╗ ██████╗ █████╗ ████████╗ ██████╗ ██████╗
  ██╔═══██╗██╔══██╗██╔════╝██║   ██║██╔════╝██╔════╝██╔══██╗╚══██╔══╝██╔═══██╗██╔══██╗
  ██║   ██║██████╔╝█████╗  ██║   ██║███████╗██║     ███████║   ██║   ██║   ██║██████╔╝
  ██║   ██║██╔══██╗██╔══╝  ██║   ██║╚════██║██║     ██╔══██║   ██║   ██║   ██║██╔══██╗
  ╚██████╔╝██████╔╝██║     ╚██████╔╝███████║╚██████╗██║  ██║   ██║   ╚██████╔╝██║  ██║
   ╚═════╝ ╚═════╝ ╚═╝      ╚═════╝ ╚══════╝ ╚═════╝╚═╝  ╚═╝   ╚═╝    ╚═════╝ ╚═╝  ╚═╝
```

**By:** ꧁ঔৣ☬ Muhannad Daher ☬ঔৣ꧂

---

![Version](https://img.shields.io/badge/Version-1.0-blue?style=for-the-badge)


![Platform](https://img.shields.io/badge/Platform-Android-green?style=for-the-badge&logo=android)

![Platform](https://img.shields.io/badge/Platform-Kali_Linux-green?style=for-the-badge&logo=kalilinux)


![Python](https://img.shields.io/badge/Python-3.x-yellow?style=for-the-badge&logo=python)


![License](https://img.shields.io/badge/License-Commercial-red?style=for-the-badge)


![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge)

---

**📚 المحتويات**
</div>


- [📌 ما هي الأداة؟](#-ما-هي-الأداة)
- [⚙️ كيف تعمل؟](#️-كيف-تعمل)
- [📋 المتطلبات](#-المتطلبات)
- [🚀 التثبيت](#-التثبيت)
  - [تطبيق 🤖 Termux (Android)](#-termux-android)
  - [نظام 🐉 Kali Linux](#-kali-linux)
- [▶️ طريقة الاستخدام](#️-طريقة-الاستخدام)
- [📁 هيكل الملفات](#-هيكل-الملفات)
- [💡 ملاحظات مهمة](#-ملاحظات-مهمة)
- [👨‍💻 المطوّر](https://github.com/mmuhacker/obfuscator/blob/main/README.md#%E2%80%8D-%D8%A7%D9%84%D9%85%D8%B7%D9%88%D9%91%D8%B1)

---

## 📌 ما هي الأداة؟

**Python Obfuscator** هي أداة سطر أوامر مكتوبة بلغة Python تقوم بتشويش وحماية ملفات `.py` من القراءة والسرقة، مع الحفاظ على عملها بشكل طبيعي تماماً.

---

## ⚙️ كيف تعمل؟

تعتمد الأداة على **3 طبقات حماية**:

| الطبقة | العملية |
|--------|---------|
| الأولى | ضغط الكود باستخدام `zlib` بأقصى مستوى |
| الثانية | تشفير الناتج بـ `Base85` |
| الثالثة | تقطيع الكود إلى أجزاء + توليد أسماء متغيرات عشوائية |

الملف المحمي يعمل بشكل طبيعي ولا يمكن قراءته أو فهمه دون فك التشويش.

---

## 📋 المتطلبات

- Python 3.6 أو أحدث
- مكتبة `arabic-reshaper` (لعرض النصوص العربية)
- مكتبة `python-bidi` (لعرض النصوص العربية)

---

## 🚀 التثبيت

### 🤖 Termux (Android)

```bash
# 1. تحديث الحزم
pkg update && pkg upgrade -y

# 2. تثبيت Python
pkg install python -y

# 3. تثبيت المكتبات المطلوبة
pip install arabic-reshaper python-bidi

# 4. تحميل الأداة مباشرة من GitHub
curl -o $PREFIX/bin/ob https://raw.githubusercontent.com/mmuhacker/obfuscator/main/mud_ob.py

# 5. منح صلاحية التنفيذ
chmod +x $PREFIX/bin/ob

# 6. الآن يمكنك تشغيلها من أي مكان:
ob
```

---

### 🐉 Kali Linux

```bash
# 1. تحديث النظام
sudo apt update && sudo apt upgrade -y

# 2. التحقق من Python (مثبت افتراضياً)
python3 --version

# 3. تثبيت pip إذا لم يكن موجوداً
sudo apt install python3-pip -y

# 4. تثبيت المكتبات المطلوبة
pip3 install arabic-reshaper python-bidi

# 5. تحميل الأداة مباشرة من GitHub
sudo curl -o /usr/local/bin/ob https://raw.githubusercontent.com/mmuhacker/obfuscator/main/mud_ob.py

# 6. منح صلاحية التنفيذ
sudo chmod +x /usr/local/bin/ob

# 7. الآن يمكنك تشغيلها من أي مكان:
ob
```

---

## ▶️ طريقة الاستخدام

### تشغيل مباشر (بدون تثبيت):
```bash
# Termux
python mud_ob.py

# Kali Linux
python3 mud_ob.py
```

### تشغيل كأمر عالمي (بعد التثبيت):
```bash
ob
```

### خطوات الاستخدام:
```
1. اختر [1] لتشويش ملف

2. أدخل مسار الملف المراد حمايته
   مثال: /sdcard/Download/myapp.py

3. أدخل مسار حفظ الملف المحمي
   (أو اضغط Enter للحفظ تلقائياً بجانب الملف الأصلي)

4. أكّد بـ y للبدء

5. ستجد الملف المحمي جاهزاً باسم: myapp_protected.py
```

---

## 📁 هيكل الملفات

```
mud_ob.py              ← الأداة الرئيسية
README.md              ← هذا الملف
```

---

## 💡 ملاحظات مهمة

- ✅ الملف المحمي يعمل بنفس طريقة الأصلي تماماً
- ✅ يدعم كل ملفات Python 3
- ⚠️ احتفظ دائماً بنسخة من الملف الأصلي
- ⚠️ التشويش لا يعني التشفير الكامل — هو حماية من القراءة السريعة

---

## 👨‍💻 المطوّر

**Muhannad Daher**

[![GitHub](https://img.shields.io/badge/GitHub-mmuhacker-black?style=for-the-badge&logo=github)](https://github.com/mmuhacker)

[![Contact Us](https://img.shields.io/badge/Contact_Us-black?style=for-the-badge&logo=gmail&logoColor=red)](mailto:madarik.ai.info@gmail.com)

---
</div>



- بوت التداول الذكي
- البيئة: Termux (Android)
- الإصدار: v1.0

---

<div align="center">



*"حافظ على كودك، حافظ على عملك."*

**⭐ إذا أعجبتك الأداة، لا تنسَ النجمة! ⭐**
</div>
