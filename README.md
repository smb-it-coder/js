# js 
# Custom own Map function into javascript

/**
* Write a custom map function into javascript with example
*/

Array.prototype.myMap = function(callback) {
  let newArray = [];
  let x = this.length;
  for (let i = 0; i < x; i++) {
    let counter = callback(this[i]);
    newArray.push(counter);
  }
  return newArray;
};

let arr = [1, 2, 3];
arr = arr.myMap(e => e * 2);
console.log(arr);

Array.prototype.myOwnMap = function(callback) {

    let newArray = [];
    
    /**
     * let len = this.length;
    for(let i = 0; i < len; i++){
        let temp = callback(this[i]);
        newArray.push(temp);
    }


    for(let ele =of this){
        let temp = callback(ele);
        newArray.push(temp);
    }


     this.forEach((item)=> {
        let newT = callback(item);
        newArray.push(newT);
        
    });

    **/

   
 for(let ele of this){
        let temp = callback(ele);
        newArray.push(temp);
    }
    return newArray;
}

var arrr = [11, 2, 3].myOwnMap(e => e * 2);
console.log(arrr);
