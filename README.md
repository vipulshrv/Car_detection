# Car_detection

Problem Statement- We need to find the presence and location of cars in an image and produce bounding boxes over the cars.

YOLO-
For completing this project we will be using You Only Look Once algorithm which currently is the most popular algorithm because of it's capability to run in real time.
It is much faster as it requires only one forward pass to detect and locate the objects present in the image.

Steps used in the project :

1) preprocess_image: Converts the image into the shape which could be fed into the neural network.
2) YOLO model: Downloaded the pretrained weights of a pretrained YOLOv2 model and results a (19,19,5,85) dimension output.
3) yolo_filter_boxes: throw away boxes that have detected a class with a score less than the threshold
4) Non-max suppression: Compute the Intersection over Union and avoid selecting overlapping boxes
5) yolo_eval: Gives the final prediction of the location of objects after non-max supression
6) scale_boxes:Scales the predicted boxes in order to be drawable on the image
7) draw_boxes: Draws boxes over input images to detect objects and gives an image as the final output.
