
<h1 style="text-align:justify; font-size:2vw; text-align:center;" > CAD设计 </h1>
<h2 style="text-align:justify; font-size: 1.5vw; text-align:center;" > 欢迎来到我们的项目 </h1>
<br> <br>


### 装配 Cad 设计和程序


<iframe src="https://myhub.autodesk360.com/ue28cacf9/shares/public/SH35dfcQT936092f0e43fec32ea03667fe3c?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true" frameborder="0"></iframe>

<h3 align="left"><u>如何逐步在 Fusion 中进行设计</u></h3>

<div>
<p class="p1"><b>步骤1:New Design</b><br>
Open Fusion>file>new design</p>
<img align="center" src="/img/AndryEricstep1inFusion.png" alt="box" width="600" height="400" class="center">


<p class="p1"><b>步骤 2:Create a box</b></br>
Select axis><br></p>
<img align="center" src="/img/AndryEricinfusionselectaplaneorplanarface.png" alt="box" width="600" height="400" class="center">
<img align="center" src="/img/AndryEricstep2infusionselectaxis.png.png" alt="box" width="600" height="400" class="center">

<img align="center" src="/img/AndryEricstep2infusionselectaxis.png" alt="box" width="600" height="400" class="center">

<img align="center" src="/img/AndryEricstep2infusionselectaxis.png" alt="box" width="600" height="400" class="center">
<p class="p1">solid>create>box</p>
<img align="center" src="/img/AndryEricstep2znfusionsolidcreatebox.png" alt="box" width="600" height="400" class="center">


<p class="p1"><b>步骤 3:Specify the dimensions</b><br>
Clicking + hold>drag from a corner<br> 
Specify dimensions: length 44 mm, press tab,  width 22 mm> click "enter"</p>
<img align="center" src="/img/AndryEricforfusionspecifythedimensions.png" alt="box" width="600" height="400" class="center">


<p class="p1"><b>步骤 4:Extrude</b><br>
Click + hold>drag>Extrude<br> 
Height 10 mm</p>
<img align="center" src="/img/AndryEricinfusionstep4extrude.png" alt="box" width="600" height="400" class="center">


<p class="p1"><b>步骤 5:Bevel the corners</b><br>
Select an edge>Modify>chamfer>choose 2 mm>do it for 4 edges</p>
<img align="center" src="/img/AndryEricinfusionstep5bevelthe1stcorner.png" alt="box" width="600" height="400" class="center">

<img align="center" src="/img/AndryEricstep1inFusion.png" alt="box" width="600" height="400" class="center">

<img align="center" src="/img/AndryEricinfusionstep5bevelthe4corners.png" alt="box" width="600" height="400" class="center">


<p class="p1"><b>步骤 6:Shell</b><br>
utilities>modify>shell: the body becomes hollow<br>
choose 9 mm</p>
<img align="center" src="/img/AndryEricinfusionstep6shell.png" alt="box" width="600" height="400" class="center">

<img align="center" src="/img/AndryEricinFusionstep6createahollowcavity.png" alt="box" width="600" height="400" class="center">

<img align="center" src="/img/AndryEricinFusionstep6createahollowcavity2.png" alt="box" width="600" height="400" class="center">


<p class="p1"><b>步骤 7: Create the inside walls</b><br>
- Same as 步骤s 2 to 4<br>
- Specify the dimensions: length 10 mm, width 1 mm , height 22 mm> and in the dialog box> operation>join</p>
<img align="center" src="/img/AndryEricstep2znfusionsolidcreatebox.png" alt="box" width="600" height="400" class="center">

<img align="center" src="/img/ndryEricinFusionstep7createinsidewalls.png" alt="box" width="600" height="400" class="center">


<p class="p1"><b>步骤 8:Create a square hole for the Digital Fingerprint  Reader component</b><br>
Specify the dimensions and and in the dialog box> operation>cut</p>
<img align="center" src="/img/AndryEricinFusioncreateasquarehole.png" alt="box" width="600" height="400" class="center">


<p class="p1"><b>步骤 9:Create a hole</b><br>
solid>create>hole and specify the dimensions: here diameter 2 mm</p>
<img align="center" src="/img/AndryEricinFusionstep10createaroundhole2.png" alt="box" width="600" height="400" class="center">


<p class="p1"><b>步骤 10:Create a rode</b><br>
solid>create>cylinder and extrude: length 12.252 mm and diameter of 1.95 mm because has to go inside the hole of a diameter of 2 mm</p>
<img align="center" src="/img/AndryEricinFusionstep9createaroundhole.png" alt="box" width="600" height="400" class="center">


<p class="p1"><b>步骤 11:Solid>create>coil</b><br>
Specify the dimensions: loop length 55.441 mm and surface 41.595 mm^2</p>
<img align="center" src="/img/AndryEricinfusionstep11createacoil.png" alt="box" width="600" height="400" class="center">

