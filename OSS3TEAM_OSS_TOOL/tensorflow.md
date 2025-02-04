# 📢 텐서플로우(TensorFlow)
**데이터 그래프를 수치적으로 연산하기 위해 구글에서 만든 오픈 소스 라이브러리이다.**


|확장성|Android, iOS, Linux, OS X, 여러 CPU,GPU(CUDA) 활용 가능|
|:---:|:---:|
|쉬운 API|Python API 제공(아파치 2.0 라이센스)|
|Data flow graph|데이터 흐름 그래프 이용한 연산 표현|

## 텐서플로우를 사용하는 이유

▶️ 머신러닝 개발에서 텐서플로우의 가장 큰 이점은 추상화다. 개발자는 알고리즘 구현을 위한 세부 사항을 일일이 처리하거나 한 함수의 출력을 다른 함수의 입력으로 넘기는 적절한 방법을 알아내느라 고생할 필요 없이 전체적인 애플리케이션 로직에만 집중할 수 있다. 세부적인 부분은 텐서플로우가 알아서 처리해준다.

▶️ 텐서플로우 앱을 디버그하고 조사해야 하는 개발자를 위한 부가적인 편의 기능도 제공한다. 전체 그래프를 하나의 불투명한 객체로 구성해 한꺼번에 평가하는 것이 아니라 각 그래프 연산을 개별적으로 투명하게 평가하고 수정할 수 있다.

▶️ 텐서보드(TensorBoard) 시각화 제품군을 이용하면 인터랙티브한 웹 기반 대시보드를 통해 그래프 실행을 검사, 프로파일링할 수 있다. 텐서플로우에 만들어진 머신러닝 작업을 구글이 호스팅하는 Tensorboard.dev 서비스에서 호스팅하고 공유할 수 있다. 

▶️ 텐서플로우에는 구글 최상급 상용 제품의 지원을 통한 이점도 많다. 구글은 텐서플로우의 빠른 개발을 위해 투자해왔고, 텐서플로우를 더 쉽게 사용, 배포할 수 있는 많은 제품을 만들었다. 앞서 언급한 구글 클라우드에서의 가속을 위한 TPU 실리콘이 대표적인 사례다.

|장점|단점|
|:--:|:---:|
|데이터 플로우 그래프를 통한 풍부한 표현이 가능함|메모리를 효율적으로 사용하지 못하고 있음|
|계산 구조와 목표 함수만 정의 자동으로 미분 계산을 처리함|Symbolic Loop 기능이 유연하지 못하며, 함수가 있어도 텐서 타입으로만 적용해야 함|
|텐서보드를 통해서 파라미터 변화 양상 및 DNN 구조를 알 수 있음|딥러닝 모델을 만드는 데 기초 레벨부터 직접 작업해야 하기 때문에 초보자가 사용하기 어려울 수 있다.|

## 텐서플로우 특징
```
1. 데이터 플로우 그래프를 통한 풍부한 표현력
2. 코드 수정 없이 CPU/GPU 모드로 동작
3. 아이디어 테스트에서 서비스 단계까지 이용 가능
4. 계산 구조와 목표 함수만 정의하면 자동으로 미분 계산을 처리
5. Python/C++를 지원하며, SWIG를 통해 다양한 언어 지원 가능
```

## 텐서플로우 구성요소
|구분|설명|비고|
|:---:|:-----|:---:|
|노드(Node)|- 수학적 계산 데이터 입/출력 그리고 데이터의 읽기/저장 등의 작업 수행<br> - 역전파방법/플레이스 홀더/소프트맥스/크로스 엔트로피 등의 기술사용|연산|
|엣지(Edge)|- 노드들 간 데이터의 입출력 관계<br> - 동적 사이즈의 다차원 데이터 배열을 전송|관계|
|텐서(Tensor)|- 모든 데이터는 텐서를 통해 표현<br> - 학습 데이터가 저장되는 다차원 배열|데이터|
|오퍼레이션(Operation)|- 그래프 상의 노드가 오퍼레이션<br> - 오퍼레이션은 하나 이상의 텐서를 받을 수 있으며 계산을 수행하고<br> 결과를 하나 이상의 텐서로 변환|노드|
|세션(Session)|- 그래프를 실행하기 위해서는 세션 객체가 필요<br> - 세션은 오퍼레이션의 실행 환경을 캡슐화|객체|
|변수(Variables)|- 메모리 상에서 텐서를 저장하는 버퍼<br> - 변수는 그래프 실행시 파라미터를 저장하고 갱신하는데 사용|버퍼|

#### <a href="https://needjarvis.tistory.com/204">텐서플로우 설치 및 간단사용</a>
