## Functional Programming

### Implement map on a Prototype
```js
var s = [23, 65, 98, 5];

Array.prototype.myMap = function(callback){
  var newArray = [];
  this.forEach(a => newArray.push(callback(a)));
  return newArray;

};

var new_s = s.myMap(function(item){
  return item * 2;
});
```

### Implement filter on a Prototype
```js
var s = [23, 65, 98, 5];

Array.prototype.myFilter = function(callback) {
    var newArray = [];
    this.forEach(val => callback(val) && newArray.push(val));
    return newArray;
};

var new_s = s.myFilter(function(item){
  return item % 2 === 1;
});
```

### Split a String into an Array Using the split Method
```js
function splitify(str) {
  return str.split(/\W/);
}
splitify("Hello World,I-am code"); // OP => ["Hello", "World", "I", "am", "code"]
splitify("Earth-is-our home") // OP => ["Earth", "is", "our", "home"]
splitify("This.is.a-sentence") // OP => ["This", "is", "a", "sentence"]
```

### Combine an Array into a String Using the join Method
```js
function sentensify(str) {
  return str.split(/\W/).join(' '); 
}
sentensify("May-the-force-be-with-you") // OP => "May the force be with you".
sentensify("The.force.is.strong.with.this.one") // OP => "The force is strong with this one".
sentensify("There,has,been,an,awakening") // OP => "There has been an awakening"
```