<p class="p1"><b>步骤 12:Assemble the rod with the case</b><br>
-Click on the original component in the browser:here “Inner mechanism of a locker”<br>
>dropdown>choose “rigid group”: locks the relative positions of the selected components</p>
<img align="center" src="/img/AndryEricstep12assembletherodwiththecase2.png" alt="box" width="600" height="400" class="center">
![Alt text](../img/AndryEricstep12assembletherodwiththecase2.png)
<img align="center" src="/img/AndryEricinFusionstep12assembletherodwiththecase3.png" alt="box" width="600" height="400" class="center">

<p class="p1">-Click on utilities>assemble>joint>select carefully the faces of each object we want to join in this case the case of the locker with the rod</p>
<img align="center" src="/img/AndryEricinFusionstep12assembletherodwiththecase.png" alt="box" width="600" height="400" class="center">

<img align="center" src="/img/AndryEricstep12assembletherodwiththecase4.png" alt="box" width="600" height="400" class="center">
<br>
<img align="center" src="/img/AndryericinFusionstep12assembletherodwiththecase5.png" alt="box" width="600" height="400" class="center">
<img align="center" src="/img/AndryEricinFusionstep12Assembletherodwiththecase6.png" alt="box" width="600" height="400" class="center">

<img align="center" src="/img/AndryEricinfusionstep12assembletherodwiththecase7.png" alt="box" width="600" height="400" class="center">


<p class="p1"> Push the rod inside by clicking and dragging</p>
<img align="center" src="/img/ndryEricinfusionstep13pushtherodinsidebyclickinganddragging.png" alt="box" width="600" height="400" class="center">


<p class="p1"><b>步骤 13:Assemble the coil with the inserted rod</b><br>
Click on utilities>assemble>joint>select carefully the faces of each object we want to join in this case the coil with the inserted rod</p>
<img align="center" src="/img/AndryEricinfusionstep13pushtherodinsidebyclickinganddragging.png" alt="box" width="600" height="400" class="center">

<img align="center" src="/img/AndryEricstep13pushtherodinsideparclickinganddragging2.png" alt="box" width="600" height="400" class="center">


</div>
</div>

# Some Other Fusion

> ## by Abdiaziz Omar Hassan

<iframe src="https://myhub.autodesk360.com/ue2fba46f/shares/public/SH9285eQTcf875d3c53903b9d04fb3842395?mode=embed" width="1024" height="768" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

## by Mohamed Khaled

<iframe src="https://myhub.autodesk360.com/ue28cacf9/shares/public/SH35dfcQT936092f0e43b14627f50a6167e7?mode=embed" width="300" height="280" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

### Process
**1<sup>st</sup> 步骤** Click Creat then <span style="color: green"> select Circle</span> then creat a circle with 200mm and center small circle inside circle 40 mm then Extrode 30 mm
<br><br>

<img width=500 src="img/1.png">
<br><br>

**2<sup>nd</sup> 步骤**
<br><br>

<img width=500 src="img/2.png">
<br><br>

**3<sup>rd</sup> 步骤**
<br><br>

<img width=500 src="img/3.png">
<br><br>

**4<sup>th</sup> 步骤**
<br><br>

<img width=500 src="img/4.png">
<br><br>

**5<sup>th</sup> 步骤** : <span style="color:green"> Finish the Sketch </span>
<br><br>

<img width=500 src="img/5.png">
<br><br>

**6<sup>th</sup> Step**
<br><br>

<img width=500 src="img/6.png">
<br><br>

**7<sup>th</sup> 步骤**
<br><br>

<img width=500 src="img/7.png">
<br><br>

**8<sup>th</sup> 步骤** <span style="color:green"> Finish the Sketch </span>
<br><br>

<img width=500 src="img/8.png">
<br><br>

**9<sup>th</sup>步骤** : 
<br><br>

<img width=500 src="img/9.png">
<br><br>

**10<sup>th</sup> 步骤**
<br><br>

<img width=500 src="img/10.png">
<br><br>

**11<sup>th</sup> 步骤**
<br><br>

<img width=500 src="img/11.png">
<br><br>

## by Winkee

<iframe src="https://myhub.autodesk360.com/ue28cacf9/shares/public/SH35dfcQT936092f0e43efa7ca21b2232176?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>
<br><br>
<iframe src="https://myhub.autodesk360.com/ue28cacf9/shares/public/SH35dfcQT936092f0e43eb87905180cdbab7?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

## By Peter

#### Golf Ball 

<iframe src="https://myhub.autodesk360.com/ue28cacf9/shares/public/SH35dfcQT936092f0e430700ac2bb3369af7?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

Autodesk Fusion 360 showing how to design a golf ball.

<br><br>

<img width=500 src="img/p9.png">

<br><br>

Tools used in this tutorial are

1. Revolve
<br>

<br><br>

<img width=500 src="img/p1.png">

<br><br>

<br>
2. Extrode

<img width=500 src="img/p2.png">

<br><br>

<br>
3. Pattern

<br><br>

<img width=500 src="img/p5.png">

<br><br>

<br><br>

<img width=500 src="img/p6.png">

<br><br>

4. Shell
<br><br>

<img width=500 src="img/p7.png">

<br><br>
5. Mirror
<br><br>

<img width=500 src="img/p8.png">

<br><br>


6. Combine
<br><br>

<img width=500 src="img/p9.png">

<br><br>