
### Vanilla Javascript Lightning Talk Pech Kucha Markdown HTML README.md


##### version 1.2.0-99

Fork this repo, fill in your markdown and <html> for the 15 slides (max 20 slides), record your presentation and save it as ```recorded-talk.m4a``` (or change the code to reflect the new name.)
 
 Setup gitPages --> settings-->pages-->none to master-->save--> copy the link and replace below.

Demo of this Github Markdown can be viewed at this GitPages site (replace this link with your Gitpages link) [https://hpssjellis.github.io/multi-language-edgeimpulse-tutorial-vision-cell-phone/](https://hpssjellis.github.io/multi-language-edgeimpulse-tutorial-vision-cell-phone/)


This Github Repository (replace this link with your Repository Link) [https://github.com/hpssjellis/multi-language-edgeimpulse-tutorial-vision-cell-phone](https://github.com/hpssjellis/multi-language-edgeimpulse-tutorial-vision-cell-phone)


Number of Slides: <input type="text" id="myCountLinks" size="6" value="15" >, Seconds for each Slide: <input type="text" id="myCountMax" size="30" value="10,12" >   Can be a list of seconds example: 17, 20, 24, 20 The last number continues.
 
 
 To convert to any language click <a href="https://translate.google.com/?sl=en&tl=es&op=websites">here</a><br>
 For example This page in: <a href="https://hpssjellis-github-io.translate.goog/multi-language-edgeimpulse-tutorial-vision-cell-phone/?_x_tr_sl=en&_x_tr_tl=fr&_x_tr_hl=en&_x_tr_pto=wapp">French</a>, <a href="https://hpssjellis-github-io.translate.goog/multi-language-edgeimpulse-tutorial-vision-cell-phone/?_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=en&_x_tr_pto=wapp">Spanish</a>, Original in <a href="https://hpssjellis.github.io/multi-language-edgeimpulse-tutorial-vision-cell-phone/">English</a>
 
  



<input  type="button" value="initilize speak" onclick="{  
   let myVoice = 'Russian Female'
   responsiveVoice.speak(document.getElementById('google_translate_element').innerText, myVoice, {pitch: 1, rate: 1, volume : 1})                                              
}"><br><br>
  
  
 <input type=button value="Sound by Mr. Ellis in English" onclick="{ 
   document.getElementById('myCountMax').value = '2,5,1,3,1,6,3,20';    
   mySetup();                                             
   myAudio01 = new Audio('recorded-talk.m4a');
   myAudio01.play(); 
   carousel();                                                
}"> 

 
 
<div id="myNumSlides" style=" position:sticky; top:0px; left:20px; height:25px; "> ...</div>  <br>

  


<div id="myStick"  style=" position:sticky; top:30px; display:inline; ">
 
 <input type=button value="Start-No-Sound" onclick="{
   mySetup()
   carousel();  
}">
 
 
 
  <input type=button value="Rewind" onclick="{
   myIndex = 0;  
   clearInterval(myLooper);
   clearInterval(myCounting);
   if (myAudio01.paused && myAudio01.currentTime > 0 && !myAudio01.ended) {
      } else {
         myAudio01.pause();
     }
}">   

 <input type=button value="-" onclick="{
   clearInterval(myLooper);
   clearInterval(myCounting);
   myIndex -= 1;    
   window.location.href='#'+myIndex;
}">   
  
<input type=button value="+" onclick="{
  clearInterval(myLooper);
  clearInterval(myCounting);
  myIndex += 1;  
  window.location.href='#'+myIndex;
}"> 
  
<input type=button value="Back" onclick="{
   myIndex = myIndex - 2;    
   if (myIndex <= 0){myIndex=0};                                      
   myNext();
}">   
  
<input type=button value="Next" onclick="{
   myNext();
}"> 
 
    
  
 <input id="myPause" type=button value="Pause" onclick="{ 
   clearInterval(myLooper);
   clearInterval(myCounting);
   if (this.value == 'Pause'){                                                     
       this.value = 'Play / Pause'; 
       if (myAudio01.paused && myAudio01.currentTime > 0 && !myAudio01.ended) {
      } else {
         myAudio01.pause();
     }
   } else {    
     myIndex -= 1; 
     myCountUp += 1;
     carousel();                                                 
     this.value = 'Pause';  
     if (myAudio01.paused && myAudio01.currentTime > 0 && !myAudio01.ended) {
         myAudio01.play();
      }                                                    
   }
}"> 
 
