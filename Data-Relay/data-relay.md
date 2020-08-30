## Data Relay Task :vibration_mode:

**NOTE:**  _Code in **C/C++**_

Consider you have deployed various sensors in your office like temperature, pressure, gas, smoke, motion, proximity, etc. 
These sensors are present on different floors and rooms with 50 edge boards. 
You need to get the sensor readings to a single device like your mobile phone. Also, since sensors will be working the whole day, 
the size of data will increase tremendously. Considering that you need at least one week's data to provide the user with some statistics, 
you will have to compress and store the data on the user's device.  

_Data will be in JSON format (Also note the data types) →_
```
msg = {
          'device_id': “1”,
          'timestamp': “30/08/2020 22:15:25”,
          'temperature': 30.25,
          'humidity': 25.345,
          'air_pressure': 56,
          'ph': 6.7, 
          'distance': 10.20,
          'switch_state': “ON”,
      }
```
--- 
### Stage 0

* Use **MQTT** protocol to receive data from different streams (multiple senders and one receiver)
* Create 50 bots using **multithreading** that will push data streams (json type strings) @frequency of 500ms
* 30 bots publish data {temperature, humidity, air_pressure, ph} and 20 bots {distance and switch_state}

### Stage 1

* Segregate the received data based on the data types
* Can use library for parsing the json string
* First segregate this based on deviceID, and then based on data type. For example:  
Device1  
|----------temperature.txt → -40 to 110 degree Celcius (upto 2 decimal places)  
|----------humidity.txt → 0% to 100% (upto 3 decimal places)  
|----------air_pressure.txt → 3 to 300 psi (integer)  
|----------ph.txt → 0 to 14 (upto 1 decimal place)  
Device2  
|----------distance.txt → 0 to 100m (upto 2 decimal places)  
|----------switch_state.txt → “ON” or “OFF”  


### Stage 2

* Server should compress the data @frequency of 2 minutes
* Write the compression algorithm from scratch


#### Questions you should be able to answer after doing this task:  
1. What is MQTT?
2. Why MQTT?
3. How multithreading works?
4. What is JSON?
5. What are different compression algorithms and how they work?
