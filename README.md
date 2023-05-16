# YoloV5ImageDetection
## Using the best.pt Output of YOLOv5

In this section, we will guide you on how to use the best.pt output from the YOLOv5 model for object detection.
Prerequisites

Before starting, make sure you have the following:

 - Python 3.6 or later installed.
 - The YOLOv5 repository cloned: git clone https://github.com/ultralytics/yolov5.git
 - The necessary packages installed, you can do this by navigating to the YOLOv5 directory and running: pip install -r requirements.txt
 - A trained YOLOv5 model. After the training, you should have a file called best.pt which is the trained model weights.

### Step 1: Load the Trained Model

You can load the trained model with the following line of code:

      model = torch.hub.load('ultralytics/yolov5', 'custom', path='path/to/best.pt')

Replace 'path/to/best.pt' with the actual path to your best.pt file.

### Step 2: Load an Image for Detection

To load an image that you want to perform detection on, use the following code:

      img = 'path/to/image.jpg'  # replace with your image path

### Step 3: Perform Object Detection

You can now use the loaded model to perform detection on the image:

      results = model(img)

### Step 4: Display the Results

To display the detection results, use the results.show() function:

      results.show()

### Step 5: Get Detailed Results

If you want to get detailed results, such as the bounding box coordinates, detected class, and confidence, you can do this:

      results.print()  # print results to screen
      results.save()  # save as results1.jpg, results2.jpg... etc.

You can also access detailed results as follows:

      results.xyxy[0]  # tensor of xyxy coordinates for image 0
      
Just replace the paths with the actual paths to your best.pt file and the image you want to perform detection on.
