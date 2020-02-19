Deep Residual Learning for Image Recognition
============================================

논문 링크 : <https://arxiv.org/pdf/1611.05431.pdf>

Introduce
---------
VGGnet 이후 망이 깊어 질수록 성능이 올라간다고 하지만 layer가 일정 수 이상 많아져 인공신경망이 깊어지면 Gradient Vanishing/Exploding 문제로 학습 장애가 온다.   
> plane network 20-layer와 56-layer의 train error와 test error   

<img src="/image/1.JPG" width="80%" height="80%" title="img1" alt="img1"></img>   

그래서 더 깊은 레이어까지 잘 학습이 되도록하는 방법을 Kaming he가 shorcut(Skip) connection을 고안했습니다.   

Related work
------------

<img src="/image/2.JPG" width="80%" height="80%" title="img1" alt="img1"></img>   

