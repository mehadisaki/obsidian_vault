Relative humidity (RH) can be calculated using the dry bulb temperature and the wet bulb temperature, along with the atmospheric pressure. The calculation involves determining the saturation vapor pressure at the wet bulb temperature and the actual vapor pressure of the air at the dry bulb temperature.

Here are the steps to calculate relative humidity:

1.  Measure the dry bulb temperature (Tdb) using a regular thermometer.
    
2.  Measure the wet bulb temperature (Twb) using a thermometer with a wet wick wrapped around the bulb.
    
3.  Determine the saturation vapor pressure (Pws) at the wet bulb temperature using a psychrometric chart or an online calculator.
    
4.  Calculate the actual vapor pressure (Pwa) of the air using the following formula:
    
    Pwa = Pws x (relative humidity/100)
    
    In this formula, "relative humidity" is expressed as a percentage.
    
5.  Calculate the relative humidity (RH) using the following formula:
    
    RH = (Pwa / Pws) x 100
    
    In this formula, "Pwa" is the actual vapor pressure of the air, and "Pws" is the saturation vapor pressure at the wet bulb temperature.
    
6.  Round the relative humidity to the nearest whole number.
    

Note that atmospheric pressure should be considered when calculating relative humidity. Standard atmospheric pressure is 101.325 kPa or 29.921 inches of mercury.


## Formula

Humidity (RH) from the dry bulb temperature (Tdb) and wet bulb temperature (Twb):
Magnus-Tetens equation
```excel 
=100*(EXP((17.625*Twb)/(243.04+Twb))/EXP((17.625*Tdb)/(243.04+Tdb)))
```
