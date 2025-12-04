# Code Examples

This directory contains code examples and templates for each level of the Carenuity IoT Smart Home Challenge.

## Directory Structure

```
examples/
├── level-1/          # Soldering and WOKWI examples
├── level-2/          # PCB design and GPIO examples
├── level-3/          # API integration examples
├── level-4/          # 3D modeling and automation
├── level-5/          # Database integration examples
├── level-6/          # Edge AI and ML examples
└── libraries/        # Shared libraries and utilities
```

## Example Projects

### Level 1: Triple Adapter & WOKWI Simulation
- Basic LED blink simulation
- Temperature sensor reading
- Multi-sensor dashboard

### Level 2: PCB Design & GPIO Viewer
- KiCAD project templates
- GPIO Viewer firmware
- Custom silkscreen examples

### Level 3: API Usage & App Development
- Weather station with OpenWeatherMap
- MQTT home automation
- Telegram notification bot
- News ticker display

### Level 4: 3D Modeling & Custom Enclosures
- TinkerCAD enclosure templates
- Home Assistant configurations
- Snap-fit joint designs

### Level 5: Database Integration & Machine Learning
- ThingSpeak data logger
- Firebase real-time sync
- InfluxDB time-series storage
- Data visualization dashboards

### Level 6: AI-Assisted Edge Computing
- ESP32-CAM object detection
- Edge Impulse model training
- Real-time inference examples
- Multi-model deployment

## Code Standards

### Arduino Sketches

```cpp
/**
 * Project: [Project Name]
 * Level: [1-6]
 * Description: [Brief description]
 * Author: [Your name]
 * Hardware: [ESP32, D1-Mini, etc.]
 * Dependencies: [List required libraries]
 */

// Include required libraries
#include <WiFi.h>

// Configuration constants
const char* WIFI_SSID = "your-ssid";
const char* WIFI_PASSWORD = "your-password";

// Global variables
int sensorValue = 0;

void setup() {
  Serial.begin(115200);
  // Initialization code
}

void loop() {
  // Main code
}
```

### Python Scripts

```python
"""
Project: [Project Name]
Level: [1-6]
Description: [Brief description]
Author: [Your name]
Dependencies: [List required packages]
"""

import sys

def main():
    """Main function"""
    pass

if __name__ == "__main__":
    main()
```

## Using Examples

### Downloading

**Clone entire repository:**
```bash
git clone https://github.com/[username]/home-challenge.git
cd home-challenge/examples
```

**Download specific example:**
Navigate to the example folder and download individual files.

### Running Examples

1. **Read the README** in each example folder
2. **Install dependencies** listed in the code
3. **Configure settings** (WiFi, API keys, etc.)
4. **Upload to your board** using Arduino IDE
5. **Monitor serial output** for debugging

## Contributing Examples

We welcome example contributions! Please:

1. **Follow code standards** shown above
2. **Test thoroughly** on actual hardware
3. **Document well** with comments and README
4. **Include wiring diagrams** if needed
5. **List all dependencies** with versions
6. **Provide license information**

See [CONTRIBUTING.md](../CONTRIBUTING.md) for detailed guidelines.

## License

Unless otherwise noted, examples are licensed under the MIT License.

Individual examples may have different licenses - check the file header.
