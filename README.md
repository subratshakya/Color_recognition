Color Detection Program
This program allows you to identify the name and RGB values of colors in an image by double-clicking on any pixel. It uses OpenCV to handle image processing and pandas to manage color data from a CSV file.

Prerequisites
Make sure you have the following libraries installed:

OpenCV
pandas
You can install these libraries using pip:


pip install opencv-python pandas


Usage
Prepare the Image: Ensure you have an image named colorpic.jpg in the same directory as the script. This image will be used for color detection.

Color Data CSV: Ensure you have a CSV file named colors (1).csv in the same directory as the script. This CSV should contain color names and their corresponding RGB values. The CSV should not have a header row, and columns should be ordered as: color, color_name, hex, R, G, B.

Run the Script: Execute the script using Python:

python color_detection.py


Interacting with the Program: Once the image is displayed, you can double-click on any pixel to see a rectangle filled with the detected color and text showing the color name and RGB values. If the color is too light, the text will be displayed in black for better readability.

Exit the Program: Press the Esc key to exit the program.

Code Explanation
Global Variables
clicked: A boolean indicating if the mouse was clicked.
r, g, b: Variables to store the red, green, and blue values of the pixel.
x_pos, y_pos: Variables to store the x and y coordinates of the mouse click.
Functions
get_color_name(R, G, B): This function calculates the minimum distance between the given RGB values and the colors in the CSV file to find the closest matching color name.

draw_function(event, x, y, flags, param): This function is called when a mouse event occurs. If a double-click is detected, it captures the RGB values of the clicked pixel and sets the clicked flag to True.

Main Loop
The main loop displays the image and waits for user interaction. When a double-click is detected, it draws a rectangle and displays the color name and RGB values on the image. The loop continues until the Esc key is pressed.

Dependencies
Ensure that you have the following files in the same directory as your script:

colorpic.jpg: The image file on which you want to perform color detection.
colors (1).csv: The CSV file containing the color data.
License
This project is licensed under the MIT License - see the LICENSE file for details.
