<h2 style="font-size :3.1rem; text-align:center"> Arduino and Processing Visualization </h2>

<p class="p2" style="font-size :1.1rem; text-align:Justify"> We showed a project that makes use of an Arduino Uno Rev 3 and a phototransistor. The phototransistor data is parsed and passed to Processing. Processing, like the Arduino IDE, is an open source integrated development environment (IDE) that is utilized by both designers and artists! You can use Processing to create beautiful visual and interactive experiences. With a serial library, you may transfer Arduino serial data to Processing (in Processing). This enables you to use data from a wide range of sensors!</p>

<h4 style="font-size :2.1rem; text-align:center">Circuit</h4>

<img align="center" src="img/proc1.jpg" alt="box" width="100%" class="center"> 
<h4 style="font-size :1.1rem; text-align:left">List of components</h4>

- Arduino Mega
<br>
- Photoresistor
<br>
- 10k Ω resistor
<br>
- Jumper cables
<br>

<h4 style="font-size :2.1rem; text-align:left">Phototransistor</h4>
<p class="p2" style="font-size :1.1rem; text-align:Justify" >The phototransistor is a transistor that responds to light hitting it by generating and amplifying an electric current. In this project we use it to control the visuals created in Processing. </p>
<h4 style="font-size :2.1rem; text-align:left">Code</h4>
<h5 style="font-size :1.2rem; text-align:left"> Arduino Sketch </h5>

```Arduino
unsigned int ADCValue;
void setup(){
    Serial.begin(9600);
}

void loop(){

 int val = analogRead(0);
   val = map(val, 0, 300, 0, 255);
    Serial.println(val);
delay(50);
}

```

<p class="p2" style="font-size :1.1rem; text-align:Justify" >Connect the Arduino to the computer using a USB cable and upload the code to your board. Make sure that the serial monitor is printing the values from the phototransistor. When you are done uploading, you can move on to Processing. </p>


<h5 style="font-size :1.2rem; text-align:left"> Processing </h5>

<p class="p2" style="font-size :1.1rem; text-align:Justify" > In this project we are going to control Processing sketches with the Arduino via serial communication. Processing is free, open source software based on Java. It was designed for the visual arts community for creating drawings, animations, and interactive programs. Download the latest version of Processing from Processing.org. Select the right file according to your operating system. Processing is available for Linux, Mac OS X, and Windows. Extract all the files and click the Processing icon inside the folder to open it. The Processing IDE interface is very simple. The play icon in the toolbar allows you to compile and run the program and the stop icon will stop the program. In the bottom of the IDE there is a message area that, when you compile your program, gives you information about errors if any. Upload the different examples found below and play around with them! </p>

<h5 style="font-size :1.1rem; text-align:left"> Example 1: Directional light </h5>
<h6 style="font-size :1.1rem; text-align:left"> Processing Sketch: </h6>

``` Processing 
import processing.serial.*;

Serial myPort;  // Create object from Serial class
static String val;    // Data received from the serial port
int sensorVal = 0;

void setup()
{
  fullScreen(P3D);
  noStroke();
  fill(204);
  String portName = "COM11";// Change the number (in this case ) to match the corresponding port number connected to your Arduino. 

  myPort = new Serial(this, portName, 9600);
}

void draw()
{
  if ( myPort.available() > 0) {  // If data is available,
  val = myPort.readStringUntil('\n'); 
  try {
   sensorVal = Integer.valueOf(val.trim());
  }
  catch(Exception e) {
  ;
  }
  println(sensorVal); // read it and store it in vals!
  }  
  noStroke(); 
  background(0); 
  float dirY = (sensorVal/ float(height) - 0.5) * 2 * -1;
  float dirX = (mouseX / float(width) - 0.5) * 2;
  directionalLight(204, 204, 204, -dirX, -dirY, -1); 
  translate(width/2 - 100, height/2, 0);  
  translate(200, 0, 0); 
  sphere(200);


  fill(255);
  ellipse(random(width), random(height), 3, 3);

}
```
<img align="center" src="img/proc8.png" alt="box" width="100%" class="center"> 
<br>
<img align="center" src="img/procg1.gif" alt="box" width="100%" class="center"> 

<h5 style="font-size :1.1rem; text-align:left"> Example 2: Bezier </h5>
<h6 style="font-size :1.1rem; text-align:left"> Processing Sketch: </h6>

``` Processing
import processing.serial.*;

Serial myPort;  // Create object from Serial class
static String val;    // Data received from the serial port
int sensorVal = 0;

void setup()
{
   size(720, 480);
  stroke(255);
  noFill();
  String portName = "COM11";// Change the number (in this case ) to match the corresponding port number connected to your Arduino. 

  myPort = new Serial(this, portName, 9600);
}

void draw()
{
  if ( myPort.available() > 0) {  // If data is available,
  val = myPort.readStringUntil('\n'); 
  try {
   sensorVal = Integer.valueOf(val.trim());
  }
  catch(Exception e) {
  ;
  }
  println(sensorVal); // read it and store it in vals!
  }  
 background(0);
  for (int i = 0; i < 200; i += 20) {
    bezier(sensorVal-(i/2.0), 40+i, 410, 20, 440, 300, 240-(i/16.0), 300+(i/8.0));
  }

}
```

<img align="center" src="img/proc3.jpg" alt="box" width="100%" class="center"> 
<img align="center" src="img/procg4.gif" alt="box" width="100%" class="center"> 

