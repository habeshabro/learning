#html #frontend #intermediate #web

### Doctype
The <!DOCTYPE> tag shows what type of html is being used. Usually it is simple, when using html5 just use
```html
<!DOCTYPE html>
```
### HTML Tag
The html tag is the root of all elements except for the doctype tag, also it is good form to use the lang keyword to show the language of the page.
```html
<!DOCTYPE html>
<html lang="en"></html>
```

### Head
This is the part that contains all the metadata of the document including:
- Title: It is required and it show what is displayed on the tab
- Style: allows the definition of css in the html document
- Base: Defines the default and "starting" point for every url in document so if base defines the url "a.com" and the link is href="b/e" then when the link is clicked, it will navigate to "a.com/b/e". Also Specifies the default target for all hyperlinks and forms in the page
- ### Link
- #### Meta
- #### Script
- #### No Script
```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<title>Coolio</title>
		<style>
				h1{
					color: red;
				}
				p{
					color: blue;
				}
		</style>
		<base href="https://www.w3schools.com" target="_blank">	
		<link rel="stylesheet" href="styles.css">
	</head>
</html>
```