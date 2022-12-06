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


Given a certain power received profile from the 5 (Access Points) APs you should return an estimated location for the user.
