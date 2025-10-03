# HHHH-LED
int ledPin = 9; // لازم يكون Pin يدعم PWM

void setup() {
  pinMode(ledPin, OUTPUT);
}

void loop() {
  // زيادة الإضاءة تدريجياً
  for (int i = 0; i <= 255; i++) {
    analogWrite(ledPin, i); // القيمة 0 = مطفي، 255 = أقوى إضاءة
    delay(10);              // سرعة التدرج
  }

  // تقليل الإضاءة تدريجياً
  for (int i = 255; i >= 0; i--) {
    analogWrite(ledPin, i);
    delay(10);
  }
}
