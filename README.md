Gesture-Controlled Vehicle Interface

Project Description:

This project is a contactless control system for vehicle accessories. It allows the driver to control devices like fans, lights, or infotainment systems without touching buttons. The system uses gestures, tilt, touch, and rotary controls, and the Arduino processes the inputs to control a relay safely.

Objective:

To provide safe and convenient contactless control of vehicle accessories.

To demonstrate the use of sensors and microcontrollers for real-world applications.

To create an edge-triggered system that prevents repeated switching.

Components Used:

Arduino Uno R3 – The brain of the system, reads sensors and controls the relay.

Magic Light Cup Module – Detects tilt; turns LED on/off; can trigger the relay.

IR Module (Emitter + TSOP38238 Receiver) – Detects hand gestures to control the relay.

Metal Touch Sensor – Capacitive touch input to toggle relay.

Rotary Encoder – Used to navigate menus and toggle the relay via its button.

Relay Module – Acts as an electronic switch to control accessories safely.

LED (Optional) – Provides visual feedback for the tilt sensor.

Wiring Connections:
Component	Pin → Arduino	Power	Ground
Magic Cup S	A0	+5V	GND
Magic Cup L (LED)	D9	+5V	GND
IR Emitter S	D3	+5V	GND
IR Receiver OUT	D2	+5V	GND
Metal Touch Sensor	D4	+5V	GND
Rotary Encoder CLK	D5	+5V	GND
Rotary Encoder DT	D6	+5V	GND
Rotary Encoder SW	D7	+5V	GND
Relay Module S	D10	+5V	GND
How It Works:

Magic Light Cup: Tilting the cup turns on its LED and toggles the relay.

IR Gesture: A hand in front of the IR sensor toggles the relay.

Metal Touch Sensor: Touching the sensor toggles the relay.

Rotary Encoder: Turning it changes menu values; pressing the button toggles the relay.

Relay: Acts as a safe electronic switch to turn an accessory ON or OFF.

Edge-triggered logic ensures each input only toggles the relay once per action, preventing accidental repeated switching.

Serial Monitor Output:

The Serial Monitor shows which input triggered the relay and the current relay state. Examples:

Relay ON by Magic Cup

Relay OFF by IR Gesture

Relay ON by Touch Sensor

Relay OFF by Encoder Button

This helps in testing and debugging the system.

Applications:

Controlling vehicle lights or fans without touching buttons

Modern infotainment control

Smart home appliance control (similar principle)

Any system needing safe, edge-triggered ON/OFF control

Notes:

Ensure all components are powered with 5V.

Do not connect high-voltage appliances directly to the Arduino; always use the relay module.

Adjust the tilt sensor thresholds if needed for more precise detection.
