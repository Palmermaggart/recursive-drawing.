void setup() {
  size(600, 600);
  background(255);
  noFill();
  stroke(0, 120);
  
  drawSquare(width/2, height/2, 250, 0);
}

void draw() {
}

void drawSquare(float x, float y, float size, float angle) {
  
  // base case
  if (size < 10) {
    return;
  }
  
  pushMatrix();
  translate(x, y);
  rotate(radians(angle));
  
  rectMode(CENTER);
  rect(0, 0, size, size);
  
  popMatrix();
  
  // smaller
  drawSquare(x, y, size * 0.85, angle + 12);
}
# recursive-drawing.
