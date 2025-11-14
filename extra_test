int currentScreen = 0;          // 0 = start screen, 1 = screen A, 2 = screen B, …
final int START   = 0;
final int SCREEN_A = 1;
final int SCREEN_B = 2;

final int BTN_W = 180;
final int BTN_H = 50;

void setup() {
  size(600, 400);
  textAlign(CENTER, CENTER);
  textSize(18);
}

void draw() {
  background(220);

  if (currentScreen == START)   drawStartScreen();
  else if (currentScreen == SCREEN_A) drawScreenA();
  else if (currentScreen == SCREEN_B) drawScreenB();
}

void Button(float x, float y, String text, int nextScreen) {
  boolean hover = mouseX > x && mouseX < x + BTN_W &&
                  mouseY > y && mouseY < y + BTN_H;
  boolean pressed = hover && mousePressed;

  if (hover) fill(100, 149, 237);   // hover colour
  else       fill(70, 130, 180);    // normal colour

  stroke(255);
  strokeWeight(2);
  rect(x, y, BTN_W, BTN_H, 12);    // rounded corners

  fill(255);
  text(text, x + BTN_W/2, y + BTN_H/2);

  if (pressed) {
    switchScreen(nextScreen);      // <-- this is the "event switch"
  }
}

void switchScreen(int newScreen) {
  currentScreen = newScreen;
}

void drawStartScreen() {
  fill(0);
  textSize(32);
  text("START SCREEN", width/2, 80);

  Button(100, 180, "Go to Screen A", SCREEN_A);
  Button(320, 180, "Go to Screen B", SCREEN_B);
}

void drawScreenA() {
  fill(0);
  textSize(32);
  text("SCREEN A", width/2, 80);

  Button(210, 250, "Back to Start", START);
}

void drawScreenB() {
  fill(0);
  textSize(32);
  text("SCREEN B", width/2, 80);

  Button(210, 250, "Back to Start", START);
}
