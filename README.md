# דאשבורד פרנדוס + גדולים במדים

דאשבורד חודשי המכליל את נתוני מוקד הטלמרקטינג (פרנדוס) והסושיאל (פייסבוק, אינסטגרם, טיקטוק).

## מה יש בתיקייה

| קובץ | תפקיד |
|---|---|
| `index.html` | הדאשבורד — קובץ עצמאי שעובד בכל דפדפן |
| `data.json` | הנתונים (משוקללים מה-Excel וה-PDFs) |
| `Master-Dashboard-Data.xlsx` | מאגר הנתונים המלא ב-Excel (6 Tabs) |
| `build_master.py` | סקריפט הבנייה — יוצר מחדש את ה-xlsx וה-JSON |

## תהליך חודשי

כל חודש:
1. שלח לי לצ'אט: קובץ Excel של פרנדוס + PDF של גדולים במדים
2. אני מוסיף את הנתונים ל-`build_master.py`
3. מריץ את הסקריפט → `index.html` מתעדכן
4. דחיפה ל-GitHub → האתר מעודכן אונליין

---

## העלאה ל-GitHub Pages (פעם אחת, 10 דקות)

### 1. פתח חשבון GitHub
https://github.com/signup (חינמי)

### 2. צור ריפו חדש
- לחץ על "+" → "New repository"
- שם: `prandos-dashboard` (או כל שם)
- **חשוב:** Public (נדרש לשימוש חינמי ב-Pages)
- אל תיצור README / gitignore (יש לנו כבר)
- Create repository

### 3. העלה את הקבצים
GitHub יציג הוראות. הפשוטות ביותר:
```bash
cd /Users/zecharialandau/Zecharia-Cloude/the-system-v8/dashboard-prandos
git init
git add index.html data.json
git commit -m "Initial dashboard"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/prandos-dashboard.git
git push -u origin main
```

### 4. הפעל GitHub Pages
- בריפו → **Settings** → **Pages**
- Source: **Deploy from a branch**
- Branch: **main** → **/ (root)** → **Save**
- המתן 1-2 דקות

### 5. קבל את הקישור
`https://YOUR-USERNAME.github.io/prandos-dashboard/`

זה הקישור הקבוע — שלח לצוות.

---

## עדכון חודשי (אחרי שהאתר עובד)

```bash
# 1. עדכן את data.json או build_master.py עם הנתונים החדשים
# 2. דחוף ל-GitHub:
cd /Users/zecharialandau/Zecharia-Cloude/the-system-v8/dashboard-prandos
git add .
git commit -m "Add April 2026 data"
git push
```

תוך 30 שניות האתר מתעדכן אונליין.

---

## אבטחה

- אל תעלה את ה-xlsx המקור (מכיל מידע עסקי מפורט)
- העלה רק: `index.html`, `data.json`, `README.md`
- הנתונים המוצגים בדאשבורד הם המצרפיים בלבד (ללא שמות לקוחות, דאטה אישית וכו')
