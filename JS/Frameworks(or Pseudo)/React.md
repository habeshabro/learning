
```jsx
const app = document.getElementById('app');
const root = ReactDOM.createRoot(app);
const [variable, setVariable] = React.useState(0);
function handleClick(e){
	
}
function Header({title}) {
	return(<div>
	<h1 >{title}</h1>
	<button onClick={handleClick}></button>
	</div>
	)
}
root.render(<Header title="Hello World"/>)
//
ReactDOM.render(componentToRender, targetNode)//JSX
ReactDOM.render(<componentToRender />, targetNode)//react component
const map = {
	class: className,
	onclick: onClick,
	onChange: onChange,
	"<br>": "<br />"
}
```



```jsx
class Kitten extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      name: 'freeCodeCamp'
    }
  }
  this.setState({
  name: 'smthnElse'})
	componentDidMount(){}
  render() {
    return (
      <h1>{this.state.name}</h1>
    );
  }
}
```
```jsx
Items.defaultProps = {
  quantity: 0
};
MyComponent.propTypes = { handleClick: PropTypes.func.isRequired }
<ErrorBoundary fallback={comp} >
<Suspense fallback="...loading"> comp </Suspense>
</ErrorBoundary>

setForm({
...form,
[e.target.name]: e.target.value
})
```

[[Redux]]