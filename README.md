A raspberry pi 5 enclosure with a 3.2 inch screen and a small keyboard. All in a simple and easy to carry clamshell form factor.

A little demo video can be found here: https://youtu.be/wP34KrAoiqU
<img width="1505" height="1962" alt="IMG_E5924" src="https://github.com/user-attachments/assets/6325c8c1-67d7-4974-8383-b55a81814a8b" />

I did this project because I really like small computers but specifically in a clamshell shape. There is also no battery 
because the RPI 5 is very picky and I did not want to deal with that yet.

I have done a project like this before but with a RPI CM 4 and M5Stack cardcomputer but having a pi 5 
and being exposed to the stardance challenge I could not resist to remake it from scratch but with a pi 5 and my
additional knowledge which I gained over the years.

What you will need:
- raspberry pi 5
- [Waveshare 3.2 inch hdmi display](https://www.waveshare.com/3.2inch-hdmi-lcd-h.htm)
- Four M2.5x6 screws
- HDMI in ribbon cable format, you can find these on places like aliexpress
- [M5Stack CardKB](https://shop.m5stack.com/products/cardkb-mini-keyboard-programmable-unit-v1-1-mega8a)
- [heatsink](https://www.aliexpress.us/item/3256807144291878.html?spm=a2g0o.productlist.main.41.4c7c4080np6g24&algo_pvid=c77e5fc2-3ae9-4ca8-b024-34884b6d3c75&algo_exp_id=c77e5fc2-3ae9-4ca8-b024-34884b6d3c75-40&pdp_ext_f=%7B%22order%22%3A%2284%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21USD%216.46%211.09%21%21%216.46%211.09%21%400b15831117904546162572846e1063%2112000040293851977%21sea%21US%210%21ABX%211%210%21n_tag%3A-29910%3Bd%3A5ec1ce60%3Bm03_new_user%3A-29895%3BpisId%3A5000000210792313&curPageLogUid=AYNZNWzQDDan&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005007330606630%7C_p_origin_prod%3A) (optional)
- somewhat thin (jumper) cables and solder supplies

## For printing:

First thing to decide is wether you use the heatsink I used or another one.
This decision is important because if you do not use my heatsink then
use "case_bottom_main_OPEN" and print two additional "standoff_OPEN", 
you can find these files in the "open" folder in "STEP".
If you do have my heatsink then only use "case_bottom_main" in the
"heatsink" folder. 

For printing I used my bambu lab A1 with a 0.4mm nozzle and PLA.
A layer height of 0.2mm so almost just the standard settings in bambu studio.
I do recommend enabling the setting for detecting thin walls and supports.
The parts were design with these variables in mind but should also work with
similar specs.

Every part should be printed on its biggest surface except face_plate.
Face_plate should be printed on the side which faces the front/where two
latches are.

The spring also needs to be printed on its side so it looks like a snake from
the top down.

## Assembly:
The first step after (or during) printing is desoldering the grove connector 
from your CardKB. Then put your four cables through the hole on the CardKB and
the hole on the RPI 5 close to it which would normaly be for a cooler but we
will use it to pass through the cables.
Then solder them to the CardKB. You may have to remove your jumper heads and
resolder them later so that it can fit through the hole. You should make your
cables long enough because you can always shorten them later if you need to.
It could look something like this:

<img width="2444" height="2641" alt="IMG_5873" src="https://github.com/user-attachments/assets/d2d62036-1263-40eb-bbf8-f11718d51895" />
(Note: I butchered my CardKB so I had to find other solder points
and even another resistor. You should do a better job than me ^-^)

As you may have already noticed there is an extra pair of wires on the right
of the image. These are for the screen.

Now that the wires are soldered you can route them. Basically just bend them
towards the GPIOs. Keep the IC near the USB-C connector free so that you can
still put the thermal pads for cooling on it. The pair of wires for the
screen should be put in between the USB and HDMI port. 
For now it should look something like this:

<img width="2329" height="2148" alt="IMG_5869" src="https://github.com/user-attachments/assets/fe22706c-f7b6-4d41-b79b-15a7494240d5" />

Now that the cables are somewhat routed correctly you can put the heatsink
on. After putting the heatsink on you can connect the cables with the pins.
Connect the 3.3V cable for the CardKB with pin 1, the SDA cable with pin 3,
the SCL cable with pin 5, both ground cables with pins like 6, 9, or 14
for example. And finally the 5V cable for the screen with pin 4. Could look
like this:

<img width="3521" height="1768" alt="IMG_5876" src="https://github.com/user-attachments/assets/095c86ca-35ed-42a6-a396-47d8615ccb37" />

As seen in the image already you can put the power cables for the display
through the hole in the back of the case. Before putting the pi in don't 
forget to put the power button into its slot on the left. Then put the 
pi 5 with the CardKB into the bottom case. With the display power cables 
it is a bit of a tight fit but should be managable. After putting it in 
you can also put the face cover on while making sure that the CardKB is 
correctly aligned.

Now for the screen you should desolder the pogo pins and then solder on
either some jst connector or headers of some kind. Desoldering was a bit tedious
but it should be possible. Put the spring into the hole on the right 
then just put the screen case into the hinge
by overextending it by a bit more than 180 degrees. Should not be difficult.
After connecting both parts you can put the screen buttons in, connect the
power cables with the headers on the display. Ground should be on the left 
and 5V on the right. And after making sure the cables are secure and you put
in the buttons for the display you can screw the screen in with four M2.5x6 
screws. Then just plug your mix of HDMI connectors in and it should be finished!

For the keyboard software I used this: https://github.com/ian-antking/cardkb

If you have any questions or feedback you can dm me on discord! User is "keks357"
