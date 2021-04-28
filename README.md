# NumberPlateRecognition
To download classes.txt, yolov3-testing.cfg and yolov3-train_final.weights go to https://github.com/TheLostBoi/NumberPlateRecognition
These are very essential to run the source code.
#Evnvironment 
-Jupyter Notebook Python 3 
Libraries used 
-Make sure to pip install the following files 
    -pip install numpy 
    -pip install matplotlib
    -pip install colorthief

Instructions to run the the file : 
In order to execute the code : 
You will have to create a project folder which should contain 
  -classes.txt
  -yolov3-testing.cfg
  -yolov3-train_final.weights
  -NumberPlateDetection.ipynb
  -sample-confidential(Folder with all images)
 
 Step 1 - Make sure all these files are present in the project folder.
 Step 2 - Create 2 empty folders called "BoundedBoxOutput" and "NumberPlateCropped"
          -The "BoundedBoxOutput" folder will be used to store the images after drawing the rectangle around the number plate.
          -The "NumberPlateCropped" folder will store the cropped bounded box with number plates, which is necessary 
            for the 2nd part of the program.
 Step 3 - Open this project folder in jupyter notebook.
 Step 4 - Run the first cell with the program.This part of the program will identify the number plate for each image in 'sample-confidential'
          folder and draw a bounnding box around the number plates.
          This bounding boxes with the number plates are then cropped and stored in another folder that we created called "NumberPlateCropped".
          We are saving thesecropped image so that we can count the number of yellow pages. 
 Step 5 - Run the 2nd cell, This has a method definition to convert Rgb to hsv. first we use color thief and fins the dominant color in the cropped number plates, 
          then we convert this rgb value to hsv and then use the upper and lower limit of yellow hsv to find all the yellow number plates and count them.
          Although this is not that accurate and misses some of the yellow number plates , It works for the real yellow ones , if i could find a better way to detect yellow
          it would be more efficient.
Step 6 - The count is then given as output in the jupyter notebook.


 
