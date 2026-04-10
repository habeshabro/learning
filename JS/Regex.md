```js
const regex = /[+-\s]/g; //global character class
const regex = /\d+e\d+/i; //case insensitive
const regex = /yes|definitely/; //alternate sequence "or"
const regex = /h(ey|i)/; //capture group
const numRegex = /([\d.]+)/ 
const freeRegex = /(?:^|\s)fr[e3][e3] m[o0]n[e3]y(?:\s|$)/i; //non capturing group
str.replace(regex, '');
str.match(regex)
regex.test(str)
const lookBehind = /(?<=a)b/
const lookAhead = /a(?=b)/
```

```js
const rangeRegex = /([A-J])([1-9][0-9]?):([A-J])([1-9][0-9]?)/gi;
const rangeExpanded = x.replace(rangeRegex, (match, char1, num1, char2, num2) => {
	
});
```