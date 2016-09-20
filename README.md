int x = 50;
int y = 50;
float b1Color = 0;
float b2Color = 255;
float b1Change = 1;
float b2Change = -1;


void setup (){
  size (200, 200);
  background (0);
}
void draw () {
  rectMode (CENTER);

  fill(b2Color);
  rect ( x, y, x, y);
  fill(b1Color);
  rect ( x*3, y, x, y);
  fill(b1Color);
  rect ( x, y*3, x, y);
  fill(b2Color);
  rect ( x*3, y*3, x, y);
  b1Color = b1Color + b1Change; 
  b2Color = b2Color + b2Change;
  if (b1Color>254 || b1Color<1){
   b1Change *= -1;
   } 
   if (b2Color<1 || b2Color>254){
    b2Change *= -1;
  } 
}
