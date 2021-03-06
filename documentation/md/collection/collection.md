A collection contains a set of nodes and edges.  Calling a function applies the function to all elements in the collection.  When reading values from a collection, [`eles.data()`](#collection/data/eles.data) for example, the value of the first element in the collection is returned.  For example:

```js
var weight = cy.nodes().data("weight");

console.log( cy.nodes()[0].data("weight") + ' == ' + weight ); // weight is the first ele's weight
```

You can ensure that you're reading from the element you want by using a [selector](#selectors) to narrow down the collection to one element (i.e. `eles.size() === 1`) or the [`eles.eq()`](#collection/iteration/eles.eq) function.

Also note that collections are iterable for modern browsers which support the [iteration protocols](https://exploringjs.com/es6/ch_iteration.html). This enables the use of features such as the spread operator, for-of loops, and destructuring.
