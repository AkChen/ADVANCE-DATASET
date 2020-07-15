## Cross-Task Transfer for Multimodal Aerial Scene Recognition 
## ECCV 2020
Authors: Di Hu, Xuhong Li, Lichao Mou, Pu Jin, Dong Chen, Liping Jing, Xiaoxiang Zhu, Dejing Dou


## Brief Introduction

To our knowledge, the audiovisual aerial scene recognition task has not been explored before, for further facilitating the research in this field, we construct a new dataset, with high-quality images and scene labels, named as Aerial sceNe reCognition datasEt(ADVANCE), which in summary contains 5075 pairs of aerial images and sounds, classified into 13 classes.
some introductions

## Statistics and some samples
#Statistics

![PNG](/statistics.png)

#Audiovisual samples
![PNG](/samples.png)

## Dataset collection

  The audio data are collected from [Freesound](https://freesound.org/browse/geotags/), where we remove the audio recordings that are shorter than 2 seconds, and extend those that are between 2 and 10 seconds to longer than 10 seconds by replicating the audio content. Each audio recording is attached to the geographic coordinates of the sound being recorded. From the location information, we can download the updated aerial images from [Google Earth](https://earthengine.google.com/). Then we pair the downloaded aerial image with a randomly extracted 10-second sound clip from the entire audio recording content. Finally, the paired data are labeled according to the annotations from [OpenStreetMap](https://www.openstreetmap.org/), also using the attached geographic coordinates from the audio recording. Those annotations have manually been corrected and verified by participants in case that some of them are not up to date.

  Due to the inherent uneven distribution of scene classes, the collected data are strongly unbalanced, which makes difficult the training process.
So, two extra steps are designed to alleviate the unbalanced-distribution problem. Firstly we filter out the scenes whose numbers of paired samples are less than 10, such as desert and the site of wind turbines. Then for scenes that have less than 100 samples, we apply a small offset to the original geographic coordinates in four directions. So, correspondingly, four new aerial images are generated from Google Earth and paired with the same audio recording, while for each image, a new 10-second sound clip is randomly extracted from the recording. 

## Spliting strategy
   The dataset was splited by train/Val/test with the ratio of 0.7:0.1:0.2. [Data construction demo](https://github.com/DTaoo/Multimodal-Aerial-Scene-Recognition/blob/master/data/data_partition.py)

## Download

[Paper Repo](https://github.com/DTaoo/Multimodal-Aerial-Scene-Recognition)

[Dataset](https://zenodo.org/record/3828124)


## Reference

If you use this repo or the ADVANCE dataset in your research, please cite our paper:

      Cross-Task Transfer for Geotagged Audiovisual Aerial Scene Recognition 
      Di Hu, Xuhong Li, Lichao Mou, Pu Jin, Dong Chen, Liping Jing, Xiaoxiang Zhu, Dejing Dou
      ECCV 2020

