# STRATAGUARD FINAL READY

## Run
Open PowerShell in this folder:
```powershell
npm install
npm run dev
```
Open the localhost URL shown by Vite, normally `http://localhost:5173/`.

## ESP8266
Use `ARDUINO/STRATAGUARD_SENSOR_TEST.ino`. Close Arduino Serial Monitor/Plotter before using the browser `CONNECT ESP8266` button.

Expected serial format:
`Vibration = 0 | Tilt = 1 | Flex = 15`

Firmware logic:
- Vibration HIGH = detected
- Tilt LOW = detected
- Flex displayed, no alarm
- Alert = vibration OR tilt
- Green LED normal, red LED + buzzer during alert

## Digital Twin
The dashboard contains a procedural engineering-style 3D cross-section Digital Twin with surface, road, vegetation, house, soil/rock, coal seam, mine gallery, pillars, mining vehicle, and T1/V1/F1 sensor markers.

Live behaviour:
- T1 Tilt -> blue rings + visible surface/soil tilt animation
- V1 Vibration -> orange pulsing wave rings
- F1 Flex -> purple deformation animation
- Model Layers buttons toggle the corresponding visual layers
- Drag the 3D view to rotate the model
