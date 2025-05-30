# barcode-reader
This is an implementation of the algorithm described in the paper "Robust Recognition of 1-D Barcodes Using Camera Phones Steffen Wachenfeld, Sebastian Terlunen, Xiaoyi Jiang Computer Vision and Pattern Recognition Group, Department of Computer Science, University of Munster, Germany"

This uses opencv libraries for the initial processing of the input jpg files. Please note that the sample jpeg images have been cropped.

To compile, you will have to include opencv c++ libraries. 

zypper install -y gcc-c++ make cmake gdb opencv opencv-devel&& \
zypper clean -a

to compile
g++ -g main.cpp \
    -o main \
    `pkg-config --cflags --libs opencv4` \
    -lpthread

to run

./main barcode1_mbdb.jpg true

the first parameter is the file path of the jpeg image and the second parameter turns debug output on or off

Ten sample images have been uploaded, of which all are correctly read.
