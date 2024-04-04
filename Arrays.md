## Arrays
Enables storing a collection of multiple items under a single variable name.

Javascript arrays are resizable and can contain a mix of different data types.
JavaScript arrays are zero-indexed.

### Array Methods.
#### Slice Method:
The slice() method of Array instances returns a shallow copy of a portion of an array into a new array object selected from start to end (end not included) where start and end represent the index of items in that array. 

The original array will not be modified.

**Syntax:**

arr.slice(start)

arr.slice(start, end)

arr.slice()

_**Example Code:**_
```javascript
  let arr = ['a', 'b', 'c', 'd', 'e'];
  arr.slice(2)  //output: ['c', 'd', 'e']
  arr.slice(2, 4) //output: ['c', 'd']
  arr.slice()    //output: ['a', 'b', 'c', 'd', 'e']
```
#### Splice method:
The splice() method of Array instances changes the contents of an array by removing or replacing existing elements and/or adding new elements in place.

**Syntax:**
splice(start)
splice(start, deleteCount)

#### Reverse method
The reverse() method of Array instances reverses an array in place and returns the reference to the same array, the first array element now becoming the last, and the last array element becoming the first. 

In other words, elements order in the array will be turned towards the direction opposite to that previously stated.

**Syntax:**
reverse()
_**Example code:**_
```javascript
const arr2 = ['a', 'b', 'c', 'd', 'e']
console.log(arr2.reverse()); //output: ['e','d','c','b','a']
```

#### Concat method
#### Join method
#### at method
### Looping Arrays
#### forEach method
#### Map method
#### Filter method
#### Reduce method
#### Find method
#### Some and every methods
#### Flat and flatMap
#### Sorting Arrays
#### More ways of creating and filling Arrays.
















