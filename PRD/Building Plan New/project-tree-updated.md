# עץ קבצי הפרויקט המעודכן

## מקרא סימונים
- ✅ = קיים ועובד, לא לגעת
- 🔄 = קיים, דורש שינוי/עדכון
- ➕ = חדש, צריך ליצור
- ❌ = למחיקה
- 📝 = קיים אבל ריק, צריך למלא

```
bid-optimizer-mockup/
│
├── .streamlit/
│   └── config.toml                      ✅ (תצורת סטרימליט - עובד)
│
├── app/
│   ├── main.py                          ✅ (נקודת כניסה ראשית)
│   ├── pages/                           ❌ (תיקייה ריקה - למחיקה)
│   ├── state/
│   │   └── session.py                   🔄 (להוסיף מונה איטרציות)
│   └── ui/
│       ├── layout.py                    ✅ (עיצוב ופריסה)
│       ├── messages.py                  🔄 (להוסיף פינק נוטיס)
│       ├── style.py                     ✅ (עיצוב מותאם אישית)
│       ├── widgets.py                   ✅ (רכיבי יו-איי)
│       └── tabs/
│           ├── upload_tab.py            ✅ (טאב אפלואוד עובד)
│           ├── validate_tab.py          🔄 (400 שורות - דורש הפרדת לוגיקה)
│           └── output_tab.py            🔄 (לחבר לקבצי אאוטפוט אמיתיים)
│
├── config/
│   ├── constants.py                     ✅ (קבועים)
│   ├── settings.py                      ✅ (הגדרות)
│   └── ui_text.py                       ✅ (טקסטים למשתמש)
│
├── core/
│   ├── errors/
│   │   └── messages.yaml                ✅ (הודעות שגיאה)
│   ├── io/
│   │   ├── readers.py                   🔄 (לבדוק שעובד)
│   │   └── writers.py                   🔄 (לבדוק שעובד)
│   ├── mapping/
│   │   └── virtual_map.py               📝 (ריק - קריטי למימוש)
│   ├── output/
│   │   ├── files_builder.py             🔄 (להוסיף שמות דינמיים)
│   │   └── filenames.py                 ❌ (למחוק - להעביר לפיילס בילדר)
│   ├── checklist/                       ❌ (תיקייה ריקה - למחוק)
│   └── validate/
│       ├── bulk_cleanse.py              🔄 (לשפר סינון)
│       ├── portfolio_comparison.py      📝 (ריק - קריטי למימוש)
│       ├── completion_validator.py      📝 (ריק - קריטי למימוש)
│       └── titles.py                    ✅ (בדיקת כותרות)
│
├── models/
│   ├── file_schemas.py                  ✅ (סכמות קבצים)
│   ├── portfolio.py                     📝 (ריק - למימוש)
│   ├── state.py                         📝 (ריק - למימוש)
│   └── step2_models.py                  📝 (ריק - למימוש)
│
├── optimizers/
│   ├── base.py                          📝 (ריק - למימוש תשתית)
│   └── zero_sales/
│       ├── optimizer.py                 📝 (ריק - למימוש מוקאפ)
│       └── processors/
│           ├── data_cleaner.py          📝 (ריק)
│           └── sheet_creator.py         📝 (ריק)
│
├── services/
│   ├── file_io/                         ❌ (כפילות עם core/io - למחוק)
│   ├── portfolio_service.py             📝 (ריק - אופציונלי)
│   ├── step2_service.py                 📝 (ריק - קריטי למימוש)
│   ├── virtual_map_service.py           ❌ (כפילות - למחוק)
│   └── validation/
│       ├── data_validator.py            ✅ (ולידציית נתונים)
│       └── file_validator.py            ✅ (ולידציית קבצים)
│
├── utils/
│   ├── debug_manager.py                 ➕ (להוסיף לדיבאג)
│   ├── file_utils.py                    ✅ (פונקציות עזר לקבצים)
│   ├── format_utils.py                  ➕ (להוסיף עיצוב מספרים)
│   └── session_manager.py               ❌ (כפילות עם app/state - למחוק)
│
├── tests/
│   ├── fixtures/
│   │   ├── valid/                       ➕ (תיקייה לקבצי בדיקה תקינים)
│   │   ├── invalid/                     ➕ (תיקייה לקבצי בדיקה שגויים)
│   │   └── edge_cases/                  ➕ (תיקייה למקרי קצה)
│   ├── test_virtual_map.py              ➕ (טסטים לוירטואל מאפ)
│   ├── test_step2_service.py            ➕ (טסטים לסרוויס)
│   └── test_integration.py              ➕ (טסטים לזרימה מלאה)
│
├── PRD/                                  ✅ (מסמכי איפיון)
├── docs/
│   ├── development/
│   │   ├── phase0-cleanup-checklist.md  ➕
│   │   ├── phase1-core-logic.md         ➕
│   │   ├── phase2-service.md            ➕
│   │   ├── phase3-ui.md                 ➕
│   │   ├── phase4-output.md             ➕
│   │   └── phase5-testing.md            ➕
│   ├── missing-functions.md             ➕
│   ├── flow-diagrams.md                 ➕
│   └── faq.md                           ➕
│
├── .gitignore                            ✅
├── README.md                             🔄 (לעדכן הוראות הרצה)
├── requirements.txt                      ✅
├── __init__.py                           ❌ (בשורש - למחוק)
├── Empty Template Example.xlsx          ✅ (קובץ דוגמה)
└── Bulk File Example.xlsx                ✅ (קובץ דוגמה)
```

