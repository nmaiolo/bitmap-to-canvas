# PGM Render in Browser

This project contains an PGM ASCII file. PGM is a file format that stands for "Portable Gray Map"; it contains a 2D grayscale image written in plain text. You can open and edit the file in a text editor.

The header of a PGM image has the following fields:

 - *Magic Number*: This tells what format the image data will be in. The magic number P2 means a gray-tone image in ASCII format. P4 means a gray-tone image in binary (internal machine) format. P3 means a color image in ASCII format, etc. Color images are called PPM and have 3 values (red, green, blue) per pixel.
 - *Comment*: Beginning with a #, this is a text field to contain information about the image, such as "CT scan of Jack's abdomen, slice 5".
 - *Number of Columns*: An integer indicating the number of columns in the image array.
 - *Number of Rows*: An integer indicating the number of rows in the image array.
 - *Maximum Value*: An integer indicating the maximum value of a pixel in the given image.

The remainder of the file is gray values, each in ASCII decimal, between 0 and the specified maximum value, separated by whitespace, starting at the top-left corner of the graymap, proceeding in normal English reading order. A value of 0 means black, and the maximum value means white.

Edit the included `index.html` so that it loads the included PGM file (with `fetch`) and renders the image in the browser window (using `<canvas>` and `ImageData`).
