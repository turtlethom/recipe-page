# Frontend Mentor - Recipe page solution

This is a solution to the [Recipe page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/recipe-page-KiTsR8QQKm). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)


## Overview

### Screenshot

#### **Desktop View**
![](/assets/screenshots/recipepage-desktop.png)
#### **Mobile View**
![](/assets/screenshots/recipepage-mobile.png)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 Markup
- CSS Custom Properties
- CSS Functions (clamp, min, max...)
- CSS Grid

## What I learned

### Tables And Its Child Elements
```html
<table>
  <tr class="nutrition-item">
    <td>Calories</td>
    <td>277kcal</td>
  </tr>
  <tr class="row-divider">
    <td colspan="2" class="custom-hr"></td>
  </tr>
  ...
  </table>
```
```css
.nutrition-item td {
    padding: 1rem;
}

.nutrition-item td:last-child {
    color: var(--brown-800-color);
    font-weight: 700;
}

.custom-hr {
    border-top: 1px solid var(--stone-150-color);
}
```

I have never used a table within HTML before and it was eye-opening to learn what the `<tr>` and `<td>` elements could do as well as how they can be styled.

I would now use tables because:
- Similar to grid
- Better than just using a bunch of non-semantic `<div>`'s

I also discovered I had to create a custom `<hr>` style in order for it to be shown within the table.
- There could be a better way of putting the dividers between rows, but this was my solution.

### Learned About `:not()` Operator
```css
.container > *:not(:first-child) {
  color: var(--stone-600-color);
    font-family: var(--outfit-font);
}

```
  Instead of using a utility class and applying it tediously to every paragraph tag to change the text color, I figured out I could select each container by not including the first child (heading).
  - Makes the CSS more maintainable
  - Can easily change color of paragraphs across entire page in one area.
### Use of The `Owl (* + *)` Operator
```css
* + * {
    margin-top: 1rem;
}
```

This CSS selector made it easier to apply margins and control the flow of the content on the page without being repetitive with applying `margin-top` everywhere.
- Reduced bloating the base CSS file.

### Continued development

Personally, I'd love to work on these concepts more:
- Avoiding unnecessary redundancies in CSS.
- Understand when to utilize CSS `LOCAL` variables.
- Creating more useful CSS utility classes.
- Avoid colliding styles (know more about CSS Specificity)

### Useful resources

- [Axiomatic CSS and Lobotomized Owls](https://alistapart.com/article/axiomatic-css-and-lobotomized-owls/) - This helped me understand the owl operator and why it's useful. I will definitely be using this more and recommend others to learn more about it.
- [Kevin Powell](https://www.youtube.com/@KevinPowell) - By far, Kevin is the **BEST** teacher I've found when learning about the fundamentals of CSS. When it comes to simple CSS principles to more advanced techniques in web design, Kevin is the undisputed GOAT!

## Author

- Website - [Add your name here](https://www.your-site.com)
- Frontend Mentor - [@turtlethom](https://www.frontendmentor.io/profile/turtlethom)
- Twitter - [@wjamesthomas3](https://x.com/wjamesthomas3)
