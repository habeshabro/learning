```js
window.onload = callbackfn
const resetButton = document.createElement("button")
let h1 = document.querySelector("h1");
const justText = document.createTextNode("text")
const inputContainers = Array.from(document.querySelectorAll('.input-container'));
const calorieCounter = document.getElementById('calorie-counter');
div2.textContent = "some text"
button3.innerText = "Go to town square";
button1.onclick = buyHealth;
addEntryButton.addEventListener = ('click', addEntry)
container.innerHTML = "<div>huzzah</div>";
targetInputContainer.insertAdjacentHTML("beforeend", HTMLString);
for(const item of array){}
Number('10')

output.classList.add('hide')
output.classList.remove('hide')
output.classlist.toggle('hide')

output.removeAttribute('attrName')
output.setAttribute('attrName', 'value')
resetGameBtn.style.display = "none"

parent.appendChild(child)
child.remove()

confirmCloseDialog.showModal();
dialog.close();

	taskForm.addEventListener("submit" || "keydown", e => {
  e.preventDefault();
})

window.addEventListener("keydown", ({ key }) => {
  movePlayer(key, 8, true);
});

```
```js
localStorage.setItem("key", value);
localStorage.getItem("key")
localStorage.removeItem("key")
localStorage.clear()
JSON.stringify(obj)
JSON.parse(string)
```

```js
//closure depends on "capture" of the external data by the internally defined function
for(let i=0; i<3; i++){
	const log = () => {
		console.log(i);
	}
	setTimeout(log, 100)
}
```
callback function is a function passed to another function
```js
array.map(callbackfuncion) //return an array of the results of the cbf
userData?.songs //optional chaining
array.sort((a,b) => {return condition? -1 : 1})// -1 change place of a and b
array.find(x => x.id == 1)
array.indexOf()
array.reverse()
array.findIndex(x=> x > 2)
array.shift()
array.unshift(1)
array.pop()
array.push(2)
array.splice(startIndex, numberofelements)
array.some(callBackFunction) // check and return true if callback return true for one element of array
array.all(callBackFumction) // check and return true and if all true
array.filter(callBackFunction)
array.reduce((accumilator, element) => {}, initial_value)
Array(numOfEls).fill(defaultValue)

Object.assign(target, source)
Object.keys()
Object.values()

const someSet = new Set(array)

Math.floor(num)
Math.min(...arr)
Math.max(...arr)
Math.pow(base, exponent);

(22.2222).toFixed(2) // gives 22.22

```

```js
const audio = new Audio();
audio.src = song.src;
audio.title = song.title;
audio.currentTime = 0;
audio.play()
const duh.innerHtml = `<button class="playlist-song-info" onclick="playSong(${song.id})">`
```

```js
const setPlayerCards = (arr = players) => {};
const { sport, team, year, players } = myFavoriteFootballTeam; //destructuring
switch(variable){
	case "a":
		smthn();
		break;
	case "b":
		...
	case "e":
	case "f":
	case "g":
		smthnElse();
		break;         // this grouping is valid for "e" || "f" || "g"
	default:
		finally do smthn();
}
```

```js
paserInt()
isNaN()
window.alert() // same as alert()
setTimeout(() => {console.log("Camp")}, 1500);
```

```js
class ShoppingCart {
	constructor() {
		this.propert = "a"; // this refers to the object being instantiated
	}
	function(a,b) {
	} 
}
let x = new ShoppingCart()
jj.addEventListener("click",x.funtion.bind(x)); //.bind(x) makes new function with x as this
const ctx = canvas.getContext("2d")
canvas.width = (window).innerWidth
ctx.fillStyle = "#99c9ff";
ctx.fillRect(this.position.x, this.position.y, this.width, this.height);
requestAnimationFrame(animate);
ctx.clearRect(0, 0, canvas.width, canvas.height);
```

