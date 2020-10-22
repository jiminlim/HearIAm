# :four_leaf_clover: Hear I Am :four_leaf_clover:

    Hear I Am은 청소년과 전문 상담가의 매칭을 통한 실시간 및 녹화 상담 서비스입니다.

### 팀명 : :muscle:온청센 (온라인 청소년 센터) 

* 팀장: 이재인(Full Stack)
  * 팀원: 김영남(Full Stack), 노휘종(Full Stack), 임도현(Full Stack), 임지민(Full Stack)
  * 주소: http://k3b202.p.ssafy.io/

## :paperclip: 목차

* [프로젝트개요](#프로젝트개요) 
* [프로젝트흐름](#프로젝트흐름) 
* [기대효과](#기대효과) 
* [구현기능](#구현기능)
* [사용된API](#사용된API) 

## :paperclip: 프로젝트개요

* ### 청소년 상담

  국내 청소년 고민 상담이 연간 100만건 이상으로 크게 증가하고 있다. :disappointed_relieved:  
  상담사유별로 살펴보면 ‘정보제공’이 19.2%로 가장 많았고,     
  ‘대인관계(18.0%)’, ‘정신건강(12.1%)’, ‘가족(12.0%)’, ‘학업/진로(11.8%)’ 등이 뒤를 이었다.     
  국내 청소년 상담 서비스들은 크게 온라인과 오프라인으로 나뉜다. 

* ### 기존 상담 서비스 현황 

  학교폭력 피해가 증가함에 따라 최근 서비스 중인 피해 상담 서비스를 살펴보면  
  온라인 상담의 같은 경우 피해학생과 대면하여 얻을 수 있는 정보가 부족한 상황이고,    
  오프라인 상담의 경우 피해학생이 학교의 상담사나, 상담센터에 찾아가기 힘든 것이 사실입니다.

* ### Hear I Am의 :sparkles:차별화:sparkles:

  * WebRTC를 이용한 실시간 화상 통신이 가능합니다.  
  * AI 감정인식으로 상담사에게 감정 정보를 전달 할 수 있습니다. 
  * STT 를 이용한 상담 키워드 추출이 가능합니다.    
  * Chart.js, WordCloud 등으로 상담 결과를 시각화하여 보여줍니다.   
  * Selenium 으로 상담사의 자격정보를 판단할 수 있습니다.   

##  :paperclip: 프로젝트흐름

* ### 실시간 상담

  1. 상담을 원하는 청소년이 실시간 상담 서비스를 신청
  2. 상담사가 요청을 수락 후 화상 통화 연결
  3. 청소년의 얼굴은 보이지 않고 상담사의 얼굴만 보임
  4. 청소년의 감정정보가 실시간으로 차트화되어 상담사에게 전달
  5. 상담사는 상담을 하면서 상담일지를 작성가능
  6. 상담 종료후 청소년의 감정 정보와 키워드, 상담일지를 저장
  7. 청소년이 재상담을 신청할 시 기존의 상담 정보를 이용해 더욱 정확한 상담이 가능

* ### 예약상담

  1. 실시간으로 상담 가능한 상담사가 없을 시 예약
  2. 상담사가 시간을 확인 후 실시간 상담을 수락
  3. 이후는 실시간 상담과 같음

* ### 녹화상담

  1. 청소년이 직접 통화하기 어려운 상황인 경우 녹화상담 신청
  2. 여러가지 질문을 보고 청소년이 대답을 하고 이를 녹화하여 표정정보와 키워드를 추출
  3. 상담사가 이를 확인 후 댓글로 상담 내용을 적어준다

## :paperclip: 기대효과

* ### 학생측 :girl:

  * COVID-19로 인해 비대면 상담의 필요성 증가
  * 개인 정보가 노출될 걱정이 없어 학생들이 믿고 사용 가능 
  * 혼자서는 고민이 풀리지 않을 경우 도움을 받을 수 있음    
  * 청소년 문제로 인한 자살률 감소   
  * 실시간 상담, 녹화 상담, 예약 상담을 통한 다양한 매체로 상담사만 있다면 언제든 상담 가능! 

* ### 상담사측 :older_woman:

  * 상담사의 지속적이고 체계적인 관리를 통한 학생 관리  
  * 상담 경험을 쌓을 수 있음 (직무 경험)    
  * 재능기부를 통한 사회적 문제 해결에 도움 

## :paperclip: 구현기능

* ###  :family: 회원가입

  * #### 청소년 회원가입  

    이름, 인적사항 없이 회원가입 가능,  
    상담 후 데이터 처리 및 동일한 상담자 매칭을 위한 회원가입

  * #### 상담사 회원가입  

    셀레니움과 문자인식을 이용한 자격조회를 통해 상담자격 여부를 확인

* ### :computer: 실시간 상담

  WebRTC를 이용하여 실시간으로 상담을 진행, 현재 접속되어있는 상담자와 매칭됨.    
  피상담자는 얼굴대신 실시간으로 분석된 감정만 상담자에게 전달되어 피상담자의 부담을 덜 수 있음.     
  상담자가 메모한 상담내용이 저장되어 상담일지에서 불러올 수 있음.    

* ### :movie_camera: 녹화 상담

  실시간으로 상담하는 것조차 부담스러워 하는 청소년을 위한 기능으로 고민거리를 녹음하고,  
  녹음내용을 STT와 WordCloud를 이용해 어떤 고민인지 대략적으로 분석.  

* ### :date: 예약 상담 

  실시간 상담을 원하는데 매칭되지 않을 경우에 예약을 통한 실시간 상담 일정을 잡음

* ### :chart_with_upwards_trend: 상담 일지 

  상담일지를 (상담자 – 피상담자) 별로 관리하여 상담을 진행하면서 변화하는 것을    
  그래프로 시각화하고 상담자는 이전에 한 상담내용을 열람할 수 있도록 제작.

  

## :globe_with_meridians: 사용된API

* ### 감정인식

  face-api

* ### 화상통화

  WebRTC

* ### Speech To Text

  Google Speech-to-Text

* ### 차트 시각화

  Chart.js    
  WordCloud 

* ### 자격정보확인

  Selenium    
  네이버 클로바 ocr