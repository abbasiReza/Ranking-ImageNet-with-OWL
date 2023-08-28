# Ranking ImageNet with OWL and Mitigating Spurious Correlations

## Description

This project applies the OWL model to rank the ImageNet dataset. OWL helps mitigate spurious correlations during ranking without human supervision.

The confidence scores from OWL are used to rank the ImageNet images. The top and bottom ranked images are then used to fine-tune the model to be more robust to spurious correlations.


## Ranking ImageNet  

The OWL confidence scores are used to rank the ImageNet validation set from most to least prototypical examples.

Spurious correlations in the pretrained model likely result in errors in this ranking.

## Mitigating Spurious Correlations

The top and bottom 100 images according to the OWL ranking are used to fine-tune the last layer of the model. 

This makes the model more robust to spurious biases by providing challenging examples.

## Usage

The ranking and fine-tuning process could be used to clean an image dataset and improve model generalization. 

## References

- OWL Paper: https://arxiv.org/pdf/2205.06230
- ImageNet Dataset: https://image-net.org/
