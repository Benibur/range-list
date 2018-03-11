# RANGE-LIST

A vanila js, heavy tested, library to manage a list of ranges.
* a list of range is : [ [a,b], [c, d], ... [m,n] ]
* where a < b < c ... < m < n

## Usage :
* add the following files to your code (no other dependencies) :
  * `./src/linked-list.js`
  * `./src/range-list.js`
* Exemple :
``` javascript
const RangeList = require('../src/range-list')
const list = new RangeList()
list.addRange(10,20)
list.addRange(15,25)
list.addRange(-10,5)
// get an array of all ranges
console.log( list.ranges() )
// [[-10,5], [10,25]]
```

## API

* `addRange (a, b)`
  * add a range [a,b] to the list. Indexes can be Integers or Flot, positive or negative.
  * Can overlap an existing range, will unifomize so that in the end there is no overlaping.

* `ranges ()`
  * returns an array of all ranges [[a,b], ... , [c,d]]


## Tests :
Run tests :
```
npm install
npm run test
````

Run tests in debug mode :
```
npm install
npm run test-debug
#  then run chrome devtools on port 3467
````
.
