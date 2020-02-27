## Halo Detector

**Introduction:** 
Is vital in pharmaceutical and chemistry research develop new and different methods to measure the efficiency of a medicament. In general a variety of pharmaceuticals discs are attached to a bacterial sample, a circular area is generated as the pharmaceuticals kills the bacteria, like a halo of contrast. The radius of this circular area or halo is determined to measure the efficiency of the pharmaceutical. Normally this procedure take several samples and all of them are measure by hand with a caliper by a human, taking more that 4 hours to complete just one experiment and having the risk of mesurment mistakes. The goal of this project is to innovate a machine able to automate this process, make it faster and precise.

<img src = "images/Halo_Detector/Manual.png?raw=true">
Caption: Manual mesurment halos.

**Methods and Materials:**
This project requires knowledge in hardware/software engineering, computer vision, biotechnology and product design. 
The principal materials for this product were:
- Raspberry Pi
- RGB LED strips
- Logitech C920 Webcam

All the develope was made in Python with Linux OS and late develop in Debian OS. 

**Development:**

(*Software design*):
In automatic image analysis, it is common to find the problem of detecting simple ﬁgures such as straight lines or circumferences. The first approach to detect the halos was to use what is called the Hough transform. This method give some good results, but the model wasn't robust. It has a high rate of false positive detections or detect the smallest pharmaceuticals discs, which there is not interest in find. 

<img src = "images/Halo_Detector/Hough.png?raw=true">
Caption: Hough transform detection.

As this approach is not trustworthy I decide to do an intensive image analysis. Applying a simple threshold and filters is easy to detect the borders of the halos because of there contrast. Choosing 3 points in the line of the halo is possible to calculate the radius and the center of a circle and represent the whole circumference (for more information see <a href="https://www.geeksforgeeks.org/equation-of-circle-when-three-points-on-the-circle-are-given/">Circle from three points calculator</a>). Also for the analysis I take advantage of the geometry of the problem as the samples are always going to have 6 halos separated in the same way for performance agility. 

<img src = "images/Halo_Detector/Analisis.gif?raw=true">
Caption: Full image analysis.

For the final product a basic GUI was develope. It make the analysis via streaming, controlling the levels of light and filter values. 

<img src = "images/Halo_Detector/GUI.mp4?raw=true">
Caption: Basic GUI. 

(*Hardware design*):
In innovation is essential to understand the concept of "viable minimums". It means to reach the most requirements for satisfying a product with the minimum materials and time. First prototype was developed with the use of a Raspberry Pi. 

<img src = "images/Halo_Detector/prototipo.png?raw=true">
<img src = "images/Halo_Detector/RGB.png?raw=true">
Caption: First prototype. It takes photos in RGB for early analysis. 

**Results:**
At the end of the image analysis the plugin delivers an image series with the different segmentations according to the restrictions. Three conected regions where found: the skull, the jaw and the spine. It should be taken into consideration that in the delivered image there has to be no point of contact between the lower part of the jaw with the rest of the skull. The only part that can be contact between this two bones is in the teeth. 
It is vitally important that this fact is taken into consideration when taking an X-ray, since if there is any point of contact, segmentation could be difficult. This happens because when there is a point of contact, the method recognizes the entire skull as a single segment.

<img src = "images/JawDetachmentResults/Img_final.png?raw=true">
Caption: Jaw detach form the original image.

**Conclusion:**
The need for interaction with people in the area of dentistry to know the exact requirements and the way in which it is desired to continue this project were fundamental to take the initial step of this research, since without this approach, more expensive segmentation options could have been chosen to perform and maybe unnecessarily extensive.

For more information see <a href="https://github.com/RodrigoAlzola/RodrigoAlzola.github.io/blob/master/pdf/JawDetach_Alzola_Valenzuela_Beckdorf.pdf">here</a>.

_(3 of July, 2017) Los Andes Univeristy, Santiago, Chile. <br>
This project was develope in colaboration of the Faculty of Odontology and the Faculty of Engineering of Los Andes University.
Credit goes to  Diego Beckdorf and Matías Valenzuela for their primary role in the development of this project._

