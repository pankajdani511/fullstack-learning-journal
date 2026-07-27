# 🎨 CSS (Cascading Style Sheets)

CSS (Cascading Style Sheets) is a stylesheet language used to design and style HTML documents. It controls how elements appear on a webpage including colors, layouts, spacing, fonts, animations, and responsiveness.

HTML creates the structure of a webpage, CSS makes it beautiful .

```
HTML      → Structure
CSS       → Design & Styling

```

---

# 📌 Why Do We Need CSS?

Without CSS, websites would look plain and difficult to use.

CSS helps to:

- Add colors and backgrounds
- Change fonts and text styles
- Create layouts
- Make websites responsive
- Add animations
- Improve user experience


# 🌐 History of CSS

- CSS was created by **Håkon Wium Lie** in 1996.
- It was developed to separate webpage structure from design.
- The latest standard is CSS3.

---

# 🏗️ How CSS Works

When a browser loads a webpage:

```
HTML File
    |
    ↓
Browser Creates DOM Tree
    |
    ↓
CSS File Loaded
    |
    ↓
CSS Rules Applied
    |
    ↓
Render Tree Created
    |
    ↓
Webpage Displayed
```

---

# 📂 Adding CSS to HTML

There are three ways to add CSS.

---

# 1. Inline CSS

CSS is written inside the HTML tag.

Example:

```html
<h1 style="color:red;">
Hello World
</h1>
```

### Advantages

- Quick styling
- Useful for testing

### Disadvantages

- Not reusable
- Makes HTML messy

---

# 2. Internal CSS

CSS is written inside the `<style>` tag.

Example:

```html
<head>

<style>

h1{
    color:blue;
}

</style>

</head>
```

### Advantages

- Good for single pages

### Disadvantages

- Not suitable for large projects

---

# 3. External CSS (Recommended)

CSS is written in a separate file.

HTML:

```html
<link rel="stylesheet" href="style.css">
```

style.css:

```css
h1{
    color:green;
}
```

### Advantages

- Reusable
- Clean code
- Easy maintenance

---

# 📝 CSS Syntax

Basic structure:

```css
selector{

    property: value;

}
```

Example:

```css
h1{

    color:red;
    font-size:40px;

}
```

Explanation:

```
h1        → Selector

color     → Property

red       → Value
```

---

# 💬 CSS Comments

Comments are ignored by browsers.

Syntax:

```css
/* This is a CSS comment */

```

---

# 🎯 CSS Selectors

Selectors are used to select HTML elements and apply styles.

---

# 1. Universal Selector (*)

Selects all elements.

```css
*{
    margin:0;
    padding:0;
}
```

---

# 2. Element Selector

Selects elements by tag name.

```css
p{

color:black;

}
```

---

# 3. Class Selector

Used with `.className`

HTML:

```html
<p class="text">
Hello
</p>
```

CSS:

```css
.text{

color:red;

}
```

---

# 4. ID Selector

Used with `#id`

HTML:

```html
<h1 id="title">
Hello
</h1>
```

CSS:

```css
#title{

color:blue;

}
```

---

# 5. Group Selector

Apply same style to multiple elements.

```css
h1,h2,p{

color:green;

}
```

---

# 6. Attribute Selector

Select elements based on attributes.

Example:

```css
input[type="text"]{

border:1px solid black;

}
```

---

# 🎨 CSS Colors

CSS provides different ways to define colors.

---

## Color Name

```css
color:red;
```

---

## RGB

```css
color:rgb(255,0,0);
```

---

## HEX

```css
color:#ff0000;
```

---

## HSL

```css
color:hsl(0,100%,50%);
```

---

# 📏 CSS Units

Units define sizes in CSS.

---

# Absolute Units

Fixed size units.

Examples:

```
px
cm
mm
in
```

Example:

```css
font-size:20px;
```

---

# Relative Units

Size depends on other elements.

Examples:

```
%
em
rem
vw
vh
```

---

# Percentage (%)

Relative to parent element.

```css
width:50%;
```

---

# em

Relative to parent font size.

```css
font-size:2em;
```

---

# rem

Relative to root element.

```css
font-size:2rem;
```

---

# Viewport Units

## vw

Viewport width

```css
width:50vw;
```

## vh

Viewport height

```css
height:100vh;
```

---

# 🌊 Cascade in CSS

CSS stands for Cascading Style Sheets because multiple styles can apply to the same element.

Example:

```css
p{

color:red;

}

p{

color:blue;

}
```

The last rule will apply.

Output:

```
Blue text
```

---

# 🎯 CSS Specificity

When multiple rules apply, browser decides based on specificity.

Priority:

```
!important

↓

Inline CSS

↓

ID Selector

↓

Class Selector

↓

Element Selector

↓

Universal Selector
```

Example:

```css
#title{

color:red;

}

.title{

color:blue;

}
```

ID will win.

---

# 🔄 CSS Inheritance

Some properties automatically pass from parent to child.

Example:

```css
body{

color:red;

}
```

All text inside body becomes red.

Inherited properties:

- color
- font-family
- font-size

---

# 📚 Summary

In this section we learned:

✅ What CSS is  
✅ Why CSS is used  
✅ CSS syntax  
✅ Adding CSS  
✅ Selectors  
✅ Colors  
✅ Units  
✅ Cascade  
✅ Specificity  
✅ Inheritance  

---

