## Compare jQuery with Vanilla ES6 functionality 

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
| ```const cloned = $el.clone()``` | ```const cloned = $el.cloneNode(true)``` | Clone the el |
