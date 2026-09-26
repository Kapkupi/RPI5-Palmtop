A raspberry pi 5 enclosure with a 3.2 inch screen and a small keyboard. All in a simple and easy to carry clamshell form factor.
<img width="1469" height="969" alt="Screenshot 2026-09-20 141923" src="https://github.com/user-attachments/assets/97c48196-442f-422c-b956-ff0a6b9bd649" />
I did this because I really like small computers but specifically in a clamshell shape. There is also no battery 
because the RPI 5 is very picky and I did not want to deal with that yet.

I have done a project like this before but with a RPI CM 4 and M5Stack cardcomputer but having a pi 5 
and being exposed to the stardance challenge I could not resist to remake it from scratch but with a pi 5 and my
additional knowledge which I gained over the years.

What you will need:
- raspberry pi 5
- [Waveshare 3.2 inch hdmi display](https://www.waveshare.com/3.2inch-hdmi-lcd-h.htm)
- HDMI in ribbon cable format, you can find these on places like aliexpress
- [M5Stack CardKB](https://shop.m5stack.com/products/cardkb-mini-keyboard-programmable-unit-v1-1-mega8a)
- [heatsink](https://www.aliexpress.us/item/3256807144291878.html?spm=a2g0o.productlist.main.41.4c7c4080np6g24&algo_pvid=c77e5fc2-3ae9-4ca8-b024-34884b6d3c75&algo_exp_id=c77e5fc2-3ae9-4ca8-b024-34884b6d3c75-40&pdp_ext_f=%7B%22order%22%3A%2284%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21USD%216.46%211.09%21%21%216.46%211.09%21%400b15831117904546162572846e1063%2112000040293851977%21sea%21US%210%21ABX%211%210%21n_tag%3A-29910%3Bd%3A5ec1ce60%3Bm03_new_user%3A-29895%3BpisId%3A5000000210792313&curPageLogUid=AYNZNWzQDDan&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005007330606630%7C_p_origin_prod%3A)
- somewhat thin (jumper) cables and solder supplies

So now time for the assembly:

First thing to decide is wether you use the heatsink I used or another one.
This decision is important because if you do not use my heatsink then
use "case_bottom_main_OPEN" and print two additional "standoff_OPEN", 
you can find these files in the "open" folder in "STEP".
If you do have my heatsink then only use "case_bottom_main" in the
"heatsink folder". 

For printing I used my bambu lab A1 with a 0.4mm nozzle and PLA.
A layer height of 0.2mm so almost just the standard settings in bambu studio.
I do recommend enabling the setting for detecting thin walls and supports.
The parts were design with these variables in mind but should also work with
similar specs.

Every part should be printed on its biggest surface except face_plate.
Face_plate should be printed on the side which faces the front/where two
latches are.

# First Step:
The first step

For the keyboard I used this: https://github.com/ian-antking/cardkb
