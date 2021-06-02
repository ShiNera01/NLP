Machine Translation - rule based
  - Source 언어의 모든 단어를 Target 언어의 단어로 치환
  - 단어 번역을 위한 단어 사전의 구축
  - 1:1 치환 번역을 시도하면 문법과 문맥을 무시한 번역이 이루어지기 때문에 결과 저조
  
Machine Translation - statistical based
  - 확률 및 통계 기반의 모델을 사용하는 새로운 접근 방법
  - 동일한 텍스트가 최소 2가지 언어로 번역되어 있는 많은 훈련 데이터 필요
  - 병렬 말뭉치(corpus), 이 것을 이용해 Source언어에서 Target언어로 변환하는 방법을 통계적으로 알아낼 수 있다.
  
  - 확률 기반 번역 시스템은 통계 기반 번역과 달리 하나의 정확한 번역을 생성 하지 않음.
  - 수 천개의 가능한 번역을 생성하여 각각의 번역이 얼마나 정확한가에 대해 확률적으로 순위를 메김
  - 훈련 데이터와 번역본이 얼마나 유사한지에 따른 정확도를 평가

 Neural Machine Translation
  - 기존의 LSTM은 하나가 들어오면 바로 하나의 output을 생산
  
  Seq2Seq
    - input이 들어오면 그 다음 어떤 단어가 나오는지 생성 softmax를 이용해서 확률적으로 접근
    - softmax를 활용해 다양항 문장을 생성할 수 있음
    - i 다음에 say도 나올 수 있고 like나 다른 단어들이 나올 수 있다. softmax를 통해 이러한 것들을 커버
    
    Encoder - Decoder 모델
      Encoding
       - 정보를 규칙에 따라 변환
      Decoding
       - 인코딩된 정보를 되돌리는 것
       - encoder가 인코딩한 정보에는 정보가 응축되어 있고 Decoder는 이 정보를 가지고 문장을 생성한다.
       
       
    - Encoder는 LSTM을 통해 받고 h라는 벡터를 뽑아낸다. (고정벡터)
    - Decoder는 h벡터를 받아서 <eos> 토큰을 받아 시작한다. 맨 처음 단어를 softmax를 통해 뽑아내고 그 다음 단어가 embedding에 들어간다.
    
    
    - 두 번째 모델은 reverse하는 것 
    
    
    - 세 번째 모델은 다른 LSTM모델에도 h를 부여하는 것
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
