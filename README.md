# MAIC-RS
SNUH MAIC Robotic Surgery AI Challenge, 전립선암 로봇수술 동영상을 이용해 수술도구를 Segmentation

## 한우정과 아이들 팀
- **팀장:  [장성준](https://github.com/junnei)**
- 팀원: [한우정](https://github.com/dnwjddl)


### 파일 가이드 (FINAL_SUBMISSION)
- ```Data Analysis.ipynb``` : 필수 제출 항목 1, 2 만족. (1. 학습 데이터셋을 input으로 받아 모델 weight를 output으로 저장 / 모델 weight와 테스트 데이터의 메타데이터 등을 input으로 받아 최고 점수에 해당하는 csv를 제출하는 .ipynb와 weight )
- ```ckpt.index``` ,```ckpt.data-00000-of-00001``` : 필수 제출 항목 2 만족. 최고 점수에 해당하는 csv를 제출하는 weight (약간의 차이가 있을 수 있음.)


### 실행 가이드

```python
#tensorflow_addons 를 pip로 설치 후 실행.
import tensorflow_addons as tfa
```

1. ```FINAL_SUBMISSION``` 폴더 내의 ```Data Analysis.ipynb``` Open
2. 전체 실행 (외부 데이터 및 weight를 사용하지 않음.)
 
 
-  ```<Evaluate>``` 테스트 데이터에 대한 자체 메트릭 값을 출력함

```python
#테스트 스코어
np.mean(np.array(mean))
```

-  ```<Inference>``` 인퍼런스 데이터에 대한 csv파일을 만듦.

```python
results.to_csv('results.csv',index = False)
```
