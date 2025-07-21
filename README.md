# 🚗 RiverPark Mate
> 실시간 주차 정보와 혼잡도 예측이 필요한 당신에게  
> 서울 한강공원의 주차장을 더 똑똑하게 사용하는 방법

한강공원을 방문할 때마다 주차장이 만차일까 걱정되셨다면,  
RiverPark Mate가 그 고민을 덜어드릴 거예요.  
이 앱은 **실시간 주차 가능 대수**와 **머신러닝 기반 시간대별 혼잡도 예측**을 통해  
더 효율적인 외출을 도와주는 어플리케이션입니다.

---

## 📽️ 데모 영상  
> 실제 앱 사용 흐름이 궁금하다면 아래 링크를 클릭해주세요!  
[👉 유튜브 시연 영상 보러가기](https://youtu.be/fRToL5UWEd4)

---

## 🧩 프로젝트 개요

RiverPark Mate는 서울시 공공데이터를 활용해  
한강공원(여의도/뚝섬)의 **실시간 주차 정보**와  
**시간대별 주차 혼잡도 예측**을 제공하는 모바일 앱입니다.

Firebase를 통한 로그인과 실시간 채팅,  
FastAPI를 통한 머신러닝 모델 연동 등  
프론트-백-ML이 연결된 서비스 전체 흐름을 직접 설계하고 구현했습니다.

---

## 👨‍💻 맡은 역할 (기여도 100%)

| 분야        | 주요 내용 |
|-------------|-----------|
| **프론트엔드** | - Figma 기반 UI/UX 설계<br>- Flutter 메인화면 전체 구현<br>- 지도 마커, 새로고침, 시간대별 인사말 등 기능 |
| **백엔드 연동** | - FastAPI 서버 구축<br>- Flutter와의 API 통신 구조 설계 및 JSON 포맷 처리 |
| **머신러닝** | - 서울시 교통량/유동인구 데이터 전처리<br>- 시간대별(XGBoost 기반) 주차 예측 모델 구현<br>- 예측 API 설계 및 실서비스 적용 |

---

### 🛠 기술 스택

- **Frontend** :  
  <img src="https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white" height="28"/>
  <img src="https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white" height="28"/>

- **Backend** :  
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" height="28"/>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" height="28"/>

- **ML** :  
  <img src="https://img.shields.io/badge/Scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white" height="28"/>
  <img src="https://img.shields.io/badge/XGBoost-EC0000?style=for-the-badge&logo=xgboost&logoColor=white" height="28"/>

- **Database** :  
  <img src="https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black" height="28"/>
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" height="28"/>

- **Design & Tools** :  
  <img src="https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white" height="28"/>
  <img src="https://img.shields.io/badge/Miro-050038?style=for-the-badge&logo=miro&logoColor=white" height="28"/>
  <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" height="28"/>
  <img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white" height="28"/>
  <img src="https://img.shields.io/badge/VSCode-007ACC?style=for-the-badge&logo=visualstudiocode&logoColor=white" height="28"/>

---

## 🌟 주요 기능

| 기능         | 설명 |
|--------------|------|
| ✅ 실시간 주차 정보 | 서울 열린데이터 API로 실시간 주차 가능 대수 수집 |
| 📊 혼잡도 예측 | FastAPI로 호출된 ML 모델이 아침/낮/저녁 시간대 혼잡도 예측 |
| 💬 실시간 채팅 | Firestore를 통한 주차장별 사용자 간 실시간 의견 공유 |
| 🔐 사용자 인증 | Firebase Auth 기반 로그인 / 회원가입 처리 |

---

## 🖥️ 시스템 아키텍처

Flutter → FastAPI → ML 모델 → 응답 반환  
+ Firebase를 통한 인증 및 실시간 채팅  

> ![아키텍처 이미지](./assets/riverpark_architecture.png)

---

## 📘 API
### 예측 요청
POST/predict_yeouido
Content-Type:application/json
###Request Body
{
"hour":10,
"weekday"2,

## 🖼 UI 미리보기  

| 메인 페이지 | 예측 결과 | 채팅 기능 |
|-------------|------------|-----------|
| ![main](~~main.gif 필요) | ![predict](~~predict.gif 필요) | ![chat](~~chat.gif 필요) |
| 메인 페이지 | 예측 결과 | 채팅 기능 |
| ![main](~~main.gif 필요) | ![predict](~~predict.gif 필요) | ![chat](~~chat.gif 필요) |
|-------------|------------|-----------|

> 한눈에 주차 가능 여부를 확인할 수 있는 UI와  
> 새로고침, 시간대별 인사말, 지도 마커 등 다양한 기능을 직접 구현했습니다.

---

## 🧠 트러블슈팅 기록

| 문제 | 해결 방법 |
|------|-----------|
| JSON 구조 불일치 | `pandas`로 feature 순서를 고정 정렬 후 예측 |
| 타입 오류 (np.float32) | Python float로 변환하여 Flutter 디코딩 오류 해결 |
| 모델 분기 처리 | 여의도/뚝섬 각각의 모델을 라우터 분리로 대응 |
| 공공데이터 누적값 처리 | 교통량 데이터와 결합하여 일별 주차 대수 추정 |

---

## 📊 머신러닝 분석 요약

- 데이터: 서울시 교통량, 유동인구, 요일/시간 등  
- 상관계수 분석을 통해 Feature 선정  
- 모델 성능 평가:  
  - XGBoost가 높은 R2 Score와 낮은 MSE로 최종 선택됨  
  - 실제값과 예측값 간 분산이 작고, 대체로 y=x 선형 분포를 따름

> ![산점도 그래프](~~predict_result.png 필요)

---

## 💬 느낀 점

처음에는 단순히 “예측 결과를 보여주는 앱”이라고 생각했지만,  
데이터 전처리부터 모델링, API 설계, Flutter UI 구성까지  
직접 손으로 구현하면서 **개발이란 다양한 기술의 연결**임을 배웠습니다.

특히 FastAPI와 Flutter의 연동, JSON 처리, Firebase와의 통합은  
신입 개발자로서 실무 수준의 경험을 얻기에 충분한 도전이었습니다.

---

## 📌 GitHub Repo  
> 소스코드와 더 자세한 정보는 아래 링크에서 확인할 수 있어요  
[🔗 RiverPark Mate GitHub](https://github.com/donghun-ha/RiverPark-Mate)
