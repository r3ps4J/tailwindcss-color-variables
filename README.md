# Tailwind CSS Color Variables

All credit goes to [Merott](https://github.com/Merott). I simply took his code and made it into a package, because I wanted a cleaner looking `tailwind.config.js` in one of my projects.

From the [original gist](https://gist.github.com/Merott/d2a19b32db07565e94f10d13d11a8574):

> This is a simple Tailwind plugin to expose all of Tailwind's colors, including any custom ones, as custom css properties on the `:root` element.
>
> There are a couple of main reasons this is helpful:
>
> -   You can reference all of Tailwind's colors—including any custom ones you define—from handwritten CSS code.
> -   You can define _all_ of your colors within the Tailwind configuration, and access the final values programmatically, which isn't possible if you did it the other way around: referencing custom CSS variables (defined in CSS code) from your Tailwind config.

Used the edited code from [Maybach91](https://github.com/Maybach91)'s [comment](https://gist.github.com/Merott/d2a19b32db07565e94f10d13d11a8574?permalink_comment_id=4194451#gistcomment-4194451) to expose `--color-<name>` instead of `--color-<name>-DEFAULT`.

# How to use

Install the plugin with your preferred package manager:

```
npm install @r3ps4j/tailwindcss-color-variables --save-dev
```

Then add the plugin to your `tailwind.config.js` file:

```js
module.exports = {
	//...
	plugins: [require("@r3ps4j/tailwindcss-color-variables")],
};
```

Now you can use Tailwind's colors as CSS variables:

```css
div {
	background-color: var(--color-blue-500);
}
```
