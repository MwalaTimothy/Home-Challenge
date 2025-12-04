# Quick Start Guide

Get started with the Carenuity IoT Smart Home Challenge in just a few steps!

## Prerequisites

Before you begin, make sure you have:

1. **Basic Electronics Knowledge**
   - Understanding of voltage, current, and resistance
   - Ability to read simple circuit diagrams
   - Basic component identification

2. **Programming Fundamentals**
   - Basic understanding of variables and functions
   - Familiarity with conditional statements and loops
   - Willingness to learn C/C++ (Arduino)

3. **Computer Setup**
   - Windows, macOS, or Linux computer
   - Stable internet connection
   - At least 5GB of free disk space
   - USB port for microcontroller programming

## Getting Your Free Triple Adapter

The challenge starts with a free Triple Adapter for participants in eligible cities:

**Eligible Cities:**
- **Germany:** Munich, Hamburg, Wuerzburg
- **Italy:** Trieste
- **Greece:** Thessaloniki, Patras
- **Serbia:** Belgrade
- **Kenya:** Mombasa, Nairobi, Kisii

**How to Claim:**

1. Visit [carenuity.com/home-challenge](https://carenuity.com/home-challenge/)
2. Fill out the registration form
3. Verify your location
4. Receive your free Triple Adapter by mail

**Not in an eligible city?**

You can still participate! Purchase a Triple Adapter or compatible hardware from [ChipGlobe.shop](https://chipglobe.shop/) or other electronics suppliers.

## Essential Tools and Software

### Hardware Tools

**Required:**
- Soldering iron (25-60W recommended)
- Solder (lead-free, 0.8mm diameter)
- Wire cutters
- USB cable (Micro-USB or USB-C depending on your board)

**Recommended:**
- Helping hands or PCB holder
- Multimeter
- Wire stripper
- Anti-static mat or wrist strap
- Safety glasses

**Where to Buy:**
- [SparkFun](https://www.sparkfun.com/)
- [Adafruit](https://www.adafruit.com/)
- [DigiKey](https://www.digikey.com/)
- [ChipGlobe.shop](https://chipglobe.shop/)
- Local electronics stores

### Software Installation

#### 1. Arduino IDE (Required for Levels 1-6)

**Download:**
- Visit [arduino.cc/en/software](https://www.arduino.cc/en/software)
- Download Arduino IDE 2.x for your operating system
- Install following the on-screen instructions

**Initial Setup:**
```
1. Open Arduino IDE
2. Go to File > Preferences
3. Add ESP32 Board Manager URL:
   https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
4. Go to Tools > Board > Boards Manager
5. Search for "esp32" and install "esp32 by Espressif Systems"
6. Restart Arduino IDE
```

#### 2. Git and GitHub (Required for Level 1)

**Windows:**
```powershell
# Download from https://git-scm.com/download/win
# Or use winget:
winget install --id Git.Git -e --source winget
```

**macOS:**
```bash
# Using Homebrew:
brew install git
```

**Linux (Ubuntu/Debian):**
```bash
sudo apt update
sudo apt install git
```

**GitHub Account:**
1. Visit [github.com](https://github.com/)
2. Sign up for a free account
3. Verify your email address

#### 3. KiCAD (Required for Level 2)

**Download:**
- Visit [kicad.org/download](https://www.kicad.org/download/)
- Download latest stable version for your OS
- Install with default settings

**First Launch:**
```
1. Open KiCAD
2. Go to Preferences > Manage Symbol Libraries
3. Ensure default libraries are loaded
4. Go to Preferences > Manage Footprint Libraries
5. Ensure default libraries are loaded
```

#### 4. TinkerCAD (Required for Level 4)

**Setup:**
1. Visit [tinkercad.com](https://www.tinkercad.com/)
2. Sign up with email or Autodesk account
3. No download required - web-based tool
4. Complete introductory tutorials

#### 5. Edge Impulse (Required for Level 6)

**Account Creation:**
1. Visit [edgeimpulse.com](https://www.edgeimpulse.com/)
2. Sign up for free account
3. Install Edge Impulse CLI (optional):
   ```bash
   npm install -g edge-impulse-cli
   ```

## Level-by-Level Quick Start

### Level 1: Triple Adapter & WOKWI Simulation

**Time Required:** 4-6 hours

**Quick Steps:**
1. Solder 6 pin headers to Triple Adapter
2. Create account on [wokwi.com](https://wokwi.com/)
3. Build a sensor simulation project
4. Fork [Carenuity/WOKWI](https://github.com/Carenuity/WOKWI) repository
5. Add your project URL to the repository
6. Email photo and URL to team@carenuity.com

**Resources:**
- [Soldering Tutorial](https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering)
- [WOKWI Documentation](https://docs.wokwi.com/)
- [Level 1 Full Guide](../README.md#level-1-triple-adapter--wokwi-simulation)

---

### Level 2: PCB Design & GPIO Viewer

**Time Required:** 6-8 hours

**Quick Steps:**
1. Install KiCAD
2. Clone [Carenuity/KiCAD-PCB](https://github.com/Carenuity/KiCAD-PCB)
3. Modify silkscreen with your logo
4. Generate Gerber files
5. Flash GPIO Viewer app to C3-Mini
6. Take screenshot of GPIO interface
7. Email Gerber ZIP and screenshot to team@carenuity.com

**Resources:**
- [KiCAD Tutorial](https://docs.kicad.org/master/en/getting_started_in_kicad/)
- [GPIO Viewer App](https://carenuity.com/c3-mini)
- [Level 2 Full Guide](../README.md#level-2-pcb-design--gpio-viewer)

---

### Level 3: API Usage & App Development

**Time Required:** 8-10 hours

**Quick Steps:**
1. Choose an API to integrate (weather, news, etc.)
2. Write Arduino code (use ChatGPT for help)
3. Test on your microcontroller
4. Generate merged binary in Arduino IDE
5. Upload to [solutions.carenuity.com](https://solutions.carenuity.com/)
6. Share URL with team@carenuity.com
7. Optional: Post on LinkedIn

**Resources:**
- [Arduino Reference](https://www.arduino.cc/reference/en/)
- [Popular APIs](https://github.com/public-apis/public-apis)
- [Level 3 Full Guide](../README.md#level-3-api-usage--app-development)

---

### Level 4: 3D Modeling & Custom Enclosures

**Time Required:** 10-12 hours

**Quick Steps:**
1. Sign up for TinkerCAD
2. Measure your electronic components
3. Design custom enclosure
4. Export STL file
5. Create rendered images
6. Optional: Set up Home Assistant
7. Submit design files and images

**Resources:**
- [TinkerCAD Tutorials](https://www.tinkercad.com/learn)
- [Enclosure Design Guide](https://www.protocase.com/resources/electronic-enclosure-design-guide.php)
- [Level 4 Full Guide](../README.md#level-4-3d-modeling--custom-enclosures)

---

### Level 5: Database Integration & Machine Learning

**Time Required:** 12-15 hours

**Quick Steps:**
1. Choose a database platform (ThingSpeak, Firebase, etc.)
2. Create account and API keys
3. Program microcontroller to log sensor data
4. Set up data visualization dashboard
5. Create Edge Impulse account
6. Prepare dataset for ML training
7. Document your USP and potential applications

**Resources:**
- [ThingSpeak Guide](https://www.mathworks.com/help/thingspeak/)
- [Firebase Setup](https://firebase.google.com/docs/database)
- [Level 5 Full Guide](../README.md#level-5-database-integration--machine-learning)

---

### Level 6: AI-Assisted Edge Computing

**Time Required:** 15-20 hours

**Quick Steps:**
1. Set up ESP32-CAM module
2. Collect image dataset (500+ images)
3. Upload to Edge Impulse
4. Train object detection model
5. Deploy to ESP32-CAM
6. Test and validate accuracy
7. Create product description on Solution Builder
8. Submit for hero website and device stocking

**Resources:**
- [ESP32-CAM Guide](https://randomnerdtutorials.com/esp32-cam-video-streaming-face-recognition-arduino-ide/)
- [Edge Impulse Documentation](https://docs.edgeimpulse.com/)
- [Level 6 Full Guide](../README.md#level-6-ai-assisted-edge-computing)

---

## Common Issues and Solutions

### Hardware Issues

**Problem:** Soldering creates cold joints
**Solution:** Ensure iron is hot enough (350-400°C), use proper technique, and clean the tip regularly

**Problem:** Microcontroller not recognized by computer
**Solution:** Install CH340 or CP2102 drivers, try different USB cable, check USB port

**Problem:** Code uploads but doesn't run
**Solution:** Check power supply, verify GPIO pin assignments, reset the board

### Software Issues

**Problem:** Arduino IDE can't find ESP32 board
**Solution:** Re-install ESP32 board package, check Board Manager URL, restart IDE

**Problem:** Git push rejected
**Solution:** Pull latest changes first (`git pull`), resolve conflicts, then push

**Problem:** KiCAD libraries missing
**Solution:** Update symbol and footprint libraries in Preferences

## Getting Help

### Official Support
- **Email:** team@carenuity.com
- **Phone:** +49 89-1222469-40
- **Website:** [carenuity.com/home-challenge](https://carenuity.com/home-challenge/)

### Community Resources
- **GitHub Issues:** Report bugs and ask questions
- **Arduino Forums:** [forum.arduino.cc](https://forum.arduino.cc/)
- **ESP32 Community:** [esp32.com](https://esp32.com/)
- **r/arduino:** Reddit community
- **r/esp32:** ESP32-specific subreddit

### Documentation
- [Main Roadmap](../README.md)
- [Contributing Guide](../CONTRIBUTING.md)
- [Carenuity Blog](https://carenuityblog.wixsite.com/embedded-ai-journal)

## Tips for Success

### Time Management
1. **Set aside dedicated time** - Block 2-3 hour sessions for focused work
2. **Don't rush** - Quality over speed; take time to understand concepts
3. **Break down tasks** - Complete one deliverable at a time
4. **Track progress** - Keep notes on what works and what doesn't

### Learning Strategy
1. **Follow tutorials first** - Don't skip the basics
2. **Experiment** - Try variations once you understand the fundamentals
3. **Document everything** - Take photos, save code versions, write notes
4. **Ask for help** - Don't struggle alone; reach out when stuck

### Best Practices
1. **Version control** - Commit code frequently with clear messages
2. **Test incrementally** - Don't write all code before testing
3. **Back up work** - Save copies of important files
4. **Safety first** - Use proper safety equipment when soldering

## Next Steps

**Ready to start?**

1. **Complete prerequisites** - Install required software
2. **Claim your Triple Adapter** - Register on the website
3. **Join the community** - Connect with other participants
4. **Start Level 1** - Begin your IoT journey!

**Questions before starting?**

- Read the [full roadmap](../README.md)
- Check the [FAQ section](#common-issues-and-solutions)
- Email team@carenuity.com

---

**Good luck on your IoT journey!**

Remember: This is a learning experience. Take your time, experiment, make mistakes, and most importantly - have fun building!

---

*Last Updated: December 2025*
