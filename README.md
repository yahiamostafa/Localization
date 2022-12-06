# Localization
There Are two Types of Localizations:
1) Outdoor Localization.
2) Indoor Localization.

## Outdoor Localization:
Usaully done by **GPS** (Global Positioning System) which uses the **Trilateration** technique. There are 30+ satelliats that transmit radio signals from medium earth orbit. (Radio Waves traveled by the speed of light **C**).
Those satelliates are sending important information such as:
1) The **timestamp** of this siganl.
2) The **location** of this satelliate.
When the GPS receiver gets this signal it will calculate the time taken by this siganl to reach it (Arrival time - timestamp), then the receiver can calculate the distance between it and the satelliate. (**distance = time * speed)**

We need at least four satelliates to have a **LoS** (Line of Sight Path) to the receiver because if we have only one device there are an infinite number of points where the receiver could be (A point in circumference of a circle), If we have onlt two (the receiver could be in one of two locations (the intersection between two circles).

This image is From  [Geocommons](http://giscommons.org/?page_id=879):
![image](https://user-images.githubusercontent.com/61708947/205941836-c77bb4b3-c8a7-450a-8f34-d6128009caa1.png)

- **GPS** can't be used in In-door localization because:
It need a **LoS**, beacuse the readio signal is very week, so it can't penetrate buidlings.

## Indoor Localizaion
There are several techniques can be used in indoor localizaion such as:
1) Received Signal Strength Indicator (RSSI-based).
2) Channel State Information (CSI-based).
3) Finger Printing (FP).
4) Time of Arrival (ToA).

We also can use different technolgies such as:
1) WiFi.
2) Bluetooth.
3) Lora.
4) Zigbee.

This project is **FB** based on, so I will illustrate the fingerprinting technique.

### FingerPrinting Using WiFi
Finger printing can two stages:
#### 1)  Offline stage (Learning Phase).
In This Stage, We measure the **RSS** (Received Signal Strength) from different Access Points and store them in the database.
#### 2)  Online stage.  
In this stage, We compare the received **RSS** against the ones stored in the database, using the euclidean distance between the received **RSS** and the stored ones, the reference point with minimum distance is considered as the estimated point.

#### Notes About FP
1) As the number of reference points increase, the accuracy increases, the storage needed also increases and the processing time also increases.
2) As the number of Access points increase, the accuracy increases, the storage needed also increases and the processing time also increases.

Given a certain power received profile from the 5 (Access Points) APs you should return an estimated location for the user.
