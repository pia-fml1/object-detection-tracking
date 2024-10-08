# yolov7-object-tracking

### New Features
- Added Label for Every Track
- Code can run on Both (CPU & GPU)
- Video/WebCam/External Camera/IP Stream Supported
  
### Steps to run Code
- Goto the cloned folder.
```
cd yolov7-object-tracking
```
- Create a virtual envirnoment (Recommended, If you dont want to disturb python packages)
```
### For Linux Users
python3 -m venv yolov7objtracking
source yolov7objtracking/bin/activate

### For Window Users
python3 -m venv yolov7objtracking
cd yolov7objtracking
cd Scripts
activate
cd ..
cd ..
```
- Upgrade pip with mentioned command below.
```
pip install --upgrade pip
```
- Install requirements with mentioned command below.
```
pip install -r requirements.txt
```
- Run the code with mentioned command below (by default, pretrained [yolov7](https://github.com/WongKinYiu/yolov7/releases/download/v0.1/yolov7.pt) weights will be automatically downloaded into the working directory if they don't already exist).
```
# for detection only
python detect.py --weights yolov7.pt --source "your video.mp4"

#if you want to change source file
python detect_and_track.py --weights yolov7.pt --source "your video.mp4"

#for WebCam
python detect_and_track.py --weights yolov7.pt --source 0

#for External Camera
python detect_and_track.py --weights yolov7.pt --source 1

#for specific class (person)
python detect_and_track.py --weights yolov7.pt --source "your video.mp4" --classes 0

#for colored tracks 
python detect_and_track.py --weights yolov7.pt --source "your video.mp4" --colored-trk

#for saving tracks centroid, track id and bbox coordinates
python detect_and_track.py --weights yolov7.pt --source "your video.mp4" --save-txt --save-bbox-dim
```


- Output file will be created in the ```working-dir/runs/detect/obj-tracking``` with original filename


### Results
<table>
  <tr>
    <td>YOLOv7 Detection Only</td>
    <td>YOLOv7 Object Tracking with ID</td>
    <td>YOLOv7 Object Tracking with ID and Label </td>
  </tr>
  <tr>
    <td><img src="output/detection.png"></td>
    <td><img src="output/tracking.png"></td>
     <td><img src="output/tracking_label.png"></td>
  </tr>
 </table>

