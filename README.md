# @fkui-community/theme-int

This theme is designed for applications used regularly by experienced users, such as case management tools and other internal systems at Försäkringskassan.

## Usage

`npm i @fkui-community/theme-int`

Then import it into your Sass stylesheet:

```scss
@use "@fkui-community/theme-int";
```

## Color mode (light/dark)

The `data-color-mode` attribute on the `<html>` element controls the color mode. If the attribute is omitted, the theme uses light mode.

| Value               | Behavior                                                   |
| ------------------- | ---------------------------------------------------------- |
| (attribute omitted) | Light mode.                                                |
| `light`             | Light mode.                                                |
| `dark`              | Dark mode.                                                 |
| `auto`              | Follows the user's browser or operating system preference. |

To make the application follow the user's browser or operating system preference, set `data-color-mode="auto"`:

```html
<html data-color-mode="auto">
    ...
</html>
```

The theme reads only this attribute. To let users change the color mode in your application, update the attribute. For example, to enable dark mode:

```js
document.documentElement.dataset.colorMode = "dark";
```

### Always auto (`/auto`)

If the application should always follow the user's browser or operating system preference, import the `auto` variant. This does not require a `data-color-mode` attribute:

```scss
@use "@fkui-community/theme-int/auto";
```

The `auto` variant ignores `data-color-mode` and always follows the user's browser or operating system preference. Import either the `auto` variant or the main theme, but not both.
