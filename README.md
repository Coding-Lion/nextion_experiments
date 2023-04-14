# Nextion - Custom Rounded Sliders

I think I have found a solution to achive rounded corners, while still having all colors available.

I created a custom font, that will serve as the colored bar:

![custom font](images/custom_font.png)

Then I removed the pic (Background Image) and pic1 (Foregropund Image) of the slider.

To display the bar I added this code Touch Release Event and the Touch Move Event of the Slider:

````
//draw colored bar
xstr 61,261,340,58,7,col.val,6371,0,0,1,"ab"
//draw black strip to the right of the slider
xstr hBrightness.val*33/10+61,261,400,58,7,6371,6371,0,0,1,"ab"
//(only for the Touch Release Event) force a redraw of the slider, to ensure it is on top
vis hBrightness,1
````

Result:

![custom font](images/simulator_1.png)
![custom font](images/simulator_2.png)
