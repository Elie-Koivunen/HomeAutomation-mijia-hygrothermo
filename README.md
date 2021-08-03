# HomeAutomation-mijia-hygrothermo
A quick/dirty hack to connect xiaomi mijia devices and collect data

This project is based on the following components:
- raspberry pi zero + raspbian
  https://www.raspberrypi.org/blog/zero-wh/
  
  Note1: The zero variant has a much better signal range than what is on rasp3b or rasp4
  Note2: You may want to consider using an addon bluetooth module (e.g. usb based) to gain more range and more clearly receive end point broadcasts.
  https://shop.espruino.com/accessories/usb-bluetooth
  Note3: Different BLE standards have different capabilities and ranges. 
  https://blog.nordicsemi.com/getconnected/things-you-should-know-about-bluetooth-range
  https://blog.nordicsemi.com/getconnected/tested-by-nordic-bluetooth-long-range
  
- xiaomi mijia devices
  https://tinyl.io/4Y7f

  note1: the original firmware is not optimal. an alternative optimized firmware is available at:
  https://www.youtube.com/watch?v=NXKzFG61lNs
  https://github.com/pvvx/ATC_MiThermometer
  note2: you will need to remove the battery twice during the process of updating the firmware. 
  
- bluetooth support for raspberry pi
  #apt install bluetooth pi-bluetooth bluez blueman  
  note1: reboot the raspberry pi after the installation in order to recognize the native bluetooth device
  note2: bluetoothctl utility is not reliable and wont necessarily always display the BLE devices. alternatively you can use "gatttool" and "hcitool lescan".

