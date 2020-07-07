# Programming Concepts


## 1. Shapes
circle means player can direct something. 

And after you direct, that circle changed to something different what mean initiate or fail to give instructions.


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


          function rangecolor(x, y) {
          
            var col;
            
            if (range(x, y)) {
           
             col = 155;
             
            } else {
            
              col = 0;
              
            }
            
            return col
            
          }





## 3. Variables

It used to Remember the value.

It used to indicate various states.

and It makes a judgment to next behavior


code:

          var time = 'daytime'
          var daycount = 1;
          var camplevel = 1;
          var buildingstate = 'non'




## 4. Conditional Statements
It used to judge from Variables's condition.

And order action according to the condition.

code:

                    if (time == 'daytime') {
                       timer += 1 / 60;
                     }
                     if (timer > 30 + daycount) {
                      time = 'night';
                       timer = 0;
                       ohohohoh.setVolume(effectvolume);
                       ohohohoh.loop();
                     }


## 5. Loops

It used to make map.

It used to randomly put values into a map array variable.

Random values will locate resources.

code:

          for (var i = 0; i < 100; i++) {
          
              land[i][0] = floor(random(5));
              
              land[i][1] = 0;
              
              if (land[i][0] == 2) {
              
                land[i][1] = 1;
                
              }
              
            }
            

## 6. Functions
It used to determine the range of circles used to receive instructions.

it'll give you a range of orders.


code:

          function range(x, y) {
          
            let dx = mouseX - (x);
            
            let dy = mouseY - (y);
            
            let mouse = dx * dx + dy * dy;
            
            return mouse <= 10 * 10;
            
          }




## 7. Classes
It used to make unit base.

it used to another unit(enemy, soldier ...)'s base.

It used to make and update units, enemies, soldiers.

code:

          class unitbase {
            constructor(x, y,xspeed) {
              this.x = x;
              this.y = y;
              this.atpow = 1;
              this.atspeed = 1;
              this.hp = 1;
              this.speed = 1;
              this.state = 'going';
              this.xspeed = xspeed;
            }
            draw() {}
            update() {
            }
          }





## 8. Arrays
It used to receive map values.

It used to make effects.

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



