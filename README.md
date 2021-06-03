# AI Cost Management and Prediction Platform

<br>
의사 결정 지원(DSS)을 위한 '인공지능 원가(손익/예산) 관리 및 예측 플랫폼'
<br><br>

### : Main Services
#### :heavy_check_mark: 원가 통합 관리
#### :heavy_check_mark: 전년/전월 , 당기사용/당기 투입 정보 차트 시각화
#### :heavy_check_mark: 외부요인(환율,유가 등) 자동 크롤링
#### :heavy_check_mark: 3개월 후 매출액 예측(Prediction)
#### :heavy_check_mark: 내부 요인 변경을 통한 예측 시뮬레이션(Simulation)
#### :heavy_check_mark: 예측에 대한 해석정보(Explainer)

<br><br>
## 시연 영상 🔽🔽
### [![AI Cost Management and Prediction Platform](http://img.youtube.com/vi/N9mTU6sIqak/0.jpg)](https://youtu.be/N9mTU6sIqak?t=0s)  

#### Youtube: https://www.youtube.com/watch?v=N9mTU6sIqak

***
<br/>

# How to execute _ For Screen works
1. 깃허브 팀 원격저장소를 개인 원격저장소로 포크한다.


2. 깃데스크탑으로 로컬 위치에 깃을 만들고 개인 원격저장소와 연결한다.( 팀 원격저장소에 연결하면 안됩니다.)


3. 해당 소스가 있는 폴더에서 파이참 들어가서 new project에서 그 폴더를 선택한 후 존재하는 소스로 프로젝트만들기 선택(영어라 되어 있음)
((new interpreter 환경으로 설치된 아나콘다와 파이썬 3.7선택(아나콘다는 검색해서 홈페이지에서 깔으세요)))


4. terminal 열어서 website폴더 진입(터미널은 이 위치에서 거의 모든작업한다고 생각) 


5. conda install django해서 장고설치 


6. pip3 install -r requirements.txt 장고 내부 패키지들을 자동 설치


7. master/website/board/templates/board 여기 폴더에 있는 html 작업




# 추가 공지

  - 각자 작업한 것에 대한 주석 

  - config/templates/register 안에 있는건 로그인 만들어놓앗던 폼들인데  그 바깥에 있는 것들과 병합될 예정

  - 작업하고 깃데스크탑으로 개인 원격저장소에 올릴 것.

  - 깃허브 홈페이지 들어가서 개인 원격저장소와 팀 원격저장소 compare해서 pull request 보낼 것.

# 프로젝트 요약
  - 제조회사를 타겟팅한 프로젝트로 제품을 생성하는데 사용되는 비용인 재료비, 노무비, 경비를 체계적으로 관리 
  - 원가를 구성하는 변동비 고정비 재료비의 과거 데이터를 시계열 분석을 통해 향후 3개월 매출액을 예측하여 기업의 매출액 예측 지원
  - 원가 예측 Simulation을 통해 고정비, 변동비, 재료비의 변동에 따라 매출 예측액을 확인하여 경영권자가 최선의 선택을 하도록 의사결정을 지원해주는 것이 KNOWHOW 원가 예측 플렛폼의 핵심

# 프로그램 설명 및 사용법

1. 회사의 기준정보 관리를 입력한다. (법인정보, 사업장, 사업부, 공장, 작업장, 품목, BOM...etc)
2. 매달 재무부에서 만드는 제조비용 I/F, 재료비I/F, 품목별 제조비용 I/F, 제품원가수불 I/F를 DB연결 혹은 엑섹을 통해 업로드를 한다. (업로드된 데이터는 년월/version에 따라 확인 가능하고 계속 축적되어 조회가 가능)
3. 업로드된 4가지 I/F를 통해 자동적으로 원가계산서가 완성되어 한달간 기업이 제품생산에 사용한 기초제공품 비용, 당기투입 비용, 당기사용 비용, 기말 제공품 비용을 계산. 계산된 원가계산서를 통해 한달간 매출액과 비용을 확인할 수 있다.
4. 메인화면 죄측의 '원가분석'을 클릭하여 막대 그래프와 선그래프 차트를 통해 1년 주기로 당기투입, 당기사용 금액을 확인
5. 마찬가지로 '원가분석' 클릭후 '전년/월대비'를 클릭하면 전년, 전월 대비 성장률을 비교하여 회사 매출 변화 트렌드를 보여준다.
6. 좌측의 '기준정보관리', '원가기준정보', '원가계산'의 I/F를 전부 업로드 하면 메인 화면에서 시계열 차트 생성하여 매출액의 변화 확인이 가능하다.
7. 향후 3개월 예측을 하기위해서는 메인 화면에 '학습' 버튼 클릭한다. '완료'라는 알림이 뜨기 전까지 대기하도록 한다. '완료' 알림이 생성 되면 메인 화면에 '예측'을 클릭, '완료'라는 알림이 뜨면 메인화면에 3개월 예측치가 나타난다. 
(기간이 길경우 메인화면의 '조회시작 시점'을 클릭하여 그래프를 늘리고 줄일 수 있다.)
8. 메인화면의 'Simulate' 화면 클릭시 화면에 오늘의 환률, 기준금리를 알수 있고 우측에 '변동비', '고정비', '재료비' 3가지 원가 요소들을 변동시켜 다음 3개월을 예측한다. 이를 통해 어떤 원가 요소가 매출액에 영향을 끼치는지 인사이트를 얻을 수 있다.
10. 메인화면에 'Explanation' 이미지를 클릭한다. 그러면 시계열 데이터 분석시 사용된 내부변수인 '변동비', '고정비', '재료비'와 외부변수인 '환률'과 '금리'가 매출액어 어떤 긍정적 영향 혹은 부정적 영향을 끼치는 지 차트가 생성되어 더 쉽게 인사이트를 얻을 수 있다.

## 시스템 버전
 - Anaconda Python 3.7
 - tensorflow==1.15
 - bs4==0.0.1
 - django==3.1.5
 - django-pandas==0.6.4
 - django-widget-tweaks==1.4.8
 - et_xmlfile==1.0.1
 - explainerdashboard==0.2.20.1
 - h5py==2.10.0
 - hdf4==4.2.13
 - hdf5==1.10.4
 - keras==2.4.3
 - keras-applications==1.0.8
 - mysqlclient==2.0.2
 - numpy==1.19.5
 - openpyxl==3.0.6
 - pandas==1.2.1
 - pymysql==1.0.2
 - pythorch==1.7.0
 - scikit-learn==0.24.1
 - selenium==3.141.0
 - shap==0.39.0
 - tensorboard==1.15.0
 - tensorflow-base==2.3.0
 - torch==1.7.0
## 소스코드 실행 방법
 - 시스템 버전을 전부 다운 받은후 작업을 진행
 - rest-api를 이용하여 rest-api server 실행을 위해 /rest_framework/Restful_framework 레포지토리에 가서 python manage.py runserver 8080 실행
 - django server 실행을 위해 Terminal을 하나더 실행하여 /master/website 레포지토리에 가서 python manage.py runserver 실행후 로컬 ip에 접속

 - ...
