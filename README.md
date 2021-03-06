# Faces2Anime
## Cartoon Style Transfer in Faces using GANs
[paper](https://drive.google.com/file/d/1RDCE9Vh-qo_KDapTL2BGo61hYMvvtF1A/view?usp=sharing) | [video](https://youtu.be/Pm6jFcl_nxk) | [slides](https://drive.google.com/file/d/1alsyNJ1gT1JAXikqMwOybJaGUcXXpHsL/view?usp=sharing)

![./imgs/tx_interpolation.gif](./imgs/tx_interpolation.gif)
![./imgs/tx_interpolation.PNG](./imgs/tx_interpolation.PNG)
This project is aim to accomplish style transfer from human faces to anime / manga / cartoon styles.


## Results
### Trained styles
The styles used below are from our training dataset.

![./imgs/trained_style.PNG](./imgs/trained_style.PNG)

![./imgs/trained_style2.PNG](./imgs/trained_style2.PNG)


### Un-trained styles
The styles used below are randomly collected from the internet.

![./imgs/un-trained_style.PNG](./imgs/un-trained_style.PNG)

![./imgs/un-trained_style2.PNG](./imgs/un-trained_style2.PNG)


### Mean style transference
`Mean style` denotes the mean of all texture codes of our training styles.

![./imgs/mean_style_transfer.PNG](./imgs/mean_style_transfer.PNG)


### Texture interpolation
```
Tx rate = n
tx1 : tx2 = 1-n : n
```
![./imgs/tx_interpolation2.PNG](./imgs/tx_interpolation2.PNG)


### Structure interpolation
Unfortunately, our model fail to interpolate structures as it can only be applied to texture semantic style transfer.
```
Stu rate = n
stu1 : stu2 = 1-n : n
```
![./imgs/stu_interpolation.PNG](./imgs/stu_interpolation.PNG)

<br />

Results with removing backgrounds using [removebg](https://www.remove.bg/zh).

![./imgs/stu_interpolation2.PNG](./imgs/stu_interpolation2.PNG)


## Comparison
* **Compared methods**
    * U-GAT-IT [[paper]](https://arxiv.org/abs/1907.10830) [[web]](https://selfie2anime.com/) [[github]](https://github.com/taki0112/UGATIT)
    * Artbreeder [[web]](https://www.artbreeder.com/)
    * neural-style-tf [[github]](https://github.com/cysmith/neural-style-tf)
    * deepart io [[web]](https://deepart.io/)
    * Deep Image Analogy [[paper]](https://arxiv.org/abs/1705.01088) [[github]](https://github.com/msracver/Deep-Image-Analogy)
    * FaceBlit [[paper]](https://dcgi.fel.cvut.cz/home/sykorad/Texler21-I3D.pdf) [[github]](https://github.com/AnetaTexler/FaceBlit)
    * Adobe Characterizer [[web]](https://www.adobe.com/products/character-animator.html) [[video]](https://www.youtube.com/watch?v=z02AcZhxSfs)
    * original SwapAE [[paper]](https://arxiv.org/abs/2007.00653) [[github]](https://github.com/taesungp/swapping-autoencoder-pytorch)
    * WCT2 [[paper]](https://arxiv.org/abs/1903.09760) [[github]](https://github.com/clovaai/WCT2)

![./imgs/comparison1.PNG](./imgs/comparison1.PNG)

![./imgs/comparison2.PNG](./imgs/comparison2.PNG)

<br />

* **Lighting preservation**

![./imgs/comparison3.PNG](./imgs/comparison3.PNG)

## Further Transformation
### In-Domain GAN Inversion for Real Image Editing
Zhu et al. 2020. [[paper]](https://arxiv.org/abs/2004.00049) [[github]](https://github.com/genforce/idinvert)

![./imgs/further_in-domain.PNG](./imgs/further_in-domain.PNG)

### Toonify!
Justin Pinkney. 2020. [[web]](https://toonify.photos/)

![./imgs/further_toonify.PNG](./imgs/further_toonify.PNG)

## Datasets
:warning: **Warning:** All images are only used for research purpose. Prohibited for commercial use.

### Training data
* **Anime**
    * Images randomly collected from [WEBTOON](https://www.webtoons.com/zh-hant/). (Total: 22,741; Titles: 128)
    * Images generated from StyleGAN2 anime pre-train [model](https://www.gwern.net/Faces#stylegan-2). (Total: 300)
* **Human faces**
    * Images generated from StyleGAN2 FFHQ pre-train [model](https://github.com/NVlabs/stylegan2). (Total: 3,802)
    * Celebrity faces selected from the [CelebA](https://mmlab.ie.cuhk.edu.hk/projects/CelebA.html) dataset and randomly collected from the internet. (Total: 1,311)

### Testing data
* **Anime**
    * Images randomly collected from the internet. (Total: 170)
* **Human faces**
    * Images randomly collected from the internet. (Total: 17)
    * Images selected from the [FFHQ](https://github.com/NVlabs/ffhq-dataset) dataset. (Total: 63)


## Acknowledgement
* The related research papers:
    * _Swapping Autoencoder for Deep Image Manipulation_ [[paper]](https://arxiv.org/abs/2007.00653) [[github]](https://github.com/taesungp/swapping-autoencoder-pytorch)
    * _Learning to Cartoonize Using White-box Cartoon Representations_ [[paper]](https://github.com/SystemErrorWang/White-box-Cartoonization/blob/master/paper/06791.pdf) [[github]](https://github.com/SystemErrorWang/White-box-Cartoonization)
* Face cartoonization for pre-processing [here](https://github.com/SystemErrorWang/FacialCartoonization).
* The idea of this project is highly inspired from [naver-webtoon-faces](https://github.com/bryandlee/naver-webtoon-faces) by bryandlee.
* Our code implementation is based on [swapping-autoencoder-pytorch](https://github.com/rosinality/swapping-autoencoder-pytorch) by rosinality.


## BibTeX Citation
If you find this work useful for your research, please cite:
* [NDLTD in Taiwan](https://hdl.handle.net/11296/j8jm9n)
* [NTUST ETD](http://etheses.lib.ntust.edu.tw/cgi-bin/gs32/gsweb.cgi?o=dstdcdr&s=id=%22G0M10815032%22.&searchmode=basic)

\< English version \>
```
@mastersthesis{huang2021cartoon,
  author={Cheryl Huang},
  title={Cartoon Style Transfer in Faces using Generative Adversarial Networks},
  school={National Taiwan University of Science and Technology},
  year={2021},
  note={\url{https://hdl.handle.net/11296/j8jm9n}}
}
```

\< Chinese version \>
```
@mastersthesis{huang2021cartoon,
  author={?????????},
  title={???????????????????????????????????????????????????},
  school={?????????????????????????????????????????????},
  year={2021},
  note={\url{https://hdl.handle.net/11296/j8jm9n}}
}
```


## License

[![./imgs/Logo-NTUST.png](./imgs/Logo-NTUST.png)](https://www.ntust.edu.tw/home.php)  [![./imgs/Logo-GAMELab.png](./imgs/Logo-GAMELab.png)](http://gamelab.csie.ntust.edu.tw/)

Copyright &copy; 2021 Cheryl Huang. All rights reserved.