# Use Icon fonts. Ex. FontAwesome

1. Put your FontAwesome.ttf file in app/fonts folder.

2. Create a CSS class to apply it in app.css. **Important:** For the font-family name, use the same value as the file name without the extension.

3. Create a label using the unicode char of the char you want to use. **Important:** Unicode chars are represented starting with "&#x" and ending with ";"

4. Enjoy :)

```css
.fa {
    font-family: "FontAwesome";
}
```
```xml
<Label class="fa" text="&#xf07a;"/>
```