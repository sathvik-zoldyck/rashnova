<div align="center">

<img src="assets/rashnova-banner.png" alt="Rashnova, הקופסה השחורה של המחשב הנייד שלך, מבית Alcyone Secure" width="100%">

# Rashnova

### מקליט פעילות ל-Windows שחושף כל שינוי ברישום

**מסרו את המחשב. קבלו אותו בחזרה עם רישום חתום של מה שנעשה בו.**

[![Latest release](https://img.shields.io/github/v/release/sathvik-zoldyck/rashnova?style=flat-square&label=release&labelColor=111111&color=F25C05)](https://github.com/sathvik-zoldyck/rashnova/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/sathvik-zoldyck/rashnova/total?style=flat-square&labelColor=111111&color=F25C05)](https://github.com/sathvik-zoldyck/rashnova/releases)
[![Platform](https://img.shields.io/badge/Windows-10%20%7C%2011%20%28x64%29-F25C05?style=flat-square&labelColor=111111)](#requirements)
[![Price](https://img.shields.io/badge/price-free-F25C05?style=flat-square&labelColor=111111)](#download)
[![Licence](https://img.shields.io/badge/licence-proprietary-555555?style=flat-square&labelColor=111111)](LICENSE)

[**הורדה**](https://github.com/sathvik-zoldyck/rashnova/releases/latest) ·
[**אתר**](https://www.alcyonesecure.com) ·
[**מגבלות ידועות**](KNOWN_LIMITS.md) ·
[**פרטיות**](#privacy) ·
[**אבטחה**](SECURITY.md)

</div>

> **שפות** &nbsp;·&nbsp; [English](README.md) · [हिन्दी](README.hi.md) · [ಕನ್ನಡ](README.kn.md) · [മലയാളം](README.ml.md) · [Español](README.es.md) · [Français](README.fr.md) · [Deutsch](README.de.md) · [Português](README.pt.md) · [日本語](README.ja.md) · [Bahasa Indonesia](README.id.md) · **עברית**

---
> [!NOTE]
> דף זה תורגם מאנגלית. אפליקציית Rashnova עצמה באנגלית, ולכן שמות הכפתורים והמסכים מופיעים כאן באנגלית.
> אם יש הבדל בין דף זה לבין [הגרסה באנגלית](README.md), הגרסה באנגלית היא הקובעת.

<div dir="rtl">

Rashnova מתעד מה קורה במחשב Windows בזמן שהוא אצל מישהו אחר: במעבדת תיקונים, במחלקת ה-IT, או אצל כל מי
שמוסרים לו אותו. התחילו **Repair session** לפני המסירה. כשהמחשב חוזר, סיימו אותה, ו-Rashnova נותן לכם הכרעה
(verdict) ודוח: מה נפתח, הועתק, שונה שמו ונמחק, אילו תוכנות רצו ואילו כונני USB חוברו.

כל רשומה נחתמת יחד עם הרשומה שלפניה, ולכן הרישום מראה אם משהו בו שונה או הוסר, ומראה כל פרק זמן שבו לא ניתן היה
לתעד דבר. הכול נשאר במחשב שלכם. בלי חשבון, בלי ענן, בלי טלמטריה.

</div>

> [!NOTE]
> במאגר הזה Rashnova **משוחרר**: קובצי התקנה, הערות גרסה, מגבלות ידועות ומדיניות אבטחה. Rashnova הוא תוכנה
> קניינית של [Alcyone Secure](https://www.alcyonesecure.com); קוד המקור שלה אינו מתפרסם כאן.

<div dir="rtl">

## תוכן העניינים

- [למה Rashnova קיים](#why)
- [מה הוא עושה](#what-it-does)
- [מה הוא לעולם לא מתעד](#never)
- [איך זה עובד](#how)
- [הורדה והתקנה](#download)
- [דרישות מערכת](#requirements)
- [פרטיות](#privacy)
- [מגבלות ידועות](#limits)
- [עדכונים](#updates)
- [עזרה ואבטחה](#support)
- [רישיון](#licence)

<a name="why"></a>
## למה Rashnova קיים

במטוסים, ברכבות ובאוניות יש קופסה שחורה. במחשב שיוצא מהידיים שלכם אין דבר, ולמי שמחזיק בו יש גישה לכל מה שיש
בו.

והגישה הזו מנוצלת. ב[מחקר משנת 2022 של חוקרים מאוניברסיטת Guelph](https://arxiv.org/abs/2211.05824) (שפורסם בכנס
IEEE Symposium on Security and Privacy 2023), הושארו מחשבים ניידים עם רישום פעיל ללילה אחד ב-12 מעבדות תיקונים. טכנאים
בשש מהן ניגשו למידע האישי שהיה בהם, ובשתיים העתיקו מידע מהמחשב. אנטי-וירוס וכלי אבטחת קצה מעולם לא נבנו לשים לב לכך:
לאדם הזה נמסרו המפתחות.

Rashnova אינו מניעה. הוא ראיה, כדי שאפשר יהיה לבדוק מה קרה במקום להתווכח על כך.

> *אמון זה טוב. הוכחה טובה יותר.*

<a name="what-it-does"></a>
## מה הוא עושה

<table>
<tr>
<td width="50%" valign="top">

**Repair Mode (מצב תיקון).** סשן מנוטר, שמתחיל עם ה-PIN שלכם לפני המסירה ומסתיים עם ה-PIN שלכם כשהמחשב חוזר.
הוא מתעד קבצים שנפתחו, נוצרו, שונה שמם, הועתקו ונמחקו, תוכנות שהופעלו, פקודות PowerShell שהורצו, כניסות לחשבון,
ואחסון USB שחובר, כולל כל קובץ שנכתב אליו. הפעלה מחדש, כיבוי או שינה לעולם אינם מסיימים את הסשן: הדוח מציג כל הפסקה
ואת משכה.

</td>
<td width="50%" valign="top">

<img src="assets/screenshots/session-summary.png" alt="סיכום סשן: הכרעה, האירועים הבולטים ביותר ובדיקת השרשרת">

</td>
</tr>
<tr>
<td width="50%" valign="top">

<img src="assets/screenshots/session-explorer.png" alt="סייר הסשן: כל אירוע לאורך הזמן, לפי תוכנה ולפי תיקייה">

</td>
<td width="50%" valign="top">

**רישום שאפשר לבדוק.** כל סשן מסתיים בהכרעה ובדוח שאפשר לשמור כ-PDF, כדף אינטרנט או כגיליון אלקטרוני. סייר
הסשן מציג כל אירוע לאורך הזמן, לפי תוכנה ולפי תיקייה, ובדיקת השרשרת אומרת אם הרישום שלם. מה ששומרים הוא עותק; המקור
נשאר במקום שבו Rashnova שומר אותו.

</td>
</tr>
<tr>
<td width="50%" valign="top">

**ה-Readout השבועי.** השבוע שלכם בהכרעה אחת, ולכל היותר כמה דברים ששווה להציץ בהם. סמנו כל אחד כ-"that was me"
(זה הייתי אני) או "that wasn't me" (זה לא הייתי אני). הוא גם אומר במילים פשוטות מה Rashnova יכול ומה הוא לא יכול לראות.

</td>
<td width="50%" valign="top">

<img src="assets/screenshots/weekly-readout.png" alt="ה-Readout השבועי: הכרעה לשבוע, דברים ששווה להציץ בהם, פעילות לפי יום">

</td>
</tr>
<tr>
<td width="50%" valign="top">

<img src="assets/screenshots/always-on-choice.png" alt="הבחירה בין הקלטה רק בסשנים לבין הקלטה רציפה">

</td>
<td width="50%" valign="top">

**הקלטה רציפה (always-on), רק אם תבחרו בה.** כבויה עד שתפעילו אותה. היא שומרת את מה שאי אפשר לבטל ואת מה
שמדאיג (מחיקות לצמיתות, קבצים שנראים רגישים, כל דבר שעובר אל כונן נשלף או ממנו), לא את השימוש היומיומי שלכם בקבצים
שלכם. כיבוי שלה הוא לחיצה אחת ממגש המערכת או מ-Settings, ולעולם אינו דורש PIN.

</td>
</tr>
<tr>
<td width="50%" valign="top">

**ממגש המערכת.** ראו שסשן מקליט, סיימו אותו, הריצו בדיקה של 30 שניות של פעילות קבצים בזמן אמת (Monitor Now),
או פתחו את הדוח האחרון.

</td>
<td width="50%" valign="top" align="center">

<img src="assets/screenshots/quick-panel.png" alt="החלונית המהירה במגש המערכת של Windows" width="70%">

</td>
</tr>
</table>

<sub>צילומי המסך מציגים את Rashnova עם סשן לדוגמה (משתמשת בדויה, "Riya").</sub>

**חדש ב-1.2.0:** Handover Mode, להשאלת המחשב לבני משפחה, לחבר או לעמית, עם אותו דוח חתום; חסימת אחסון USB;
ו-Start with Windows. ראו את [יומן השינויים](CHANGELOG.md).

<a name="never"></a>
## מה הוא לעולם לא מתעד

Rashnova מתעד **שמשהו** קרה, לא מה היה על המסך. הוא אינו מתעד:

- הקשות מקלדת
- תוכן הלוח (clipboard)
- את המסך שלכם, לא כתמונה ולא כווידאו
- את המצלמה או המיקרופון שלכם
- את התוכן של המסמכים, התמונות, המיילים או ההודעות שלכם
- את דפי האינטרנט שאתם מבקרים בהם, או את מה שיש בהם

כדאי לדעת על שני דברים שהוא כן מתעד. במהלך Repair session, פקודות PowerShell מתועדות בזמן הרצתן, וכך גם שורת
ההפעלה המלאה של כל תוכנה שאדם מפעיל; לכן דפדפן שנפתח מקישור מציג את הקישור הזה.

דוח אומר, לדוגמה, ש-`Bank_Statement_Aug2026.pdf` נפתח מתוך `Documents\Finance` על ידי Microsoft Edge בשעה
15:01:16. הוא אינו אומר מה היה כתוב בדף החשבון.

<a name="how"></a>
## איך זה עובד

1. **התקינו.** קובץ ההתקנה מתקין את Rashnova ואת המקליט שפועל ברקע.
2. **הגדירו PIN.** את ה-PIN בודק המקליט, לא חלון האפליקציה.
3. **לפני המסירה:** **Repair Mode > Activate**, ואז ה-PIN שלכם.
4. **מסרו את המחשב.** כל מה שמופיע ב"מה הוא עושה" נכתב לרישום חתום.
5. **כשהמחשב חוזר:** **Deactivate**, ואז ה-PIN שלכם. תקבלו הכרעה, דוח ובדיקת שרשרת.

המקליט פועל כשירות של Windows, ולכן הוא ממשיך להקליט בין אם מישהו פותח את חלון Rashnova ובין אם לא, ועולה
מחדש מעצמו אחרי הפעלה מחדש.

**כל סשן מסתיים באחת מארבע הכרעות:**

| הכרעה | משמעות |
| --- | --- |
| **Quiet** | הרישום מאומת, שלם, ולא קרה דבר בעל חשיבות גבוהה. |
| **Notable** | לפחות אירוע אחד ברמה גבוהה (high) או קריטית (critical): שווה לקרוא. |
| **Compromised** | המקליט של Rashnova נעצר בזמן ש-Windows המשיך לפעול, או שנראית ברישום התערבות, ולכן אינו יכול לערוב לסשן כולו. הפעלה מחדש, כיבוי או מצב שינה מוצגים עם משכם ואינם נחשבים נגד הסשן. |
| **Chain broken** | הרישום אינו עובר אימות. הכול עדיין מוצג, מסומן כלא מאומת. |

<a name="download"></a>
## הורדה והתקנה

| קובץ | למי |
| --- | --- |
| **`Rashnova-1.2.1.msi`** | לכולם. מתקין את Rashnova עם עותק משלו של .NET 10, כך שאין צורך להתקין שום דבר אחר קודם. |
| `SHA256SUMS.txt` | ה-SHA-256 של כל קובץ, לבדיקת ההורדה. |

1. הורידו את `Rashnova-1.2.1.msi` מ[הגרסה האחרונה](https://github.com/sathvik-zoldyck/rashnova/releases/latest). אם הדפדפן אומר שהקובץ אינו מורד לעתים קרובות, בחרו **Keep** (השלבים לכל דפדפן נמצאים ב[מגבלות ידועות](KNOWN_LIMITS.md)).
2. **בדקו את הקובץ** (מומלץ). ב-PowerShell:
   ```powershell
   Get-FileHash "$env:USERPROFILE\Downloads\Rashnova-1.2.1.msi"
   ```
   ה-hash חייב להיות זהה בדיוק לזה שב-`SHA256SUMS.txt` ובהערות הגרסה.
3. הריצו אותו. Windows SmartScreen מציג **"Windows protected your PC"** עם מפרסם לא ידוע, כי קובץ ההתקנה עדיין
   אינו חתום דיגיטלית (ראו [מגבלות ידועות](KNOWN_LIMITS.md)). בחרו **More info**, ואז **Run anyway**.
4. אשרו את [תנאי הרישיון](https://www.alcyonesecure.com/terms), התקינו ופתחו את Rashnova.
5. הגדירו PIN, ובחרו אם להישאר עם הקלטה רק בסשנים (ברירת המחדל) או להפעיל הקלטה רציפה.

</div>

> [!IMPORTANT]
> PIN שנשכח אינו ניתן לשחזור, לא על ידינו ולא על ידי אף אחד אחר. רשמו אותו במקום בטוח.
> כיבוי ההקלטה הרציפה לעולם אינו דורש את ה-PIN.

<div dir="rtl">

**מגיעים מ-1.1.0?** התקינו את 1.2.1 מעליו; הרישום, ה-PIN וההגדרות נשמרים. **מגיעים מ-BlackBox 1.0.1?** Rashnova הוא השם החדש של BlackBox. הורידו והתקינו את 1.2.1.

<a name="requirements"></a>
## דרישות מערכת

- Windows 10 או Windows 11, ‏64 סיביות (נבדק על Windows 10)
- שום דבר נוסף: Rashnova מביא עותק משלו של Microsoft .NET 10
- אישור מנהל מערכת להתקנה, כי המקליט פועל כשירות של Windows

<a name="privacy"></a>
## פרטיות

- **מקומי בלבד.** הרישום נכתב ונשמר במחשב שלכם. בגרסה זו אין חשבון ואין ענן, ו-Rashnova אינו שולח נתוני
  שימוש.
- **שתי בקשות קטנות,** ואף אחת מהן אינה כוללת דבר מהרישום שלכם: בדיקה יומית ב-alcyonesecure.com אם יש גרסה חדשה,
  ובמהלך Repair session, בדיקת השעה מול שרת הזמן של Microsoft.
- **מי יכול לקרוא את הרישום.** חשבון ה-Windows שהגדיר את ה-PIN, ומנהלי המערכת של המחשב. העותק השני מוצפן,
  ו-Rashnova פותח אותו רק אחרי שה-PIN שלכם נבדק. מנהלי המערכת של המחשב עדיין יכולים לקרוא אותו.
- **ספרו לאנשים שמשתמשים במחשב שלכם.** הקלטה רציפה חלה על כל המחשב, כולל אנשים שמעולם לא פותחים את Rashnova.
- **הגדרה אחת של Windows, בגלוי.** במהלך סשן Repair או Handover, Rashnova מפעיל את רישום הסקריפטים של PowerShell
  ב-Windows, ומחזיר אותו למצבו הקודם כשהסשן מסתיים. הוא לעולם אינו מכבה הגדרה שמישהו אחר הפעיל.

<a name="limits"></a>
## מגבלות ידועות

אנחנו מפרסמים את מה ש-Rashnova אינו עושה, כדי שתוכלו להחליט על סמך עובדות. החשובות ביותר:

- **לא ניתן לתעד דבר בזמן שהמחשב כבוי, במצב שינה או בהפעלה מחדש.** הסשן ממשיך, והדוח מציג כל הפסקה ואת משכה.
- **מנהלי מערכת יכולים לקרוא את הרישום.** אף תוכנה אינה יכולה להסתיר את הקבצים שלה ממנהל מערכת של Windows.
- **קובץ ההתקנה עדיין אינו חתום דיגיטלית,** ולכן הדפדפן ו-Windows SmartScreen עשויים להזהיר לפני ההרצה.
- **חסימת אחסון USB עוצרת כונני USB, לא כל דרך להעביר קבצים.** טלפונים, חריצי כרטיסי SD המובנים במחשב וכונני רשת אינם
  נחסמים, וכונן שכבר מחובר ממשיך לעבוד עד שמנתקים אותו.

הרשימה המלאה, עם הסיבה לכל מגבלה ומה מתוכנן (באנגלית): **[KNOWN_LIMITS.md](KNOWN_LIMITS.md)**.

<a name="updates"></a>
## עדכונים

פעם ביום Rashnova בודק ב-alcyonesecure.com אם יש גרסה חדשה ומודיע לכם. אתם מורידים ומתקינים אותה בעצמכם;
הרישום, ה-PIN וההגדרות שלכם נשמרים. כל גרסה מתפרסמת כאן עם הערות הגרסה וה-SHA-256 שלה. ראו את
[יומן השינויים](CHANGELOG.md).

<a name="support"></a>
## עזרה ואבטחה

- **עזרה:** ראו [SUPPORT.md](SUPPORT.md), או כתבו אל **support@alcyonesecure.com**.
- **באגים:** [פתחו issue](https://github.com/sathvik-zoldyck/rashnova/issues/new/choose). לעולם אל תפרסמו ב-issue את
  הרישום שלכם, שמות קבצים או כל דבר אישי.
- **פרצות אבטחה:** אל תפתחו issue ציבורי. פעלו לפי [SECURITY.md](SECURITY.md).

<a name="licence"></a>
## רישיון

Rashnova הוא תוכנה קניינית, חינמית לשימוש במכשירים שבבעלותכם או שאתם מורשים לנטר. ראו [LICENSE](LICENSE)
ואת [התנאים](https://www.alcyonesecure.com/terms) (באנגלית; הם הקובעים). המסמכים והתמונות במאגר זה הם © Alcyone Secure.

</div>

---

<div align="center">

<img src="assets/rashnova-icon.png" alt="Rashnova" width="72">

**Alcyone Secure** · נבנה בבנגלור, הודו · [alcyonesecure.com](https://www.alcyonesecure.com)

*אבטחה היא לא רק מניעה. אבטחה היא אחריותיות.*

</div>
