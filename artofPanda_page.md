[Back to Home Page](../index.md)

## Photo Mosaic - Art of Panda

**Project PPT:**
[Art of Panda PowerPoint](/pdf/artofPanda.pdf)

**Project Video link:** [Art of Panda Video](https://www.canva.com/design/DAFTExZ_91c/OJWxk7Bs6SC5zPDljDYXcA/view?utm_content=DAFTExZ_91c&utm_campaign=designshare&utm_medium=link&utm_source=recording_view)

<img src="images/artofPanda_1.png" width="600" height="410"/>

<img src="images/artofPanda_2.png" width="600" height="410"/>

<img src="images/artofPanda_3.png" width="600" height="410"/>

**Project description:**

The goal of the Photo Mosaic project is to automatically create a photo mosaic using a given photo and build an image library using Google's stable diffusion model v1.5. The project utilizes Python and MATLAB as the tech stack.

**The project involves the following steps:**

### Image Preparation:

The base image is divided into thousands of grids.

### Stable Diffusion Model:

A prompt message is generated, such as "Panda by (a famous artist)," and the user inputs the artist name. The stable diffusion model is then used to generate an image library based on the prompt message.

### Photo Mosaic Algorithm Implementation:

The photo mosaic algorithm is implemented in MATLAB. The average RGB value of each grid in the base image is calculated, and the algorithm searches for the closest RGB value from the image library. The grid in the base image is replaced with one of the closest tile images randomly selected to avoid repetitions.

### Saving Average RGB Values:

The average RGB values of all 5,000 tile images are saved. To improve efficiency, a KD tree data structure is used instead of an array to store the average color for each tile. This reduces the time complexity of searching for the closest image from O(n) to O(log(n)).

### Finding the Closest Image and Drawing Tiles:

Euclidean distance is used as a similarity metric to measure the distance between the average RGB value of a grid and a tile image. The K-nearest neighbors (KNN) search is performed to find the top 3 closest tile images. A random number is generated using the 'randi' function, and this random number is used as an index to select one tile image from the top 3 results, reducing repetition.

### Conclusion:

By implementing these steps, the Photo Mosaic project achieves the goal of automatically creating a photo mosaic using a given photo and an image library generated with the stable diffusion model. The project overcomes the challenge of time complexity by using a KD tree for efficient searching, making it feasible to generate a photo mosaic even with a large number of grids and tile images.