<input type=button value="Hide" onclick="{
   document.getElementById('myStick').style.display = 'none';
}"> 
  <input type=button value="TOP" onclick="{ 
   window.location.href='#top'; 
}">  
  
 </div>





<div id="google_translate_element">I really like javascript</div>


#### 1
# Intro to Edge Impulse before using the Arduino Machine Learning Kit.

First login to <a href="https://edgeimpulse.com/">edgeImpulse.com</a> and then create a new Project

<img src="https://user-images.githubusercontent.com/5605614/190931142-55689c3c-124b-4558-ba9c-d025ef148461.png" title="EdgeImpulse login or setup" width=400 /> <img src="https://user-images.githubusercontent.com/5605614/190931666-39a92ca7-e8d6-435c-86ac-ef1ed825008d.png" title="Create new project" width=500 />


<hr>

#### 2
# Dashboard

Check the dashboard far right to see if you have vision set to a single label per item and the latency calculations to the Arduino ML Kit, or whatever microcontroller board you will be working with. Note: Some screens must be increased to see the left menu that shows the main EdgeImpulse steps.

<img src="https://user-images.githubusercontent.com/5605614/190931807-c63b069a-307e-454b-998e-839cde729637.png" title="Check Dashboard" width=500 /> <img src="https://user-images.githubusercontent.com/5605614/191381569-e775786f-43c3-46b3-87bc-f10ebb24acb5.png****" title="Check Dashboard" width=500 />

<br><br><br>
<hr>

#### 3
# Connect Device  
Select Devices. For this demonstration we will connect a cell phone to EdgeImpulse instead of your Arduino ML kit. Click "Connect a Device". Then click Generate QR Code"

<img src="https://user-images.githubusercontent.com/5605614/190931865-eabede2e-8e10-4117-bf73-c1fe8f2c0d21.png" title="Connect a device" width=600 /> <img src="https://user-images.githubusercontent.com/5605614/190931905-0f4e8889-e4db-450e-8503-d01cd5c0258f.png" title="Generate QR Code" width=300 />

Many students will have QR code reading ability on their cell phones. Read the QR code and let it load the page.

Click "Allow Permissions"

<img src="https://user-images.githubusercontent.com/5605614/190932524-d2c92bff-5ee6-4b2d-bf19-d4c423a584b9.png" title="QR code loads" width=200 /> <img src="https://user-images.githubusercontent.com/5605614/190932534-3966d36a-18fb-4004-aa35-6c529a520765.png" title="Permissions" width=200 />

<br><br><br><br><br>
<hr>

#### 4
# Edge Impulse Web App Data Collection: Label Unknown

Make sure the label says "unknown" before taking about 50 images of things that do not look like "pens". Note: There is a small advantage to make your labels numerical by putting a number directly before the label. For example:  "0unknown"
 
<img src="https://user-images.githubusercontent.com/5605614/190932549-b12f03d2-0416-4d1f-9966-ea1df91285b2.png" title="Unknown" width=200 />

<br><br><br><br><br>
<hr>

#### 5
# Edge Impulse Web App Data Collection: Label Pen

Make sure the label says "pen" before taking about 30 images of pens or pencils. Note: There is a small advantage to make you labels numerical by putting a number directly before the label for example: "1pen", if you have more labels "2stapler" etc. For later coding this allows checking the first digit to see what the whole label is. 

<img src="https://user-images.githubusercontent.com/5605614/190932565-18a1cd7a-e056-4f85-805d-e19b13d1a102.png" title="Pen" width=200 />

<br><br><br><br><br>
<hr>

#### 6
# Data Acquisition and Labels

