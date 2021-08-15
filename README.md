# Handwritten_Word_Counter
## Inspiration
Counting out handwritten essays is time consuming. This interface and algorithm are aimed at helping students generate a word count of their handwritten work so that they can focus their efforts on more important things.
## How It Works
I used OpenCV-Python to create bounding boxes for individual words. I started by pixelating the image so that each word became a black blob on a white background. To highlight the contrast, I applied a binary threshold to turn the image black and white. Using that threshold, I applied an OpenCV contour to look for contiguous shapes (the blurry word blobs). I applied a standard deviation filter so that blobs that appeared too big weren't included (it had a tendency to see the entire block of text as one word sometimes). 
## Future Improvements
- distinguish line by line so that letters that hang down (j, g, q, p, etc.) don't get grouped in with the line below them
- create a lower bound filter so that punctuation or stray marks aren't counted as words
- (for largest piece of text) adjust for shadows on paper and imperfect cropping
- improve tkinter GUI so that word count displays as a label
