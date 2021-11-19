# split-array
Split array in equal number of parts
 
`function splitArray(flatArray, numCols){
  const newArray = []
  for (let c = 0; c < numCols; c++) {
    newArray.push([])
  }
  for (let i = 0; i < flatArray.length; i++) {
    const mod = i % numCols
    newArray[mod].push(flatArray[i])
  }
  return newArray
}

function splitToChunks(array, parts) {
    let result = [];
    for (let i = parts; i > 0; i--) {
        result.push(array.splice(0, Math.ceil(array.length / i)));
    }
    return result;
}
function split(array, n) {
  let [...arr]  = array;
  var res = [];
  while (arr.length) {
    res.push(arr.splice(0, n));
  }
  return res;
}

console.log(splitArray([1,2,3,4], 3))
console.log(splitToChunks([1,2,3,4], 3))
console.log(split([1,2,3,4], 3))`
