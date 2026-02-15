# lab5_mlpr

In this lab, we implemented a distance-based learning approach using face detection and clustering. First, faces were detected from the image Plaksha_Faculty.jpg using OpenCV’s Haar Cascade classifier. The image was converted to grayscale for detection, and bounding boxes were drawn around all detected faces.

After detecting the faces, feature extraction was performed. The image was converted to HSV color space, and for each detected face, the mean Hue and mean Saturation values were calculated. These two values were used as numerical features to represent each face in a 2D feature space.

K-Means clustering with K = 2 was then applied on the extracted features. Since K-Means uses Euclidean distance internally, faces were grouped based on similarity in their color characteristics. The clustered faces were visualized on a scatter plot (Hue vs Saturation), with different colors(blue and green) representing different clusters. Cluster centroids were also plotted to show the center of each group by orange and red crosses.

In the next part, a template image (Dr_Shashi_Tharoor.jpg) was processed in the same way. Its mean Hue and Saturation were computed and passed to the trained K-Means model to predict its cluster label. The template point was then plotted on the same graph to visualize which cluster it belongs to.

From the results, it was observed that faces with similar color properties were grouped together effectively. This experiment demonstrated how feature extraction and distance-based clustering work in practice. It also reinforced concepts such as Euclidean distance, cluster centroids, and the importance of choosing meaningful features for classification.

