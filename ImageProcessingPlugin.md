# Introduction #

The image processing pipeline plug-in for imageViewer provides a graphical user interface-based method to interact with a collection of algorithms that have been released [individually here](http://code.google.com/p/cdsc-image-processing-pipeline/wiki/IndividualAlgorithms).

For the initial release, we have pre-integrated the plugin to a modified version of the imageViewer distributable. In subsequent releases, we will make the plugin available separately with instructions on how to install the plugin with the latest version of the imageViewer application available [here](http://code.google.com/p/cdsc-image-processing-pipeline/wiki/ImageViewer).

The following algorithms have been included as part of the image processing plugin:
  * Rician denoising
  * Rician deblurring
  * Fluid registration

# Download #

A version of imageViewer with the plugin already integrated can be downloaded by **[clicking here](http://cdsc-image-processing-pipeline.googlecode.com/files/imageviewer-v2.1-w-pipeline.zip)**.

# Instructions #

## Pre-compilation Steps ##
To compile the pipeline for your specific platform (Windows, Linux), you need the following tools:
  * Apache ant
  * make
  * gcc
  * g++

And external libraries:
  * [fftw3](http://www.fftw.org/) - Follow the instructions to unzip, configure, and compile these libraries for your specific platform

You will need to set your `JAVA_HOME` variable to where your Java Virtual Machine base directory is.

NOTE: If you wish to statically link the external library code into the final .dll or .so file for the pipeline, use the flag `-Wl,-Bstatic,-l<libname>,-Bdynamic` instead of just `-l<libname>`.  Specify this flag as part of LDFLAGS in the Makefiles, and not CFLAGS or CXXFLAGS.  This is because there is a gotcha for gcc and g++: their arguments are position dependent.  LDFLAGS is dereferenced in the correct position in the call to gcc and g++, as these linker flags should come last.

## Compile Code ##
  1. cd to the project directory, where the build file `build.xml` resides
  1. execute `ant clean` to build from scratch, starting from a clean slate
  1. execute `ant` to build the sequential version of the pipeline.

## Execute Code ##
In the command line prompt, execute `java -Djava.library.path=<system library path in case pipeline object needs to load external libraries>:build/imageviewer/src/imageviewer/tools/plugins/cdsc/native -classpath build/imageviewer/imageviewer.jar imageviewer.system.ImageViewerClient`

# Running the Plugin #
Once you have compiled the pipeline code and started imageViewer, you can pull up the plugin graphical user interface by going to Tools, Plugins, and select CDSC Imaging Pipeline.