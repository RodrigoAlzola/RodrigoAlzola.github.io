## Halo Detector

**Introduction:** 
Is vital in pharmaceutical and chemistry research develop new and different methods to measure the efficiency of a medicament. In general a variety of pharmaceuticals discs are attached to a bacterial sample, a circular area is generated as the pharmaceuticals kills the bacteria, like halos of contrast. The radius of this circular area or halo is determined to measure the efficiency of the pharmaceutical. Normally this procedure take several samples and all of them are measure by hand with a caliper by a human, taking more that 4 hours to complete just one experiment and having the risk of mesurment mistakes. The goal of this project is to innovate a machine able to automate this process, make it faster and precise.

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

(*Hardware design*):
In innovation is essential to understand the concept of "viable minimums". It means to reach the most requirements for satisfying a product with the minimum materials and time. The product must take a shot of the sample and calculate the radius automatically. Also it must regulate the intesity of light, as the sample is sensitive to some emissions. First prototype was developed with the use of a Raspberry Pi. 

<img src = "images/Halo_Detector/prototipo.png?raw=true">
<img src = "images/Halo_Detector/RGB.png?raw=true">
Caption: First prototype. It takes photos in RGB for early analysis. 

The second prototype was a much more close to the final product. At this stage the client starts already testing the product, so that correction and modifications can be performed.

<img src = "images/Halo_Detector/prototip2.png?raw=true">
Caption: Second prototype.

(*Software design*):
In automatic image analysis, it is common to find the problem of detecting simple ﬁgures such as straight lines or circumferences. The first approach to detect the halos was to use what is called the Hough transform. This method give some good results, but the model wasn't robust. It has a high rate of false positive detections or detect the smallest pharmaceuticals discs which there is not interest in find it. 

<img src = "images/Halo_Detector/Hough.png?raw=true">
Caption: Hough transform detection.

As this approach is not trustworthy I decide to do an intensive image analysis. Applying a simple threshold and filters is easy to detect the borders of the halos because of there contrast. Choosing 3 points in the line of the halo is possible to calculate the radius and the center of a circle and represent the whole circumference (for more information see <a href="https://www.geeksforgeeks.org/equation-of-circle-when-three-points-on-the-circle-are-given/">Circle from three points calculator</a>). Also for the analysis I take advantage of the geometry of the problem as the samples are always going to have 6 halos separated in the same way for performance agility. 

<img src = "images/Halo_Detector/Analisis.gif?raw=true">
Caption: Full image analysis.

For the final product a basic GUI was develope. It make the analysis via streaming, controlling the levels of light and filter values.  

**Results:**
This is the final version of the machine, this one was delivered to the client:

<img src = "images/Halo_Detector/FinalM.png?raw=true"> <br>
Caption: Final product.

A robust image anlyisis to detect halos was implement with a frendly interface for automatisation of pharmaceutical mesurments. The final results is show next:

<img src = "images/Halo_Detector/results1.png?raw=true">
<img src = "images/Halo_Detector/results2.png?raw=true">
Caption: Final halo detection.


**Conclusion:**
Having been able to invent a machine from scratch was something extremely entertaining and challenging. This project was requested by the Chemical Analyisi Center of Universidad Catolica, Santiago, Chile. After all requirements were satisfy the machine was delivered to the client and a training was performed in the Chemical Analysis Center to introduce the product to the officials.

<img src = "images/Halo_Detector/training.png?raw=true">
Caption: Officials training.


_(January, 2018) C3D Open Innovation, Santiago, Chile. <br>
This project was develope for the Chemical Analysis Center of the Faculty of Chemistry, Universidad Catolica, Santiago, Chile.<br>
All the intellectual property of this project belongs to C3D Open Innovation._
