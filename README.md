# [2021 Spring Class] Ajou ML by JBR

1. **대회목표**: 
   
   팀별로 자신만의 바둑 경기 기력 예측 머신러닝  만들기
   
   주어진 train data와 train label을 이용하여 기력 예측 인공지능을 만들고 test data의 기력을 예측하여 github에 

2. **세부 프로토콜**

   원본데이터셋: Fox Go Dataset

   실습데이터셋: https://drive.google.com/drive/folders/1yP8hk7Pg1_VVMScAilLeOwdUn7LZq-NJ?usp=sharing

   네트워크 파라미터: 제한없음

   아키텍쳐: 제한없음

   학습알고리즘: 제한없음

   딥러닝 프레임워크: PyTorch, TensorFlow 권장, 다른 프레임워크도 사용 가능

3. **순위산정:** 바둑 데이터셋 기력예측 Top-1 Accuracy

4. **팀 구성**: 5인 구성된 팀

5. **제출 데이터**: 각 Test data 별 예측한 기력값 (github 제출) + Test data 별 예측한 기력 별 확률 (email 제출) #num_of_test_data * 27(9단+18급)

6. **대회진행**

   |     날짜      |      일정       |
   | :-----------: | :-------------: |
   |     시작      | 2021년 3월 24일 |
   |     중간      | 2021년 5월 21일 |
   |     기말      | 2021년 6월 15일 |
   | 최종결과 발표 | 2021년 6월 22일 |

7. **최종 결과 산출 방법:** 중간, 기말 시점의 정확도를 일정 비율로 합쳐서 최종 결과에 반영한다.

8. **확률값 제출:** 중간, 기말 시점의 팀별로 구축한 모델의 "Test data 별 예측한 기력 별 확률"을 저장하여(kimsungeun@ajou.ac.kr) 메일로 제출



## 퍼블릭 랭킹

  
- Total Score가 아직 업데이트되지 않았습니다. 
 - 다음 업데이트 일정은 중간 점수 집계(2021-05-21) 입니다.
  
**현재 랭킹 1위는 team13 입니다. 평균 accuracy는 10.34% 입니다.**
|Ranking|Name|Penalty|Accuracy(%)|Last Submission|Total Submission Count|Total Score(%)|
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|1|team13|0|12.18519|2021-05-18 15:38:39.012358+09:00|19|0.0|
|2|team1|0|12.14815|2021-05-15 12:25:49.995395+09:00|38|0.0|
|3|team3|0|11.14815|2021-05-19 16:07:20.824716+09:00|9|0.0|
|4|team5|0|10.96296|2021-05-12 10:35:46.431084+09:00|4|0.0|
|5|team9|0|10.66667|2021-05-20 03:01:21.167039+09:00|44|0.0|
|6|team12|0|10.44444|2021-05-20 00:26:17.970010+09:00|9|0.0|
|7|team8|0|10.37037|2021-05-13 19:30:49.411719+09:00|15|0.0|
|8|team11|0|10.2963|2021-05-20 02:05:20.581840+09:00|21|0.0|
|9|team7|0|10.0|2021-05-17 15:06:34.257573+09:00|16|0.0|
|10|team10|0|9.96296|2021-05-14 19:24:42.322027+09:00|2|0.0|
|11|team2|0|9.88889|2021-05-19 21:20:56.136985+09:00|3|0.0|
|12|team6|0|9.33333|2021-05-14 17:17:07.445864+09:00|4|0.0|
|13|team4|0|9.11111|2021-05-19 17:04:39.981991+09:00|3|0.0|
|14|professor|0|8.22222|2021-04-30 11:24:12.169892+09:00|2|0.0|


**정확도는 소숫점 5자리 까지 출력됩니다.**
**Time zone is seoul,korea (UTC+9:00)**
## 퍼블릭 랭킹 제출 방법

팀별로 구성한 모델의 테스트 데이터 셋을 예측한 결과값을 `Encrypt.py` 를 이용해 암호화하여 `submission` 폴더의 해당 팀 폴더에 제출합니다. 

**주의사항** : 

1. 제출 파일명은 자유롭게 작성할 수 있습니다.(단, 폴더당 하나의 파일만 존재해야 합니다. 그렇지 않을 경우 채점이 되지 않습니다.)
2. `.github` 폴더는건들지 않도록 합니다.
3. 총 100회 까지 제출할 수 있고 이 이상 제출해도 채점 되지 않습니다.

Example) Team1인 경우 제출 방법

1. 예측 파일 만들기. 다음과 같은 예측 파일이 있다고 가정 (기력을 예측한 결과 파일)

   `ans.txt` 예시

   ```tex
   9d
   2k
   2k
   4k
   ```
   
   
   
2. 예측 파일(`ans.txt`)과 전달받은 키를 `Encrypt` 폴더에 넣고 `Encrypt.py`를 실행 시켜서 암호화한 예측 파일(`ans.json`)을 생성합니다. 
생성한 파일을 (`submission/team1`)에 넣고 commit 후 push 를 실행하면 완료됩니다.

   ```python
   # 1.이메일을 통해서 전달 받은 키 파일의 경로 입력
   key_path = "key.pem"
   # 2. 예측한 결과를 텍스트 파일로 저장했을 경우 리스트로 다시 불러오기
   # 본인이 원하는 방식으로 리스트 형태로 예측 값을 불러오기만 하면 됨(순서를 지킬것)
   raw_ans_path = "ans.txt"
   ans = read_txt(raw_ans_path)
   # 3. 암호화된 파일을 저장할 위치
   encrypt_ans_path = "../submission/team1/ans.json"
   # 4. 암호화!(pycrytodome 설치)
   encrypt_data(key_path, ans, encrypt_ans_path)
   ```

이 때 꼭 로컬에서 이 스크립트를 실행해서 제출하지 않고 코랩에서 pycryptodomex 라이브러리를 설치한 후 스크립트 실행시켜서 정답 파일 만든 뒤에 제출해도 무방합니다.



## 퍼블릭 랭킹 평가 방법

기력예측값의 정확도가 퍼블릭 랭킹에 그대로 반영됩니다.

ex) `ans.txt`=(기력 예측값, k=급, d=단), top 1 acc = 98%

```tex
9d
2k
2k
4k
```



## 암호화 모듈 설치 방법

설치 방법 설명은 [공식 문서](https://pycryptodome.readthedocs.io/en/latest/src/installation.html#windows-from-sources-python-3-5-and-newer)에 잘 나와있습니다. 아래 내용은 공식 문서에서 나온 내용을 가져왔습니다. 

파이썬 3.5 이상, 윈도우에서 Pycryptodomex 설치하는 방법

1. **[Once only, C Compiler가 미설치 되어있는 경우에만]** Download [Build Tools for Visual Studio 2019](https://visualstudio.microsoft.com/downloads/#build-tools-for-visual-studio-2019). In the installer, select the *C++ build tools*, the *Windows 10 SDK*, and the latest version of *MSVC v142 x64/x86 build tools*.

2. Compile and install PyCryptodome:

   ```
   > pip install pycryptodomex --no-binary :all:
   ```

3. To make sure everything work fine, run the test suite:

   ```
   > python -m Cryptodome.SelfTest
   ```



문의사항이 있으신 분은 kimsungeun@ajou.ac.kr 로 문의주시길 바랍니다.
