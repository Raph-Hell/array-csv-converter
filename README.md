<center> <h3> ARRAY TO CSV CONVERTER </h3> </center>

---

##### TO USE

-   Import the `CSV` class.

```js
import CSV from "./csv.js";
```

-   Create a new instance of the `CSV` class and enter the `array` and the `name` you want the file to have as parameter.

```js
const name = "productsTable";
const array = [
    {
        id: 1,
        name: "Rice",
        price: "100",
        currency: "NGN",
        category: "Food",
    },
    {
        id: 2,
        name: "Beans",
        price: "80",
        currency: "NGN",
        category: "Food",
    },
    {
        id: 3,
        name: "Laptop",
        price: "86000",
        currency: "NGN",
        category: "Tech",
    },
];

// Instance of the CSV class
const csv = new CSV(array, name);
```

-   To download the file, simply call the csv method `download()`.

```js
csv.download();

/* 
    The download will start automatically.
    For best practice add the download() in a "click" event.
*/
```

---

###### Example

`index.html`

```html
<!DOCTYPE html>
<html>
    <head>
        <title>CSV</title>
        <script type="module" src="main.js" defer></script>
    </head>
    <body>
        <button>Download File</button>
    </body>
</html>
```

> `IMPORTANT!: The <script> tag MUST contain the type="module" for the import to be successful.`

---

`main.js`

```js
import CSV from "./csv.js";

const btn = document.querySelector("button");

const name = "productsTable";
const array = [
    {
        id: 1,
        name: "Rice",
        price: "100",
        currency: "NGN",
        category: "Food",
    },
    {
        id: 2,
        name: "Beans",
        price: "80",
        currency: "NGN",
        category: "Food",
    },
    {
        id: 3,
        name: "Laptop",
        price: "86000",
        currency: "NGN",
        category: "Tech",
    },
];

const csv = new CSV(array, name);

btn.onclick = () => {
    csv.download();
};
```

---

###### Image Guild

![click](/img/click.jpg)
![file](/img/file.jpg)
![downloaded](/img/downloaded.jpg)
![csv](/img/csv.jpg)

> Note: To avoid CORS errors the page needs to be served on a host. Fortunately, VScode and other IDEs out there already have an extension that can help with that. You may also use XAMMP or WAMP or any other local server machine you know. :)

...and that's it.

---

### JACE ALEXANDER

###### Contact me on

[Facebook](https://facebook.com/chidindu.aneke)
[Gmail](mailto:alexjace151@gmail.com)
#   a r r a y - c s v - c o n v e r t e r  
 