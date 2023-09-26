
# Car hacking handbook
## Chapter 1
  this chapter gives a breif introduction about the the vehicle's componetns and interconnections. it shows us how to identify the highest risk components and threat modelling

  ## THREAT MODELLING:
  - to model a threat we must be aware of the car's architecture
  - it explains about various ECU'S( electronic contol units)
  - the level 0 threat model: bird's eye veiw, basically consider the vehcles internal and extranal connections and network
    this is the basic model of a vehicle to be made before making plans to hack, it alos teaches us how to structure threat models
  - level 1: receivers- the connections get more specific, three processess, immobilizer, ECU, and TPMS Receiver.
  - level 2: the communication inside the vehicle is explained,here kernel space is introduced,which is a trust boundary inside the informiant console, and it shows why some channels are more vulnerable than others for example, the cellular channel is higher risk than the
Wi-Fi channel because it crosses a trust boundary into kernel space,the Wi-Fi
channel, on the other hand, communicates with the WPA supplicant process in user space.
  - all these basically help use in giving an idea about the threat systems and how we can create threat models

  ## THREAT IDENTIFICATION:
  - identifiying threats, from basic level
  - level 0: basic threats likeRemotely take over a vehicle, Shut down a vehicle, Spy on vehicle occupants, Unlock a vehicle, Steal a vehicle
   ### level 1:
  - this focuses more on internal connection threats than the ones given from input
  - there r many components explained here;
      - cellular
      - -wifi
      - key fob
      - pressure monitor sensor
      - infotainment console
      - usb and bluetooth
      - CAN
  - level 2:recevier breakdown, more specific identifying threats
  - examples, bluez, wpa_supplicant, hsi, udev,kvaser driver
