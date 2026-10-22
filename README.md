# גיאופוליטיקה ומשטרי שלטון בעולם – מצגת אינטראקטיבית בתלת-ממד
## Geopolitics & Global Regimes: Interactive 3D Presentation & Python Engine

מצגת אינטראקטיבית חדשנית ועשירה בקובץ HTML עצמאי יחיד (`index.html`), הכוללת סצנות תלת-ממדיות אינטראקטיביות באמצעות Three.js, מנוע הרצת קוד פייתון מקומי בדפדפן (Pyodide WebAssembly), תמיכה מלאה ומדויקת בשפה העברית ובתקני RTL ו-BiDi, עיצוב מודרני מרהיב מותאם למסך מלא (Fullscreen) וניווט רב-ערוצי.

---

## 📋 The Original Prompt (בקשת המשתמש המקורית)

```text
Create an interactive presentation in HTML format contained within a single file, including navigation buttons and the necessary control scripts.

Key Requirements:
1. Topic: Geopolitics and regimes around the world — covering democratic regimes, monarchies, and dictatorships (structures, characteristics, and global distribution).
2. Structure: Include an introductory opening slide, a well-structured series of topic slides, and a closing slide with a thank-you note (no strict limit on the exact number of slides).
3. 3D Elements: Utilize Three.js to render interactive 3D elements/visualizations directly within the slides.
4. Language & Direction: The content must be in Hebrew, properly adhering to RTL layout and BiDi standards.
5. Python Execution: In one of the slides, embed and run functional client-side Python code in the background (e.g., using Pyodide/Brython or a dedicated script runner), regardless of whether its output directly relates to the slide's visual content.
6. Display: Ensure the presentation is fully responsive, optimizes for fullscreen display, and runs smoothly in the Google Chrome browser.
7. Documentation:
   - Provide a README.md file listing all changes, version history, setup notes, and this prompt.
   - Provide a PRD.md file detailing the product requirements and project specifications. The presentation will be in Hebrew while adhering to RTL and BIDI.
```

---

## 🌟 עיקרי המערכת והתכונות המרכזיות (Key Features)

1. **קובץ יחיד ועצמאי (Single-File Architecture - `index.html`):**
   - כל ה-HTML, ה-CSS, סקריפטי ה-JavaScript, סצנות ה-3D והלוגיקה מרוכזים בקובץ יחיד.
   - אין תלות בנכסים מקומיים כבדים (תמונות, אודיו מקומי); כל האייקונים הינם קוד SVG טהור מוטמע, והצלילים מיוצרים בזמן אמת ע"י סינתסייזר Web Audio API פנימי.

2. **עברית תקנית, RTL ובידוד BiDi מדויק:**
   - כיווניות מימין לשמאל (`dir="rtl"`, `lang="he"`).
   - שימוש בגופנים מודרניים: `Heebo` לקריאות גבוהה, `Rubik` לכותרות, ו-`Fira Code` לקוד.
   - בידוד BiDi מושלם למונחים טכניים ומספרים בלועזית (כגון Three.js, Pyodide, EIU Index, GDP) באמצעות תגיות `<bdi>` וכללי `unicode-bidi: isolate;` למניעת שיבושי פיסוק.

3. **סצנות תלת-ממדיות אינטראקטיביות (Three.js):**
   - **שקף 1 (Hero):** גלובוס הולוגרפי תלת-ממדי מסתובב, מוקף בהילת חלקיקים קוסמיים (Particles Atmosphere) וטבעות מסלול גיאופוליטיות. ניתן לסיבוב ידני באמצעות גרירת עכבר.
   - **שקף 5 (דיקטטורות):** מודל תלת-ממדי של "פירמידת השליטה והדיכוי הטוטליטרית" — פירמידה בעלת 4 מפלסים צבעוניים הניתנת לסיבוב 3D מלא.
   - **שקף 8 (חוקר הגלובוס העולמי):** גלובוס תלת-ממדי שלם עם בקרת מצלמה `OrbitControls`, סמני מדינות צבעוניים לפי סוגי משטר, כפתורי סינון מהירים, ואינטראקציית Raycaster (לחיצה על מדינה פותחת פרופיל גיאופוליטי מקיף).

