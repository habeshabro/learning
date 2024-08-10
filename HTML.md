HTML stands for :
- Hyper-text: means text that links objects 
- Markup: means that the language "marks up" text to give it extra meaning and functionality
- Language is language

The two most important functions of html is:
- Organizing information
- Linking objects together
objects can be: files, images, text, etc...

Here is a snipper of boiler-plate HTML code:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="stylesheet.css">
    <script type="module" src="app.js"></script>
    <title>Document</title>
</head>
<body>
</body>
</html>
```

Here are some more important tags that can be used to organize text: 

```html
<p> used to organize text into paragraphs </p>
<br /> used to insert a new line or line break in text
<hr /> inserts a horizontal line 
<h1>Main Title</h1>
<h2>Medium Title 1</h2>
<h3>Teenie Title 1</h3>
<h2>Medium Title 2</h2>
The h series tags create a hierarchical structure for all the titles
```

```html
<dialog id="confirm-close-dialog">
        <form method="dialog">
          <p class="discard-message-text">Discard unsaved changes?</p>
          <div class="confirm-close-dialog-btn-container">
            <button id="cancel-btn" class="btn">
              Cancel
            </button>
            <button id="discard-btn" class="btn">
              Discard
            </button>
          </div>
        </form>
      </dialog>
```