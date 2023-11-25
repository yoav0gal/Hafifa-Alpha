# Alpha Magic Factory Task

![The Magic Factory](../../../../Pictures/theMagicFactorypng.png)

### הקדמה

ברוך הבא לתרגיל Data Processer בוא נתנסה קצת בעבודה עם מערכים , חשיבה מחוץ לקופסא ונתרגל לרעיון של פונקציות כמשתנים.

### התרגיל

מפעל הקסמים שלנו מסוגל לקבל מידע בצורת מערך ולפי הנחיות שלנו להוציא ממנו מערך בכמעט כל צורה שנרצה.

המפעל עושה זאת בעזרת הפונקציה הבאה:

```js
function AlphaMagicFactory(
  data,
  filterFunc = () => true,
  transformFunc = (item) => item,
  sortFunc = (a, b) => b.id - a.id
) {
  return data.filter(filterFunc).map(transformFunc).sort(sortFunc);
}
```

מערך המידע שלנו במפעל נראה ככה:

```js
const products = [
  { id: 1, name: "מחשב נייד", price: 3000, category: "אלקטרוניקה" },
  { id: 2, name: "ספר תכנות", price: 120, category: "ספרים" },
  { id: 3, name: "כסא משרדי", price: 450, category: "ריהוט" },
  { id: 4, name: "טלפון חכם", price: 2400, category: "אלקטרוניקה" },
  { id: 5, name: "מקרר", price: 1500, category: "מכשירי חשמל" },
  { id: 6, name: "ספה", price: 2000, category: "ריהוט" },
  { id: 7, name: "טאבלט", price: 1400, category: "אלקטרוניקה" },
  { id: 8, name: "שולחן כתיבה", price: 800, category: "ריהוט" },
  { id: 9, name: "אוזניות אלחוטיות", price: 300, category: "אלקטרוניקה" },
  { id: 10, name: "מחברת", price: 20, category: "ספרים" },
];
```

### משימתכם:

לתת לפונקציה AlphaMagicFactory את ההוראות המתאימות כדי לקבל את ההזמנה הרצויה.

לדוגמה:
עבור מוצרי אלקטרוניה במפעל

```js
function filterElectronics(product) {
  return product.category === "אלקטרוניקה";
}

const electronics = processArrayData(products, filterElectronics);
```

#### הזמנות

- מוצרים עם האות ר
- מוצריך שמחירם מתחלק ב 300 ללא שארית מיקר לזול
- 10 הזמנות של כל מה שישי לנו במחיר גבוה מ 1000 (סכ"ה 50 מוצרים - 10 הזמנות של 5 מוצרים)
- החלף כל מוצר אלקטרוניקה בחיה (אובייקט עם שם גיל מין וסוג חיה) והחזר רק חיות וספרים ממויינים לפי ה"א-ב"
- חזר מערך של צוות אלפא (חייב עוד מהם)
- צמצם את המערך בחצי הפוך אותו לשירים (שם, אמן/להקה ואורך) ותחליף בסדר המקומות (shuffle)
- צור מצב בוא בתא הראשון מוצר אחד רנדומלי, בתא השני 2 מוצרים רנדומלים בשלישי 3 וככה עד הסוף, מיין את המערך הכולל לפי ממוצע המחירים של כל תת מערך.
- גרום לכך שבזמן המיון כל תא במערך ידפיס ערך של תא רנדומלי שונה ממנו וכל התאים יודפסו
