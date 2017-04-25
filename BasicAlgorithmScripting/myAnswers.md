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

#### Method 1 

```javascript
function chunkArrayInGroups(arr, size) {
  var resultArray = [[]];
  
  var i = 0;
  var count = 0;
  while(arr.length>0){
    
    if(count==size){
      count=0;
      resultArray.push([]);
      i++;
    }
    resultArray[i].push(arr.shift());
    count++;
  }

  return resultArray;
}
```

#### Method 2 (using .slice)

```javascript
function chunkArrayInGroups(arr, size) {
  var resultArray = [];
  
  for(var i =0;i<arr.length;i+=size){
    resultArray.push(arr.slice(i,i+size));
  }

  return resultArray;
}
```

## Slasher Flick

```javascript
function slasher(arr, howMany) {
  return arr.slice(howMany,arr.length);
}
```

## Mutatoins

```javascript
function mutation(arr) {
  var word1 = arr[0].toLowerCase();
  var word2 = arr[1].toLowerCase();
  
  for(var i=0;i<word2.length;i++){
    if(word1.indexOf(word2[i])<0){
      return false;
    }
  }
  return true;
}
```

## Falsy Bouncer

```javascript
function bouncer(arr) {
  
  return arr.filter(function(value){
    return (value)
  });
}
```

## Seek and Destroy

```javascript
function destroyer(arr) {
  var tempArray = [];
  var argumentArray = Array.from(arguments);
  
  tempArray = arr.filter(function(value){
        for(var i = 0;i<argumentArray.length;i++){
          if(value==argumentArray[i]){
            return false;
          }
        }
        return true;
     });
    
  
  return tempArray;
 }
```

## Where do I belong

```javascript
function getIndexToIns(arr, num) {
  
  arr = arr.sort((a,b)=>a-b);
  for(var i=0;i<arr.length;i++){
    if(num<=arr[i]){
      return (i);
    }
  }
  return arr.length;
}
```

## Caesars Cipher

```javascript
function rot13(str) { // LBH QVQ VG!
  var tempArray = [];
  
  for(var i = 0;i < str.length;i++){
    var code = str.charCodeAt(i);
    if(code>=65 && code<=90){
      code = code - 13;
      if (code<65){
        code = 64 - code;
        code = 90 - code;
      }
    }
    tempArray.push(String.fromCharCode(code));
  }
  return tempArray.join("");
}
```