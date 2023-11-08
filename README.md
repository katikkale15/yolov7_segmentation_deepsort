## Segmentation
Segmentation provides fine-grained information about object boundaries and regions, while detection focuses on identifying specific objects and their locations. Classification assigns labels to images or regions, providing a holistic understanding of content.

## Deep-sort
DeepSORT, a Multiple Object Tracking (MOT) algorithm, enhances the efficiency and accuracy of object tracking in computer vision. Extending the SORT algorithm, DeepSORT uniquely identifies and tracks objects by employing an advanced association metric that integrates both motion and appearance descriptors.

The only drawback is that it is slow, hence for real-time applications using deepsort is nearly impossible. For video processing, deep-sort stitches the frames after detections and processing, but for a live feed it has to have a processing time of less than 16ms for the video to appear smooth or "real-time" which is not the case for deep-sort, it takes about 45ms for processing. This results in the video feed being very choppy and the detections are rendered moot because, in a live feed, the object is already passed by that instant.

The real use of segmentation is displayed in this image:
![image](https://github.com/katikkale15/yolov7_segmentation_deepsort/assets/98995391/7e7ad187-3dde-4f84-b75a-473766b05646)

This shows how much of the detection area is useless, and this will help with the IOU.
