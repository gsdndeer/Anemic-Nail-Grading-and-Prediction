# Anemic-Nail-Grading-and-Prediction
Now, hemoglobin values are usually obtained by drawing blood. But it's time-comsuing. I evaluated hemoglobin values directly from nail images in this repository.



## I. Grading


```
Grade
x >= 8 	        => 1
11 >= x > 8    	=> 2
x > 11 	        => 3
```

I used classification to grade nail images.

| Model number | Backbone | Image size | Optimizer | Learning rate | Criterion | Vadlidation accuracy |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| 1 | EffcientNet-b7 | 512x386 | Adam | CEL | 0.001 | 0.89 |
| 2 | EffcientNet-b7 |512x386 | Ranger | CEL | 0.001 | 0.87 |
| 3 | EffcientNet-b7 |512x386 | SGD | CEL | 0.001 | 0.83 |


## II. Prediction


| Model number | Backbone | Image size | Optimizer | Learning rate | Criterion | Vadlidation accuracy |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| 1 | EffcientNet-b2 | 512x386 | Adam | 0.001 | MSE | 0.90 |
| 2 | EffcientNet-b7 |512x386 | Adam | MSE | 0.001 | 0.92 |
| 3 | EffcientNet-b7 |512x386 | Ranger | MSE | 0.001 | 0.91 |


## Acknowledgement
1. [EfficientNet PyTorch](https://github.com/lukemelas/EfficientNet-PyTorch)
