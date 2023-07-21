# Image Manipulation Tool - README

## Introduction

The Image Manipulation tool is a command-line application written in Java that processes and manipulates .ppm (Portable PixMap) images. It employs several classes and interfaces to provide a rich set of image manipulation features.



## Structure & Design

The project is organized into a handful of classes, each with a specific role:

- Pixel: This class represents a pixel in an image. Each pixel has red, green, and blue components.
- ImageManipulator: This is the core class that manages the images. It maintains a map of image names to images. It exposes methods to load, save, brighten, darken, and adjust different color components of images.
- ImageUtil: This class contains utility methods to read and write a PPM image from/to file. It also includes a method to copy an image.
- ImageUtil main method: This is the application's entry point and acts as a controller. It waits for the user's input, interprets it, and executes the corresponding commands.


## Prerequisites

- Java Runtime Environment (JRE)
- PPM image file (P3 format)


## Usage
Compiling:
```console
javac imageManipulation/*.java
```


## Commands
- 'load' <imagePath> <imageName>: Load an image from a file at <imagePath> and assigns it the name <imageName> for future reference.
- save <imageName> <destinationPath>: Save the image named <imageName> to a file at <destinationPath>.
- brighten <increment> <sourceImageName> <destinationImageName>: Brighten the image named <sourceImageName> by the amount <increment> and store the result as <destinationImageName>.
- darken <decrement> <sourceImageName> <destinationImageName>: Darken the image named <sourceImageName> by the amount <decrement> and store the result as <destinationImageName>.
- red-component <sourceImageName> <destinationImageName>: Extract the red component of the image named <sourceImageName> and store the result as <destinationImageName>.
- green-component <sourceImageName> <destinationImageName>: Extract the green component of the image named <sourceImageName> and store the result as <destinationImageName>.
- blue-component <sourceImageName> <destinationImageName>: Extract the blue component of the image named <sourceImageName> and store the result as <destinationImageName>.
- value-component <sourceImageName> <destinationImageName>: Extract the value (max of RGB components) of the image named <sourceImageName> and store the result as <destinationImageName>.
- intensity-component <sourceImageName> <destinationImageName>: Extract the intensity (average of RGB components) of the image named <sourceImageName> and store the result as <destinationImageName>.
- luma-component <sourceImageName> <destinationImageName>: Extract the luma (perceived brightness) of the image named <sourceImageName> and store the result as <destinationImageName>.
- quit: Exit the program.

## Running a Script of Commands


