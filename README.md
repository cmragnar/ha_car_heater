First, Go support kotope as he is the original developer of the package.
https://github.com/kotope
Big thanks to him!

### **🚗 Car Heater Automation Blueprint - How It Works**  

1. **User Configuration:**  
   - Selects the **car heater switch** (must support power monitoring).  
   - Selects an **outdoor temperature sensor** to calculate the heating duration.  
   - Sets the **departure time** when the car should be warm.  
   - Chooses which days the automation runs:  
     - **Weekdays (Mon–Fri)**  
     - **Saturday**  
     - **Sunday**  
   - Sets a **max runtime** (default: **3 hours**) for safety.  
   - Selects a **mobile device** for notifications.  

2. **Automation Logic:**  
   - **Checks if today is an allowed heating day** (based on weekday toggles).  
   - **Calculates when to start the heater** (based on temperature and departure time).  
   - **Turns on the car heater at the right time.**  
   - **Checks if power is detected** (prevents failures due to unplugged cables).  
   - **Turns off the heater at departure time.**  
   - **Failsafe auto-off** if the heater runs longer than the max runtime.  

3. **Smart Notifications:**  
   - 📢 **Heater started**  
   - ⚠️ **Alert if no power detected** (possible unplugged cable)  
   - ✅ **Heater turned off at departure time**  
   - 🛑 **Failsafe shutoff if max runtime exceeded**  

### **🎯 Key Benefits:**  
✔ **Fully automated car heating** – No manual toggling required!  
✔ **Saves energy** – Runs only when needed.  
✔ **Safety first** – Prevents overheating & detects unplugged cables.  
✔ **Easy scheduling** – Simple toggles for weekdays and weekends.  

---

## 🔧 **Setup Instructions**
1. **Make sure your car heater switch supports power monitoring** (check if it reports `current_power_w`).  
2. **Go to Home Assistant → Blueprints → Import Blueprint.**  
3. **Select your car heater switch, temperature sensor, and notification device.**  
4. **Enable heating for weekdays (Mon–Fri), Saturday, or Sunday as needed.**  
5. **Set your departure time and max runtime.**  
6. **Enjoy a warm car every morning! 🚗🔥**  

Would you like **any further tweaks or features?** 😊
