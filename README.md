First, Go support kotope as he is the original developer of the package. Big thanks to him!
 (https://github.com/kotope) :metal:

## **Car Heater Automation for Home Assistant**  

### **Description**  
This automation controls a car engine heater based on outdoor temperature and a scheduled departure time. It ensures the car is warm when needed while optimizing energy usage.  

- **Automatically starts** the heater at a calculated time before departure.  
- **Prevents overheating** by enforcing a **max runtime of 3 hours**.  
- **Sends a notification** if the heater turns on but no power is detected (cable unplugged).  
- **Works only on weekdays** if enabled via `input_boolean.car_heater_weekday`.  
- **Samples temperature 3 hours before departure** to calculate required heating time.  

---

### **Installation Guide**  
1. **Update Required Placeholders**  
   - All locations that need modification are marked with **"CHANGE-ME"** in the YAML file.  
   - Replace `sensor.balkong_temperature` with your **outdoor temperature sensor**.  
   - Replace `switch.motorvarmare` with your **car heater power switch**.  
   - Replace `sensor.motorvarmare_power` with your **power consumption sensor**.  
   - Modify notification settings (`notify.mobile_app_christian`) to match your **mobile device**.  

2. **Add to `configuration.yaml`**  
   - Ensure `input_boolean`, `input_number`, `input_datetime`, and `sensor` sections exist in your `configuration.yaml`.  
   - If they don’t exist, copy them from the provided automation.  

3. **Restart Home Assistant**  
   - Navigate to **Developer Tools → YAML**  
   - Click **Check Configuration**  
   - Restart Home Assistant  

4. **Set Your Preferences**  
   - In Home Assistant UI, go to **Settings → Devices & Services → Helpers**  
   - Set `car_heater_departure_time` to your usual departure time  
   - Toggle `car_heater_enable` to turn the automation on  
   - Toggle `car_heater_weekday` if you want it to run only on weekdays  

5. **Monitor and Adjust**  
   - Check **Developer Tools → States** to verify `sensor.car_heater_status` displays expected messages.  
   - Adjust threshold values or timings if needed.  

Once set up, the automation will manage your car heater efficiently and notify you if something goes wrong. 🚗🔥
