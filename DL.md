## 1. CNN에 대해 설명해 보세요.  

**CNN**은 입력 이미지에서 feature를 자동으로 추출하여, 이미지 분류를 하는 신경망 구조입니다.  
주요 구성 요소는 convolutional layer, pooling layer, fully connected layer가 있습니다.  
**Convolutional layer**는 입력 이미지와 필터를 합성곱하여 feature를 추출합니다.  
**Pooling layer**는 feature map의 차원을 축소하여, 계산량을 줄이는 동시에, 중요한 feature 정보는 유지합니다.  
**Fully connected layer**는 추출된 feature를 바탕으로, 최종 이미지 분류를 수행합니다.  

<br><br>

## 2. 순환 신경망(RNN)의 개념과 장단점에 대해 설명해 보세요.  

**RNN**은 순차적인 데이터를 처리할 수 있는 신경망입니다.  
RNN은 이전 시점의 상태와 현재 시점의 입력을 이용해 출력을 생성합니다.  
장점으로는 시퀀스 데이터의 시간적 의존성을 모델링할 수 있다는 것이고,  
단점으로는 시퀀스가 길어지면, gradient vanishing 문제가 발생해, 초기 정보가 점점 사라질 수 있다는 점이 있습니다.  

<br><br>

## 3. LSTM(Long Short-Term Memory) 네트워크 구조와 특징에 대해 설명해 보세요.  

**LSTM**은 RNN의 변형으로, 긴 시퀀스 데이터의 시간적 의존성을 모델링 할 수 있도록 설계되었습니다.  
기존 RNN은 시퀀스가 길어질수록 과거 정보가 손실되는 기울이 소실 문제가 발생했는데,  
LSTM은 이를 셀 상태와 게이트 구조로 보완했습니다.  
LSTM의 기본 구성 요소는 아래 3가지 게이트와 1개의 셀 상태입니다.  
**Forget Gate**는 과거 정보를 얼마나 잊을지 결정합니다.  
**Input Gate**는 새로운 정보를 얼마나 저장할지를 결정합니다.  
**Output Gate**는 다음 시점으로 보낼 출력을 결정합니다.  

동작 순서는, 먼저 Forget Gate로 불필요한 과거 정보를 지우고,  
Input Gate로 새로운 정보를 더하며,  
업데이트된 셀 상태를 기반으로 Output Gate가 출력을 결정하는 흐름입니다.  
이런 구조 덕분에 LSTM은 긴 시퀀스에서도 중요한 정보만 선택적으로 유지하며, 기울기 소실 문제를 완화할 수 있습니다.  

<br><br>

## 4. AutoEncoder와 Variational AutoEncoder(VAE)에 대해 설명해 보세요.  

**AutoEncoder**는 입력 데이터를 인코더를 통해 저차원 latent space로 압축하고, 디코더를 통해 이를 다시 복원하는, 비지도 학습 기반 신경망 구조입니다.  
학습 목표는 입력과 복원된 출력 차이를 최소화하는 것으로, reconstruction loss를 사용합니다.  
주요 용도는 데이터 압축, 특징 추출, 노이즈 제거 등입니다.  
**VAE**는 AutoEncoder를 확률적 형태로 확장한 모델로, latent space를 feature가 아닌 정규 분포로 가정하고 데이터를 인코딩합니다.  
그리고 그 확률 분포에 따라 데이터를 샘플링하는 방식으로 디코더에서 이미지를 복원합니다.  

<br><br>

## 5. Transformer의 구조에 대해 설명해 보세요.  

**Transformer**는 Self-Attention 메커니즘을 기반으로 하는 시퀀스 변환 모델입니다.  
기존 시퀀스 변환 모델로 RNN이 대표적이지만, RNN은 순차적으로 시퀀스 데이터를 처리하여, 긴 시퀀스에서는 과거 정보가 소실되고, 병렬 처리가 어렵다는 한계가 있었습니다.  
Transformer는 RNN을 사용하지 않고, Attention만을 사용하여, 입력을 한 번에 병렬적으로 처리하여, 이러한 한계를 해결했습니다.  

기본 구성은 Encoder-Decoder 구조로,  
**Encoder**는 입력 시퀀스를 인코딩하여 문맥 정보를 포함한 latent representation으로 매핑하고,  
**Decoder**는 이 latent representation을 바탕으로 출력 시퀀스를 생성합니다.  
각 layer 블록은 Multi-Head Self-Attention과 Feed-Forward Network, 그리고 Residual Connection + Layer Normalization으로 이루어져 있습니다.  

<br><br>

## 6. GAN(Generative Adversarial Network)에 대해 설명해 보세요.  

**GAN**은 생성자 네트워크와 판별자 네트워크가 경쟁하면서 학습하는 모델입니다.  
생성자는 가짜 데이터를 만들어 판별자를 속이려 하고,  
판별자는 진짜와 가짜를 구별하려 합니다.  
이 두 네트워크가 경쟁적으로 학습되면서, 결국 생성자는 실제 분포와 유사한 데이터를 만들게 됩니다.  

<br><br>

## 7. Transfer Learning과 Pre-training과 Fine-tuning의 차이에 대해 설명해 보세요.  

**Transfer Learning**은 한 작업에서 배운 지식을 다른 작업에 활용하는 학습 방법입니다.  
**Pre-training**은 대규모 데이터로 일반적인 특징을 학습하는 과정이고,  
**Fine-tuning**은 그 사전학습된 모델을 특정 도메인에 맞게 추가 학습하는 과정입니다.  
Pre-training과 Fine-tuning은 Transfer Learning의 전형적인 형태입니다.  

<br><br>

## 8. Reinforcement Learning(강화 학습)에 대해 설명해 보세요.  

**강화 학습**은 환경과 에이전트가 상호작용하면서 보상을 최대화하도록 학습하는 방법입니다.  
에이전트는 매 시점에서 상태를 관찰하고, 정책 네트워크에 따라 행동을 선택합니다.  
환경은 그에 대한 보상과 새로운 상태를 반환합니다.  
목표는 누적 보상을 최대화하도록 최적 정책 네트워크를 찾는 것입니다.  

<br><br>

## 9. PPO(Proximal Policy Optimization)에 대해 설명해 보세요.  

기존의 강과학습 알고리즘에서는 업데이트가 너무 커지면 정책이 불안정해지는 문제가 있었는데,  
**PPO**는 이를 안정화하기 위해 정책 변화 폭을 제한하는 손실함수를 도입했습니다.  

<br><br>

## 10. 로지스틱 회귀에 대해 설명해 보세요.  

**로지스틱 회귀**는 선형 회귀의 결과 값을 그대로 사용하지 않고, 그 값을 시그모이드 함수에 통과시켜, 0~1 사이의 확률로 변환합니다.  
그리고 특정 임계값을 기준으로 0 또는 1 클래스로 분류할 수 있습니다.  
이름은 회귀이지만, 실제로는 분류 문제를 해결하는 모델입니다.  

<br><br>
