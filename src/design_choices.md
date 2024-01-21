# Design choices

Here we will go over our design and explain why we made certain decisions. For a more detailed description of the system with pictures please look at the design overview first. 
The system consists of multiple parts that are all mounted on top of a wooden plate. I will divide the system into multiple sub systems.
•	The motor box
o	The motor holders
o	The motors
o	The motor attachments for holding the parts
The motor box is an acrylic/3dprinted box that contains the motor holders, the motors and attachment pieces for holding the parts. The box itself consists of a 3d printed bottom plate which has engraved circles for positioning the motor holders. It has 4 acryllic plates, 1 at the top, 1 for each side and 1 for the back. The front of the box is open so the motors can be wired. 
The motor holders are 3d printed. These holders are glued to the bottom plate of the box. Each motor holder has 2 openings at the sides for wiring of the motors. They keep the motors in place using friction, so that when something goes wrong the motors just pop out of the holders instead of the system breaking. 
The motors are 24V DC motors which have a low RPM. We chose for low RPM motors so we could have a controlled testing environment where breakage of the system is very unlikely. The motors are powered by a 24V power supply and are controlled with the PLC which was delivered by Saxion. 
Attached to the shaft of each motor is an attachment piece which holds the parts. This attachment is 3d printed using TPU plastic which is flexible. The reason for this is that the attachment acts like a spring so that when pressure is applied, the part gets pushed against the main body of the valve without the risk of breaking the attachment or motor. The attachment pieces are also designed to make up for any offset- or angular misalignments. 
The attachment pieces are attached to the motor shaft with an air tight seal. This is possible because of the flexible plastic. I printed this with an infill percentage of 70%, with this the attachment is strong enough and also just flexible enough to be able to push it onto the motor shaft. Because of this the seal is air tight.
•	The storage bridge
o	The storage tubes
o	3 inductive sensors.
The storage bridge is also made from acryllic. It consist of 2 side plates and a top plate. Attached to the top of the storage bridge are 3 storage tubes which hold 3 different parts. The tubes are attached to the bridge using super glue. There are 3 inductive sensors which check if all the parts are in storage. 
•	The air cylinder
o	The pusher on the air cylinder
o	Attachment pieces
o	Throttle valve
The air cylinder is a single-acting cylinder from Rexroth. It pushes the motor box underneath the storage bridge to load the parts onto the motor attachments. It is attached to one of the motor holders with a 3d printed pusher using nuts and bolts. The reason we are pushing the box instead of the bridge is because the bridge has a very high center of gravity which would cause that it would easily fall over if pushed.  The air cylinder is attached to a wooden base using 3d printed attachment pieces and screws. 
The air cylinder has a threaded shaft. First the pusher was attached with a 3d printed thread this was later changed to a 3d printed pusher with a metal nut inside of it because the 3d printed thread could brake easily because of the force of the air cylinder. 
•	The robot
o	The grippers
The robot and the grippers are used to pick up the main body of the valve and also to pick up the small ring and cylinder of the valve. The ring and cylinder are delivered to the robot using a storage plate which has chamfered cylinders, so that when the rings and cylinders are placed on top it is always centered. 
•	Wooden plate
Al of the parts are attached to a wooden plate using either screws or glue. 
Improvements:
The motor box and its parts
1.	We recommend attaching the motors using screws for a more sturdy and secure attachment. 
2.	The motor box currently has 3 walls and 1 open section. We recommend to have 2 open ends at the front and back because with the current system it is very difficult to wire the motors and attach the pusher. When changing this structural strength has to be carefully looked at. 
3.	The attachments pieces are made only of TPU plastic. This plastic is pretty slippery. For improving the speed of the system, rubber should be added to the attachment pieces. When this is done you can probably test the system which motors that have a much higher RPM. 
The storage bride
1.	The storage bridge is currently attached to the wooden plate using glue. The bridge should be altered so that it is attached to the plate using screws. 
2.	The storage tubes are also attached to the bridge using glue. This should definitely be changed since the parts are heavy. We recommend using nuts and bolts for the most secure attachment. 
The air cylinder
1.	In the future we recommend using a double acting cylinder, because then you can program the timings of closing the cylinder using the program. Currently we are stuck with a duration of about 8 seconds before it retracts. 
2.	Using a better throttle valve. The current throttle valve doesn’t limit the speed enough. The air cylinder is still too fast which isn’t very save for the operator and also can lead to breakage pretty easily. 
3.	Using an air cylinder with a longer stroke length. The current air cylinder has a stroke length of 50 mm because of this there isn’t much clearance between the storage tubes and the robot. We recommend using an air cylinder with at least double the stroke length to prevent collisions.
The robot & gripper
1.	using an electric gripper. The current gripper is pneumatic, this means that it can only open and close. Because of this we needed to separate grippers to be able to pick up the parts we wanted to pick up. When using an electric gripper you can determine how much the gripper opens and closes, so you would only need 1 gripper.  
