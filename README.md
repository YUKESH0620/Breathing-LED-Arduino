# Breathing LED using Arduino UNO

This is a beginner-level embedded systems project that creates a smooth breathing (fade-in, fade-out) LED effect using *PWM (Pulse Width Modulation)*.

## What it Does
- Gradually increases and decreases LED brightness
- Simulates a breathing LED using analogWrite() and delay loops

## Components Used
- Arduino UNO
- Breadboard
- LED
- 220Ω resistor
- Jumper wires

## Concepts Applied
- PWM (Pulse Width Modulation)
- Analog signal control via code
- Timing with delay()

##  Preview
![Breathe LED Tinkercad Template](https://github.com/user-attachments/assets/c5739a30-0fcb-4a9f-b429-b54da96c34fb)

##  Code
```cpp
int ledPin = 9; // PWM pin

void setup() {
  pinMode(ledPin, OUTPUT);
}

void loop() {
  for (int brightness = 0; brightness <= 255; brightness++) {
    analogWrite(ledPin, brightness);
    delay(10);
  }
  for (int brightness = 255; brightness >= 0; brightness--) {
    analogWrite(ledPin, brightness);
    delay(10);
  }
}
