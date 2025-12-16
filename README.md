```markdown
# Improving YOLO11n Model with knowledge Distillation approach

### Our code is based on [yolo_distillation](https://github.com/username/repository) Github Repository with some modification to match with our project goals.


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

Our model was then integrated into a gradio python app, and can be accessed on this link: [Fabric defect detector](http://13.60.184.181:7860/)
