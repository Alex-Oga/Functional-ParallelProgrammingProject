# 2023-t1-finalproject-alexander
2023-t1-finalproject-alexander created by GitHub Classroom

Project:
Python Program that is able to process multiple manipulated images and outputs the original image without any manipulation.

Measure of Success:
Difference in runtime.

Simple way of making the program is using multiple for loops to run through every pixel, take the most occuring pixel and insert it into a new image.
The running time of the program therefore depends on the number of images and the size of the image.

Structure:
  For Loop (X)
    For Loop (Y)
      Comparison
    Pixel Change

Using range is alot faster than it is to go into the array's themselves and then slice them in half repeatedly.
I got down to each pixel and added them to an updating dict, that added unseen pixels or updated seen ones to help decrease runtime,
which then got the most occuring pixel of the dict to update the an image which would then be returned as the original unedited one.

In order to bring the idea of Concurrency/Parallelism. I decided to use Futures.
I implemented futures in multiple ways.
The first was to run use it on X.
The second was to use it on Y.
The third was to use it on Comparison.
Through running the code, it shows that the further down the loop futures is implemented, the worse the performance gets. The overhead affecting the performance too much.
But if I used it on X, then it was able to have similar or better performance than the simple implementation of the code did.

During testing, I had added multiple sets of images in order to test out the different running times of differing image sizes and number of images.
Showing that the smaller the image and the less images to compare, the closer the performance of using futures and not using futures was.
