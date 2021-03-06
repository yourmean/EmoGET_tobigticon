# 🙂Moving-Emoticon-Generation🤥 
[![Google drive](https://img.shields.io/badge/report-Link-orange)](https://drive.google.com/file/d/1PowTASaBUWvX2XWNrMg54-u1QjPwraMZ/view?usp=sharing)
[![notion](https://img.shields.io/badge/notion-Link-lightgrey)](https://www.notion.so/EmoGE-T-Tobigticon-c2336796af8e4029b252a3090548fd4a)

<p align="center"><img src="https://user-images.githubusercontent.com/55529646/105634653-7d9baf80-5ea2-11eb-9e62-8d035a163564.jpg"></p>
<br>

## Tobigticon - Create Your Own Moving Emoticons Based on Image2Video.

Tobigticon is a service that provides the production of your own moving emoticon using GAN based image2video method.  

Our model, learned by unsupervised manner, generates an emotional video of an image without _ground truth_ through network blending parmas and landmark generation.

EmoGE'T, which is derived from Emoticon GEnerated by Tobigs, is a team of 8 members of Tobigs who worked on an image2video based project.

Make your own moving emoticons with Tobigticons! \
Following the below options, the model creates your own animated emoticon.
<br>

**Select an Image Style**
| Animation  |  Baby | Painting  | 
|---|---|---|
|  <img src="images/anime.jpg" width="150" height="150"> |  <img src="images/baby.jpeg" width="150" height="150"> |  <img src="images/painting.jpeg" width="150" height="150"> | 


**Select an Emotion**
| Happiness  |  Disgusted | Surprised  | 
|---|---|---|
|  <img src="images/happy.png" width="150" height="150"> |  <img src="images/disgust.png" width="150" height="150"> |  <img src="images/surprise.png" width="150" height="150"> | 
<br>

## DEMO SCREENSHOT
<img src="https://user-images.githubusercontent.com/55529646/104742200-80552100-578d-11eb-9b2e-ab6464d9b285.jpg" width="850" height="850">  

You can see more information about web demo [here](https://github.com/yourmean/Moving-Emoji-Generation_Web). <br>


<br>

## Requirements

We have tested on:

- CUDA 11.0
- python 3.8.5
- pytorch 1.7.1
- numpy 1.19.2
- opencv-python  4.5.1
- dlib 19.21.1
- scikit-learn 0.24.0
- Pillow 8.1.0
- Ninja 1.10.0
- glob2 0.7

## Usage

### Generate your own Emoticon

You can generate your own moving emoticon :)
```
python emoticon_generate.py --file ImagePath --transform Animation --emotion Emotion --type OutputType
```

For example,
``` 
python emoticon_generate.py --file 00001.jpg --transform baby --emotion disgusted --type mp4 
```

### Training

Training the landmark generation model using the Sol1 approach.

``` 
python sol1/train.py --data_path DataPath --conditions Conditions
```

Train the video generation model using sol2 

```
# Train the model
python sol2/train.py --image_discriminator PatchImageDiscriminator --video_discriminator CategoricalVideoDiscriminator --dim_z_category 3 --video_length 16  
# Generate the video using the model
python sol2/generate_videos.py [model path] [image] [class] [save_path]
```


## Pretrained Checkpoints

[Animation](https://drive.google.com/file/d/1JO5-MJwjzrCYCVL-2StAKJbGy-VuwBSp/view?usp=sharing)
[Baby](https://drive.google.com/file/d/1Oplgd05plKLa76QzmFE8GsghpZOiMia-/view?usp=sharing)
[Painting](https://drive.google.com/file/d/1I0BpprKG3hXixQsnzOezTaG8SZr97OkB/view?usp=sharing)

## Samples
  
### Animation - Happy
|Blend style|Generate video|
|---|---|
|<img src="images/anime-happy.png" width="300" height="300">|<img src="https://github.com/minjung-s/Moving-Emoji-Generation/blob/main/images/anime-happy.gif" width="300" height="300">|  
  
###  Baby - Happy
|Blend style|Generate video|
|---|---|
|<img src="images/baby-happy.png" width="300" height="300">|<img src="https://github.com/minjung-s/Moving-Emoji-Generation/blob/main/images/baby-happy.gif" width="300" height="300">|  
  
### Painting - Happy  
|Blend style|Generate video|
|---|---|
|<img src="images/painting-happy.png" width="300" height="300">|<img src="https://github.com/minjung-s/Moving-Emoji-Generation/blob/main/images/painting-happy.gif" width="300" height="300">|   
  
### Animation - Surprise  
|Blend style|Generate video|
|---|---|
|<img src="images/anime-surprise.png" width="300" height="300">|<img src="https://github.com/minjung-s/Moving-Emoji-Generation/blob/main/images/anime-surprise.gif" width="300" height="300">|  
  
### Baby - Surprise
|Blend style|Generate video|
|---|---|
|<img src="images/baby-surprise.png" width="300" height="300">|<img src="https://github.com/minjung-s/Moving-Emoji-Generation/blob/main/images/baby-surprise.gif" width="300" height="300">|    

## Reference
- Rosinality, stylegan2-pytorch,  2019, [https://github.com/rosinality/stylegan2-pytorch](https://github.com/rosinality/stylegan2-pytorch)
- PieraRiccio, stylegan2-pytorch, 2019, [https://github.com/PieraRiccio/stylegan2-pytorch](https://github.com/PieraRiccio/stylegan2-pytorch)
- justinpinkney, toonify, 2020, [https://github.com/justinpinkney/toonify](https://github.com/justinpinkney/toonify)
- marsbroshok, face-replace, 2016, https://github.com/marsbroshok/face-replace
- sergeytulyakov, mocogan, 2017, https://github.com/sergeytulyakov/mocogan
- Yaohui Wang, Piotr Bilinski, Francois Bremond, Antitza Dantcheva. ImaGINator: Conditional Spatio-Temporal GAN for Video Generation. 2019.


## Contributor 🌟
<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->

<table>
  <tr>
    <td align="center"><a href="https://github.com/minjung-s"><img src="https://user-images.githubusercontent.com/41895063/104710310-45d68e80-5763-11eb-8bca-3d11bab3f636.png" width="150" height="150"><br /><sub><b>MinJung Shin</b></sub></td>
    <td align="center"><a href="https://github.com/simba-pumba"><img src="https://user-images.githubusercontent.com/41895063/104711155-576c6600-5764-11eb-8a1e-a7a011cfe17d.png" width="150" height="150"><br /><sub><b>YeJi Lee</b></sub></td>
    <td align="center"><a href="https://github.com/yourmean"><img src="https://user-images.githubusercontent.com/41895063/104711276-7cf96f80-5764-11eb-8473-99c5c0dc8a8a.png" width="150" height="150"><br /><sub><b>YuMin Lee</b></sub></td>
    <td align="center"><a href="https://github.com/lilly9117"><img src="https://user-images.githubusercontent.com/41895063/104711018-29872180-5764-11eb-9858-53c5f4cc26e4.png" width="150" height="150"><br /><sub><b>Hyebin Choi</b></sub></td>
  </tr>
</table>

<table>
  <tr>
    <td align="center"><a href="https://github.com/mink7878"><img src="https://user-images.githubusercontent.com/55529646/104719170-6a386800-576f-11eb-8b55-36b524c4d166.jpg" width="150" height="150"><br /><sub><b>MinKyeong Kim</b></sub></td>
    <td align="center"><a href="https://github.com/shkim960520"><img src="https://user-images.githubusercontent.com/55529646/104719176-6d335880-576f-11eb-849f-4d6756824d68.jpg" width="150" height="150"><br /><sub><b>SangHyeon Kim</b></sub></td>
    <td align="center"><a href="https://github.com/Jeong-JaeYoon"><img src="https://user-images.githubusercontent.com/55529646/104719173-6b699500-576f-11eb-9a42-a8569be057bc.jpg" width="150" height="150"><br /><sub><b>JaeYoon Jeong</b></sub></td>
    <td align="center"><a href="https://github.com/Yu-Jin22"><img src="https://user-images.githubusercontent.com/41895063/104711416-afa36800-5764-11eb-85c1-1a9ad50033b7.png" width="150" height="150"><br /><sub><b>YuJin Han</b></sub></td>
  </tr>
</table>
