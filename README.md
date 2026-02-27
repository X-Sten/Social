# أزرار شبكات التواصل الاجتماعي

يعرض هذا المشروع مجموعة من أزرار شبكات التواصل الاجتماعي مع تأثيرات التحويم باستخدام **HTML** و **CSS**. تمثل الأزرار المنصات الشهيرة: **إنستغرام**، **تويتر**، **جيت هاب**، و **واتساب**.

## المميزات

- تأثير التحويم: ترتفع الأزرار وتغير لونها عند المرور عليها بالماوس.
- أشكال مخصصة لكل زر بزوايا مختلفة لإطلالة عصرية.
- أيقونات SVG قابلة للتكبير بدون فقدان الجودة.
- تصميم مرن باستخدام flexbox لصفين من الأزرار.

## الترتيب

- الصف العلوي (`.up`): إنستغرام وتويتر  
- الصف السفلي (`.down`): جيت هاب وواتساب  

### ألوان التحويم

- إنستغرام → أحمر/وردي (#fd1d1d)  
- تويتر → أزرق (#24a0ed)  
- جيت هاب → أصفر (#f7b733)  
- واتساب → أخضر (#4cd137)  

تتحول الأيقونات إلى اللون الأبيض عند التحويم.

## طريقة الاستخدام

1. انسخ المشروع أو قم بتحميله.  
2. افتح ملف `index.html` في المتصفح.  
3. حرّك الماوس فوق الأزرار لمشاهدة تأثير التحويم.

## مثال الهيكلية HTML

```html
<div class="main">
  <div class="up">
    <button class="card card1">
      <!-- أيقونة إنستغرام -->
    </button>
    <button class="card card2">
      <!-- أيقونة تويتر -->
    </button>
  </div>
  <div class="down">
    <button class="card card3">
      <!-- أيقونة جيت هاب -->
    </button>
    <button class="card card4">
      <!-- أيقونة واتساب -->
    </button>
  </div>
</div>

مثال CSS
.main {
  display: flex;
  flex-direction: column;
  gap: 0.75em;
}

.up, .down {
  display: flex;
  gap: 0.75em;
}

.card {
  width: 90px;
  height: 90px;
  background: white;
  border-radius: 5px;
  border: 3px solid #2d2d2d;
  box-shadow: 6px 6px 0px #2d2d2d;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.2s cubic-bezier(0.68, -0.55, 0.27, 1.55);
}

.card:hover {
  cursor: pointer;
  transform: translate(-6px, -6px);
  box-shadow: 12px 12px 0px #2d2d2d;
}

.card1:hover { background-color: #fd1d1d; }
.card2:hover { background-color: #24a0ed; }
.card3:hover { background-color: #f7b733; }
.card4:hover { background-color: #4cd137; }

.card:hover svg { fill: white; }
