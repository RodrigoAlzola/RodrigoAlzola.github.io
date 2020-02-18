## Jaw Detachment

**Introduction:** 
In odontology various treatments are performed for each patient's bite, for which, a study and observation of each particular case is required, since each denture is different. It is intended to optimize the procedure in time, resources and personnel by developing a computational tool that can digitally display and manipulate the dentures of each patient (digital articulator). For this procedure to be successful, there is a step that is crucial, it is about untying the jaw of the skull in such a way to be able to identify the axis of the mandibular joint by tracking all this bone. The goal of this project is by recibing a 3D images of a human skull as the input, detach the jaw in a different image and give it as the output.


**Materials:**
Image processing is needed to solve this project. The open source tool <a href="https://fiji.sc/">Fiji</a> (V.2015 December 22) is an image processing package distribution of ImageJ, bundling many plugins which facilitate scientific image analysis.

**Development:**
For a first visualization the stack of images is import to render the bone scan:

<img src = "images/JawDetachmentResults/Img_original_sinT.png?raw=true">
Caption: 3D Human Bone Scan.

As the skull is what is needed to show up, an appropriate threshold is apply to convert the image:

<img src = "images/JawDetachmentResults/Img_original.png?raw=true">
Caption: 3D Human Bone Scan after treshold.

There is a characteristic in the anatomy of the skull and jaw, from which it was taken advantage of to use the selected methodology. The jaw is not attached to the skull by any bone. Taking advantage of this feature, it was decided to use a plugin that find connected regions which makes segmentation. For this is necesary to set a restriction of minimum density. The way to operate this plugin is to identify some starting point that meets the minimum density restriction and start generating a segmented object by adding all the points adjacent to this object that meet the minimum density restriction, once all the adjacent points have been found it is evaluated if this object contains more points. 

**Results:**
At the end of the image analysis the plugin delivers an image series with the different segmentations according to the restrictions. Three conected regions where found: the skull, the jaw and the spine. It should be taken into consideration that in the delivered image there has to be no point of contact between the lower part of the jaw with the rest of the skull. The only part that can be contact between this two bones is in the teeth. 
It is vitally important that this fact is taken into consideration when taking an X-ray, since if there is any point of contact, segmentation could be difficult. This happens because when there is a point of contact, the method recognizes the entire skull as a single segment.

<img src = "images/JawDetachmentResults/Img_final.png?raw=true">
Caption: Jaw detach form the original image.

**Conclusion:**
The need for interaction with people in the area of dentistry to know the exact requirements and the way in which it is desired to continue this project were fundamental to take the initial step of this research, since without this approach, more expensive segmentation options could have been chosen to perform and maybe unnecessarily extensive.

For more information see <a href="RodrigoAlzola.github.io/blob/master/pdf/JawDetach_Alzola_Valenzuela_Beckdorf.pdf">target="_blank">PDF.</a>.

_(3 of July, 2017) Los Andes Univeristy, Santiago, Chile. <br>
This project was develope in colaboration of the Faculty of Odontology and the Faculty of Engineering of Los Andes University.
Credit goes to  Diego Beckdorf and Matías Valenzuela for their primary role in the development of this project._


