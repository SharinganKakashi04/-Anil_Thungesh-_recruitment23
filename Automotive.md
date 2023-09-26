
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

## Chapter 2:BUS protocols
these r the common bus protocols used in vehic,le communications. bus protocols govern and transfer packets through network of the vehicle.CAN bus is the most used. the CAN bus, exists in a standard
location on all vehicles: on the OBD-II connector.critical vehicle communications like rpm  management and breaking happens on high speed bus lines, while no so critical communications happen through low speed ones
### CAN BUS:
- it is a simple protocol used in cars.
- Modern vehicles are full of little embedded systems and electronic control units (ECUs) that can communicate using the CAN protocol
- CAN runs on two wires: CAN high (CANH) and CAN low (CANL).
CAN uses differential signaling
### The OBD-II Connector:
- Many vehicles come equipped with an OBD-II connector, also known as the
diagnostic link connector (DLC), which communicates with the vehicle’s internal network.

after this the CAN bus packet layout was epxlained
- they contain 4 main elements:
     - Arbitration ID
     - Identifier extension(IDE) - 0 bit for standard CAN
     - data length code(DLC)
     - data
  ### ISO-TP protocol:
  - ISO 15765-2, also known as ISO-TP, is a standard for sending packets over
the CAN bus that extends the 8-byte CAN limit to support up to 4095 bytes
20 Chapter 2
by chaining CAN packets together

lack of time so im ending it here

  
