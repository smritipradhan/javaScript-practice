# javaScript-practice
Practice Questions and Solutions

### Create Phone Numbers
Link - https://www.codewars.com/kata/525f50e3b73515a6db000b83/train/javascript

function createPhoneNumber(numbers){
  var format = "(xxx) xxx-xxxx";
  
  for(var i = 0; i < numbers.length; i++)
  {
    format = format.replace('x', numbers[i]);
  }
  
  return format;
}

### Popution
function nbYear(p0, percent, aug, p) {
    
  for (var years = 0; p0 < p; years++) {
    p0 = Math.floor(p0 + p0 * percent / 100 + aug);
  }
  return years
}

### Remove Duplicates
https://www.codewars.com/kata/57a5b0dfcf1fa526bb000118/solutions

function distinct(a) {
  return [...new Set(a)];
}

### Array Diff
https://www.codewars.com/kata/523f5d21c841566fde000009/train/javascript
function arrayDiff(a, b) {
  var difference = a.filter(x => b.indexOf(x) === -1);
  return difference
}
