# opensw23-gaegury  
## 팀소개  
### 멤버구성  
---
- 최해원 202011906 발표자  
- 이승민 202013002 코더  
- 조용찬 202011374 코더  
- 천송현 201911219 조장  


## Topic Introduction  
---
- 이미지의 빠진 영역을 채우는 Image inpainting은 자연스러움이 중요시 되는 만큼, 그 방법들이 다양한 종류의 mask를 다루거나 빈 곳을 채울 수 있어야 한다.
  기존의 GAN기반 혹은 autoregressive 모델들은 mask의 분포에 대해서 학습을 진행해 그 다양한 종류에 대한 일반화가 거의 충족되지 않았다. 
  그러나 Repaint는 unconditional하게 학습된 기존 DDPM(Denoising, Diffusion Probabilistic Models)만을 활용하여 특정 mask에 의존하는 학습 없이도 다양하고 품질이 좋은 dl   미지를 생성해낸다. Repaint는 inpainting mask 자체를 학습하지 않아 2가지 이점을 갖는다.

  1. 신경망이 어떠한 mask에 대해서도 일반화가 가능하다.
  2. 강력한 DDPM 이미지 합성 prior가 있으므로 더 의미론적인 생성을 학습할 수 있게 한다.

  표준 DDPM 샘플링 방법이 종종 의미상 올바르지 않은 이미지를 생성하는 것을 보완하기 위해 resampling에 개선된 denoising 전략이 도입됐다. 비록 diffusion process가 느려    지는 단점이 있지만, forward와 backward를 동시에 진행하여 의미론적으로 맞는 이미지를 생성할 수 있게 된다.  
## Results  
---  
- Input Image  
  ![KakaoTalk_20230531_223008127](https://github.com/opensw23-gaegury/opensw23-gaegury/assets/90510391/1bde6a5e-0f68-419c-81ea-f2ddc7e00517)
  
- Results  
  ![KakaoTalk_20230531_222857692](https://github.com/opensw23-gaegury/opensw23-gaegury/assets/90510391/1d604b78-361b-48b9-ac1d-89907a761dbc)
  ![KakaoTalk_20230531_222857775](https://github.com/opensw23-gaegury/opensw23-gaegury/assets/90510391/5485a51f-9ccb-4cf2-a5fa-6110ec39beed)
  ![KakaoTalk_20230531_222857870](https://github.com/opensw23-gaegury/opensw23-gaegury/assets/90510391/7c0af7f8-737e-405a-8efe-26eb5e0ef826)
  ![KakaoTalk_20230531_222857952](https://github.com/opensw23-gaegury/opensw23-gaegury/assets/90510391/c9c6262e-6123-446d-b5b3-6932e955ae42)



## Analysis/Visualization    
---  
- this is Analysis  


## Installation  
---
- 설치 방법
```c
  git clone https://github.com/opensw23-gaegury/opensw23-gaegury
```
```c
  pip install numpy torch blobfile tqdm pyYaml pillow     
```
```c
  pip install --upgrade gdown && bash ./download.sh  
```

- 실행 방법   
```c
  python test.py --conf_path confs/face_example.yml  
```

- to get more pretrained model  
```c
https://openaipublic.blob.core.windows.net/diffusion/jul-2021/256x256_classifier.pt # Trained by OpenAI  
https://openaipublic.blob.core.windows.net/diffusion/jul-2021/256x256_diffusion.pt # Trained by OpenAI  
```

## Presentation  
---  
- this is presentation video link  
