* Objects in JS can be created using object literal & "new Object()" keyword.
```javascript
const backpack = {
  name: "Everyday Backpack",
  volume: 30,
  color: "grey",
  pocketNum: 15,
  strapLength: {
	    left: 26,
	    right: 26,
	  },
  lidOpen: false,
  toggleLid: function (lidStatus) {
	    this.lidOpen = lidStatus;
	  },
  newStrapLength: function (lengthLeft, lengthRight) {
	    this.strapLength.left = lengthLeft;
	    this.strapLength.right = lengthRight;
	  }
  }
```
* In order to increase code reusability we can use "Class" & "Object Constructor function" to create objects of same type.
* Object creation using a "Class" should be preferred as compared to "Object Constructor function".
```javascript
class Backpack {
  constructor(
    // Defines parameters:
    name,
    volume,
    color,
    pocketNum,
    strapLengthL,
    strapLengthR,
    lidOpen
  ) {
    // Define properties:
    this.name = name;
    this.volume = volume;
    this.color = color;
    this.pocketNum = pocketNum;
    this.strapLength = {
      left: strapLengthL,
      right: strapLengthR,
    };
    this.lidOpen = lidOpen;
  }
  // Add methods like normal functions:
  toggleLid(lidStatus) {
    this.lidOpen = lidStatus;
  }
  newStrapLength(lengthLeft, lengthRight) {
    this.strapLength.left = lengthLeft;
    this.strapLength.right = lengthRight;
  }
}

export default Backpack;
```