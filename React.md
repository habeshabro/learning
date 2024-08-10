
```jsx
const app = document.getElementById('app');
const root = ReactDOM.createRoot(app);
const [variable, setVariable] = React.useState(0);
function handleClick(e){
	
}
function Header({title}) {
	return(<div>
	<h1>{title}</h1>
	<button onClick={handleClick}></button>
	</div>
	)
}
root.render(<Header title="Hello World"/>)
```

