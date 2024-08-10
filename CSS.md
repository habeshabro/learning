```css
.stripy{
background: repeating-linear-gradient(90deg, var(--col1) 0%, var(--col1) 2%, var(--col2) 2%, var(--col2) 4% )
}
```

```css
@media (max-width: 1000px) {
	display: grid;
	grid-template-columns: minmax(2rem, 1fr) minmax(min-content, 94rem) minmax(2rem, 1fr);
	grid-template-columns: repeat(5, 1fr);
  row-gap: 3rem;
}
.heading {
  grid-column: 2 / 3;
}
.text-grid {
  grid-column: 2 / 3;
  font-size: 1.8rem;
  letter-spacing: 0.6px;
  column-width: 25rem;
}
hr {
  margin: 1.5rem 0;
  border: 1px solid rgba(120, 120, 120, 0.6)
}

.line:nth-of-type(6) {}
transform-origin: 0% 0%;
transform: rotate(60deg) skew(x, y)
@keyframes wheel{
	x% {}
	y% {}
}
  animation-name: wheel;
  animation-duration: 10s;
  animation-iteration-count: infinite;
  animation-timing-function: linear;
  animation: cabins 10s linear infinite;
```

```css
:root {  --blue: #1e90ff;  
  --white: #ffffff;}  
  
body { background-color: var(--blue); }
```