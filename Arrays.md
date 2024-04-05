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

The concat() method of Array instances is used to merge two or more arrays. This method does not change the existing arrays, but instead returns a new array.

**Syntax:**
concat() //if parameters are omitted, concat returns a shallow copy of the existing array on which it is called.
concat(value1) 
concat(value1, value2)

**_Example Code_**
```javascript
  const arr = ['a', 'b', 'c', 'd', 'e'];
  const arr2 = ['j', 'i', 'h', 'g', 'f'];
  arr.concat(arr2) //Returns ['a', 'b', 'c', 'd', 'e', 'j', 'i', 'h', 'g', 'f']
```

#### Join method

The join() method of Array instances creates and returns a new string by concatenating all of the elements in this array, separated by commas or a specified separator string.

**Syntax:**

join()
join(separator) //Separator(optional) is a string to separate each pair of adjacent elements of the array. if omitted, the array elements are separated with a (",").

_**Example Code**_

```javascript
const arr = ['a', 'b', 'c', 'd', 'e'];
arr.join('-') //Returns a string "a-b-c-d-e"
```

#### at method

The at() method of Array instances takes an integer value and returns the item at that index, allowing for positive and negative integers. Negative integers count back from the last item in the array.

**Syntax:**

at(index) //returns an element in the given index, or undefined if not found.

_**Example code:**_

```javascript
  const arr = [23, 11, 64]
  arr.at(0) //returns an element which is at index 0
```

### Looping Arrays
#### forEach method

The forEach() method of Array instances executes a provided function once for each array element.

**Syntax:**




#### Map method
#### Filter method
#### Reduce method
#### Find method
#### Some and every methods
#### Flat and flatMap
#### Sorting Arrays
#### More ways of creating and filling Arrays.
















