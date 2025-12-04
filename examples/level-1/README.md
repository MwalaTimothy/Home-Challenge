# Level 1 Examples

Code examples and projects for Level 1: Triple Adapter & WOKWI Simulation

## Basic Examples

### Example 1: LED Blink

Simple LED blink example for WOKWI simulation.

**WOKWI Project:** [Create your own at wokwi.com](https://wokwi.com/)

**Code:**
```cpp
/**
 * Project: Basic LED Blink
 * Level: 1
 * Description: Simple LED blink example to get started
 * Hardware: Any Arduino-compatible board
 */

const int LED_PIN = 2;  // Built-in LED on most ESP32 boards

void setup() {
  pinMode(LED_PIN, OUTPUT);
  Serial.begin(115200);
  Serial.println("LED Blink Example Started!");
}

void loop() {
  digitalWrite(LED_PIN, HIGH);
  Serial.println("LED ON");
  delay(1000);
  
  digitalWrite(LED_PIN, LOW);
  Serial.println("LED OFF");
  delay(1000);
}
```

### Example 2: Temperature Sensor

Read temperature from a DHT22 sensor.

**Required Library:** DHT sensor library by Adafruit

**Code:**
```cpp
/**
 * Project: Temperature Sensor Reading
 * Level: 1
 * Description: Read temperature and humidity from DHT22
 * Hardware: ESP32 + DHT22 sensor
 * Dependencies: DHT sensor library
 */

#include <DHT.h>

#define DHTPIN 4        // GPIO pin connected to DHT22
#define DHTTYPE DHT22   // DHT22 sensor type

DHT dht(DHTPIN, DHTTYPE);

void setup() {
  Serial.begin(115200);
  Serial.println("DHT22 Temperature Sensor");
  dht.begin();
}

void loop() {
  delay(2000);  // Wait between measurements
  
  float humidity = dht.readHumidity();
  float temperature = dht.readTemperature();
  
  if (isnan(humidity) || isnan(temperature)) {
    Serial.println("Failed to read from DHT sensor!");
    return;
  }
  
  Serial.print("Temperature: ");
  Serial.print(temperature);
  Serial.print("°C | Humidity: ");
  Serial.print(humidity);
  Serial.println("%");
}
```

### Example 3: Multi-Sensor Dashboard

Combine multiple sensors for a comprehensive dashboard.

**Required Libraries:**
- DHT sensor library
- Adafruit SSD1306 (for OLED display)

**Code:**
```cpp
/**
 * Project: Multi-Sensor Dashboard
 * Level: 1
 * Description: Read multiple sensors and display on OLED
 * Hardware: ESP32 + DHT22 + LDR + OLED
 * Dependencies: DHT sensor library, Adafruit SSD1306
 */

#include <DHT.h>
#include <Wire.h>
#include <Adafruit_GFX.h>
#include <Adafruit_SSD1306.h>

// Sensor pins
#define DHTPIN 4
#define LDRPIN 34  // Analog pin for light sensor

// Display configuration
#define SCREEN_WIDTH 128
#define SCREEN_HEIGHT 64
#define OLED_RESET -1

DHT dht(DHTPIN, DHT22);
Adafruit_SSD1306 display(SCREEN_WIDTH, SCREEN_HEIGHT, &Wire, OLED_RESET);

void setup() {
  Serial.begin(115200);
  dht.begin();
  
  if(!display.begin(SSD1306_SWITCHCAPVCC, 0x3C)) {
    Serial.println("SSD1306 allocation failed");
    while(1);
  }
  
  display.clearDisplay();
  display.setTextSize(1);
  display.setTextColor(SSD1306_WHITE);
}

void loop() {
  float temp = dht.readTemperature();
  float hum = dht.readHumidity();
  int light = analogRead(LDRPIN);
  
  // Display on OLED
  display.clearDisplay();
  display.setCursor(0, 0);
  display.println("Sensor Dashboard");
  display.println();
  display.print("Temp: ");
  display.print(temp);
  display.println(" C");
  display.print("Humidity: ");
  display.print(hum);
  display.println(" %");
  display.print("Light: ");
  display.println(light);
  display.display();
  
  // Print to serial
  Serial.printf("Temp: %.1f°C | Hum: %.1f%% | Light: %d\n", 
                temp, hum, light);
  
  delay(2000);
}
```

## WOKWI Project Templates

### Creating Your WOKWI Project

1. Go to [wokwi.com](https://wokwi.com/)
2. Sign up for a free account
3. Click "New Project"
4. Choose your board (ESP32, Arduino Uno, etc.)
5. Add components from the left panel
6. Wire components in the diagram
7. Write or paste your code
8. Click "Run Simulation"
9. Save and share your project URL

### Recommended Components to Experiment With

- LEDs and resistors
- Push buttons
- Potentiometers
- Temperature sensors (DHT22)
- Light sensors (LDR)
- Ultrasonic sensors
- Servos
- OLED displays
- LCD displays

## Tips for Level 1

### Soldering Tips

1. **Preparation:**
   - Clean the iron tip before use
   - Heat to 350-400°C
   - Use flux for better flow

2. **Technique:**
   - Heat both the pad and component lead
   - Apply solder to the joint, not the iron
   - Create a cone shape
   - Remove iron quickly

3. **Safety:**
   - Work in ventilated area
   - Use safety glasses
   - Keep iron in stand when not in use
   - Wash hands after soldering

### WOKWI Tips

1. **Start Simple:**
   - Begin with basic LED circuits
   - Gradually add complexity
   - Test each component individually

2. **Use Serial Monitor:**
   - Debug with Serial.print()
   - Monitor sensor values
   - Verify logic flow

3. **Save Frequently:**
   - Projects auto-save
   - Copy code to backup
   - Share URL with others

## Deliverables Checklist

- [ ] Triple Adapter with 6 soldered pin headers
- [ ] Clear photo of soldering work
- [ ] WOKWI project created and tested
- [ ] Project URL from WOKWI
- [ ] Fork of Carenuity/WOKWI repository
- [ ] Added project URL to repository
- [ ] Email sent to team@carenuity.com with:
  - Photo of soldered Triple Adapter
  - WOKWI project URL
  - GitHub username

## Common Issues

**Issue:** Solder won't stick to pin
**Solution:** Clean surfaces, use more flux, ensure iron is hot enough

**Issue:** WOKWI simulation doesn't start
**Solution:** Check for code errors, verify component connections

**Issue:** Can't see serial output in WOKWI
**Solution:** Click "Serial Monitor" button at bottom of screen

## Next Steps

After completing Level 1:
1. Wait for confirmation email
2. Receive D1-Mini or C3-Mini reward
3. Review Level 2 requirements
4. Install KiCAD software
5. Start Level 2: PCB Design & GPIO Viewer

## Additional Resources

- [Arduino Reference](https://www.arduino.cc/reference/en/)
- [WOKWI Documentation](https://docs.wokwi.com/)
- [Soldering Tutorial](https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering)
- [Level 1 Full Guide](../../README.md#level-1-triple-adapter--wokwi-simulation)

---

Good luck with Level 1!
