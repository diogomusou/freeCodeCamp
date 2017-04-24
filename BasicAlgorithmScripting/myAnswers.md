## Reverse a string

#### Method 1 

```javascript
function reverseString(str) {
  var array = [""];
  
  for(var i=0;i<str.length;i++){
    array.unshift(str[i]); //populate the array from the left to reverse
  }
  str = array.join(""); //array to string
  
  return str;
}
```

#### Method 2

```javascript
function reverseString(str) {
  var array = str.split("");
  array.reverse();
  str = array.join("");
  
  return str;
}
```

#### 1 line code

```javascript
function reverseString(str) {
  return ((str.split("")).reverse()).join("");
}
```
## Factorialize a Number

```javascript
function factorialize(num) {
  if (num==0) {return 1};
  
  for(var i = num-1;i>0;i--){
    num *= (i);
  }
  return num;
}
```

## Check for Palindromes

```javascript
function palindrome(str) {
  // Good luck!
  str = (str.toLowerCase().replace(/[^a-z0-9]+/g,"")).split("");
  
  if(str.join("") === (str.reverse()).join("")){
    return true;
  }else{
    return false;
  }
}
```

## Find the Longest Word in a String

```javascript
function findLongestWord(str) {
  str = str.split(" ");
  
  var maxLength = 0;
  for(var i=0;i<str.length;i++){
    if(str[i].length>maxLength){
      maxLength = str[i].length;
    }
  }
  return maxLength;
}
```

## Title Case a Sentence

```javascript
function titleCase(str) {
  str = str.split(" "); //array of words
  
  for(var i=0;i<str.length;i++){
    str[i] = str[i].toLowerCase(); //lower case the word
    var tempArray = str[i].split(""); //array of letters
    tempArray[0] = tempArray[0].toUpperCase(); //upper case the first
    str[i] = tempArray.join(""); //join letters to reconstruct word
  }

  return str.join(" "); //join words to reconstruct sentence
}
```

## Return Largest Numbers in Array

```javascript
function largestOfFour(arr) {
  
  var largestNumbers = [];
  for(var i=0;i<arr.length;i++){
    var largest = 0;
    for(var j=0;j<arr[i].length;j++){
      if(arr[i][j]>largest){
        largest=arr[i][j];
      }
    }
    largestNumbers.push(largest);
  }
  return largestNumbers;
}
```

## Confirm the Ending

```javascript
function confirmEnding(str, target) {
    if(target == str.substr(-(target.length),(target.length))) {
      return true;
    }else{
      return false;
    }

}
```

## Repeat a string repeat a string

```javascript
function repeatStringNumTimes(str, num) {
  var repeatedString = "";
  for(var i = 1;i<=num;i++){
    repeatedString+=str;
  }
  return repeatedString;
}
```

## Truncate a string

```javascript
function truncateString(str, num) {
  if(num<str.length) {
    if(num>3){
      str = str.slice(0,num-3);
    }else{
      str = str.slice(0,num);
    }
    str = str + "...";
  }
  return str;
}
```

## Chunky Monkey

```javascript

```

## Title Case a Sentence

```javascript

```