## סיכום פעולות נדרשות

### למחיקה (7 קבצים/תיקיות)
- `app/pages/`
- `services/file_io/`
- `services/virtual_map_service.py`
- `utils/session_manager.py`
- `core/checklist/`
- `core/output/filenames.py`
- `__init__.py` (בשורש)

### קבצים קריטיים למימוש (4 קבצים)
1. **`core/mapping/virtual_map.py`** - הלב של המערכת
2. **`services/step2_service.py`** - לוגיקה עסקית ראשית
3. **`core/validate/portfolio_comparison.py`** - השוואת פורטפוליוז
4. **`core/validate/completion_validator.py`** - ולידציית קומפלישן

### קבצים לעדכון (8 קבצים)
1. `app/state/session.py` - הוספת מונה איטרציות
2. `app/ui/messages.py` - הוספת פינק נוטיס
3. `app/ui/tabs/validate_tab.py` - הפרדת לוגיקה (400→100 שורות)
4. `app/ui/tabs/output_tab.py` - חיבור לקבצים אמיתיים
5. `core/io/readers.py` - וידוא שעובד
6. `core/io/writers.py` - וידוא שעובד
7. `core/output/files_builder.py` - שמות דינמיים
8. `core/validate/bulk_cleanse.py` - שיפור סינון

### קבצים חדשים להוספה (15 קבצים)
- 6 מסמכי פרקי בנייה
- 3 קבצי טסטים
- 2 קבצי יוטילס
- 4 מסמכי תיעוד

### סטטיסטיקה
- **קבצים קיימים שעובדים**: 20
- **קבצים למחיקה**: 7
- **קבצים ריקים למימוש**: 12
- **קבצים לעדכון**: 8
- **קבצים חדשים**: 15

## עדיפות מימוש לפי ימים

### יום 0 (2 שעות)
- מחיקת כל הקבצים המסומנים ❌

### יום 1
- `core/mapping/virtual_map.py`
- `core/validate/portfolio_comparison.py`
- `core/validate/bulk_cleanse.py` (עדכון)

### יום 2
- `services/step2_service.py`
- `app/state/session.py` (עדכון)
- `core/validate/completion_validator.py`

### יום 3
- `app/ui/tabs/validate_tab.py` (ריפקטור)
- `app/ui/messages.py` (עדכון)

### יום 4
- `app/ui/tabs/output_tab.py` (עדכון)
- `core/output/files_builder.py` (עדכון)
- `optimizers/zero_sales/optimizer.py`

### יום 5
- בדיקות בלבד
- תיקוני באגים
- תיעוד סופי