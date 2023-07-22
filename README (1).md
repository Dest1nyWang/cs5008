# Image Manipulation Tool - README

## Introduction

The Image Manipulation tool is a command-line application written in Java that processes and manipulates .ppm (Portable PixMap) images.



## Structure & Design

The project is organized into a handful of classes, each with a specific role:

- `Pixel`: This class represents a pixel in an image. Each pixel has red, green, and blue components.
- `ImageManipulator`: This is the core class that manages the images. It maintains a map of image names to images. It exposes methods to load, save, brighten, darken, and adjust different color components of images.
- `ImageUtil`: This class contains utility methods to read and write a PPM image from/to file. It also includes a method to copy an image.
- `ImageUtil` main method: This is the application's entry point and acts as a controller. It waits for the user's input, interprets it, and executes the corresponding commands.




## Prerequisites

- Java Runtime Environment (JRE)
- PPM image file (P3 format)




## Usage
Navigate to the directory containing the compiled Java classes and then compiling.
Compiling:
```terminal
javac imageManipulation/*.java
```
After compiling,start the program with the following command:
```terminal
java imageManipulation.ImageUtil
```
Upon starting, you'll see a command prompt ">". You can enter commands there.




## Commands
- `load <imagePath> <imageName>`: Load an image from a file at `<imagePath>` and assigns it the name `<imageName>` for future reference.
- `save <imageName> <destinationPath>`: Save the image named `<imageName>` to a file at `<destinationPath>`.
- `brighten <increment> <sourceImageName> <destinationImageName>`: Brighten the image named `<sourceImageName>` by the amount `<increment>` and store the result as `<destinationImageName>`.
- `darken <decrement> <sourceImageName> <destinationImageName>`: Darken the image named `<sourceImageName>` by the amount `<decrement>` and store the result as `<destinationImageName>`.
- `red-component <sourceImageName> <destinationImageName>`: Extract the red component of the image named `<sourceImageName>` and store the result as `<destinationImageName>`.
- `green-component <sourceImageName> <destinationImageName>`: Extract the green component of the image named `<sourceImageName>` and store the result as `<destinationImageName>`.
- `blue-component <sourceImageName> <destinationImageName>`: Extract the blue component of the image named `<sourceImageName>` and store the result as `<destinationImageName>`.
- `value-component <sourceImageName> <destinationImageName>`: Extract the value (max of RGB components) of the image named `<sourceImageName>` and store the result as `<destinationImageName>`.
- `intensity-component <sourceImageName> <destinationImageName>`: Extract the intensity (average of RGB components) of the image named `<sourceImageName>` and store the result as `<destinationImageName>`.
- `luma-component <sourceImageName> <destinationImageName>`: Extract the luma (perceived brightness) of the image named `<sourceImageName>` and store the result as `<destinationImageName>`.
- `quit`: Exit the program.



## Script Runner
While you can type any command manualy, you also can prepare a script file with all commands and use a pipe to feed these commands into the program. Each command should be on a new line. Here's an example script:
```termnial
load /Users/user/Desktop/image.ppm blackbuck
brighten 50 blackbuck blackbuck_brightened
save blackbuck_brightened /Users/user/Desktop/blackbuck_brightened_50.ppm
quit
```
You can save these commands in a text file (commands.txt). Now, you can run this script using the following command:
```terminal
cat commands.txt | java imageManipulation.ImageUtil
```


## Error Handling
If there's an error while executing a command, the program will print an error message detailing what went wrong.For example, if you tried to load a file that doesn't exist or isn't a valid P3 PPM file, the program would let you see an error message detailing what went wrong.

Remember, if you want to manipulate an image, the first step is always to load a P3 PPM file with correct path into the program using the `load` command.

## Exiting the program
If you want to exit the program, you can simply enter `quit` at the command prompt or include `quit` at the end of your script.

## Image Citation
- Image: bc-flowers.ppm. (2016). Retrieved from [https://cs.berea.edu//courses/csc226/tasks/L3.ppm.html](https://cs.berea.edu//courses/csc226/tasks/L3.ppm.html) Accessed on July 19, 2023.
- [bc-flowers.ppm](https://cs.berea.edu//courses/csc226/tasks/bc-flowers.ppm)
- Image: blackbuck.ascii.ppm. (2011). Retrieved from https://people.sc.fsu.edu/~jburkardt/data/ppma/ppma.html Accessed on July 19, 2023.