Select Data Acquisition.  
Many students mess up and forget to label the items. You can manually edit the label names,  also filter by names and select multiple filters. (But be carefully you don't really mess up the labels)

<img src="https://user-images.githubusercontent.com/5605614/190932155-952cbfa1-9609-4482-9e52-61fee6be4833.png" title="Data and labels" width=600 />

<br><br><br>
<hr>

#### 7
# Design your Impulse (Machine Learning Model)
Select Design Impulse 
This page looks complex but we are just going to use the defaults. 96 x 96 image (the maximum image would be 320 x 320 but wont work on many devices). Note the image  is always square.
 
 For both "Add a Processing Block" and "Add a learning Block" we are just going to use the default identified with a yellow star. Make sure you check that you only have 2 labels (unknown and pen) for this demo and that you click "Save Impulse"

<img src="https://user-images.githubusercontent.com/5605614/190932775-779d6926-d510-4ab4-973a-d37c23ba127f.png" title="Impulse Design" width=600 />

<br><br>
<hr>

#### 8
# Image Features
Select Image and then click "Save Parameters" and then click "Generate Features". It takes a few minutes to show the graph "Feature Explorer" See if your data looks like it will be easily seperated.


<img src="https://user-images.githubusercontent.com/5605614/190932896-2894d08c-42e4-40bf-b2f8-699435c0332b.png" title="Image Features" width=500 /> <img src="https://user-images.githubusercontent.com/5605614/190932937-2733d1aa-f882-46cc-ba0f-4b900251a9cd.png" title="Features finished" width=500 />


<hr>

#### 9
# Transfer Learning
Select Transfer learning and then change the Training Cycles from 20 to 200, Select Auto balance Dataset and Data Augmentation and click "Start Training" This step might take several minutes. Check the "loss" if you can read it. Hopefully is is gracefully reducing. The smaller the loss is, the relatively better your dataset is learning. When finished, your model will show the accuracy, Confusion Matrix which is faily easy to understand and the Data Explorer which gives a visual graph of how well your data has been sperated into distinct sets.
 
<img src="https://user-images.githubusercontent.com/5605614/190945162-03662614-cdeb-43ec-92fa-0fe9201ec8ce.png" title="Transfer Learning" width=600 />
 

<hr>

#### 10
# Check your data, on EdgeImpulse with the testing dataset.
Choose Live Classification  
Choose a test sample, preferably one that has the pen in it first. 

Note: For the later WASM example the RAW FEATURES will be useful to copy for later.
 
<img src="https://user-images.githubusercontent.com/5605614/190945290-6d11060f-0e88-4b8a-9f09-0d06eac74baf.png" title="Live Classification" width=600 />


<hr>

#### 11
# Check you data using your cell phone loaded with the EdgeImpulse Web App

Back to your cell phone which you might have to re-connect to edgeImpulse. Click the button "Switch to Classification". Scan many objects and see the percent in decimal format 0.73 = 73%. Notice how fast the model analyses objects. 

<img src="https://user-images.githubusercontent.com/5605614/191164011-0ea13926-6579-43bc-b950-0cc8f7f38dfc.png" title="Switch to Classification" width=200 /> <img src="https://user-images.githubusercontent.com/5605614/191164153-81ebd3d8-c789-4bd8-835b-e343c7d2965b.png" title="Inference1" width=200 /> <img src="https://user-images.githubusercontent.com/5605614/191164252-8c164b99-df14-4b87-986e-f27ad79ee2ad.png" title="Inference2" width=200 /> <img src="https://user-images.githubusercontent.com/5605614/191164328-1ef2203d-203f-4ec7-abe1-30aed6350a91.png" title="Inference3" width=200 />
 
 
 
 
<br><br><br>
<hr>

#### 12
# Check you data using EdgeImpulse WASM (Web Assembly Language)

For this optional, but well worth it, step you would need an HTTPS web server like github that has be converted to show gitpages. Very easy in github: select "settings" then pages then change "none" to "master" and save, then wait 30 seconds and refresh to see your website URL.

On EdgeImpulse select "Deployment" choose "WASM and click "Build". Then look in your downloads folder. Then unzip the downloaded folder and upload the "browser" folder to your HTTPS webserver. 
 
 
  
<img src="https://user-images.githubusercontent.com/5605614/190945653-509f70ef-2da5-4e1f-89a8-ffd34e560a0f.png" title="WASM Deployment" width=400 /> <img src="https://user-images.githubusercontent.com/5605614/190945861-240340df-ccd4-4726-acca-1c2e74bfc190.png" title="unzip WASM for browser" width=400 />
 
 
 <br><br><br><br><br>
<hr>

#### 13
# Check you data using EdgeImpulse WASM (web Assembly Language)

Reminder: you would need an HTTPS web server such as github setup to use Gitpages.

Note: This step will not work from your computer even though it looks like the page loads fine. 

Paste your RAW FEATURES that you copied from the "Live Classification" into the test box of the WASM index.html and see if you get similar results to what you got with the Live Classification.

<img src="https://user-images.githubusercontent.com/5605614/190948297-cce2cc02-2539-418c-8f1b-d0b474ae3328.png" title="EdgeImpulse and Rocksetta WASM" width=600 />
 
 

<hr>

#### 14
# Check you data using Rocksetta index.html and EdgeImpulse WASM

On your HTTPS webserver (I use gitpages) the "browser" folder you uploaded with the edgeImpulse WASM code, replace the index.html file with my (Twitter @Rocksetta) Javascript HTML WebCam Demo page That can be dowloaded at  [downloads/index.html](downloads/index.html)
 

 Then replace the index.html file with this file that I made which uses the computers webcam  [downloads/index.html](downloads/index.html)
 
 What you have is a webpage that can be edited but is similar to the Cell Phone EdgeImpulse Web App that you can use from a desktop computer or a cell phone that allows you to test out your edgeimpulse analysis on real data. The second image is an animated gif file showing what the rocksetta index.html file makes the EdgeImpulse WASM look like. 


 
 
 
<img src="https://user-images.githubusercontent.com/5605614/190948583-7f5e3540-4383-4ebe-8040-223520812e54.png" title="Rocksetta WASM" width=400 /> <img src="rocksetta-edgeimpulse-wasm-small.gif" title="Rocksetta-Wasm-gif" width=400 />
 
 

<hr> 
#### 15
# End of presentation
    
   <!--   This is the end of google translate div -->

<a href="#top">Top of page</a>







 ### By Jeremy Ellis Twitter <a href="https://twitter.com/rocksetta">@Rocksetta </a> Use at your own Risk!


### By Jeremy Ellis Twitter @Rocksetta Use at your own Risk!
### Note when looking at the markdown none of the javascript buttons appear, you must go to your Gitpages Demo Link!
A few Javascript abilites do not work, such as hiding the code. So all the Javascript not in buttons is below. 

Note: 
1. Old ML presentation [here](https://hpssjellis.github.io/my-robotics-machine-learning-teaching-lightning-talk-pecha-kucha/)
2. Old TensorflowJS presentation [here](https://hpssjellis.github.io/lightening-talk-Pecha-Kucha-tensorflowjs/)
3. Teacher Presentation Feedback [here](https://hpssjellis.github.io/jeremy-ellis-tinyML-teacher-feedback-2022/)
4. Pecha Kucha template [here](https://github.com/hpssjellis/pecha-kucha-lightning-talks-template)
<br><br><br><br><br><br><br><br><br><br><br>
 <hr>
 






<a href="#top">Top of page</a>









### By Jeremy Ellis Twitter @Rocksetta Use at your own Risk!
### Note when looking at the markdown none of the javascript buttons appear, you must go to your Gitpages Demo Link!
A few Javascript abilites do not work, such as hiding the code. So all the Javascript not in buttons is below. 


<script src="https://translate.google.com/translate_a/element.js?cb=googleTranslateElementInit"></script>
<script src='https://code.responsivevoice.org/responsivevoice.js'></script>

<script>
    function googleTranslateElementInit() {
  new google.translate.TranslateElement({pageLanguage: 'en', includedLanguages: 'en,fr,de,ru', layout:google.translate.TranslateElement.InlineLayout.SIMPLE, autoDisplay: false}, 'google_translate_element');

    }
</script>

<script>
 let myIndex = 1;
 let myLooper = 0;
 let myCounting = 0;
 let myMainNum = '10,10';  
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
   console.log('myMainNum')
   console.log(myMainNum)
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
;
  myIndex++;
  if (myIndex > xSlide) {myIndex = xSlide};    
  window.location.href='#'+myIndex;
  myCountDown();
  myCounting = setInterval(myCountDown, 1000);
  if (Number.isInteger( parseInt(myMainNum[myCounting]) ) ) {myMainNumLast = parseInt(myMainNum[myCounting]) }  // check if integer or use last one
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
 
