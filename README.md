Smart Automation Projects
A collection of practical automation prototypes using microcontrollers, sensors, actuators, and connected interfaces. The first project is a smart home prototype designed for a student residence.
Projects
Project	Description	Status
Smart Home Prototype	An ESP32 system that responds to motion, indoor conditions, rain, and gas detection.	Prototype demonstrated


Smart Home Prototype
The smart home prototype explores how automation can improve comfort and reduce unnecessary energy use in student accommodation. It was built with a Keystudio Smart Home Kit and an ESP32. Sensors feed the controller, which operates lights, a fan, and a servo-driven window. An LCD displays system information, a buzzer provides gas alerts, and a connected mobile/web interface offers controls and sensor feedback.
What it does
- Motion-based lighting: A PIR sensor turns on the yellow LED when motion is detected. The LED switches off after 5 seconds without motion.
- Climate-responsive window: A servo closes the window at temperatures of at least 28 °C or humidity of at least 75%. It reopens when temperature is at most 26 °C and humidity is at most 70%. Different opening and closing thresholds help prevent repeated movement near the limit.
- Rain response: A rain/water sensor triggers the window to close when moisture is detected.
- Ventilation: A DC fan is used in the prototype's climate and motion response demonstrations.
- Gas alert: The gas sensor triggers a buzzer and an LCD warning when a hazardous level is detected.
- Feedback and control: The LCD shows readings and system status; the presentation also demonstrates a connected app interface.
Hardware and tools
Component	Role
ESP32	Reads sensors and controls outputs; provides wireless connectivity
PIR motion sensor	Detects movement
DHT11	Measures temperature and humidity
Rain/water sensor	Detects moisture
MQ-type gas sensor	Detects gas and triggers an alert
Yellow LED	Represents motion-activated lighting
Servo motor	Opens and closes the model window
DC fan	Provides ventilation
Buzzer and LCD	Provide audible and visible feedback
Arduino IDE	Used to program and upload the ESP32 sketch


GPIO map from the presentation
Connection	ESP32 pin
Yellow LED	GPIO 12
PIR sensor	GPIO 14
Fan PWM	GPIO 19
Fan enable/direction	GPIO 18
DHT11	GPIO 17
Window servo	GPIO 5
Gas sensor digital output	GPIO 23
LCD	I²C SDA/SCL; confirm exact pins against the build


The presentation does not specify every connection, library, or app communication setting. Check the actual circuit and source code before using this map to recreate the prototype.
Development process
1. Defined the student-residence comfort and energy-use problem.
2. Selected sensors, actuators, thresholds, and the ESP32 controller.
3. Assembled a model home and configured the Arduino IDE for the ESP32.
4. Tested motion lighting, temperature and humidity response, rain detection, gas alerts, the fan, and the connected interface.
5. Adjusted servo travel and refined the response of the controls.
Results and next steps
The presentation demonstrates the sensor responses, connected interface, and safety alert in a working prototype. Energy savings were a design goal; the presentation does not report measured power consumption or quantified savings.
Possible extensions include energy-use logging, voice assistant control, and battery or solar backup.

Project credit
The source presentation, “Smart Home Prototype for Student Residence: Comfort and Energy Efficiency,” credits Merilynn Imhanwa (19 September 2025). Keep this credit with the project if sharing the presentation or build publicly.
