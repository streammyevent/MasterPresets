# Atem Master Preset

## Atem Coordinate System info

XY coordinate
0.00, 0.00 = center of screen

Ancher point is center of object

X: 16.00 = left side of screen
Y: +9 = up
Y: -9 = down

Size:
1,00 = full resolution (1080)
0,50 = half resolution (540)
0,25 = quarter resolution (270)

Crop:
Same as X & Y, but now ranges 0-16 to crop from side to middle.
i.e. 0 = no crop, 16 = 50% cropped (from that side), 32 = fully cropped

Y coordinates are 0-9, i.e. 18 = full crop

```xml
<Box index="0" enabled="True" inputSource="2001" xPosition="2" yPosition="0" size="0.5" cropped="True" cropTop="0" cropBottom="0" cropLeft="0" cropRight="0"/>
<Box index="1" enabled="False" inputSource="2002" xPosition="7.58" yPosition="4.25" size="0.42" cropped="False" cropTop="0" cropBottom="0" cropLeft="0" cropRight="0"/>
<Box index="2" enabled="False" inputSource="2001" xPosition="-7.58" yPosition="-4.25" size="0.42" cropped="False" cropTop="0" cropBottom="0" cropLeft="0" cropRight="0"/>
<Box index="3" enabled="False" inputSource="2002" xPosition="0" yPosition="0" size="1" cropped="False" cropTop="0" cropBottom="0" cropLeft="0" cropRight="0"/>
```
