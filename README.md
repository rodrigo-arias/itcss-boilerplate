# ITCSS boilerplate

Sass project boilerplate following the ITCSS architecture and BEM naming convention

## What is ITCSS
ITCSS stands for Inverted Triangle CSS and it helps you to organize your project CSS files in such a way that you can better deal with CSS specifics like global namespace, cascade and selectors specificity.

One of the key principles of ITCSS is that it separates your CSS codebase to several sections (called layers), which take the form of the inverted triangle.

![triangle](https://www.xfivecdn.com/xfive/wp-content/uploads/2016/02/01083650/itcss-layers2.svg)

Those layers are as follows:

* Settings – used with preprocessors and contain font, colors definitions, etc.
* Tools – globally used mixins and functions. It’s important not to output any CSS in the first 2 layers.
Generic – reset and/or normalize styles, box-sizing definition, etc. This is the first layer which generates actual CSS.
* Elements – styling for bare HTML elements (like H1, A, etc.). These come with default styling from the browser so we can redefine them here.
* Objects – class-based selectors which define undecorated design patterns, for example media object known from OOCSS
* Components – specific UI components. This is where the majority of our work takes place and our UI components are often composed of Objects and Components
* Utilities – utilities and helper classes with ability to override anything which goes before in the triangle, eg. hide helper class

## What is BEM
BEM — Block Element Modifier is a methodology that helps you to create reusable components and code sharing in front-end development.

* Block – Standalone entity that is meaningful on its own.
* Element – A part of a block that has no standalone meaning and is semantically tied to its block.
* Modifier – A flag on a block or element. Use them to change appearance or behavior.

```html
<button class="button">
	Normal button
</button>
<button class="button button--state-success">
	Success button
</button>
<button class="button button--state-danger">
	Danger button
</button>
```

```css
.button {
	display: inline-block;
	border-radius: 3px;
}
.button--state-success {
	color: green;
}
.button--state-danger {
	color: red;
}
```

## License
[MIT](https://choosealicense.com/licenses/mit/)