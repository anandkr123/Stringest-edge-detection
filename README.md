# Strongest-edge-detection

After converting the image to a gray scale, We hardcoded the sobel matrix for X and Y direction, and
then applying the same kernel over the image ‘dew.jpg’ gave us two matrix Gx and Gy, which are
gradient in X and Y direction respectively. Then using quantile, we extracted 2 per cent strongest edges
in the image. We simple calculated the angle using ‘atan2’ over Gy/Gx which gives our result in the
interval [-pi,pi] . We converted it into degree and finally to a full 360 degree angle values by adding 180
degree to the negative degree values.


For marking the different edges of our image we simply created an RGB image of the same size as the
original image and then simply putting our image plane to each plane of our rgb image.

For marking the edges with different colors for different angle i.e. (Horizintal , vertical, and diagonal
edges )we iterated over the angle matrix and then assigned different color code to our strongest edges
image.
We tried at first without Gaussian smoothing.The resultant color coded image was quite full of noise and
the color edges marked were not smooth as compared when we applied Gaussian filtering .The results
as you can see after executing the code. The result image has very fine edges with using the Gaussian
filter.
![color_image](https://user-images.githubusercontent.com/23450113/50497144-84daff80-0a35-11e9-896c-cb61d93ba52a.jpg)
![stronges_color_edge_smoothed](https://user-images.githubusercontent.com/23450113/50497148-873d5980-0a35-11e9-9239-3ad18ed66610.jpg)
