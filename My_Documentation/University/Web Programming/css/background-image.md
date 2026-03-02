Background-size is a property that allow us to insert images in a container.

When we just create our html and we put image to out container, the image will adapt to its size according to the html elements and for this it will display the same image if it is small or it will only show a part of it if it is very big.

For example in the image below shows a 300 PX container.
![[Pasted image 20240624171639.png]]
If we use the background-size=contain property We will see the image scaled to the 300 PX container.
![[Pasted image 20240624171950.png]]
If we use the background-repeat=no-repeat property We will see the image without repeating what generate a space without using.

![[Pasted image 20240624172840.png]]

If we use the background-size=cover property We will see the image scaled to the 300 PX container, fully covered .
![[Pasted image 20240624173116.png]]

**Contain** will choose between the **smaller** value between width and height of the **container** and the rule applies if we have a smaller width then it is divided, however, if we analyze the height then it is multiplies. After applying the rule we must verify if they are the correct dimensions, otherwise we take the container dimension as a base.
	-1200 x 600 image - 100 x 300 container => 100 (width) => 100 / 2 => 50 <= 300? true then => 100 x 50 image.
	-1200 x 600 image - 300 x 100 container=> 100 (height) => 100 x 2  => 200 <= 300? true then => 200 x 100 image.
	-1200 x 600 image - 150 x 100 container => 100(height) => 100 x 2 => 200 <= 150? false then => 150/2 => 75 => 150 x 75 image. 
	-600 x 1200 image - 150 x 100 container =>  100(height) => 100 x 0.5 => 50 <= 150 ? true then 50 x 100 image.
	-600 x 1200 image - 100 x 150 container =>  100(width) =>  100 / 0.5 => 200 <= 150 ? false then 150 (container dimension) => 150 x 0.5 => 75 x 150 image.

**Cover** will choose between the **larger** value between width and height of the **container** and the rule applies, if we have a greater height then we multiply, however, if we analyze the width then it is divided, After applying the rule we must verify if they are the correct dimensions, otherwise we take the container dimension as a base. 
	-1200 x 600 image - 100 x 300 container => 300(height) => 300 x 2 => 600 >=100? true then => 600 x 300 image.
	-1200 x 600 image - 300 x 100 container => 300 (width) =>
	300 / 2 => 150 >= 100 ? true then => 300 x 150 image.
	-1200 x 600 image - 300 x 200 container => 300 (width) =>
	300/2 =>150 >= 200? false then => 200 (container dimension) => 200 x 2 => 400 x 200 image.   
	-600 x 1200 image - 150 x 100 container => 150 (width) => 150 / 0.5 => 300 >= 100? true then => 150 x 300 image.
	-600 x 1200 image - 100 x 150 container => 150 (height) => 150 x 0.5 => 75 >= 100? false then => 100 (container dimension) => 100 / 0.5 => 100 x 200 image. 

if we want to adjust an image without the ratio the background-size takes one argument or two arguments. background-size = width (the height is automatically selected with an argument, and also preserves the ratio), background-size = width height.

background-size = 300 PX 300 PX // 100% 100%
![[Pasted image 20240624194942.png]]
