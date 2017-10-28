# Introduction to CNC Milling

CNC stands for Computer Numeric Control, it is a process used in the manufacturing sector that involves the use of computers to control machine tools.  Here, instead of the operator controlling the machine, the machine follows a set of instructions to  move the gantry and  make the desired shape. A popular way of giving instructions to the machine is by using G-code. The various movements of the machine for creating a part are programmed  in code and fed into the controller, which moves the machine. Some common CNC machines include lathes, mills, routers and grinders.

The process involves creating a CAD (Computer Aided Design)  file of the desired object. Then a specialized CAM (computer aided Manufacturing) software is required to convert the 3D CAD file into a set of codes which the machines can understand. this     G -code  controls all machine parameters like feed rate, coordination, location and speeds. With CNC machining, the computer can control exact positioning and velocity.

## Shopbot PRSalpha

![Shopbot PRSalpha](https://user-images.githubusercontent.com/32607702/32045778-c49a84e2-ba5e-11e7-8a94-762c22788398.png)

ShopBot PRSalpha are the toughest, most sophisticated, gantry-based CNC routers. Using advanced technology for CNC cutting, drilling, carving and machining, the PRSalpha series tools deliver rapid transit speeds of 1800 inches per minute and cutting speeds of up to 600 inches per minute. Its easy to configure and use. The PRSalpha has a bed size of 8x4 feet and delivers full production performance in digital fabrication of wood, plastic, aluminum, and other materials. 

## Link to [Archive](http://archive.fabacademy.org/archives/2017/fablabtrivandrum/students/280/week7.html)

## Nomenclature

### Drill bit Vs End mills ###

![DrillvsEnd](https://user-images.githubusercontent.com/32607702/32131027-b7c9612a-bbc1-11e7-928b-2bd13f3e7337.jpg)

Though they might look same both of them are designed for different purposes. A drill bit need to cut straight into the material hence will have teeth at tip. But an End mill needs to cut from the sides also, that means it needs to have a cutting edge spiraling all the way up to the flute.

### Flutes 

Flutes are the spiraling shafts cut along the surface of an end mill. They serve two purposes, one for cutting the material and other for clearing the wood chips from the cutting area. Less number of flutes means chips will be cleared easily but the cut will be of rough finish. Higher the number of flutes the smoother the surface, but the chips will not be cleared easily.

### Upcut & Downcut 

![upvsdown](https://user-images.githubusercontent.com/32607702/32131032-c60d7884-bbc1-11e7-84a0-372b5625ff83.jpg)
 
In an Upcut type end mill the teeth on the flute will point upwards. This means that the end mill is cutting and drawing out the wood through the flute. This is good for cutting deep into the stock. But this leaves a bad surface finish on the top of the surface.

A downcut type end mill has teeths that point downward on the flute. This means that the end mill will cut and try to push the material into the stock. This will give good surface finish on the top, but it is not very efficient at removing material.

### Flat/ball end 

![faltvsball](https://user-images.githubusercontent.com/32607702/32131033-c79fd480-bbc1-11e7-86b8-6173057fea41.gif)
 
flat end leaves flat surface profile on the stock and are good for removing large volume of material, but steps are formed when used for making curved surfaces. Ball end leaves curved surfaces and forms smooth curved finish while cutting cavities. They are used for finishing cuts.

### Chip load 
This is the amount of material that is removed in each chip. The value is approximately = feed rate (inches per minute) / (RPM x number of flutes)

### Cut depth 
This is the measure of how deep the end mill should go in each step while milling. Ideally cut depths should be less than 1/3rd of the length of the tool. They are mentioned in the product manual of the tool bits.

### Step over 

![stepover](https://user-images.githubusercontent.com/32607702/32131034-c8f77a0e-bbc1-11e7-8e78-99a87c6a4113.gif)
 
In a pocket cut the machine will traverse the entire area of the cut. It does that with a series of paths that cover the entire length and width of the cut. While doing this the step over determines how much the adjacent paths overlap each other. Usually we use it at 50%, ie the adjacent end mill cuts will overlap 50%, which gives a better finish.

## Workflow of Milling with Shopbot

1. Design the 2D, 3D model in any CAD software like Solidworks, AutoCAD etc.
2. Export the  2D model in DXF and 3D model in STL format.
3. Import the design into Vcarve pro, set the machine parameters and export as SBP file.
4. Prep the material by securely attaching it to the bed using screws and clamps.
5. Securely attach the end mill to the spindle.
6. Set the Z-origin by using the contact plate. Set the X,Y origin to a suitable place on the material.
7. Load the SBP file into  Shopbot software interface.
8. Turn on the spindle and start cutting.

## Warning

- CNC milling is hazardous, never stand close to the machine while its operational.
- End mill spinning at such high velocity has possibility of ejecting wooden shards and hot debris.
- Always wear eye protection.
- Never reach into the machine while operating.
- Always secure the work piece and tool properly to avoid damage.
- Never leave the machine running unattended.
