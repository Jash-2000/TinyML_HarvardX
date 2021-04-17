# TinyML

![ML Pipeline](https://courses.edx.org/assets/courseware/v1/37dbe63b3b910ce9ed00658490821ebd/asset-v1:HarvardX+TinyML2+3T2020+type@asset+block/3-2-5-1.png)

Course Resources of the 3 course specialization by Harvard University on TinyML: its applications and deployment.
The Three Courses are : [Fundamentals of TinyML](https://courses.edx.org/dashboard/programs/f7868191-7d7f-4292-b117-64549f1f483a/), [Applications of TinyML](https://courses.edx.org/dashboard/programs/f7868191-7d7f-4292-b117-64549f1f483a/), [Deploying TinyML](https://courses.edx.org/dashboard/programs/f7868191-7d7f-4292-b117-64549f1f483a/), led by **[Vijay Janapa Reddi](https://scholar.harvard.edu/vijay-janapa-reddi/home)**

The scripts majorly focus on Acoustic, Motion and Image based sensors, with a focus on Firmware as well as Neural network based aspects.  I have also experimented a lot with Pruning and Quantization with Tensorflow Lite.

---

## Instruction of Use

 * The first and foremost folder to be accessed is the src folder. All the source files and their description is present in **src** folder and it's Readme. The details of other folders is also present in the src folder itself.
 * The folder named **basic** contains basic scripts involving CNN and RNN. They do not contain anything regarding TinyML.

---

There are 2 types of quantization techniques : Post training quantization and quantization training. 
  * **Post training quantization** offers reduction in size, latency and improved portablity. This has several other tradeoffs with accuracy and precision, but one of the reason why we can think of using this method is show in the figure below. Almost all the values of weight is stored between a particular range. 
  ![Weight Distribution](https://github.com/Jash-2000/TinyML/blob/main/Weights.JPG)
  
  * **Quantization aware training** effectively emulates the inference-time quantization behavior by creating a model the downstream tools will use to produce the actual quantized models. The quantized models, naturally, will be using lower precision. And so knowing that we'll be using lower precision and introducing that into the training pipeline while its training will effectively allow the network to become resilient. Simply put, this type of trainig learns the pattern of quantization and is already aware that it will be loosing some information, thus gets trained accordingly.

---

## Main differences between tensorflow's different ecosystems

![Hardware aspect](https://github.com/Jash-2000/TinyML/blob/main/Hardware.JPG)
![Software aspect](https://github.com/Jash-2000/TinyML/blob/main/Software.JPG)
