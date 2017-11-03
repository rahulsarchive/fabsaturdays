# EAGLE (Easily Applicable Graphical Layout Editor)

EAGLE is a electronic design automation application with schematic capture, PCB layout, auto-router and computer-aided manufacturing features. It widely used by many people and the learning curve is gradual. I found this software easy to use and has a lot of good features.

[Eagle tutorials for Beginners like me.](https://www.youtube.com/playlist?list=PL868B73617C6F6FAD)
The first job is to Install Eagle. It was recently bought by Autodesk hence you need an Autodesk account to install Eagle. Once installed you need to add the Fab library to the Eagle.

Download Fab Library [fab.lbr](http://archive.fabacademy.org/archives/2017/doc/electronics/fab.lbr)

The Fab library is a collection of all the electronics inventories available in the fablab. You will be designing using these components hence you need to have them in your library. You can optionally create parts of your own by drawing custom foots prints.

After adding the Fab library you can start drawing the schematic.

## Work Flow

1. Add the components from the Library
2. Draw Schematic of desired circuit
3. Arrange and route the Board
4. Check for Design rules and ERC errors
5. Give proper border and export as PNG file
6. Use fab modules to mill out the traces on copper board.
7. Solder components on the board with reference to the schematic
8. Debugging using electronics test equipment

![Drawing the schematic](https://user-images.githubusercontent.com/32607702/32375454-a4fbc604-c0c7-11e7-8b15-65bce0dfb903.PNG)
Draw the schematic by bringing in all the components from the library, arraginging them and then use the **net** tool to connect the circuit. 

## Electrical rule check (ERC)

ERC involves checking a schematic for all the electrical connections. It will show errors, warnings etc. We can check this and correct the errors from the schematic. ERC will be displayed as a tiny icon in the bottom left of the page.

After Drawing the schematic you can switch over to the Board view by click on the top icon. In this view you can see the components and their foot prints and some yellow lines representing the connection you made in the schematic.

Before routing the board, the most important step you have to do is set the Design rules. The design rules relate to the trace width, the clearance between the traces etc.

The design rules can be set by clicking on the DRC icon in the bottom left corner. Once you draw the schematic, switch over to the board view to arrange your components.

![Arranging the board](https://user-images.githubusercontent.com/32607702/32375474-b64db462-c0c7-11e7-9531-f5c5ac4a01d1.PNG)

This is the first thing which you see, when you switch to board view. All the components are connected by imaginary yellow lines which complete the circuit, arrange the components in the board and route the traces using the **route** tool.

![Routing](https://user-images.githubusercontent.com/32607702/32375346-4197243c-c0c7-11e7-8b7d-e5b24963c911.PNG)

Once routed, export the design of the board as PNG.

![traces](https://user-images.githubusercontent.com/32607702/32375349-4310db32-c0c7-11e7-9467-c474d6afd613.png)
![cut](https://user-images.githubusercontent.com/32607702/32375352-4496ddf8-c0c7-11e7-86c1-078690f4608a.png)

We use Modella MDX 20 to machine our PCB. Modella is a Desktop milling machine that is capable of milling wood, wax, MDX,and circuit board blanks. It has a small bed which moves in the Y-axis, a Tool head which moves in the X-axis and the end effector which moves in the Z-axis. It supports many milling bits and is versatile. The machine itself has a tiny foot print and can be placed on a table.

![modela](http://archive.fabacademy.org/archives/2017/fablabtrivandrum/students/280/assets/img/week4/modella/modella.jpg)

### Cutting Logic: How to Mill with Modela 
![fabmodule](http://archive.fabacademy.org/archives/2017/fablabtrivandrum/students/280/assets/img/week4/rah4.png)

Modella MDX 20 behaves like an ordinary 3-Axis CNC machines, Each axis is driven by a stepper motor and the cutting program tells the machine where to go by giving coordinates to the machine in real time.

What the software does is that it converts the .png image we give into a series of tool paths, these tool paths are defined by their coordinates. The .png image is a black and white layout of the board, and the black portions will be milled and the white portion is where the copper will be left.

We have two milling processes in cutting a PCB, The first one is milling the traces to get the circuit board pattern, and the second is cutting out the board from the base material.

For milling traces, we use the 1/64th inch (0.4mm) bit and for cutting 1/32th (0.8mm) inch bit.

Got to the terminal and run fab Now the fab module will open and the select the input format to .png and select the output you want depending on your machine (modlella MDX 20).

On the top menu select the process you want to use. For milling traces, select the milltraces(1/64) option. Now click load .png to load your traces file and click make path Now you can see the path the tool is going to move through. You can change the setting, I'm leaving it in the defaults. Now if you click make.rml and click send rml

![mill](http://archive.fabacademy.org/archives/2017/fablabtrivandrum/students/280/assets/img/week4/modella/mill1.JPG)

![finishmill](http://archive.fabacademy.org/archives/2017/fablabtrivandrum/students/280/assets/img/week4/modella/millf2.jpg)

![solder](http://archive.fabacademy.org/archives/2017/fablabtrivandrum/students/280/assets/img/week4/modella/sold3.jpg)
