# רדיו הקול שלנו – היועצים: מדריך העלאה ועריכה

האתר בנוי משלושה חלקים:

* **הדף עצמו**, בקובץ `index.html`.
* **כל הטקסטים**, בקובץ `content/site.json`.
* **מערכת עריכה עם סיסמה**, שנפתחת בכתובת `/admin`.

ההקמה נעשית פעם אחת ולוקחת בערך 20 דקות. אחריה עורכים הכול מהדפדפן, גם מהטלפון.

---

## שלב 1: חשבון GitHub (המקום שבו שמורים קבצי האתר)

1. נרשמים בחינם ב־https://github.com/signup.
2. לוחצים על **+** למעלה, ואז על **New repository**.
3. בשדה Repository name כותבים: `radio-hakol-yoatzim`. בוחרים **Public** ולוחצים **Create repository**.
4. בעמוד שנפתח לוחצים על **uploading an existing file**.
5. פותחים את קובץ ה־ZIP במחשב וגוררים לחלון **את כל התוכן שבתוכו**: התיקיות `admin`, `content`, `images` והקבצים. לא גוררים את התיקייה החיצונית.
6. לוחצים **Commit changes**.

## שלב 2: עדכון שורה אחת במערכת העריכה

1. ב־GitHub נכנסים לתיקייה `admin` ופותחים את הקובץ `config.yml`.
2. לוחצים על סמל העיפרון ✏️.
3. בשורה `repo: YOUR-GITHUB-USERNAME/radio-hakol-yoatzim` מחליפים את `YOUR-GITHUB-USERNAME` בשם המשתמש שלך ב־GitHub.
4. לוחצים **Commit changes**.

## שלב 3: העלאה ל־Netlify (אחסון ודומיין בחינם)

1. נרשמים בחינם ב־https://app.netlify.com/signup, בעדיפות עם **Sign up with GitHub**.
2. לוחצים **Add new project**, ואז **Import an existing project**, ואז **GitHub**.
3. בוחרים את המאגר `radio-hakol-yoatzim` ולוחצים **Deploy**. לא צריך לשנות אף הגדרה.
4. אחרי כדקה האתר באוויר, בכתובת כמו `something.netlify.app`.
5. כדי לשנות את הכתובת: **Project configuration**, ואז **Change project name**. למשל `radio-yoatzim`, והכתובת תהיה `radio-yoatzim.netlify.app`.

## שלב 4: חיבור הכניסה למערכת העריכה

1. ב־GitHub נכנסים ל־https://github.com/settings/developers ולוחצים **New OAuth App**.
2. ממלאים:
   * **Application name**: `Radio CMS`
   * **Homepage URL**: כתובת האתר שלך ב־Netlify
   * **Authorization callback URL**: `https://api.netlify.com/auth/done`
3. לוחצים **Register application**.
4. מעתיקים את **Client ID**.
5. לוחצים **Generate a new client secret** ומעתיקים גם אותו. הוא מוצג פעם אחת בלבד.
6. חוזרים ל־Netlify. בתוך הפרויקט נכנסים ל־**Project configuration**, ואז **Security**, ואז **OAuth**, ואז **Install provider**.
7. בוחרים **GitHub**, מדביקים את שני הקודים ושומרים.

## עריכה מעכשיו והלאה

1. נכנסים לכתובת האתר עם `/admin` בסוף, למשל `radio-yoatzim.netlify.app/admin`.
2. לוחצים **Login with GitHub**.
3. בוחרים **תוכן האתר**, ואז **דף הבית**. כל הטקסטים, התמונות, היתרונות ומספר הוואטסאפ ניתנים לעריכה.
4. לוחצים **Publish**. תוך כדקה השינוי מופיע באתר.

**טיפים**

* בשדות "שורה לכל משפט" ו"פסקה לכל שורה", כל Enter יוצר שורה חדשה באתר.
* מספר הטלפון מתעדכן אוטומטית בכל כפתורי הוואטסאפ ובקישורים שלהם.
* תמונה חדשה מעלים ישירות מתוך שדה התמונה במערכת העריכה.

## דומיין משלכם (לא חובה)

אם בהמשך תרכשו דומיין, למשל `radio-yoatzim.co.il`, מחברים אותו כך: ב־Netlify נכנסים ל־**Domain management**, ואז **Add a domain**, וממשיכים לפי ההוראות. תעודת האבטחה (https) ניתנת בחינם.
