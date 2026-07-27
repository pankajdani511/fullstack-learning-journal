# 📦 CSS Flexbox & Grid

Modern CSS provides two powerful layout systems:

- **Flexbox** → One-Dimensional Layout (Row OR Column)
- **CSS Grid** → Two-Dimensional Layout (Rows AND Columns)

Both are used to build responsive and modern websites.

---

# 🎯 What is Flexbox?

Flexbox (Flexible Box Layout) is a CSS layout model used to align and distribute space between items inside a container.

It is mainly used for:

- Navigation bars
- Cards
- Buttons
- Forms
- Centering elements
- Responsive layouts

---

# 🏗️ How Flexbox Works

```
Flex Container
│
├── Flex Item 1
├── Flex Item 2
├── Flex Item 3
└── Flex Item 4
```

The parent element becomes the **Flex Container**, and its direct children become **Flex Items**.

---

# Making a Flex Container

```css
.container{
    display: flex;
}
```

Example:

```html
<div class="container">
    <div>One</div>
    <div>Two</div>
    <div>Three</div>
</div>
```

```css
.container{
    display:flex;
}
```

Output:

```
One   Two   Three
```

---

# Main Axis & Cross Axis

```
flex-direction: row;

Main Axis  →
──────────────>

Cross Axis
     ↓
```

When using

```css
flex-direction:column;
```

```
Main Axis

↓

↓

↓

Cross Axis →
```

---

# Important Flexbox Properties

---

## 1. flex-direction

Defines the direction of items.

```css
.container{

display:flex;

flex-direction:row;

}
```

Values

```
row

row-reverse

column

column-reverse
```

---

## 2. justify-content

Aligns items on the **Main Axis**.

```css
justify-content:center;
```

Values

```
flex-start

center

flex-end

space-between

space-around

space-evenly
```

Example

```
space-between

A            B            C
```

---

## 3. align-items

Aligns items on the **Cross Axis**.

```css
align-items:center;
```

Values

```
stretch

center

flex-start

flex-end

baseline
```

---

## 4. flex-wrap

By default Flexbox keeps everything in one row.

```
nowrap
```

To move items to the next line:

```css
flex-wrap:wrap;
```

---

## 5. gap

Adds spacing between items.

```css
gap:20px;
```

---

## 6. flex-grow

Controls how much an item grows.

```css
.item{

flex-grow:1;

}
```

---

## 7. flex-shrink

Controls shrinking.

```css
flex-shrink:0;
```

---

## 8. flex-basis

Sets initial size.

```css
flex-basis:200px;
```

---

## 9. flex

Shortcut

```css
flex:1;
```

Equivalent

```css
flex-grow:1;

flex-shrink:1;

flex-basis:0;
```

---

# Complete Example

```css
.container{

display:flex;

justify-content:center;

align-items:center;

gap:20px;

height:100vh;

}
```

---

# 🎯 Advantages of Flexbox

- Easy alignment
- Responsive
- Less code
- Perfect for components
- Great for navigation bars

---

# 🌐 What is CSS Grid?

CSS Grid is a two-dimensional layout system.

Unlike Flexbox, Grid can control both rows and columns at the same time.

Used for:

- Dashboards
- Landing pages
- Galleries
- Admin Panels
- Complete Website Layouts

---

# Grid Structure

```
+-----+-----+-----+
|  1  |  2  |  3  |
+-----+-----+-----+
|  4  |  5  |  6  |
+-----+-----+-----+
```

---

# Making a Grid Container

```css
.container{

display:grid;

}
```

---

# grid-template-columns

Defines number of columns.

```css
grid-template-columns:200px 200px 200px;
```

or

```css
grid-template-columns:1fr 1fr 1fr;
```

---

# Fraction Unit (fr)

Example

```css
grid-template-columns:1fr 2fr 1fr;
```

Output

```
25%

50%

25%
```

---

# grid-template-rows

```css
grid-template-rows:100px 100px;
```

---

# gap

```css
gap:20px;
```

---

# justify-items

Align items horizontally.

```css
justify-items:center;
```

---

# align-items

Align items vertically.

```css
align-items:center;
```

---

# place-items

Shortcut

```css
place-items:center;
```

---

# Grid Item Properties

---

## grid-column

```css
grid-column:1/3;
```

Item spans two columns.

---

## grid-row

```css
grid-row:1/3;
```

Item spans two rows.

---

# repeat()

Instead of writing

```css
grid-template-columns:1fr 1fr 1fr;
```

Use

```css
grid-template-columns:repeat(3,1fr);
```

---

# minmax()

Responsive columns

```css
grid-template-columns:

repeat(auto-fit,minmax(250px,1fr));
```

Very common in real-world projects.

---

# Complete Grid Example

```css
.container{

display:grid;

grid-template-columns:repeat(3,1fr);

gap:20px;

}
```

---

# Flexbox vs Grid

| Flexbox | Grid |
|----------|------|
| One-dimensional | Two-dimensional |
| Row OR Column | Rows AND Columns |
| Best for components | Best for page layouts |
| Easier to learn | More powerful |
| Navbar | Dashboard |

---

# When to Use Flexbox?

✅ Navigation Bar

✅ Buttons

✅ Cards

✅ Forms

✅ Hero Section

✅ Centering Elements

---

# When to Use Grid?

✅ Complete Website Layout

✅ Dashboard

✅ Gallery

✅ Product Listing

✅ Admin Panel

---

# Best Practices

- Use **Flexbox** for small layouts.
- Use **Grid** for page layouts.
- Combine Flexbox and Grid when needed.
- Use `gap` instead of margins for spacing.
- Prefer `repeat()` and `minmax()` in Grid for cleaner, responsive code.

---

# Interview Questions

### What is Flexbox?

A one-dimensional layout model used for arranging items in rows or columns.

---

### What is Grid?

A two-dimensional layout system that manages both rows and columns.

---

### Difference between Flexbox and Grid?

Flexbox works in one direction (row or column), while Grid works in two directions (rows and columns).

---

### Which one is better?

Neither is better in every case.

- Use **Flexbox** for UI components.
- Use **Grid** for overall page layouts.

---

# Summary

- **Flexbox** is ideal for aligning items in a single direction and is commonly used for components like navbars, cards, and forms.
- **CSS Grid** is ideal for building complex page layouts with rows and columns.
- In real-world development, Flexbox and Grid are often used together to create responsive and maintainable designs.

---

