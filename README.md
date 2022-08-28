# Theme-Switcher
A simple theme switcher for web pages using CSS Custom Properties and a tiny amount of JavaScript

______
## HTML
```html
  <div class="themeSettings">
    <h2>Theme Selector</h2>
    <div class="theme red"></div>
    <div class="theme purple"></div>
    <div class="theme pink"></div>
    <div class="theme lilac"></div>

    <div class="theme midnight"></div>
    <div class="theme blue"></div>
    <div class="theme aqua"></div>
    <div class="theme khaki"></div>

    <div class="theme pine"></div>
    <div class="theme green"></div>
    <div class="theme yellow"></div>
    <div class="theme orange"></div>
  </div>
```

______
## JavaScript
```js
const themeSettings = document.querySelector('.themeSettings');

const changeTheme = (e) => {

  if (e.target.classList.contains('theme') === false) return;

  document.documentElement.dataset.theme = e.target.classList[1];
}

themeSettingsSubpanel.addEventListener('click', changeTheme, false);
```
______

## CSS
```css
:root {
  --mainBackgroundColor: var(--light);
  --mainHeadingColor: var(--lighter);
  --inputHeaderBackgroundColor: var(--darker);
  --inputHeaderBorderColor: var(--darkest);
  --inputBackgroundColor: var(--dark);
  --inputFocusedBackgroundColor: var(--light);
  --inputSelectionColor: var(--lightest);
  --buttonBackgroundGradient: radial-gradient(var(--light), var(--dark));
}

:root[data-theme="red"] {
  --lightest: rgb(223, 0, 0);
  --lighter: rgb(204, 51, 51);
  --light: rgb(191, 0, 0);
  --darkest: rgb(63, 0, 0);
  --dark: rgb(127, 0, 0);
  --darker: rgb(95, 0, 0);
}

:root[data-theme="purple"] {
  --lightest: rgb(197, 137, 168);
  --lighter: rgb(205, 51, 131);
  --light: rgb(192, 0, 99);
  --dark: rgb(128, 0, 66);
  --darker: rgb(96, 0, 50);
  --darkest: rgb(64, 0, 33);
}

:root[data-theme="pink"] {
  --lightest: rgb(255, 255, 255);
  --lighter: rgb(254, 210, 226);
  --light: rgb(255, 93, 150);
  --dark: rgb(232, 0, 82);
  --darker: rgb(174, 0, 61);
  --darkest: rgb(116, 0, 41);
}

:root[data-theme="lilac"] {
  --lightest: rgb(255, 255, 255);
  --lighter: rgb(237, 223, 241);
  --light: rgb(200, 123, 225);
  --dark: rgb(152, 44, 188);
  --darker: rgb(114, 33, 141);
  --darkest: rgb(76, 22, 94);
}

:root[data-theme="midnight"] {
  --lightest: rgb(101, 122, 139);
  --lighter: rgb(49, 94, 111);
  --light: rgb(46, 76, 102);
  --dark: rgb(39, 59, 75);
  --darker: rgb(36, 50, 62);
  --darkest: rgb(32, 42, 50);
}

:root[data-theme="blue"] {
  --lightest: rgb(35, 100, 204);
  --lighter: rgb(35, 126, 198);
  --light: rgb(35, 90, 180);
  --dark: rgb(35, 72, 131);
  --darker: rgb(35, 62, 106);
  --darkest: rgb(35, 53, 82);
}

:root[data-theme="aqua"] {
  --lightest: rgb(97, 177, 163);
  --lighter: rgb(42, 168, 146);
  --light: rgb(0, 158, 130);
  --dark: rgb(0, 106, 87);
  --darker: rgb(0, 80, 66);
  --darkest: rgb(0, 54, 44);
}

:root[data-theme="khaki"] {
  --lightest: rgb(231, 236, 230);
  --lighter: rgb(167, 192, 164);
  --light: rgb(106, 166, 100);
  --dark: rgb(69, 111, 65);
  --darker: rgb(52, 83, 49);
  --darkest: rgb(34, 54, 32);
}

:root[data-theme="pine"] {
  --lightest: rgb(35, 122, 35);
  --lighter: rgb(41, 143, 35);
  --light: rgb(35, 109, 35);
  --darker: rgb(35, 72, 35);
  --darkest: rgb(35, 60, 35);
  --dark: rgb(35, 85, 35);
}

:root[data-theme="green"] {
  --lightest: rgb(153, 207, 147);
  --lighter: rgb(69, 216, 54);
  --light: rgb(19, 202, 0);
  --dark: rgb(13, 134, 0);
  --darker: rgb(9, 100, 0);
  --darkest: rgb(6, 66, 0);
}

:root[data-theme="yellow"] {
  --lightest: rgb(243, 241, 13);
  --lighter: rgb(250, 238, 106);
  --light: rgb(252, 237, 0);
  --dark: rgb(188, 177, 0);
  --darker: rgb(152, 143, 0);
  --darkest: rgb(114, 107, 0);
}

:root[data-theme="orange"] {
  --lightest: rgb(248, 218, 198);
  --lighter: rgb(255, 151, 89);
  --light: rgb(255, 98, 3);
  --dark: rgb(172, 65, 0);
  --darker: rgb(128, 48, 0);
  --darkest: rgb(86, 32, 0);
}
```
