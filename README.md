# Matilda - AI Conversion : 2D to 3D
<b> Matilda can produce 3d object by only one image !! </b>

![](./image/conversion_ex.png)
![](./image/conversion_ex_shirts.png)

#### pants
![](./image/pants.gif)

#### shirts
![](./image/shirts.gif)

#### ring
![](./image/ring.gif)

#### hat
![](./image/hat.gif)

#### dress
![](./image/dress.gif)
***
<br>
we provice categories 

+ TOP : shirts
+ BTM : pants
+ RIN : ring
+ DR : dress
+ HEA : hat

to be added later
+ BRA : bracelet
+ NEC : neckless
+ BAG : bag
+ MAS : mask

## Required libraries
+ pip install -r requirements.txt 
+ in requirements.txt, you can look these libraries 

```
Python 3.7
fastapi 
uvicorn[standard] 
ipdb
trimesh
numpy
torch==1.7.1
torchvision==0.8.2
torchaudio==0.7.2
requests
scikit-image
matplotlib
cython==0.29.20
usd-core==22.3
aspose-3d
opencv-python
python-multipart
jwt
PyJWT
httpx
```


## Required Files
```
├─mask
│  └─DIS
│      └─saved_models
│         {category}.pth
│         - {category} 에는 각 카테고리에 맞는 이름 삽입
│         - ex) 반지 - ring.pth
│         - 각 pth 파일은 google drive에서 얻을 수 있음 
└─predictor
   └─network
      └─models
          isnet.pth
          - google drive 또는 DIS 사이트에서 얻을 수 있음 
```

## Training
+ process
![](./image/train.png)
+ codes and files
    + https://drive.google.com/drive/folders/1b2MMi2FvCjzxXPUgwnFJ0iK3rdLqGHio


## Please Clone Extra Loss Function 
git clone https://github.com/shubhtuls/PerceptualSimilarity.git 

in PerceptualSimilarity.util.util, change code
```
from skimage.measure import compare_ssim
```
to
```
from skimage.metrics import structural_similarity as compare_ssim
```

