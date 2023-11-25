# שאלות הבנה React 01

![React Logo](../../../Pictures/react.jpg)

## הקדמה

בקובץ זהה שאלות ומשימות הבנה שמטרתן לעזור למה שלמדת לשקוע ולהיזכר יותר טוב!
יש לשמור את התשובות בקובץ נפרד ולעבור עליהן עם החופף.

**במידה ואתם לא יודעים את אחת התשובות (זה בסדר) נסו להיעזר באינטרנט**.

---

## שאלות הבנה

#### מהיא React ומה מקור השם?

#### מה ההגדרה לMPA & SPA?

#### ציין 2 אלטרנטיבות לReact?

#### מהו הDOM? מהו הVirtual DOM? ומה ההבדל בינהם?

#### מה זה JSX?

#### מהיא קומפוננטה?

#### מהו State?

#### מתי קומפוננטה מתרנדרת מחדש?

#### מה הם Hooks?

## משימות

#### Hooks!

עבור כל אחד מההוקים הבאים הסבר מה תפקידו ותן דוגמה מילולית + קוד לשימוש בו.

- `useState`
- `useEffect`
- `useReducer`
- `useContect`
- `useCallBack`
- `useMemo`

**עבור useEffect תן דוגמה לאיך להריץ בעת הוספה והסרה מהDOM**

---

#### תקן את הבאגים

לפניך מספר קטעי קוד בעייתים, עבור כל קטע קוד, הסבר את הבעיות בו ותקן אותן.

1.

```jsx
import React from "react";
import ShoppingList from "./ShoppingList";

function App() {
  const [items, setItems] = React.useState([]);

  return <div>{items.length && <ShoppingList items={items} />}</div>;
}

export default App;
```

2.

```jsx
import React from "react";
import ShoppingList from "./ShoppingList";
import NewItemForm from "./NewItemForm";

function App() {
  const [items, setItems] = React.useState(["apple", "banana"]);

  function handleAddItem(value) {
    items.push(value);
    setItems(items);
  }

  return (
    <div>
      {items.length > 0 && <ShoppingList items={items} />}
      <NewItemForm handleAddItem={handleAddItem} />
    </div>
  );
}

export default App;
```

3.

```jsx
import React from "react";

function ShoppingList({ items }) {
  return (
    <ul>
      {items.map((item) => {
        return <li>{item}</li>;
      })}
    </ul>
  );
}

export default ShoppingList;
```

4.

```jsx
import React from "react";

function App() {
  const [count, setCount] = React.useState(0);

  function handleClick() {
    setCount(count + 1);

    console.log({ count });
  }

  return <button onClick={handleClick}>{count}</button>;
}

export default App;
```

5.

```jsx
import React from 'react';
import { API } from './constants';

function UserProfile({ userId }) {
  const [user, setUser] = React.useState(null);

  React.useEffect(() => {
    const url = `${API}/get-profile?id=${userId}`;
    const res = await fetch(url);
    const json = await res.json();

    setUser(json.user);
  }, [userId]);

  if (!user) {
    return 'Loading…';
  }

  return (
    <section>
      <dl>
        <dt>Name</dt>
        <dd>{user.name}</dd>
        <dt>Email</dt>
        <dd>{user.email}</dd>
      </dl>
    </section>
  );
}

export default UserProfile;

```

#### כתוב 3 שאלות נוספתו שאפשר לשאול על מה שלמדת עד עכשיו שיהיה אפשר לשאול את הנחפפים הבאים.
