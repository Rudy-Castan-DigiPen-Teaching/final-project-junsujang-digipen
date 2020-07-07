# Programming Concepts


## 1. Shapes
circle means player can direct something. And after you direct, that circle changed to something different what mean initiate or fail to give instructions.
code:
if (land[i][1] == 1) {
          push();
          stroke(c);
          circle(size / 2 + i * size - xmove, height - size * 2, size / 2, size / 2);
          pop();
        }





## 2. Colors
When the mouse is in a circle, it will change the circle color to indicate clickable.
code:
var c
        if (range(i)) {
          c = 255;
        } else {
          c = 0;
        }
stroke(c);





## 3. Variables
It will be used to indicate various states.
code:
var worker = 'non'
function mouseClicked() {
  for (var i = 0; i < land.length; i++) {
    if (range(i)) {
      worker = ‘working’
    }
  }
}


## 4. Conditional Statements
It would be used to command something like move, state ....
code:
function move() {
  if (keyIsDown(LEFT_ARROW)) {
    xmove += -2;
  }
  if (keyIsDown(RIGHT_ARROW)) {
    xmove += 2;
  }
}


## 5. Loops
It will be used to randomly put values into a map array variable.
code:
for (var i = 0; i < 100; i++) {
    land[i][0] = floor(random(5));
    land[i][1] = 0;
    if (land[i][0] == 2) {
      land[i][1] = 1;
    }
  }

## 6. Functions
It will be used to determine the range of circles used to receive instructions.
code:

function range(i) {
  let dx = mouseX - (size / 2 + i * size - xmove);
  let dy = mouseY - (height - size * 2);
  let mouse = dx * dx + dy * dy;
  return mouse <= 10 * 10;
}




## 7. Classes
It will be used to make and update units, enemies, player character.
code:

class unit{
  constructor(x,y){
    this.x = x;
    this.y = y;
  }
  draw(){
image();
  }
  update(){

  }
}





## 8. Arrays
It will be used to receive map values.

code:
var land;
function setup() {
land = make2Darray(100, 2)
}

function make2Darray(v, h) {
  var arr = new Array(v);
  for (var i = 0; i < arr.length; i++) {
    arr[i] = new Array(h);
  }
  return arr
}



