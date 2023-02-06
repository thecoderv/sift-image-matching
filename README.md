# sift-image-matching
Feature extraction using SIFT and image matching

Scale-Invariant Feature Transform (SIFT) is a feature extraction method in image classification tasks. It is invariant to the scale and orientation of images and robust to illumination fluctuations, noise, partial occlusion, and minor viewpoint changes in the images. These characteristics are important in this project where we are trying to extract features and find the similarity between the images of the monuments which are taken from different distances, angles, lighting and other conditions 

Dataset used contains images of monuments in India belonging to 24 different classes:
https://www.kaggle.com/datasets/danushkumarv/indian-monuments-image-dataset

In this project, I used the distance ratio of 0.8 and reject all matches in which the distance ratio is greater than this ratio.

 Successful matches
 
![image](https://user-images.githubusercontent.com/121651746/217098353-9fa7b94b-f6a5-487e-a7d0-5c296c0723ab.png)
![image](https://user-images.githubusercontent.com/121651746/217098418-ea288c78-84aa-4966-b0fc-d5b522288b19.png)
![image](https://user-images.githubusercontent.com/121651746/217098506-05750bd7-fa21-47c0-9dc3-8f5b0f797ffc.png)

Successful mismatches

![image](https://user-images.githubusercontent.com/121651746/217098612-15bbcafa-0bfe-4b1d-a189-aec3e343e363.png)
![image](https://user-images.githubusercontent.com/121651746/217098664-55aa9c36-771e-46a9-af38-42e779004623.png)
![image](https://user-images.githubusercontent.com/121651746/217098704-1ab4de24-af12-44bb-8c4d-4960bbfff0e5.png)

Unsuccessful matches

![image](https://user-images.githubusercontent.com/121651746/217098773-f3684a9b-7cce-4b2c-8764-34d1ede173d3.png)

Unsuccessful mismatches

![image](https://user-images.githubusercontent.com/121651746/217098818-a59df7c8-5d1d-43fa-b174-3932dd4fdaa3.png)

Conclusion

In conclusion, the SIFT feature extraction algorithm was highly accurate in detecting the
keypoints and descriptors which we later used for keypoint matching. It didn’t matter if the
image was rotated at a weird angle or zoomed in to show only half of the monument.
A set of two images was taken in each trial of either the same or different monument. We
displayed their keypoints, matches, score and also whether they are the images of the same or
different monument.
The unsuccessful matches occurred when there was a big difference in the lighting(day/night),
excessive noise and when the image was taken at a different location of the monument.
The unsuccessful mismatches occurred when there were a large number of similar structures in
both the images and the score was just slightly over 1.

References and Citations

[1] https://www.cs.ubc.ca/~lowe/papers/ijcv04.pdf
[2] https://docs.opencv.org/4.x/da/df5/tutorial_py_sift_intro.html
[3] https://blog.francium.tech/feature-detection-and-matching-with-opencv-5fd2394a590
[4] https://docs.opencv.org/4.x/dc/dc3/tutorial_py_matcher.html
[5] https://www.udemy.com/course/mastering-computer-vision-theory-projects-in-python/
[6] https://docs.opencv.org/3.4/d7/d60/classcv_1_1SIFT.html
[7] https://medium.com/data-breach/introduction-to-sift-scale-invariant-feature-transform-65d7f3a72d40
[8] http://weitz.de/sift/index.html?size=large
