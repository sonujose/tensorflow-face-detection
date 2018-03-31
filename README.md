# Tensorflow Face Detector
A mobilenet SSD(single shot multibox detector) based face detector with pretrained model provided, powered by tensorflow [object detection api](https://github.com/tensorflow/models/tree/master/object_detection), trained by [WIDERFACE dataset](http://mmlab.ie.cuhk.edu.hk/projects/WIDERFace/).

## Features
Speed, run 60fps on a nvidia GTX1080 GPU.

Memory, requires less than 364Mb GPU memory for single inference.

Robust, adapt to different poses, this feature is credit to [WIDERFACE dataset](http://mmlab.ie.cuhk.edu.hk/projects/WIDERFace/), I manually cleaned the dataset to balance the precision and recall trade off.

Parallel, multiple process video processing, can inference multiple input simultaneously, I tested to process 4 videos on a single GPU card at the same time, the speed is still competitive, and there's still room to accommodate more processes.

![Parallel data processing](https://github.com/yeephycho/tensorflow-face-detection/blob/master/res/parallel-processes.png?raw=true "Show result")

## Dependencies
Tensorflow > 1.2

Tensorflow object detection api (Please follow the official installation instruction, otherwise, I cannot guarantee that you can run the code)

OpenCV python

## Usage
### Effect
Click [Youtube](https://youtu.be/gw4CVz7SPEs) to view the effect or [Youku](http://v.youku.com/v_show/id_XMzE2MDc0NzcyNA==.html?spm=a2h3j.8428770.3416059.1).

### Prepare pre-trained model
Click [here](https://drive.google.com/open?id=0B5ttP5kO_loUdWZWZVVrN2VmWFk) to download the pre-trained model from google drive.
Put the model under the model folder.

### Prepare video
Put your test video (mp4 format) under the media folder, rename it as test.mp4. 

### Run video detection
At the source root
```bash
python inference_video_face.py
```
After finished the processing, find the output video at media folder.

## License
Usage of the code and model by yeephycho is under the license of Apache 2.0.

The code is based on GOOGLE tensorflow object detection api. Please refer to the license of tensorflow.

Dataset is based on WIDERFACE dataset. Please refer to the license to the WIDERFACE license.
