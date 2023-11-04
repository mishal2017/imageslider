# imageslider


<!DOCTYPE html>
<html>
<head>
    <title>My Webpage</title>
</head>
<body>
    
<button onclick="previous()"> Previous</button>

<img src="image/Screenshot (18).png" alt=""  height="300px" width="300px"> 

<button onclick="next()"> Next</button>


    <script src="Index.js">    
    </script>
</body>
</html>



var photo = ["image/Screenshot (18).png", "image/Screenshot_2023022_220342.png", "image/snap.png"]
var imgTag = document.querySelector("img");

var count = 0;

function next(){
    count ++;
if (count>=photo.length){
    count = 0;
    imgTag.src = photo[count];
}
else{
    imgTag.src = photo[count];}
    

}

function previous(){
       count--;
       if (count< 0){                   // count<0 means minus value and count= photo.length-1 means we are substracting the index value in that case -1-1=2 and it will show the indext value of 2
        count= photo.length-1;
        imgTag.src= photo[count];
       }
       else{ imgTag.src = photo[count];}
      

}