4. **הרצת קוד Python חי בצד הלקוח (Client-Side Pyodide WebAssembly):**
   - בשקף 7 משולב מנוע Pyodide 0.26.4 הרץ בזיכרון הדפדפן.
   - קוד פייתון אמיתי המבצע ניתוח סטטיסטי של מדד הדמוקרטיה (EIU Democracy Index), פילוח אוכלוסיות, חישוב מתאמי עושר-חירות וסימולציות מעברי משטר.
   - עורך קוד חי המאפשר למשתמש לערוך ולהריץ פקודות Python מותאמות אישית, ומסוף פלט (Terminal) אותנטי המציג `stdout` חי.

5. **שליטה וניווט רב-ערוצי:**
   - מקלדת: חיצים (חץ שמאלה = קדימה, חץ ימינה = אחורה בהתאם ל-RTL), Page Up/Down, Space, Home, End.
   - מקש `F` למסך מלא (Fullscreen).
   - מקש `M` לפתיחת מפת שקפים (Overview Drawer).
   - סרגל עליון עם פס התקדמות דינמי ומונה שקפים.
   - חיצים צפים בצדדים וכפתורי ניווט עגולים בתחתית.
   - תמיכה מלאה בהחלקת מגע (Touch Swipe) לטאבלטים ומובייל.
   - מערכת אפקטים קוליים מובנית (ניתנת להשתקה בלחיצה).

---

## 🗂 מבנה הקבצים בפרויקט (File Structure)

```
Vibe-Coding/
├── index.html       # המצגת האינטראקטיבית השלמה (קובץ יחיד עצמאי)
├── PRD.md           # מסמך דרישות המוצר ומפרט הפרויקט המפורט
└── README.md        # תיעוד, היסטוריית גרסאות, הוראות הפעלה ובקשת המשתמש
```

---

## 🚀 הוראות הפעלה והרצה (Setup & How to Run)

המצגת מותאמת באופן אופטימלי לדפדפן **Google Chrome** (וכל דפדפן מודרני מבוסס Chromium).

