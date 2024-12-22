# OP_SkinCareBot_GEMINI

아래는 서비스에 대한 README.md 예제입니다. 
이 문서에는 프로젝트 소개, 주요 기능, 설치 방법, 사용 방법, 매개변수 설명 등이 포함되어 있습니다.

SKINCARE BOT
피부 고민 진단 및 맞춤형 관리 팁 제공 서비스

SKINCARE BOT은 Google Gemini AI를 활용하여 사용자의 피부 고민에 대한 맞춤형 스킨케어 루틴 및 성분을 추천하는 챗봇 서비스입니다. 
사용자는 자신의 피부 고민을 입력하고, AI의 진단과 추천을 통해 피부 관리에 대한 유용한 정보를 받을 수 있습니다.

~~또한, 네이버 쇼핑 크롤링을 통해 관련된 제품 정보를 제공하여 사용자가 바로 구매를 고려할 수 있도록 돕습니다.~~ (크롤링 이슈 해결시 구현 예정)


## 주요기능
1.	피부 고민 상담:
	•	사용자가 입력한 피부 고민에 대해 AI가 적절한 질문을 던지며 상담을 진행합니다.
	•	AI는 사용자의 피부 타입과 고민을 바탕으로 맞춤형 성분 및 관리 팁을 추천합니다.

3.	맞춤형 매개변수 조정:
	•	AI의 응답 생성 과정을 사용자가 직접 조정할 수 있도록 매개변수 조정 기능 제공.
	•	temperature 옵션을 활용하여 창의성을 제어.

~~3.	네이버 쇼핑 크롤링:~~
	•	추천된 스킨케어 제품과 관련된 정보를 네이버 쇼핑에서 검색하여 제공.
	•	상위 5개의 제품 정보(이름, 가격, 구매 링크)를 보여줌.
	4.	대화 히스토리:
	•	사용자의 대화 기록이 앱 내에서 유지되어 대화 흐름을 확인할 수 있음.

## 설치 방법

1. 필수 요구 사항

	•	Python 3.8 이상
	•	아래의 Python 라이브러리 설치:
	•	streamlit
	•	google-generativeai
	•	beautifulsoup4
	•	requests

2. 설치

	1.	이 저장소를 클론합니다:

git clone https://github.com/your-repo/skincare-bot.git
cd skincare-bot

2.	필요한 라이브러리를 설치합니다:

pip install -r requirements.txt

3.	Google Gemini API 키 설정:
	•	YOUR_API_KEY에 자신의 API 키를 입력합니다.
 
4.	앱 실행:
 OP_COSMATIC_RECOMENDATION.ipynb  # 여기서 자신의 ip를 이용하여 stremlit에 접속합니다.
* 이때, 한번에 들어가지지 않을 경우가 있습니다. 그래도 계속 새로고침하여 들어가면 됩니다.
* stremlit에 정상적으로 접속이 되어도, type error가 뜨는 경우가 있는데, 이 또한 새로고침하면 정상작동됩니다. 

## 사용 방법

1.	앱 실행:
	•	앱이 실행되면 브라우저에서 Streamlit 인터페이스를 확인할 수 있습니다.
2.	피부 고민 입력:
  •	텍스트 입력란에 자신의 피부 고민을 작성합니다.
  •	예: 요즘 턱 부근에 여드름이 많이 생겨요. 어떤 제품을 사용해야 할까요?
(CAREBOT이 사용자의 피부타입을 확인할 떄까지 질문을 합니다. 요구하는 응답에 따라 적절한 응답을 해주세요. )
4.	매개변수 조정:
	•	사이드바에서 AI의 응답 생성 매개변수를 조정할 수 있습니다:
	•	temperature: 응답의 창의성을 조정 (0.0 ~ 2.0).
5.	네이버 쇼핑 결과 확인:
	•	AI가 추천한 성분과 관련된 제품 정보를 네이버 쇼핑에서 가져옵니다.

## 매개변수 설명

매개변수	설명	범위	기본값
temperature	출력의 무작위성 조정. 낮은 값은 보수적이고 높은 값은 창의적.	0.0 ~ 2.0	1.0

## 프로젝트 구조

* OP_COSMATIC_RECOMENDATION.ipynb  # 여기서 자신의 ip를 이용하여 stremlit에 접속합니다.
* chatbot.py # stremlit에서 작동하기 위한 코드
* README.md  # 프로젝트 설명서

추가적인 정보

1.	확장 가능성:
	•	다른 AI 모델로 쉽게 확장 가능.

2.	문의 및 기여:
	•	프로젝트에 기여하거나 문의 사항이 있다면 이슈를 등록해 주세요!

## 실제 앱 실행 화면
<img width="1509" alt="스크린샷 2024-12-22 오후 9 04 58" src="https://github.com/user-attachments/assets/e61fdeb7-8ab7-4784-a321-043e3687fbbd" />
처음 접속시 이런 화면이 뜹니다. 
<img width="1503" alt="스크린샷 2024-12-22 오후 9 06 17" src="https://github.com/user-attachments/assets/6262cb9d-cd53-4de9-a233-69fd757f24e1" />
자신의 피부 고민을 입력하여 carebot과 대화하세요.
<img width="1503" alt="스크린샷 2024-12-22 오후 9 06 26" src="https://github.com/user-attachments/assets/36205dca-d943-4e3b-a124-2144f2f41102" />
적당히 사용자에대한 정보가 수집되었다고 판단한 carebot은 사용자에게 맞는 피부 관리 팁과 성분을 추천해줍니다. 
<img width="1512" alt="스크린샷 2024-12-22 오후 9 06 37" src="https://github.com/user-attachments/assets/d41c786f-3d58-484c-a63b-180c40a687cf" />
<img width="1510" alt="스크린샷 2024-12-22 오후 9 06 41" src="https://github.com/user-attachments/assets/f2b4fd09-8323-45aa-b113-beee96f2292e" />
