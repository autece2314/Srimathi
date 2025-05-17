source code
#include <Wire.h>
#include <Adafruit_ADXL345_U.h>

Adafruit_ADXL345_Unified accel = Adafruit_ADXL345_Unified(123);

void setup() {
  Serial.begin(115200);

  // Initialize sensor
  if (!accel.begin()) {
    Serial.println("No ADXL345 detected. Check wiring.");
    while (1);
  }

  // Set range (optional: RANGE_2_G
