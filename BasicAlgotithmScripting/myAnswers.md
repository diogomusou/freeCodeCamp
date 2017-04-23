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