<h5 style="font-size :1.1rem; text-align:left"> Example 3: Interactive ellipse </h5>
<h6 style="font-size :1.1rem; text-align:left"> Processing Sketch: </h6>

``` Processing
import processing.serial.*;

Serial myPort;  // Create object from Serial class
static String val;    // Data received from the serial port
int sensorVal = 0;

void setup()
{
   size(720, 480);
   noStroke();
  noFill();
  String portName = "COM11";// Change the number (in this case ) to match the corresponding port number connected to your Arduino. 

  myPort = new Serial(this, portName, 9600);
}

void draw()
{
  if ( myPort.available() > 0) {  // If data is available,
  val = myPort.readStringUntil('\n'); 
  try {
   sensorVal = Integer.valueOf(val.trim());
  }
  catch(Exception e) {
  ;
  }
  println(sensorVal); // read it and store it in vals!
  }  
 background(0);
  // Scale the mouseX value from 0 to 640 to a range between 0 and 175
  float c = map(sensorVal, 0, width, 0, 400);
  // Scale the mouseX value from 0 to 640 to a range between 40 and 300
  float d = map(sensorVal, 0, width, 40,500);
  fill(255, c, 0);
  ellipse(width/2, height/2, d, d);   

}

```
<img align="center" src="img/proc5.jpg" alt="box" width="100%" class="center"> 
<img align="center" src="img/procg2.gif" alt="box" width="100%" class="center"> 

<h5 style="font-size :1.1rem; text-align:left"> Example 4: Particle system </h5>
<h6 style="font-size :1.1rem; text-align:left"> Processing Sketch: </h6>

``` Processing
int n = 1000; // number of dots 

float[] m = new float[n]; // make a new list of floating points 
float[] x = new float[n];
float[] y = new float[n];
float[] vx = new float[n];
float[] vy = new float[n];
float[] redchannel = new float[n]; 
float[] bluechannel = new float[n];
float[] greenchannel = new float[n];
float[] shape = new float[n];

import processing.serial.*;

Serial myPort;  // Create object from Serial class
static String val;    // Data received from the serial port
int sensorVal = 0;

//::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::

void setup() {
  fullScreen();
  fill(0,10);
  reset();// running the reset when you click. 10000 random values being plugged in 
  String portName = "COM11";// Change the number (in this case ) to match the corresponding port number connected to your Arduino. 
  myPort = new Serial(this, portName, 9600);
}

//::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::

void draw() {
   if ( myPort.available() > 0) {  // If data is available,
  val = myPort.readStringUntil('\n'); 
  try {
   sensorVal = Integer.valueOf(val.trim());
  }
  catch(Exception e) {
  ;
  }
  println(sensorVal); // read it and store it in vals!
  }  
  noStroke();
  fill(0,30);
  rect(0, 0, width, height); //  black background 

  for (int i = 0; i < n; i++) { // runs the loop 10,000 times
    float dx = mouseX - x[i]; // distance from the mouse 
    float dy = sensorVal - y[i];

    float d = sqrt(dx*dx + dy*dy); // calculating the distance between the points and the mouse 
    if (d < 1) d = 1; 

    float f = cos(d * 0.06) * m[i] / d*2; //decides if it gets closer or further from the mouse 

    vx[i] = vx[i] * 0.4 - f * dx; //changing the velocity so it moves towards the ring 
    vy[i] = vy[i] * 0.2 - f * dy;
  }

  for (int i = 0; i < n; i++) {
    x[i] += vx[i];
    y[i] += vy[i];

    if (x[i] < 0) x[i] = width;
    else if (x[i] > width) x[i] = 0;

    if (y[i] < 0) y[i] = height;
    else if (y[i] > height) y[i] = 0;

    if (m[i] < 0) fill(bluechannel[i], greenchannel[i] , 255);
    else fill(255, bluechannel[i],redchannel[i]);

      if (shape[i] > 2) fill(bluechannel[i], greenchannel[i] , 255);
    else fill(255, bluechannel[i],redchannel[i]);



    if (shape[i] > 2)  rect(x[i], y[i],10,10);
else if (shape[i] > 1 && shape[i] <=2) rect(x[i],y[i],2,2);
else ellipse(x[i], y[i],10,10);



  }
}

//::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::

void reset() { // counter that counts up to n 
  for (int i = 0; i < n; i++) { // i = 0, i < 10,0000, i++ what to do after each loop. 
    m[i] = randomGaussian() * 8; // gaussian distribution is a bell curve. Distribution of the mass 
    x[i] = random(width);
    y[i] = random(height);
    bluechannel[i] = random(255);
    redchannel[i] = random(255);
    greenchannel[i] = random(255); 
    shape [i] = random(0,3); 
  }
}

//::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::

void mousePressed() {
  reset();
}
```
<img align="center" src="img/proc7.jpg" alt="box" width="100%" class="center"> 
<img align="center" src="img/procg3.gif" alt="box" width="100%" class="center"> 

<h5 style="font-size :1.1rem; text-align:left"> Test your project </h5>

<p class="p2" style="font-size :1.1rem; text-align:Justify" > After uploading the initial Arduino sketch to your board, run the examples provided in this tutorial in Processing. When the Processing sketch is up and running, point a lightsource towards the phototransistor to observe the result. You can also play around with the absence of light as well! </p>