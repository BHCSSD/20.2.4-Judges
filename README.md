# 20.2.4-Judges

## What is splice()?
The splice() method in JavaScript is used to change the contents of an array by removing or replacing existing elements and/or adding new elements in place.

### Syntax:
```
array.splice(start[, deleteCount[, item1[, item2[, ...]]]])
``` 
- start: The index at which to start changing the array. If greater than the length of the array, actual starting index will be set to the length of the array. If negative, will begin that many elements from the end of the array.

- deleteCount (optional): An integer indicating the number of old array elements to remove. If deleteCount is 0, no elements are removed. If omitted, all elements from start to the end of the array will be deleted.

- item1, item2, ... (optional): The elements to add to the array, beginning from the start index.

Example Usage:
```
let fruits = ['apple', 'banana', 'cherry', 'date'];

// Removing one element starting from index 2
fruits.splice(2, 1); // ['apple', 'banana', 'date']

// Adding elements starting from index 2, removing none
fruits.splice(2, 0, 'orange', 'lemon'); // ['apple', 'banana', 'orange', 'lemon', 'date']

// Replacing 1 element at index 2
fruits.splice(2, 1, 'grape', 'kiwi'); // ['apple', 'banana', 'grape', 'kiwi', 'date']
``` 


### Notes:
- The splice() method modifies the original array and returns an array containing the deleted elements, or an empty array if no elements were removed.
- Negative values can be used for start and deleteCount to count from the end of the array.
- If start is larger than the length of the array, the splice() method will begin at the end of the array.
- If deleteCount is omitted or larger than the number of elements after start, all elements from start to the end of the array will be deleted.
- Additional items passed to splice() will be inserted into the array at the specified start index.
- Be cautious when using splice() as it modifies the original array directly. If you want to avoid modifying the original array, consider using methods like slice() instead.




### Starter Code 
```
//ex6_judges
let allJudges = ["Bob", "Serena", "Steve", "Sue"];
let allScores = [];

function setup() {
	createCanvas(800, 600);


    allScores[0] = 16;
    allScores[1] = 15;
    allScores[2] = 17;
    allScores[3] = 4;
    allScores[4] = 17;

//insert at 2
    allJudges.splice(2,0,"Diana");



    print(allJudges);
    print(allScores);
    
    //delete 1 thing starting at location 3
    allScores.splice(3,1);

    let total = 0;
    for (let i=0; i<allScores.length; i++){
        total += allScores[i];
    }
    print("Average Score: " +  ( total/allScores.length    )    );


}//end setup

function draw() {
    background(100,92,80);
   
}//end draw

```
