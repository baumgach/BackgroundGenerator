## BackgroundGenerator

Simple project for fetching and preprocessing batch data in a background thread while the 
main program does computations on the batches. 

This is intended mainly for deep learning models where speed improvements can be gained by 
parellelizing the batch preprocessing/disk read operations and the heavy GPU computations. 
 
The code is very slightly adapted from this stackoverlow [answer](https://stackoverflow.com/questions/7323664/python-generator-pre-fetch]) 
by Winston Ewert. I simply put it into a project and made it compatible with Python 3 and added 
 a working example. 
 
### Open Issues

 * If an exception happens inside BackgroundGenerator wrapped loop it will not get caught. Instead
 the loop will continue infinitely, which is hard to debug. 
 
 