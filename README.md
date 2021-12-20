# FnonSticky

Is a simple javascript file that creates a sticky note into a website similar to the windows sticky app.

> Try me [DEMO](https://superawdi.github.io/FnonSticky/)

![Demo](/demo.gif)

## Installation :

> [Use node package manager](https://www.npmjs.com/package/fnonsticky) :

```bash
npm i fnonsticky
```

> Add (css and js) to HTML

```html
<link rel="stylesheet" href="fnonsticky.min.css" />

<script src="dist/fnonsticky.js"></script>
```

>### How to use:

```js
// Simple Call
// @param1 {string}: Required, message text.
FnonSticky.Create("Good Morning Me\nCall your mother.");
// Advanced Call
// @param1 {string}: Required, message text.
// @param2 {Object}: Optional,update default settings if you need to.
FnonSticky.Create("Good Morning Me\nCall your mother.", {
  animate: true, // set false if you want to disable entrance animation
  background: null, // change the note background
  color: null, // change text color
  hidePin: false, // hide the red pin at the left-top corner
  identifier: null, // see explaination below...
  initWidth: null, // initial width of the note
  onClose: null, // function fires on note closing
  onLoaded: null, // function fires on note loaded
  saveOnRefresh: false, //if you want to save note in case of page refresh. note will be stored in sessionStorage and will load back on page loaded.
  showTime: true, // show time part at the bottom right corner
  time: null, // if null creating time will be placed. you can write anything here but the default was for time.
  zIndex: 10, // sticky z-index
});
```

>## identifier option 
> First of all, you need to know that **identifier** will not do any changes if **saveOnRefresh** is set to **false**. the identifier is a simple string that helps identify which notes belong to a user. In case you are going to use **FnonSticky** on a multiuser website and you want to store notes on **sessionStorage** and the current user just logged out and another user just logged in back within the same session, the notes will be displayed back if the identifier is not set to differentiate the users


---
>### Change Default Settings
> You can change FnonSticky default settings simply as shown:

```js
FnonSticky.DefaultSettings.identifier="Username";
FnonSticky.DefaultSettings.background="red";
FnonSticky.DefaultSettings.color="green";
FnonSticky.DefaultSettings.hidePin=true;

// if you call create function now,  changed options will be applied unless you provided another options in the create function second parameter
```

---

## Final Word

Mother is an excellent example of love, affection, and sacrifice. So show the love to your mothers before it's too late, and `PLEASE PRAY FOR MY MOTHER.`

**I love you 𝔉𝔫𝔬𝔫**

---

## License

[MIT License](https://opensource.org/licenses/MIT)
