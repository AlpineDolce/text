# sesac_card
SeSac Fintechers3 - Card Recommendation Chat bot


![image](https://github.com/user-attachments/assets/2bd8301d-81cf-4806-930f-6da0aa67434b)




# 카드 추천 챗봇 서비스

## 프로젝트 소개
RAG(검색-증강 생성) 기술을 활용한 **카드 추천 챗봇 서비스**를 개발하였습니다. 본 서비스는 사용자의 소비 내역과 성향을 분석하여 맞춤형 신용카드를 추천하고, 지속 가능한 카드 사용 환경을 지원합니다.

---

## 배경 및 필요성
- **신용카드 사용 증가**: 1인당 평균 사용 신용카드 개수 4.4개, 유효 카드 760개.
- **기존 추천 서비스 한계**:
  - 복잡한 지출내역 입력 방식.
  - 단조로운 추천 결과 및 챗봇의 피드백 미반영.
- **지속 가능성 문제**: 카드 플라스틱 분해에 약 1000년 소요, 유해물질 배출.

---

## 주요 기능
### 1. 맞춤형 카드 추천
- 사용자의 소비 내역 및 성향 기반 실시간 추천.
- 주요 혜택 요약 및 시각화 제공.
- 챗봇과의 대화를 통해 피드백 반영.

### 2. 데이터 분석 및 시각화
- 소비습관 분석 차트 제공.
- 지출 비율을 그래프로 시각화.

### 3. 지속 가능성 고려
- 불필요한 카드 발급 최소화로 환경 및 경제적 개선 효과.

---

## 기술 스택
- **데이터 수집**: Selenium 기반 웹 스크래핑.
- **데이터 전처리**: Regular Expression을 활용한 텍스트 분류 및 처리.
- **임베딩 및 검색**: Upstage 및 Pinecone를 사용하여 벡터 데이터 저장.
- **LLM 통합**: Langchain 기반 RAG 프로세스로 사용자와의 실시간 인터랙션 구현.
- **프론트엔드**: Streamlit을 활용한 직관적인 UI 설계.

---

## 개발 과정
1. **웹 스크래핑**
   - 카드 정보 사이트에서 주요 데이터 수집.
   - JSON 형식으로 저장 및 병합.

2. **데이터 전처리**
   - 카드 이름, 혜택, 브랜드 등 주요 항목 분류.
   - 정규표현식을 활용한 데이터 구조화.

3. **RAG 모델 구현**
   - Langchain을 활용한 질문 응답 체인 구성.
   - 사용자의 입력에 기반한 메타데이터 필터링 및 추천 카드 출력.

4. **결과 시각화**
   - 사용자의 지출 분석 결과를 백분율 그래프로 표현.
   - 추천 카드 이미지와 상세 정보 제공.

---

## 기대 효과
- **사용자 편의성 증대**:
  - 맞춤형 카드 추천 및 피드백 반영.
  - 지출 분석 결과 제공으로 소비 습관 개선.

- **환경 및 경제적 개선**:
  - 불필요한 카드 발급 최소화.
  - 데이터 기반 금융 트렌드 분석 가능.

- **차별화된 서비스**:
  - 기존 추천 서비스와 달리 실시간 응답 및 정확한 추천 제공.

---
1. '맞춤형 카드 추천' 버튼 클릭
   
![첫화면(맞춤형 카드 추천)](https://github.com/user-attachments/assets/22f60dda-2f5d-4834-8376-2118993628d5)

1-1. 가계부 '네' 버튼 클릭

![가계부 yes](https://github.com/user-attachments/assets/2cd3fc75-5106-4c7f-8391-c33ede104965)
![카드 소비 내역 파일 포함 진행 과정](https://github.com/user-attachments/assets/a03b333c-0a65-4d6d-982e-607fc1034f8f)
![답변 생성 기다리는 중](https://github.com/user-attachments/assets/66a9ba26-5e35-406e-82b6-794587b2e75d)
![결과1](https://github.com/user-attachments/assets/36e5138e-69cc-4466-91cd-86fa96a66abf)
![연이은 채팅 가능](https://github.com/user-attachments/assets/ce007a2b-becb-4531-8e22-39510c5c7d81)

1-2. 가계부 '아니오' 버튼 클릭

![가계부 no](https://github.com/user-attachments/assets/a3d932bf-3a6c-42c0-8dfc-c22b727031ad)
![카드소비내역 없을 시 카드 선택](https://github.com/user-attachments/assets/6d0406b9-6fc9-45fb-98ca-42bd11333e6c)

2. '챗봇 카드 추천' 버튼 클릭

![챗봇 버튼](https://github.com/user-attachments/assets/51acd368-3210-4587-bda1-83bc3eabb9a2)
![챗봇](https://github.com/user-attachments/assets/d049eb4b-3547-4f0a-8aba-4a9e553cfff3)

- 1번에서 2번으로 넘어가서 챗봇 사용시 이전 데이터가 불려와지는 부분 개선 필요
  (xlsx 파일 읽는 부분 개선을 진행하다보니 자연스럽게 또 다른 개선이 필요한 것으로 여겨짐)
- 초반 시작하고 나서 버튼을 클릭하게 되면 너무 오래 로딩되는 문제가 있어 개선 필요
- solar-pro(llm) 수준에 맞는 xlsx 파일 데이터 전처리 조치 및 데이터 정확성, 일관성 검토하면서 개선 필요
- 이후에 항후 계획 참고


---
## 향후 계획
- UI/UX 개선 및 캐시 관리 최적화.
- MyData API 활용으로 정밀도 향상.
- 체크카드 추천 서비스 추가.
- 주요 소비 카테고리 예측 모델 개발.

---

## 팀 소개
- **타임키퍼**: 김태식, 이호영
- **발표자료 작성**: 김태식, 이호영
- **기술 구현**: 서예은, 김영탁
- **커뮤니케이터**: 안효철

---

## 문의
서비스에 대한 궁금한 점이 있다면 아래 연락처로 문의해주세요.  
Email: [YourTeamEmail@example.com](mailto:YourTeamEmail@example.com)
