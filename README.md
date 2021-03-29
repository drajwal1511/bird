# Bird
# Note
You can see the output in console as well as alert dialog box.   
# Problem
![image](https://user-images.githubusercontent.com/44205030/112805536-51afcc80-9093-11eb-9379-70b6260074ba.png)   
# Code
setTimeout(bird,1000);   
function bird(){   
    var n=prompt("Enter Number of elements");   
var arr=[n];   
for(var i=0;i<n;i++){   
    arr[i]=prompt("Enter Element ",i+1);   
}   
let myMap=new Map();    
for(var i=0;i<n;i++){   
    myMap.set(arr[i],0);   
}   
for(var i=0;i<n;i++){   
    myMap.set(arr[i],myMap.get(arr[i])+1);   
}   
var maxocc,minocc,maxid,minid;   
maxocc=-1;   
minocc=Number.MAX_SAFE_INTEGER;   
for(let [num,occ] of myMap){   
    if(occ>maxocc){   
        maxocc=occ;   
        maxid=num;   
    }   
    if(occ<minocc){   
        minocc=occ;   
        minid=num;   
    }   
}   
if(maxocc===-1){   
    console.log("Enter Atleast 1 Elements");   
}else{   
    alert("Output - ["+maxid+", "+minid+"]");   
    console.log("Output - [",maxid,", ",minid,"]");   
}   
}   
