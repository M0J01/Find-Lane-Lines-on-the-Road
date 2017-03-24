
**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report



### Reflection

###1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.


There are 8 major steps in our pipeline.

Step 1: Convert a given image to greyscale and perform a Gaussian Blur
Step 2: Perform Canny edge detection on our grescale with a 1:3 low:high threshold in order to detect rapid color change.
Step 3: Mask a region of interest on our edge detected image.
Step 4: Perform a Hough Transform on our masked image in order to identify regions of pixels in close proximity that are likely part of the same line.
Step 5: Sort those lines into Left and Right based on y1 vs y2 values.
Step 6: Identify the left and right lines with the longest line length and calculate the slope intercept of those lines.
Step 7: Calculate new X min/max values for our lines based on Y min/max values from our mask boundaries.
Step 8: Draw the left/right lines on a copy of our orriginal image.


Draw Lines was modified to:
    seperate lines into Left and Right based on values of y1 and y2
    find the slope intercepts of the left and right lines with the longest line length
    return those slope intercepts to Hough Lines


Hough Lines was modified to:
    Accept a returned value from Draw Lines and pass it back to the main pipeline


Convert Area was created to:
    find new values of X min/max based off of slope intercepts and a given Y min/max


###2. Identify potential shortcomings with your current pipeline

A divide by zero error was encountered when performing our pipeline on solidYellowLeft.mp4. This was due to having no likely candidates for our lane lines uncovered during our hough transform, which caused a null value to be passed as the slope to our convert area function. This error was averted by adding a negligable value (0.001) to our calculations that would prevent a divide by zero error. This however is a sloppy solution and non ideal as a permanent fix. A better fix would be to add an exception for null values, or trigger another instance of image analysis with slightly tweaked values.

Another shortcoming was discovered when performing our pipeline on challenge.mp4. The car hood and median were falsely identifed as lane lines due to the method of determining lane lines in our draw lines function. This is because the lines detected with the longest congruous line length were not always our lane lines. A method of elminating our hood-lane detection would be to implement constraints on aceptable slope values for our lane lines. This, however, might cause issues with our lane detection during turns and bends. A method of elminating our median-lane detection would be to identify long length lines which are closest to the center of our x axis. This, however, could cause issues when there are skid marks, oil stains, or other visual markings on the road. A final method to address both our hood and our median dilema would be to further constrain our area of interest. This solution would be ideal for our hood, as there is a known fixed area that it occupies on our image. This solution may be suitable for our curb as well, though, over constraining our area of interest might have unintended consequences, up to and including preventing our system from adapting in unusual situations.

###3. Suggest possible improvements to your pipeline

An improvement would be to calculate line slopes based off of an average of many images, instead of calculating and displaying lines for each image individually. This would greatly smooth out the estimated locations of the lane lines.

Another improvemnt would be to cut the video clips into smaller sections before writing to a file. This would decrease the chance of a memory error during write.

Another improvemnt would be to rewrite/tidy up the naming and usage of our functions. The draw line function was modified to perform most of the lane identification logic. This was mostly due to the code that was prewritten, and the simplicity of modifying that code to suite our particular purpose. Ideally, the code would be rewritten in a cleaner format with dedicated functions that are well named and not quite as deeply nested. This would greatly help future trouble shooting.