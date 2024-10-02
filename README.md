# code-challenge
Accept the challenge for Web/API and provide the solution

1. code challenge: Codeland Username Validation
   ```
   Have the function CodelandUsernameValidation(str) take the str parameter being passed and determine if the string is a valid username according to the following rules:
   1. The username is between 4 and 25 characters.
   2. It must start with a letter.
   3. It can only contain letters, numbers, and the underscore character.
   4. It cannot end with an underscore character.
   If the username is valid then your program should return the string true, otherwise return the string false.
   ```
   
```
Solution:
function CodelandUsernameValidation(str) {
  const regex = /^[a-zA-Z][a-zA-Z0-9_]*[^_]$/g
  return str.length >= 4 && str.length <= 25 && regex.test(str)
}
   
// keep this function call here 
console.log(CodelandUsernameValidation(readline()));
``` 

#### 2. Have the function FindIntersection(strArr) read the array of strings stored in strArr which will contain 2 elements: the first element will represent a list of comma-separated numbers sorted in ascending order, the second element will represent a second list of comma-separated numbers (also sorted). Your goal is to return a comma-separated string containing the numbers that occur in elements of strArr in sorted order. If there is no intersection, return the string false.
```
function checkloop(str){
    var newArr =[];
    var elemStr1 = str[0].split(", ");
    var strEle2 = str[1].split(", ");
    for(let i=0 ; i< elemStr1.length; i++){
        if(strEle2.includes(elemStr1[i])){
            newArr.push(elemStr1[i])
        }
        console.log(elemStr1[i]);
    }
    if(newArr.length == 0){
        return false;
    }
    return newArr.toString();
}
console.log(checkloop(["1, 2, 4, 12, 15", "2, 4, 12, 17, 19" ]));
```
