let x;
let y;

function setup() {
  createCanvas(400, 400);
  x = random(400);
  x = int(x);
  y = random(400);
  y = int(y);
}

function draw() {
  background(220);
  x  = x + random(-5,5);
  y = y + random(-5,5);
  x = constrain(x,0,400);
  y = constrain(y,0,400);
  let distance;
  distance = dist(mouseX, mouseY, x, y);
  circle(mouseX, mouseY, distance);
  //circle(x, y, 10);
  
  if (distance < 3) {
    text("Encontrei!", 200, 200);
    noLoop();
  }
}
