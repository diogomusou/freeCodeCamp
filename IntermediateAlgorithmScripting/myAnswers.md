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

## Factorialize a Number

```javascript

```

