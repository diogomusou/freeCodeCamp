## Sum All Numbers in a Range

#### Method 1 

```javascript
function sumAll(arr) {
  if (arr[1]<arr[0]){
    var x = arr[1];
    arr[1] = arr[0];
    arr[0] = x;
  }
  
  var sum = 0;
  for(var i = arr[0];i<=arr[1];i++){
    sum+=i;
  }
  return sum;
}
```

#### Method 2

```javascript
function sumAll(arr) {
  
  var sum = 0;
  for(var i = Math.min(arr[0],arr[1]);i<=Math.max(arr[0],arr[1]);i++){
    sum+=i;
  }
  return sum;
}
```

#### Using .reduce()

I could think of a simpler way to solve this using .reduce , please tell me if you did.

## Diff Two Arrays

```javascript
function diffArray(arr1, arr2) {
  var newArr = [];
  
  for(var i = 0;i<arr1.length;i++){
    if(arr2.indexOf(arr1[i])==-1){ //not in arr2
      newArr.push(arr1[i]);
    }
  }
  
  for(var j = 0;j<arr2.length;j++){
    if(arr1.indexOf(arr2[j])==-1){ //not in arr1
      newArr.push(arr2[j]);
    }
  }
  return newArr;
}
```
## 

```javascript

```



