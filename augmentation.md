
# Albumentation survey

This file include a list of useful component from Albumentation package which can be used for any augmentation. I suggest you to visit their link for more information:

* [Github page](https://github.com/albumentations-team/albumentations)
* [Online Demo](https://demo.albumentations.ai/)
* [Online Docs](https://albumentations.ai/docs/)
    
## Intallation
First install this package

```bash
pip install albumentations
```

## How To Define It?
import useful modules

```python
import albumentations as A
from albumentations.pytorch.transforms import ToTensorV2
```

I suggest you to use these augmentation for your dataset:

```python
augment = A.Compose([
      A.Resize(width=600, height=350),
      A.Affine(rotate=(-45, 45), scale=(0.8, 1.2), translate_percent=(0, 0.1), shear=(-20, 20), p=0.5),
      A.HorizontalFlip(p=0.1),
      A.VerticalFlip(p=0.1),
      A.CLAHE(clip_limit=2, p=0.5),
      A.PixelDropout(dropout_prob=0.05, p=0.3),
      A.RandomBrightnessContrast(brightness_limit=(-0.3, 0.3), contrast_limit=(-0.3, 0.3), p=0.5),
      A.GaussNoise(p=0.5),
      A.ColorJitter(brightness=(0.8, 1), contrast=(0.8, 1), saturation=(0.8, 1), hue=(-0.5, 0.5), p=0.2),
      A.Emboss(p=0.1),
      A.FancyPCA(p=0.1),
      A.ImageCompression(quality_lower=50, quality_upper=100,p=0.1),
      A.ISONoise(p=0.1),
      A.MultiplicativeNoise(p=0.1),
      A.RandomGamma(p=0.1),
      A.RandomToneCurve(p=0.1),
      A.RingingOvershoot(p=0.1),
      A.Sharpen(p=0.1),
      A.UnsharpMask(p=0.1),
      A.Normalize(mean=(0, 0, 0), std=(1, 1, 1), always_apply=True, p=1),
      ToTensorV2(),
])
```
**Note:** If you add **ToTensorV2()** It will be automatically converted to (channels, H, W) for pytorch usage.


## How To Use It?
you directly pass any **image**, **mask**, **box**, **keypoint** to the defined augmentation. like this for only image:

```python
augment(image=img)['image']
```

And for predefined datasets in pytorch use this:

```python
from torchvision import transforms
ImageFolder('data/train', transform=Transforms(augment))
```
