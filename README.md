# flash-multiple-esp-devices

## Setup Instructions:

#### Step 1: Install Python dependencies
+ pip install -r requirements.txt


#### Step 2: Add your .bin file
+ Add your .bin file to the current directory


#### Step 3: config.json
+ Create a config.json file in the current directory
+ Add the bin file's location under 'bin_file'
+ Add your 'friendly_name', used as prefix in Device Name
+ Example
    ```
    {
      "bin_file": "tasmota-sensors.bin",
      "friendly_name": "EZsalt"
    }
    ```


## Running Script:

#### This File takes the COM port you'd like to flash as a command line argument
```
python flash_once.py COM3
```

#### This File runs a thread for every COM port available and atttempts to flash the device using the flash_once.py script which uses esptool.py
```
python flash_loop.py
```


## esptool.py - Modifications
  + Added a return_array to get the esp Object from esptool.py
  + Added the attribute MAC_ADDRESS to the esp Object


## Requirements
  + For Python Requirements check the [requirements.txt](requirements.txt)
