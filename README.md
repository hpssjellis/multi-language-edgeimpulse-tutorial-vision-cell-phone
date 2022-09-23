
### Multi-lnaguage EdgeImpulse Vision Machine Learning Tutorial


##### version 1.4.1-118


Demo of this Github  [https://hpssjellis.github.io/multi-language-edgeimpulse-tutorial-vision-cell-phone/](https://hpssjellis.github.io/multi-language-edgeimpulse-tutorial-vision-cell-phone/#top)


This Github Repository (replace this link with your Repository Link) [https://github.com/hpssjellis/multi-language-edgeimpulse-tutorial-vision-cell-phone](https://github.com/hpssjellis/multi-language-edgeimpulse-tutorial-vision-cell-phone)



 ### By Jeremy Ellis Twitter <a href="https://twitter.com/rocksetta">@Rocksetta </a> Use at your own Risk!


### By Jeremy Ellis Twitter @Rocksetta Use at your own Risk!
### Note when looking at the markdown none of the javascript buttons appear, you must go to your Gitpages Demo Link!
A few Javascript abilites do not work, such as hiding the code. So all the Javascript not in buttons is below. 

Note: 
1. Old ML presentation [here](https://hpssjellis.github.io/my-robotics-machine-learning-teaching-lightning-talk-pecha-kucha/)
2. Old TensorflowJS presentation [here](https://hpssjellis.github.io/lightening-talk-Pecha-Kucha-tensorflowjs/)
3. Teacher Presentation Feedback [here](https://hpssjellis.github.io/jeremy-ellis-tinyML-teacher-feedback-2022/)
4. Pecha Kucha template [here](https://github.com/hpssjellis/pecha-kucha-lightning-talks-template)
<br><br>
 
 ### Note when looking at the markdown none of the javascript buttons appear, you must go to your Gitpages Demo Link!
A few Javascript abilites do not work, such as hiding the code. So all the Javascript not in buttons is below. 

 
 <br><br><br><br><br>
 <hr>
 




<script>
 let myIndex = 1;
 let myLooper = 0;
 let myCounting = 0;
 let myMainNum = '10,10';  
 let myMainNum2 = '10,10'; 
 let myMainNumLast = 20;
 let myCountUp = 0;
 let xSlide = 3;
 let myAudio01 = new Audio();
 document.body.style.backgroundColor = "skyblue";
;
 
function mySetup(){
   document.getElementById('myStick').style.display = 'none';                                                 
   xSlide  = document.getElementById('myCountLinks').value; 
   myMainNum = document.getElementById('myCountMax').value.split(','); 
   myMainNumLast = myMainNum[0]
   console.log('myMainNum')
   console.log(myMainNum)
   console.log('myIndex, myMainNumLast, myMainNum[myIndex]')
   myAudio01.pause();
   myAudio01.currentTime = 0;  
   myIndex = 0;  
   clearInterval(myLooper);  
   myCountUp = -1;
} 
 
function carousel() {
  clearInterval(myCounting);
  myCountUp = -1;
  var i;
  myIndex++;
  if (myIndex > xSlide) {myIndex = xSlide};    
  window.location.href='#'+myIndex;
  if (Number.isInteger( parseInt(myMainNum[myIndex-1]) ) ) {
     myMainNumLast = parseInt(myMainNum[myIndex-1]) 
  }  
  console.log(myIndex +', '+ myMainNumLast +', '+  myMainNum[myIndex-1])
  myCountDown();
  myCounting = setInterval(myCountDown, 1000);
  myLooper = setTimeout(carousel, myMainNumLast*1000); 
}
  
function myCountDown(){
  myCountUp++;
  if (myCountUp >= myMainNumLast ) {
    myCountUp = myMainNumLast;                              
  }
  if (myIndex >= xSlide && myMainNumLast == myCountUp){ 
     document.getElementById("myNumSlides").innerHTML = `&nbsp;&nbsp;&nbsp; Slide ${myIndex} of ${xSlide} slides. ALL DONE <input type=button value="Show"  style="height:25px; " onclick="{document.getElementById('myStick').style.display = 'inline'; }"> `;
     clearInterval(myCounting);             
     clearInterval(myLooper);  
  }
  else {    
     document.getElementById("myNumSlides").innerHTML = `&nbsp;&nbsp;&nbsp; Slide ${myIndex} of ${xSlide} slides. ${myMainNumLast-myCountUp} seconds remaining <input type=button value="Show" style="height:25px; " onclick="{document.getElementById('myStick').style.display = 'inline'; }"> `;
  }
}
;
function myNext(){   
  xSlide  = document.getElementById('myCountLinks').value; 
  myMainNum = document.getElementById('myCountMax').value;                        
  clearInterval(myLooper) ; 
  carousel();  
}  
;
</script> 
 

