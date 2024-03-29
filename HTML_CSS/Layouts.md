# Basic Layout Structures to implement

## The overlapping and shifted elements

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="/HTML_CSS/CSS_Fundamentals/index_styles.css" />
    <title>Document</title>
  </head>

  <body>
    <div class="container">
      <main>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Eaque
          blanditiis dicta, rem possimus unde eos eum, neque dolore harum
          repellat distinctio ullam voluptatibus sapiente alias. Aliquam
          doloribus eligendi unde suscipit.
        </p>
      </main>
      <button class="original">SUBSCRIBE</button>
      <button class="offset">SUBSCRIBE</button>
    </div>
  </body>
</html>
```

```css
body {
  background-color: lightblue;
}

.container {
  background-color: lightgreen;
  width: 800px;
  margin: 0 auto;
  position: relative;
}

.original {
  position: absolute;
  top: 0;
  left: 0;
}

.offset {
  position: absolute;
  top: 20%;
  left: -2%;
}
```

## Building a simple Navbar

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="/HTML_CSS/CSS_Fundamentals/index_styles.css" />
    <title>Document</title>
  </head>

  <body>
    <div class="container">
      <nav class="flex-container">
        <a href="">Home</a>
        <a href="">About</a>
        <a href="">Contact Us</a>
      </nav>
    </div>
  </body>
</html>
```

```css
body {
  background-color: lightblue;
}

/* Build Container */
.container {
  background-color: lightgreen;
  width: 800px;
  margin: 0 auto;
}

.flex-container {
  display: flex;
  justify-content: space-between;
  list-style-type: none;
}

a {
  text-decoration: none;
}
```

## Article and Aside Page Layout

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="/HTML_CSS/CSS_Fundamentals/index_styles.css" />
    <title>Document</title>
  </head>

  <body>
    <div class="container">
      <div class="flex-page">
        <div class="red">
          <p>
            Lorem ipsum dolor, sit amet consectetur adipisicing elit. Sed odit
            eius totam earum ea blanditiis dolor autem aspernatur cumque
            doloremque quasi reiciendis, ratione sunt accusantium voluptas fugit
            numquam amet qui?
          </p>
        </div>

        <aside class="blue">
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Sed minima
            aperiam magni placeat perferendis possimus iusto cupiditate ipsam
            quia. Sit, laudantium possimus? Aperiam velit culpa porro nostrum
            vel non. Ab?
          </p>
        </aside>
      </div>
      <footer class="green">
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Mollitia
          laboriosam nostrum ipsa earum, optio odit est libero, sapiente totam
          soluta itaque? Maiores vero ad doloribus itaque laboriosam, quas
          autem! Illum.
        </p>
      </footer>
    </div>
  </body>
</html>
```

```css
body {
  background-color: lightblue;
}

/* Build Container */
.container {
  background-color: lightgreen;
  width: 1200px;
  margin: 0 auto;
}

.flex-page {
  display: flex;
  gap: 48px;
  /* We add this property to ensure the aside DOES NOT go all the way to the bottom of our page */
  align-items: flex-start;
}

.red {
  background-color: rgb(241, 90, 90);
  /* we use flex:1 to allow this element to take up all available space */
  flex: 1;
}

.blue {
  background-color: rgb(65, 65, 195);
  flex: 0 0 300px;
}

.green {
  background-color: green;
}
```

## Two columns with bottom sub-sections

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="/HTML_CSS/CSS_Fundamentals/index_styles.css" />
    <title>Document</title>
  </head>

  <body>
    <div class="container">
      <div class="container-one">
        <div class="el el-1">One</div>
        <div class="el el-2">Two</div>
        <div class="el el-3">Three</div>
        <div class="el el-4">Four</div>
        <div class="el el-5">Five</div>
        <div class="el el-6">Six</div>
      </div>
    </div>
  </body>
</html>
```

```css
body {
  background-color: lightblue;
}

/* Build Container */
.container {
  width: 1200px;
  margin: 0 auto;
}

.container-one {
  background-color: black;
  font-size: 24px;
  display: grid;
  grid-template-columns: 500px 500px;
  grid-template-rows: 300px 150px 150px;
  column-gap: 200px;
  row-gap: 10px;
}

.el-1 {
  background-color: red;
}

.el-2 {
  background-color: blue;
}

.el-3 {
  background-color: yellow;
}

.el-4 {
  background-color: orange;
}

.el-5 {
  background-color: brown;
}

.el-6 {
  background-color: blueviolet;
}
```

## Creating a two-thirds layout

!["What we call a 2/3 layout](../HTML_CSS/CSS_Fundamentals/img/two-thirds-grid.png)

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="/HTML_CSS/CSS_Fundamentals/index_styles.css" />
    <title>Document</title>
  </head>

  <body>
    <div class="container">
      <div class="container-one">
        <div class="el el-1">One</div>
        <div class="el el-2">Two</div>
        <div class="el el-3">Three</div>
        <div class="el el-4">Four</div>
        <!-- <div class="el el-5">Five</div>
            <div class="el el-6">Six</div> -->
      </div>
    </div>
  </body>
</html>
```

```css
body {
  background-color: lightblue;
}

/* Build Container */
.container {
  width: 1200px;
  margin: 0 auto;
}

.container-one {
  background-color: black;
  font-size: 24px;
  display: grid;
  grid-template-columns: 1fr 300px;
  gap: 15px;
}

.el {
  display: flex;
  justify-content: center;
  align-items: center;
}

.el-1 {
  background-color: red;
  height: 100px;
}

.el-2 {
  background-color: blue;
}

.el-3 {
  background-color: yellow;
}

.el-4 {
  background-color: orange;
  height: 100px;
}

.el-5 {
  background-color: brown;
}

.el-6 {
  background-color: blueviolet;
}
```

## A multiple square box layout

!["a square grid layout"](/HTML_CSS/CSS_Fundamentals/img/even-grid-layout.png)

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="/HTML_CSS/CSS_Fundamentals/index_styles.css" />
    <title>Document</title>
  </head>

  <body>
    <div class="container">
      <div class="container-one">
        <div class="el el-1">One</div>
        <div class="el el-2">Two</div>
        <div class="el el-3">Three</div>
        <div class="el el-4">Four</div>
        <div class="el el-5">Five</div>
        <div class="el el-6">Six</div>
      </div>
    </div>
  </body>
</html>
```

```css
body {
  background-color: lightblue;
}

/* Build Container */
.container {
  width: 1200px;
  margin: 0 auto;
}

.container-one {
  background-color: black;
  font-size: 24px;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: 1fr 1fr;
  gap: 15px;
  height: 400px;
}

.el {
  display: flex;
  justify-content: center;
  align-items: center;
}

.el-1 {
  background-color: red;
}

.el-2 {
  background-color: blue;
}

.el-3 {
  background-color: yellow;
}

.el-4 {
  background-color: orange;
}

.el-5 {
  background-color: brown;
}

.el-6 {
  background-color: blueviolet;
}
```
