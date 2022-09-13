# yolov5 detecting hurricane with Roboflow

### Steps to run Code
- Clone the repository.
```
!git clone https://github.com/ultralytics/yolov5  # clone repo
!pip install -U -r yolov5/requirements.txt  # install dependencies
```
- Using roboflow we will have the trained hurricane satellite image dataset
```
!curl -L 'https://app.roboflow.com/ds/JpqswqCz0F?key=xnwE41SEnv' > roboflow.zip; unzip roboflow.zip; rm roboflow.zip
```
- Upgrade pip with mentioned command below.
```
pip install --upgrade pip
```
- Install requirements with mentioned command below.
```
pip install -r requirements.txt
```
- Training the dataset
```
!python /content/yolov5/train.py --img 640 --batch 10 --epochs 20 --data data.yaml --weights yolov5s.pt --nosave --cache
```
- if you want to make for a video of youtube
```
!python /content/yolov5/ob_detect.py --weights /content/yolov5/runs/train/exp10/weights/best.pt --img 640 --conf 0.25 --source 'YOUR LINK HERE'
```
- for image
```
!python /content/yolov5/detect.py --weights /content/yolov5/runs/train/exp10/weights/best.pt --img 640 --conf 0.25 --source
```
- Output file will be created in the <b>working-dir/runs/detect/exp</b> with original filename.

### Results
<table>
  <tr>
    <td>Hurricane A</td>
    <td>Hurricane B</td>
  </tr>
  <tr>
    <td><img src="https://github.com/leticiastachelski/yolov5/blob/master/Detecting%20motion/Captura%20de%20tela%20de%202022-09-13%2003-13-59.png)"></td>
    <td><img src="https://github.com/leticiastachelski/yolov5/blob/master/Detecting%20motion/Captura%20de%20tela%20de%202022-09-13%2003-14-18.png"></td>
  </tr>
 </table>
 
 
