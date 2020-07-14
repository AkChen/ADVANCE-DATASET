## Cross-Task Transfer for Multimodal Aerial Scene Recognition 
## ECCV 2020
Authors: Di Hu, Xuhong Li, Lichao Mou, Pu Jin, Dong Chen, Liping Jing, Xiaoxiang Zhu, Dejing Dou


## Brief Introduction

The audiovisual aerial scene recognition task has not been explored before. Salem et al.[1] established a dataset to explore the correlation between geotagged sound clips and overhead images. For further facilitating the research in this field, we construct a new dataset, with high-quality images and scene labels, named as Aerial sceNe reCognition datasEt(ADVANCE), which in summary contains 5075 pairs of aerial images and sounds, classified into 13 classes.
some introductions

## Statistics and some samples
1. Statistics
![PNG](/statistics.png)
2. Audiovisual samples
![PNG](/samples.png)

## Detailed information for the ADVANCE dataset

The audio data are collected from [Freesound](https://freesound.org/browse/geotags/), where we remove the audio recordings that are shorter than 2 seconds, and extend those that are between 2 and 10 seconds to longer than 10 seconds by replicating the audio content. Each audio recording is attached to the geographic coordinates of the sound being recorded. From the location information, we can download the updated aerial images from [Google Earth](https://earthengine.google.com/). Then we pair the downloaded aerial image with a randomly extracted 10-second sound clip from the entire audio recording content. Finally, the paired data are labeled according to the annotations from [OpenStreetMap](https://www.openstreetmap.org/), also using the attached geographic coordinates from the audio recording. Those annotations have manually been corrected and verified by participants in case that some of them are not up to date.
## Download
