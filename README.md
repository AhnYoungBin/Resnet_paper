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
>Residual Block   
    
<img src="/image/2.JPG" width="80%" height="80%" title="img1" alt="img1"></img>   

ResNet의 핵심은 Residual Block이라고 생각한다. 그림 왼쪽 방식은 입력 x를 y에 매핑하는 H(x)를 얻는 것이 목적으로 하는 plane network의 direct mapping을 의미한다.     
하지만 그림 우측의 Residual Block은 입력 x와 H(x)의 차이를 0에 수렴하게 되어 입력과 출력이 같아지도록 하는 것을 목적으로 한다. F(x)를 입력 x와 출력 H(x)의 잔차(Residual)라고 가정하면 F(x)= H(x)-x 라고 표현할 수 있다. 식을 재정의하면 H(x) = F(x)+x 으로 만들어 그림과 같은 형식의 구조를 만들 수 있다. 입력 x가 y에 매핑하는 것보다 shortcut 형식의 입력 x가 0에 매핑하도록 하면 연산량의 증가없이 입력 x의 작은 움직임도 쉽게 검출 할 수있다. 또한 레이어를 건너 뛰며 입력과 출력이 연결되어 순전파와 역전파 연산 또한 단순해져서 깊은 망도 최적화 할 수 있게 되며 깊은 망으로 인한 정확도도 개선되는 효과를 얻는다. 이와같이 잔차(Residual)를 0에 수렴하게 학습 하는 network라고 하여 Resnet이라고 표현하게 된다.
 
 
Bottle neck
------------

<img src="/image/4.JPG" width="80%" height="80%" title="img1" alt="img1"></img>   
