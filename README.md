# SYZYGY Breakout Flash 1V8
SYZYGY Breakout Board strictly for 1.8V flash chips. I wanted a way to experiment with flash without having to spin a new board for each footprint or solder yet another BGA or TSOP. Flash programmers with ZIF adapters seemed like the best choice and SYZYGY would make it compatible with a wide range of FPGA boards. So I combined the ZIF and SYZYGY then added a clock (the SYZYGY-Breakout-FLASH-LVL even has level shifters!). This is the simpler version of the other two SYZYGY flash breakout boards but if you really wanted to use this board with other voltages then you could either change the SYZYGY DNA file to use a different VIO (which won't work on ZUBoard 1CG's dumb VIO) or use an add-on DIP board for shifting to whichever voltage your flash requires. Maybe you could take one of these [boards](https://www.amazon.com/gp/product/B0897TX932) and replace the 1.8V LDO with a 3.3V LDO? If you do and it works then let me know.

# Fabrication
I use JLCPCB and OSH Park. I used the DRC rules for OSH Park so the board doesn't have any special fabrication requirements. Just pick your favorite PCB shop and color.

# FPGA Development
The board has silkscreen text with corresponding pins for Avnet's [ZUBoard 1CG](https://www.avnet.com/wps/portal/us/products/avnet-boards/avnet-board-families/zuboard-1cg/). If you use a different board then you'll have to change the silkscreen and generate new gerbers. Or you can just look up the pins for your board each time. Theoretically you can use this board with any FPGA dev board that has a SYZYGY connector then you could use the respective controller for your flash device OR find someway to expose it to AXI and PS to use it with flashrom. As I figure out specific tools that work well then I'll update this README with tutorials.

# BOM
You can find datasheets for each component in the datasheets directory. All of the components can be bought from Mouser or Digikey. 
* Epson SG5032VAN
* Texas Instrument TLV1117LV
* Aries 28-6554-11

# Future Work
I consider this board feature complete. As I find/create IP and software that works with this board then I'll update this README with tutorials on how to use them. Feel free to create a GitHub issue detailing your own success story or use case.

