# Compare jQuery with ES6 functionality 

### Dom Selection

| jQuery | JavaScript |
|---|---|
| ```$('.aclass')``` | ```document.querySelector('.aclass')``` |
| | ```document.querySelectorAll('.aclass li')``` |

### Dom Manipulation
| jQuery | JavaScript | |
|---|---|---|
| ```$el.before()``` | ```el.before(anotherEl)``` | Add 'anotherEl before el |
| ```$el.prepend()``` | ```el.prepend(anotherEl)``` | Put 'anotherEl inside el before anything else |
| ```$el.append()``` | ```el.append(anotherEl)``` | Put 'anotherEl inside el after anything else |
| ```$el.remove()``` | ```el.remove()``` | Remove el |
| ```$el.addClass('someClass')``` | ```el.classList.add(someClass)``` | Add a someClass to el |
| ```$el.removeClass('someClass')``` | ```el.classList.remove(someClass)``` | Remove someClass from el |
| ```$el.toggleClass('someClass')``` | ```el.classList.toggle(someClass)``` | *true* if someClass was added, *false* if removed |
| ```const parent = $el.parent()``` | ```const parent = $el.parentNode``` | Get parent element of el |
| ```const cloned = $el.clone()``` | ```const cloned = $el.cloneNode(true)``` | Clone the el with all its child nodes |

### Events
| jQuery | JavaScript | |
|---|---|---|
| ```$el.on('click', function(e){ })``` | ```el.addEventListener('click', e => { })``` | Add an event listener |

### HTTP Requests / Ajax Calls
**jQuery**
```
$.ajax({
    url : 'http://...',
    type : 'GET',
    data : { 'numberOfWords' : 10 },
    dataType:'json',
    success : function(data) { alert('Data: '+data); },
    error : function(request, error) { alert("Request: "+JSON.stringify(request)); }
});
```
**ES6**
```
fetch('http://...').then(res => res.json()).then(data => alert(data));
```
**ES6 with Axios**
```
axios.get('http://...').then(res => alert(res.data));
```

### Utilities
| jQuery | JavaScript | |
|---|---|---|
| ```$isArray(el)``` | ```Array.isArray(el)``` | Check if el is an array |
| ```$.each(el, function(index, value) { })``` | ```el.forEach(value, index) => { })``` | Loop through an array |
| ```$.map(el, function(value, index) { })``` | ```el.map(value, index) => { })``` | Map to a new array |
| ```$.grep(el, function(value, index) { })``` | ```el.filter(value, index) => { })``` | Creates a new array that passes the test |
| ```$.parseJSON(str)``` | ```JSON.parse(str)``` | Parses JS object out of a JSON string |
