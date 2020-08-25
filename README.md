# Functional Group Detector
**An organic functional group detector using Tensorflow's object detection API.**

By Davis Thomas Daniel

Email :  forall2087@gmail.com

Here is a screengrab of one of the detections. 
![An example of detected functional groups](detection_results_fg_detector_v1/fg_detection_example.png)


In organic chemistry, [functional groups](https://en.wikipedia.org/wiki/Functional_group) are specific substituents or moieties 
within molecules that may be responsible for the characteristic chemical reactions of those molecules. The detection of functional groups can aid in the elucidation of reaction mechanisms and the structure of transition states using deep learning techniques.

FG detector is chemical functional group object detector based on Tensorflow object detection API. The main motivation behind this detector was that the existing software for detection of functional groups heavily depends on the use of substructure filtering and is therefore not automated.

The detection model was trained using transfer learning from 'ssd_efficientdet_d0_512x512_coco17_tpu-8'.  

The training dataset comprised of 300x300 sized .png images from PubChem.

Currently, the model detects the following groups : 
* Alcohol
* Aldehyde
* Amine
* Amide
* Carboxylic Acid
* Ester
* Ether
* Ketone
* Double bonds
* Benzene Ring
* Halogen
* Thiol





## Trying out the model

To try out functional group detection using the trained model, first open the notebook titled [FG_detector_v1_detection_test.ipynb](https://github.com/davistdaniel/Functional_Group_Detector_using_Tensorflow_object_detection/blob/master/FG_detector_v1_detection_test.ipynb) on [Google Colab](https://colab.research.google.com/). Everything is adequately explained in the notebook. 

**Click [here](https://colab.research.google.com/github/davistdaniel/Functional_Group_Detector_using_Tensorflow_object_detection/blob/master/FG_detector_v1_detection_test.ipynb) to directly open the notebook in Google Colab.** You might have to sign in to your google account to run the notebook.
You are welcome to contact me on my email in case of any issues.



## Limitations

I am quite new to Tensorflow, Deep Learning/Machine Learning and programming as a whole. 
This project is my first attempt at a Tensorflow project for detecting objects. 
My main aim was to learn how to set things up and make my first pass at Machine learning.
I have mostly followed online tutorials to educate myself and set everything up.
My implementations are definitely not the most efficient. 

* The model was trained on around 600 images from PubChem which I annotated. However, the sampling was not uniform.
* Therefore, the model is better at detecting :
	* Alcohol
	* Aldehyde
	* Carboxylic Acid
	* Halogen
	* Ether
	* Benzene Ring
	* Double Bond
*  Check the the directory [detection_results_fg_detector_v1](https://github.com/davistdaniel/Functional_Group_Detector_using_Tensorflow_object_detection/tree/master/detection_results_fg_detector_v1) for tested images and corresponding detections using the trained model.

* You can see few errors in detections and sometimes the model does not detect all similar groups in the structure, however, this could be solved by a bigger dataset.
* The training was done only for 3.5 hours, using 40000 steps with a batch size of 4.

## Outlook

* My plans moving ahead, is to definitely increase the training dataset both in size and heterogeneity. The current model is solely trained on PubChem images.
* My plan is to inlclude random images of functional groups from google searches.
* I also plan to increase the number of classes signficantly, once I am more experienced with the whole process.
* Multiple trials with different pre-trained models.

	
## Contributing
Suugestions and comments are very welcome! 
Let me know if you have any suggestions or other comments.I would be glad to discuss them and make required changes.
You can drop me an email at : forall2087@gmail.com

## License
[MIT](https://choosealicense.com/licenses/mit/)

##
