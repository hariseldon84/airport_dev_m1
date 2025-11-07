# Display & Screen Technology Specification (br_screen)

## 1. Overview
This document specifies the primary and secondary display technologies for the Airport Business Smartphone. The display system is engineered to provide professional-grade visual clarity, industry-leading durability, and innovative features that enhance user well-being and productivity. The architecture includes a main ProView Display and a unique, rear-mounted Info-Ink Display.

## 2. Primary Display: ProView Display
The main display is designed for immersive productivity, vibrant media consumption, and comfortable, all-day use.

### 2.1 Panel Technology & Specifications
- **Type**: 6.7-inch LTPO 3.0 AMOLED.
- **Resolution**: QHD+ (3216 x 1440 pixels), resulting in a sharp 525 ppi.
- **Refresh Rate**: Adaptive 1Hz - 144Hz. The LTPO technology allows the screen to dynamically adjust its refresh rate, providing buttery-smooth motion when needed and dropping to 1Hz for static content to conserve battery.
- **Brightness**: 1,200 nits typical, with a peak brightness of 2,500 nits for excellent HDR performance and outdoor legibility.
- **Color**: 10-bit color depth, covering 100% of the DCI-P3 color gamut. Each display is factory-calibrated to a Delta E < 1 for professional color accuracy.

### 2.2 Durability & Integration
- **Cover Glass**: Corning Gorilla Glass Victus 3 for best-in-class scratch resistance and drop protection.
- **Integration**: The display integrates the under-display front camera and an ultrasonic under-display fingerprint sensor, providing a seamless, uninterrupted, all-screen experience.

### 2.3 Intelligent Eye Care System (Powered by BeeHive AI)
This is a multi-layered system designed to minimize eye strain and support user well-being.
- **Hardware-Level Blue Light Filtering**: The display's OLED material has a custom light spectrum that shifts the peak of blue light emission away from the most harmful wavelengths (415-455nm) without creating the yellow tint common in software-based solutions.
- **High-Frequency PWM Dimming**: The display uses 2160Hz Pulse-Width Modulation (PWM) for dimming. This ultra-high frequency is imperceptible to the human eye, eliminating the invisible flicker found in many OLED screens that can cause eye strain and headaches.
- **Circadian Sync**: The BeeHive AI learns the user's sleep schedule and location. It automatically and gradually adjusts the screen's color temperature throughout the evening to reduce blue light exposure and support the body's natural production of melatonin, promoting better sleep.

## 3. Secondary Display: The Info-Ink Display
This is a small, ultra-low-power E-Ink screen on the back of the device for discreet, at-a-glance information.

### 3.1 Technology & Specifications
- **Type**: 1.5-inch Color E-Ink Display (e.g., E-Ink Kaleido 3).
- **Resolution**: 200 x 200 pixels.
- **Power Consumption**: Near-zero power consumption for static images. Power is only consumed when the display content changes.
- **Placement**: Located on the upper back of the phone, adjacent to the camera module, for easy viewing when the phone is face down.

### 3.2 Functionality & Use Cases
- **Privacy-Focused Notifications ("Glyphs")**: Instead of displaying sensitive text from notifications, the Info-Ink display shows simple, customizable icons (Glyphs). This allows the user to understand the context of a notification without exposing its content.
  - **Example**: A user could set a specific building icon for work emails, a person icon for messages from family, and a calendar icon for meeting alerts.
- **Always-On Utility**: When not showing notifications, the display can be configured to show:
  - A minimalist clock face.
  - Current weather conditions.
  - The user's daily meeting schedule.
  - A custom QR code for their digital business card.
- **BeeHive Integration**: The AI can intelligently change the Info-Ink display based on context. For example, when a boarding pass is saved to the phone, the E-Ink display could automatically show the flight's QR code when the user is at the airport.

## 4. Next Steps
1. Source and test LTPO 3.0 AMOLED panels that meet the specified resolution, brightness, and color accuracy targets.
2. Develop the custom hardware and software for the Intelligent Eye Care System, including the circadian rhythm algorithms for the BeeHive AI.
3. Design the physical integration of the 1.5-inch E-Ink display into the rear ceramic panel.
4. Create the UI/UX for customizing the Glyphs and other functions of the Info-Ink Display.
