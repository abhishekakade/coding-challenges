# Coding Challenges

## Random Questions

### 1. Make the following code work -

```
const a = [1, 2, 3, 4, 5];
// Implement this
a.multiply();
console.log(a); // [1, 2, 3, 4, 5, 1, 4, 9, 16, 25]
```

### Solution -

```
Array.prototype.multiply = function() {
	this.push(...this.map(item => item * item));
	return this;
}
a.multiply();
```

### 2. Grab all URLs from a webpage -

```
let urlArr = Array.from(document.getElementsByTagName('a'));
let allUrlContainer = urlArr.map(item => item.getAttribute('href'));
function removeEmptyUrl(value) {
  if(value !== "#" && value !== "/") {
    return value;
  }
}
let validUrlList = allUrlContainer.filter(removeEmptyUrl);
console.log(validUrlList);
```
