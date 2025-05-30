<div dir="rtl">

# מטלה מספר 4 - מיכלים

### יושרה אקדמית

במהלך העבודה על המטלות, מותר להתייעץ עם סטודנטים אחרים ולחפש מידע באינטרנט. עם זאת, חל איסור להעתיק קטעי קוד שלמים ממקורות חיצוניים, כולל סטודנטים אחרים, אתרי אינטרנט ומודלי בינה מלאכותית (כגון ChatGPT).

יש לדווח על כל עזרה שקיבלתם, בין אם מדובר בהתייעצות עם סטודנטים אחרים או במידע שנמצא באינטרנט, בהתאם ל[תקנון היושר של המחלקה](https://www.ariel.ac.il/wp/cs/wp-content/uploads/sites/88/2020/08/Guidelines-for-Academic-Integrity.pdf).
**במקרה של שימוש בכלי בינה מלאכותית (AI), יש לצרף את הפרומפטים שהוזנו ואת התשובות שהתקבלו**.

-----
* **מטרת המטלה:** הבנת החומר הנלמד בהרצאות - 7,8,9 ו-10 כגון: תבניות, פונקטורים, מיכלים ואיטרטורים.
* **שימו לב!** ההגשה של המטלה ביחידים.

---

## הוראות הגשה ב Moodle:

במערכת Moodle יש להגיש **קובץ טקסט למשל (`submission.txt`)** המכיל 3 שורות בפורמט הבא:

1. **תעודת זהות** – מספר תעודת הזהות של הסטודנט.
2. **קישור להגשה** – קישור למאגר ה-GitHub שבו נמצא הפרויקט.
3. **פרטי ה-commit האחרון** – המחרוזת המזהה של ה-commit האחרון (`commit hash`) 

 - דוגמה לקובץ הגשה תקין:
```
123456789
https://github.com/example-user/assignment
e3f1c1a 
```

---

במטלה הזאת אתם תממשו מיכלים עבור טיפוסים הניתנים להשוואה (comparable) ותממשו סוגים שונים של איטרטורים בתוך אותם המיכלים.

---

## דרישות המטלה:

### מימוש המחלקות הבאות:

הוסיפו את המחלקות במרחב שמות (namespace) חדש לבחירתכם.

#### מחלקה בשם `MyContainer`:
הקונטיינר מכיל עצמים הניתנים להשוואה (כגון, integers, doubles, string) והוא מאפשר הוספה ומחיקה של איברים בצורה דינאמית. במטלה מוגדר שבאופו דיפולטיבי הקונטיינר יכיל מספרים שלמים. עליכם לתמוך בכל סוגי העצמים.

עליכם להוסיף את הפעולות הבאות:

- הוספת איבר חדש - add - הפעולה מקבלת איבר ומכניסה אותו לקונטיינר
- מחיקת איבר קיים - remove - הפעולה מקבלת איבר ומוחקת אותו מהקונטיינר. אם האיבר לא קיים יש לזרוק שגיאה מתאימה. במידה והאיבר קיים כמה פעמים, הפעולה תמחוק את כל המופעים שלו מהקונטיינר.
- מתודה בשם size המחזירה את גודל הקונטיינר (כלומר כמות האיברים הנמצאת בתוכו).
- אופרטור פלט המדפיס את הקונטיינר בצורה הגיונית לבחירתכם.

* יש לבדוק את תקינות הקלט ולזרוק שגיאות במידת הצורך. בנוסף עליכם לכתוב טסטים לכל הפונקציות שכתבתם.

בנוסף, עליכם לממש את האיטרטורים הבאים: AscendingOrder, DescendingOrder, SideCrossOrder, ReverseOrder, Order, MiddleOutOrder

כאשר:

- האיטרטור AscendingOrder סורק את הקונטיינר בצורה עולה (כלומר מהאיבר הקטן ביותר לאיבר הגדול ביותר) למשל, עבור הקונטיינר [7,15,6,1,2] סדר הסריקה (משמאל לימין) יהיה 1,2,6,7,15    
- האיטרור DescendingOrder סורק את הקונטיינר בצורה יורדת (כלומר מהאיבר הגדול ביותר לאיבר הקטן ביותר) למשל, עבור הקונטיינר [7,15,6,1,2] סדר הסריקה (משמאל לימין) יהיה 15,7,6,2,1
- האיטרטור SideCrossOrder סורק את הקונטיינר בצורה עולה ויורדת - קודם האיבר הקטן ביותר ולאחריו האיבר הגדול ביותר וכן הלאה. למשל, עבור הקונטיינר [7,15,6,1,2] סדר הסריקה (משמאל לימין) יהיה 1,15,2,7,6 
- האיטרטור ReverseOrder סורק את הקונטיינר בצורה הפוכה. למשל, עבור הקונטיינר [7,15,6,1,2] סדר הסריקה (משמאל לימין) יהיה 2,1,6,15,7
- האיטרטור Order סורק את הקונטיינר בצורה רגילה. למשל, עבור הקונטיינר [7,15,6,1,2] סדר הסריקה (משמאל לימין) יהיה 7,15,6,1,2
- האיטרטור MiddleOutOrder סורק קודם כל את האיבר האמצעי, ולאחר מכן פונה לאיבר השמאלי ואז הימני. כלומר הסדר הוא אמצע ולאחר מכן שמאל-ימין (כאשר פעם אחת נסרק איבר משמאל ופעם אחת נסרק איבר מימין, במידה ומספר האיברים הוא זוגי אתם יכולים לבחור בעצמכם אם האינדקס של האיבר האמצעי יעוגל כלפי מעלה או מטה). למשל, עבור הקונטיינר [7,15,6,1,2] סדר הסריקה (משמאל לימין) יהיה 6,15,1,7,2

**שימו לב** שכל איטרטור חייב להכיל מתודות ``begin`` ו-``end`` ואת האופרטורים הרלוונטיים המאפשרים סריקה של קונטיינרים וגישה לאיברים.

מצורף קובץ דמו (``Demo.cpp``) המדגים את דרישות המטלה.

---


#### דרישות נוספות:

- חשוב לוודא שה-repository ציבורי.
- כתבו בתחילת **כל** קובץ את כתובת המייל שלכם.
- כתבו קוד נקי, מסודר, מחולק לקבצים, מודולרי, מתועד בצורה מספקת וכמובן בדיקות יחידה עבור כל הפונקציות.
- בדקו את תקינות הקלט ולזרוק חריגות מתאימות במידת הצורך.
- לשימושכם הקישור הבא [doctest](https://github.com/doctest/doctest) בו תוכלו לראות דוגמאות נוספות לשימוש בסיפריה זו.
- יש לבדוק שאין זליגת זיכרון באמצעות `valgrind`.
- יש לצרף גם קובץ `README` עם הסבר על פרויקט, על חלוקה למחלקות וקבצים וכל מידע אחר רלוונטי.


#### קובץ `Makefile`:
הוסיפו לפרויקט קובץ `Makefile` הכולל את הפקודות הבאות:
- הפקודה `make Main` – להרצת קובץ ההדגמה.
- הפקודה `make test` – להרצת בדיקות היחידה.
- הפקודה `make valgrind` – בדיקת זליגת זיכרון באמצעות valgrind.
- הפקודה `make clean` - מוחקת את כל הקבצים הלא רלוונטיים לאחר ההרצה.


בהצלחה!


</div>
