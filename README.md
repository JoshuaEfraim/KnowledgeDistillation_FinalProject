# Improving YOLO11n Model with knowledge Distillation approach

### Our code is based on the
[yolo_distillation GitHub repository](https://github.com/garlic-byte/yolov11_prune_distillation_v2), with modifications to match our project goals.


## Teacher and Student Model Comparison:

| Model | Params | 
|------|--------|
| YOLO11n (Student Model) | 2.6M | 
| YOLO11m (Teacher Model | 20M | 



## Model results after Distillation 
| Model | mAP@0.5 | Params | 
|------|---------|--------|
| YOLO11n (Student Model) | 0.778 | 2.6M | 
| Pruned and Fine-tuned Student Model | 0.807 | 2.2M | 
| Distilled Student Model with CWD| 0.825 | 2.4M | 
| Distilled Student Model with MGD| 0.826 | 2.4M | 

Our model was then integrated into a gradio python app, and can be accessed on this link:
[Fabric Defect Detector](http://13.60.184.181:7860/)

## To run this code, you can do these following:


## 1. Clone the GitHub Repository

First, clone this repository to your local machine:

```bash
git clone https://github.com/JoshuaEfraim/KnowledgeDistillation_FinalProject
cd KnowledgeDistillation_FinalProject
```

---

## 2. Install Dependencies

Make sure you are using a compatible Python version, then install all required dependencies:

```bash
pip install -r requirements.txt
```
---

## 3. We have 5 steps to run the training pipeline that have to be uncommented one by one in the 'train_yolov11.py'


Open the `train_yolov11.py` file.

* Locate the functions that are currently commented out.
* **Uncomment each function** that is required for training and experimentation.

This step is necessary to ensure all training stages are executed correctly.

---

## 4. Enable L1 Regularization in Ultralytics Trainer

For the second step of the setup, you must enable L1 regularization manually.

1. Navigate to the following path:

```
ultralytics/engine/trainer.py
```

2. Open `trainer.py` in a code editor.
3. Find the section related to **L1 regularization**.
4. **Uncomment the L1 regularization code block**.

This modification is required for the regularization experiments to take effect during training.

---

## 5. Run the Training Script

After completing all the steps above, run the training script:

```bash
python train_yolov11.py
```

---

## Notes

* Ensure all required files and datasets are correctly placed before running training.
* Any changes to Ultralytics core files should be done carefully, as they affect the training engine behavior.

---

