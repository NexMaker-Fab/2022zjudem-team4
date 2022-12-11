# Processing

> Processing assignment by Winkee <br><br>


## CODE

```Processing
/*
PVector []cells;
int cellW = 15;
int cellH = 15;
int nbCellW;
int nbCellH;

void setup() {
  //createCanvas (500,500);
  fullScreen();
  rectMode(CENTER);
  colorMode(HSB, 1);
  
  nbCellW = floor(width/cellW);
  nbCellH = floor(height/cellH);
  
  cells = new PVector[nbCellW*nbCellH];
  for (int i=0; i < nbCellW*nbCellH; i ++) {
    //cells.push(createVector(0,0));
    cells[i]= new PVector (0,0); 
  }
}

void draw() {
  PVector deltaMouse = new PVector (mouseX - pmouseX, mouseY - pmouseY);
  for (int i=0; i < nbCellW; i ++) {
    for (int j=0; j < nbCellH; j ++) {
      int k = i+j*nbCellW;
      int x = cellW * i + cellW/2;
      int y = cellH * j + cellH/2;
      float d = max(1, dist(mouseX, mouseY, x, y));
      
      deltaMouse. normalize();
      deltaMouse. mult(1/(d*30));
      cells[k]. add(deltaMouse);
      cells[k]. limit(10);
      
      float h = map(cells[k]. heading(), -PI, PI, 0, 1);
      float b = min(cells[k]. mag()*100, 10);
      fill(h, 1, b);
      
      rect(x, y, cellW, cellH);
      
      cells[k]. mult(.97);
    }
  }
}  
```
<video width="640" height="480" poster="img/processing%20logo.jpg" controls>
   <source src="img/Brush%20by%20wink.gif" type="video/gif">
   <source src="movie.ogg" type="video/ogg">
</video>
<br>
<br>

> Processing mini game by Winkee <br><br>

# CODE

```Processing
/*
float x, y, speedX, speedY;
float diam = 20;
float rectSize = 200;

void setup() {
  size(640,420);
  stroke(242,22,22);
  strokeWeight(3);
  fill(255);
  reset();
}

void reset() {
  x = width/2;
  y = height/2;
  speedX = random(3, 5);
  speedY = random(3, 5);
}

void draw() { 
  background(0);
  
  ellipse(x, y, diam, diam);

  rect(0, 0, 20, height);
  rect(width-30, mouseY-rectSize/2, 10, rectSize);

  x += speedX;
  y += speedY;

  // if ball hits movable bar, invert X direction
  if ( x > width-30 && x < width -20 && y > mouseY-rectSize/2 && y < mouseY+rectSize/2 ) {
    speedX = speedX * -1;
  } 

  // if ball hits wall, change direction of X
  if (x < 25) {
    speedX *= -1.1;
    speedY *= 1.1;
    x += speedX;
  }


  // if ball hits up or down, change direction of Y   
  if ( y > height || y < 0 ) {
    speedY *= -1;
  }
}

void mousePressed() {
  reset();
}
```
<video width="640" height="480" poster="img/processing%20logo.jpg" controls>
   <source src="img/PINGPONG%20by%20wink.gif" type="video/gif">
   <source src="movie.ogg" type="video/ogg">
</video>
<br>
<br>