<div align="center">

  # 🔐 Python Obfuscator
# أداة تشويش وحماية كود بايثون

**By:** ꧁ঔৣ☬ Muhannad Daher ☬ঔৣ꧂

---

![Version](https://img.shields.io/badge/1.0-%EF%BA%8D%EF%BB%B9%EF%BA%BB%EF%BA%AA%EF%BA%8D%EF%BA%AE-blue?style=for-the-badge)<br>
![Platform](https://img.shields.io/badge/%EF%BB%9B%EF%BA%8E%EF%BB%9F%EF%BB%B2%20%EF%BB%9F%EF%BB%B4%EF%BB%A8%EF%BB%9C%EF%BA%B2-%EF%BA%8D%EF%BB%9F%EF%BA%92%EF%BB%B4%EF%BA%8C%EF%BA%94-green?style=for-the-badge&logo=kalilinux)<br>
![Platform](https://img.shields.io/badge/%EF%BA%84%EF%BB%A7%EF%BA%AA%EF%BA%AE%EF%BB%AE%EF%BB%B3%EF%BA%AA-%EF%BA%8D%EF%BB%9F%EF%BA%92%EF%BB%B4%EF%BA%8C%EF%BA%94-green?style=for-the-badge&logo=android)<br>
![Python](https://img.shields.io/badge/3.x-%EF%BA%91%EF%BA%8E%EF%BB%B3%EF%BA%9C%EF%BB%AE%EF%BB%A6-blue?style=for-the-badge&logo=python)<br>
![License](https://img.shields.io/badge/MIT-%EF%BA%8D%EF%BB%9F%EF%BA%98%EF%BA%AE%EF%BA%A7%EF%BB%B4%EF%BA%BA-red?style=for-the-badge)<br>
![Status](https://img.shields.io/badge/%EF%BB%A7%EF%BA%B8%EF%BB%82-%EF%BA%8D%EF%BB%9F%EF%BA%A4%EF%BA%8E%EF%BB%9F%EF%BA%94-blue?style=for-the-badge)

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
- [الرخصة](#-الرخصة)

---
<div align="center">

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
</div>

- حزمة Python 3.x
- مكتبة `arabic-reshaper` (لعرض النصوص العربية)
- مكتبة `python-bidi` (لعرض النصوص العربية)

---
<div align="center">

## 🚀 التثبيت

### 🤖 Termux (Android)
</div>


**1. تحديث الحزم**

```bash
pkg update && pkg upgrade -y
```

**2. تثبيت Python**
```bash
pkg install python -y
```
**3. تثبيت المكتبات المطلوبة**
```bash
pip install arabic-reshaper python-bidi
```

**4. تحميل الأداة مباشرة**
```bash
curl -o $PREFIX/bin/ob https://raw.githubusercontent.com/mmuhacker/obfuscator/main/mud_ob.py
```

**5. منح صلاحية التنفيذ**
```bash
chmod +x $PREFIX/bin/ob
```

**6. الآن يمكنك تشغيلها من أي مكان:**
```
ob
```

---

### 🐉 Kali Linux


**1. تحديث النظام**
```bash
sudo apt update && sudo apt upgrade -y
```

**2. التحقق من Python (مثبت افتراضياً)**
```bash
python3 --version
```

**3. تثبيت pip إذا لم يكن موجوداً**
```bash
sudo apt install python3-pip -y
```

**4. تثبيت المكتبات المطلوبة**
```bash
pip3 install arabic-reshaper python-bidi
```

**5. تحميل الأداة مباشرة**
```bash
sudo curl -o /usr/local/bin/ob https://raw.githubusercontent.com/mmuhacker/obfuscator/main/mud_ob.py
```

**6. منح صلاحية التنفيذ**
```bash
sudo chmod +x /usr/local/bin/ob
```

**7. الآن يمكنك تشغيلها من أي مكان:**
```
ob
```

---
<div align="center">

## ▶️ طريقة الاستخدام

**تشغيل مباشر (بدون تثبيت):**

**Termux**
</div>

```bash
python mud_ob.py
```
<div align="center">
  
**Kali Linux**
</div>

```bash
python3 mud_ob.py
```

<div align="center">
  
**تشغيل كأمر عالمي (بعد التثبيت):**
```bash
ob
```
---


### خطوات الاستخدام:


| الخطوة | العملية |
|---|---------|
| 1. | اختر [1] لتشويش ملف |
| 2. | أدخل مسار الملف المراد حمايته
| مثال: | /sdcard/Download/myapp.py |
| 3. | أدخل مسار حفظ الملف المحمي |
| أو اضغط Enter | للحفظ تلقائياً بجانب الملف الأصلي |
| 4. | أكّد بـ y للبدء |
| 5. | ستجد الملف المحمي جاهزاً باسم: |
| مثال | myapp_protected.py |

---

## 📁 هيكل الملفات

</div>

```
mud_ob.py              ← الأداة الرئيسية
README.md              ← هذا الملف
```

---
<div align="center">
  
## 💡 ملاحظات مهمة
</div>

- ✅ الملف المحمي يعمل بنفس طريقة الأصلي تماماً
- ✅ يدعم كل ملفات Python 3
- ⚠️ احتفظ دائماً بنسخة من الملف الأصلي
- ⚠️ التشويش لا يعني التشفير الكامل — هو حماية من القراءة السريعة

---
<div align="center">

## 👨‍💻 المطوّر

**Muhannad Daher**

[![GitHub](https://img.shields.io/badge/GitHub-mmuhacker-black?style=for-the-badge&logo=github)](https://github.com/mmuhacker)

---


## 📄 الرخصة
**MIT License — حر الاستخدام مع ذكر المصدر**

---
</div>

- أداة تشفير أكواد Python بثلاث طبقات
- البيئة: Termux (Android) و Kali Linux
- الإصدار: v1.0



---
<div align="center">

*"حافظ على كودك، حافظ على عملك."*

***Madarik Tools — صُنع بالعربية***

⭐ **إذا أعجبتك الأداة، لا تنسَ النجمة!** ⭐
</div>
