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

Date : 23rd July 2023
### Find Even in odd or vice vers
https://www.codewars.com/kata/5526fc09a1bbd946250002dc/solutions/javascript

function findOutlier(int){
  var even = int.filter(a=>a%2==0);
  var odd = int.filter(a=>a%2!==0);
  return even.length==1? even[0] : odd[0];
}

### Printer Errors
https://www.codewars.com/kata/56541980fa08ab47a0000040/javascript

function printerError(s) {
    // your code
    var count = 0;
    for(var i = 0; i < s.length; i++) {
      if (s[i] > "m") {
        count++;
      }
    }
    return count+"/"+s.length;
}

function printerError(s) {
    
    let numerator = 0;
    for(let i=0;i<s.length;i++)
      {
        if(s.charCodeAt(i) < 97 || s.charCodeAt(i) >109)
          {
            numerator = numerator +1;
          }
      }
      return `${numerator}/${s.length}`
}


function persistence(num) {
   
  let times = 0;
  
  num = num.toString();
  
  while(num.length>1)
    {
    times++;
     num = num.split('').map(Number).reduce((a,b)=>a*b).toString();
    }
  return times;
}
### Smileys
https://www.codewars.com/kata/583203e6eb35d7980400002a/solutions
function countSmileys(arr) {
var smileys = [":)",";)",":-)",";-)",";~)",":~)",":D",";D",":-D",":~D",";-D",";~D"];
var count = 0;

for (var i=0; i<arr.length; i++){
  for (var j=0; j<smileys.length; j++){
    if (arr[i]===smileys[j]){
      count++;
    }
  }
  }
return count;
}

Write Number in Expanded Form

https://www.codewars.com/kata/5842df8ccbd22792a4000245/javascript
```sh
const expandedForm = n => n.toString()
                            .split("")
                            .reverse()
                            .map( (a, i) => a * Math.pow(10, i))
                            .filter(a => a > 0)
                            .reverse()
                            .join(" + ");
```


function rgb(r, g, b){
	return toHex(r)+toHex(g)+toHex(b);
}

function toHex(d) {
    if(d < 0 ) {return "00";}
    if(d > 255 ) {return "FF";}
    return  ("0"+(Number(d).toString(16))).slice(-2).toUpperCase()
}