### אפשרות א': פתיחה ישירה בדפדפן (הכי מהיר)
1. פתח את תיקיית הפרויקט במחשבך.
2. לחץ לחיצה כפולה על הקובץ [`index.html`](file:///c:/Users/ron/OneDrive%20-%20University%20of%20Haifa/SecondYear/MyProjects/Vibe-Coding/index.html) (או גרור אותו אל תוך חלון דפדפן Google Chrome).
3. לחץ על מקש `F` (או על כפתור המסך המלא בסרגל העליון) לחוויית צפייה מיטבית.

### אפשרות ב': הרצה באמצעות שרת מקומי (Local HTTP Server)
אם ברצונך להריץ באמצעות שרת מקומי (למשל לצורך ניטור רשת או עבודה מול Web Workers):
```powershell
# הפעלת שרת פייתון מובנה בפורט 8000
python -m http.server 8000
```
לאחר מכן פתח בדפדפן Chrome את הכתובת:
`http://localhost:8000`

---

## 🗺 פירוט שקפי המצגת (Slide Deck Breakdown)

1. **שקף 1: שער – גיאופוליטיקה ומשטרי שלטון בעולם**
   - כותרת ראשית, פתיח נושאי, נתוני פתיחה (195 מדינות, 4 משפחות משטר).
   - גלובוס תלת-ממדי הולוגרפי אינטראקטיבי (Three.js) הניתן לסיבוב ע"י גרירה.
2. **שקף 2: תפיסות יסוד במדע המדינה**
   - הבחנה יסודית בין מדינה (State), משטר (Regime) וממשלה (Government).
   - הגדרת המונופול הלגיטימי על הכוח (מקס ובר) וציר החירות מול הסדר.
3. **שקף 3: המשטר הדמוקרטי – מבנה, עקרונות וגרסאות**
   - דמוקרטיה מהותית לעומת פרוצדורלית.
   - השוואה מעמיקה: דמוקרטיה פרלמנטרית, נשיאותית, וחצי-נשיאותית.
4. **שקף 4: מונרכיות בעולם המודרני: סמליות מול אבסולוטיזם**
   - מונרכיה חוקתית (בריטניה, יפן, נורווגיה) – "המלך מולך אך אינו שולט".
   - מונרכיה אבסולוטית (סעודיה, ברוניי, עומאן) – סמכות בלתי מוגבלת.
5. **שקף 5: דיקטטורות ומשטרים אוטוריטריים**
   - הבחנה בין סמכותנות (ציות פסיבי) לטוטליטריזם (שליטה נפשית ומחשבתית כוללת).
   - מודל תלת-ממדי חי של "פירמידת השליטה והדיכוי" (Three.js).
6. **שקף 6: משטרי כלאיים (Hybrid Regimes) ושחיקה דמוקרטית**
   - אלקטורליזם סמכותני ודמוקרטיות חלולות (Illiberal Democracies).
   - תופעת הנסיגה הדמוקרטית העולמית (Democratic Backsliding).
7. **שקף 7: מעבדת פייתון: ניתוח גיאופוליטי חי**
   - מנוע Pyodide Wasm הרץ ברקע.
   - חישוב התפלגויות מדד EIU, חישוב מתאם תוצר-דמוקרטיה וסימולציות.
   - עורך קוד חי ומסוף פלט אינטראקטיבי.
8. **שקף 8: חוקר הנתונים העולמי – גלובוס 3D אינטראקטיבי**
   - סצנת Three.js מלאה עם OrbitControls.
   - הדמיית כדור הארץ פוטו-ריאליסטית: יבשות, אדמה, מדבריות ואוקיינוסים כחולים עמוקים (NASA Blue Marble + פולבק פרוצדורלי מיידי).
   - שכבת עננים מרחפת ונעה עצמאית מעל האטמוספירה.
   - בורר שכבות מפה אינטראקטיבי: מפת לוויין יום, אורות לילה (Earth at Night) ומפה טופוגרפית.
   - סמני מדינות צבעוניים מוגבהים לפי סוג משטר, כפתורי סינון, וכרטיסי מידע גיאופוליטיים מפורטים בלחיצה.
9. **שקף 9: אתגרי המאה ה-21**
   - סמכותנות דיגיטלית (מעקב ביומטרי, דירוג אשראי חברתי).
   - בינה מלאכותית, דיסאינפורמציה (Deepfakes), ומשבר האקלים כמעצבי משטרים.
10. **שקף 10: סיכום, תודות ומקורות**
    - מסקנות מרכזיות על שבריריות החירות האנושית.
    - ביבליוגרפיה: The Economist Intelligence Unit (EIU), V-Dem Institute, Freedom House.
    - לחצן חזרה לראשית המצגת ולחצן הדפסה / שמירה כ-PDF.

---

## ⌨ מקשי קיצור (Keyboard Shortcuts)

| מקש | פעולה |
| :--- | :--- |
| `←` (חץ שמאלה) / `PageDown` / `רווח` | מעבר לשקף הבא (בהתאם לכיווניות עברית RTL) |
| `→` (חץ ימינה) / `PageUp` | חזרה לשקף הקודם |
| `Home` | קפיצה לשקף הראשון |
| `End` | קפיצה לשקף האחרון |
| `F` | מעבר למסך מלא / יציאה ממסך מלא |
| `M` | פתיחת/סגירת מפת השקפים (Overview Drawer) |

---

## 📝 היסטוריית גרסאות ויומן שינויים (Version History & Changelog)

### גרסה 1.1.0 (2026-10-22)
- **שדרוג מודל כדור הארץ לטקסטורה פוטו-ריאליסטית מלאה (יבשות, אדמה וים):**
  - החלפת הכדור המופשט של שקף 8 בהדמיית כדור הארץ אמיתית ומפורטת: יבשות ברורות, שטחי ירק וסוואנה, מדבריות זהובים ואוקיינוסים כחולים עמוקים.
  - מנגנון טעינה כפול (Dual-Engine Texture): יצירת טקסטורה פרוצדורלית עשירה מבוססת HTML5 Canvas בזיכרון לתצוגה מיידית, לצד טעינה חלקה של תמונת לוויין ברזולוציה גבוהה (NASA Blue Marble).
  - הוספת שכבת עננים מרחפת (Cloud Sphere) הנעה באיטיות ובאופן עצמאי מעל פני הקרקע.
  - הוספת בורר שכבות אינטראקטיבי בשקף 8:
    - 🌍 **מפת לוויין ויבשות (NASA Blue Marble)**
    - 🌌 **אורות לילה (Earth at Night)**
    - 🗺️ **מפה טופוגרפית (Topology)**
  - שדרוג גלובוס שקף הפתיחה (Hero Globe) לתצוגת יבשות מרהיבה עם הילת אטמוספירה ותאורת שמש.
  - הגבהת סמני המדינות והטבעות מעל שכבת העננים לנראות ולחיצה מיטבית.

### גרסה 1.0.0 (2026-10-22)
- **יצירת קובץ התשתית הראשי (`index.html`):**
  - הטמעת ארכיטקטורת Single-File הכוללת HTML5, CSS3 מעוצב בסגנון Geopolitical Dark Theme ו-JavaScript מודולרי.
  - הגדרת תמיכה מלאה בעברית RTL, ייבוא גופנים ייעודיים מגוגל פונטס (`Heebo`, `Rubik`, `Fira Code`) ובידוד BiDi תקני.
- **שילוב אלמנטים תלת-ממדיים ב-Three.js:**
  - פיתוח גלובוס הולוגרפי מסתובב בשקף הפתיחה עם הילת חלקיקים זוהרת.
  - פיתוח מודל 3D של פירמידת השליטה הטוטליטרית בשקף 5.
  - פיתוח חוקר כדור הארץ התלת-ממדי בשקף 8 עם OrbitControls, סמני מדינות צבעוניים ואינטראקציית Raycaster לקבלת מידע גיאופוליטי.
- **הטמעת מנוע פייתון חי בדפדפן (Pyodide):**
  - טעינת Pyodide WebAssembly ברקע לביצוע חישובים סטטיסטיים של מדדי משטרים.
  - בניית עורך קוד אינטראקטיבי ומסוף פלט (Terminal) המציג stdout חי עם כפתורי הרצה ואיפוס.
  - מנגנון גיבוי (Graceful Fallback) מקומי המבטיח הרצה חלקה גם במצב לא מקוון.
- **מערכת ניווט ובקרה מקיפה:**
  - הוספת מקשי קיצור מלאים, כפתורי חיצים צפים, תמיכה במסך מלא ומחוות מגע (Touch Swipe).
  - פיתוח סינתסייזר צלילים עצמאי מבוסס Web Audio API.
  - יצירת מגירת סקירת שקפים (Overview Modal) המאפשרת קפיצה ישירה לכל שקף.
- **תיעוד מקיף:**
  - יצירת מסמך דרישות מוצר [`PRD.md`](file:///c:/Users/ron/OneDrive%20-%20University%20of%20Haifa/SecondYear/MyProjects/Vibe-Coding/PRD.md).
  - יצירת מסמך הדרכה והיסטוריית שינויים [`README.md`](file:///c:/Users/ron/OneDrive%20-%20University%20of%20Haifa/SecondYear/MyProjects/Vibe-Coding/README.md) הכולל את פרומפט המשתמש המקורי.
