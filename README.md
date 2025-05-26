# YOLOv8 Object Detection Project — Pascal VOC

## 📂 Dataset Used

In this project, I used the Pascal VOC 2007 and 2012 datasets. These datasets have 20 types of objects like person, car, dog, bicycle, airplane, and more. I converted the original VOC annotations (XML files) into YOLO format (TXT files) using Python code. The training set includes both VOC 2007 and VOC 2012 train+val images. The test set comes from VOC 2007 test images.

## 🧠 Model and Backbone

For object detection, I used the YOLOv8 model. YOLO stands for “You Only Look Once” and it is fast and accurate. The model I used is called `yolov8m`, which is the medium version — it balances speed and accuracy well. The backbone of the model is CSPDarknet, which helps in learning features from the images.

## ⚙️ Training

I trained the model for 10 epochs. I used pre-trained weights from the COCO dataset to start with, so the model already had a basic idea of object features. Then, it fine-tuned on the Pascal VOC data. I set batch size to 16 and image size to 640.

## 📈 Evaluation

After training, I saved the best model as `best_yolov8m_voc_10e.pt`. I also tested the model on sample test images directly in the notebook to show how it works. The evaluation results are saved in the file called `Evaluation_Metrics.txt`, which includes precision, recall, mAP\@50, and mAP\@50-95.

## 🖼️ Inference

In the code, I included a small demo that randomly picks a few test images and shows the predictions. The predictions are drawn using bounding boxes with labels and confidence scores.

## 📁 Files Included

* `best_yolov8m_voc_10e.pt` — The trained model checkpoint
* `Evaluation_Metrics.txt` — The evaluation results after training
* Sample test images — used to show inference demo

This project shows how to prepare data, train a YOLO model, and evaluate it easily.
