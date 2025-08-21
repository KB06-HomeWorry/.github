## 꼼꼼한 서류 분석과 신뢰성 있는 중개사 정보로 안전한 부동산 거래를 이끄는, **집걱정단**

**👉 [서비스 바로가기](http://home-worry-party-alb-341952107.ap-northeast-2.elb.amazonaws.com)**

**📹 [영상 보러가기](https://youtu.be/QGLd_JbfpK8)**

https://github.com/user-attachments/assets/9da407a8-96df-4990-a846-7536358232aa

<br />

## 📌 목차

- [소개](#-소개)
- [기능](#-기능)
- [기술 스택](#-기술-스택)
- [설치 및 실행 방법](#%EF%B8%8F-설치-및-실행-방법)
- [폴더 구조](#-폴더-구조)
- [스크린샷](#-스크린샷)
- [개발자](#-개발자)

<br />

## 📝 소개

**집걱정단은 사용자에게 더 안전하고 신뢰할 수 있는 부동산 거래 경험을 제공하기 위한 통합 분석 플랫폼입니다.**

부동산 거래는 정보 비대칭과 사기 위험으로 인해 사용자 불안이 높은 영역입니다.

기존 플랫폼은 매물 정보 제공에 집중하지만, **거래의 안전성**까지는 보장하지 못합니다.

우리는 거래 과정에서 **AI 분석**과 **신뢰 검증**을 도입하여,

**안전하고 투명한 부동산 거래 환경**을 만드는 것을 목표로 합니다.

<br />

## ✨ 기능
- **AI 계약서 분석**
  - OCR을 통해 계약서 이미지/PDF에서 텍스트 추출
  - KoBERT 모델로 위험 조항 분류
  - OpenAI API를 활용해 위험 조항의 제목 및 권장 조치 생성 및 시각화

- **서류 기반 매물 검증**
  - 입력된 주소 기반으로 불법건축물 여부, 지붕 구조, 용도, 허가일자 등을 확인
  - 해당 매물을 관리하는 중개사 정보와 함께 위험도 평가

- **시세 기반 위험 매물 판별**
  - 입력된 실평수와 거래가를 기준으로 해당 지역 평균 시세와 비교
	- 시세보다 현저히 낮은 경우 위험 매물로 판단해 사용자에게 경고
    
- **중개사 정보 조회 및 검증**
  - 내부 DB에 등록된 중개사 여부 확인
  - 미등록 중개사인 경우 사용자에게 주의 안내
  
- **체크리스트 자기 점검**
  - 계약 전 필수 확인 항목 리스트 제공
  - 사용자의 응답을 저장하여 자주 놓치는 항목 통계화 가능
  - 문제/템플릿 DB로 분리하여 유연한 문제 관리 구조 구축

- **부동산 용어 해석기**
  - 사용자가 입력한 어려운 용어를 OpenAI API를 통해 쉽게 풀어 설명
  - 계약서·등기부등본 등에서 등장하는 이해하기 어려운 전문 용어를 쉬운 표현으로 변환
  - 법률·거래 관련 문장을 이해해 위험 요소를 스스로 식별 가능

- **부동산 지식 퀴즈**
  - 거래 절차, 권리관계, 법적 의무 등 핵심 지식 학습
  - 안전 거래에 필요한 기본 이해도 향상
 
- **중개 수수료 계산기**
  - 거래 금액·유형 입력 시 법정 수수료 범위 자동 계산
  - 과도한 수수료 청구 등 금전적 분쟁 예방

- **지도 기반 시각화 기능**
  - 커스텀 마커 및 오버레이, 클러스터링을 이용해 매물 및 중개사 위치 표시
  - 클릭 시 정보 툴팁 또는 모달로 상세 정보 확인 가능

- **마이페이지**
  - 사용자 정보 조회, 저장한 매물 및 중개사 목록 확인, 비밀번호 변경 등 계정 관리 기능

<br />

## 🛠 기술 스택

<img width="500" src="https://github.com/user-attachments/assets/03d32983-6dfe-42b4-92ae-ef8ea3970505" />

**Frontend**
- `Vue.js 3` – UI 구성 및 상태 관리
- `Vite` – 번들링 및 개발 서버
- `Tailwind CSS` – 유틸리티 기반 CSS 프레임워크
- `Pinia` – 상태 관리 라이브러리
- `Axios` – API 통신 라이브러리

**Document Processing (문서 처리)**
- `Tesseract.js` – 이미지 기반 계약서의 텍스트 OCR 인식
- `pdf.js` – PDF 파일의 페이지 렌더링 및 이미지 변환

**Backend**
- `Spring` – MVC 아키텍처 기반 서버 및 비즈니스 로직 처리

**AI 분석 서버**
- `FastAPI` – AI 모델 연동 서버 구축
- `KoBERT` – 부동산 계약 조항 사기 가능성 분류 모델
- `OpenAI GPT API` – 부동산 용어 해석 및 위험 조항 해설 및 추천 문구 생성

**Infra / DevOps**
- `Docker / Docker Compose` – 로컬 개발 환경 및 컨테이너화
- `AWS EC2` – 프론트/백엔드 서버 배포
- `AWS RDS` – 클라우드 DB 배포

<br />

## ⚙️ 설치 및 실행 방법

```bash
# 프로젝트 클론
git clone https://github.com/KB06-HomeWorry/Front-End.git
git clone https://github.com/KB06-HomeWorry/Back-End.git
cd project-name

# 프론트엔드
cd ./Front-End/HomeWorry
npm install
npm run dev

# 백엔드
# IntelliJ에서 실행하거나 Tomcat 서버로 구동

# FastAPI 모델 서버
cd ./ai
python3 -m uvicorn server:app --reload --port 8000

🔐 .env, application.properties 등 환경변수 파일이 필요합니다.
```

<br />

## 📁 폴더 구조
```
project-root/
├── Front-End/         # Vue.js 기반 프론트엔드
├── Back-End/          # Spring 백엔드
```

<details>
<summary><b>📂 Front-End/ 구조 보기</b></summary>
<img width="202" height="448" src="https://github.com/user-attachments/assets/34f14186-50b1-41d8-9f1d-b09a3e9855a7" />

```
pages
│  NotFoundPage.vue
│
├─agency
│  │  AgencyDetail.vue
│  │  AgencyListPage.vue
│  │  AgencyReviewWrite.vue
│  │  AgencySample.vue
│  │  ListingPage.vue
│  │
│  ├─components
│  │      AgencyCard.vue
│  │      AgencyReviewSummary.vue
│  │      AgencySearchBar.vue
│  │      BarChart.vue
│  │      BtnAgency.vue
│  │      BtnMedGray.vue
│  │      CircularGauge.vue
│  │      HashTag.vue
│  │      ListingCard.vue
│  │      MapFloatingButtonWithModal.vue
│  │      ProgressBar.vue
│  │      ReviewBox.vue
│  │      ReviewChoice.vue
│  │      ReviewQuestion.vue
│  │      ReviewText.vue
│  │      SortSelect.vue
│  │
│  └─composables
│          useAllTrustScore.js
│          useTrustScore.js
│
├─ai
│  │  AIDocumentSubmitPage.vue
│  │  EstateEase.vue
│  │
│  ├─components
│  │      AIAnalysisDetailModal.vue
│  │      AIAnalysisResult.vue
│  │      AIButtonGroup.vue
│  │      AIExplain.vue
│  │      AIFileUploadButton.vue
│  │      AIUploadList.vue
│  │      ContractOcrUploader.vue
│  │      EstateEaseInput.vue
│  │
│  ├─composables
│  │      useFileUpload.js
│  │      useOcrAndAnalyze.js
│  │
│  └─mock
│          analysisMock.js
│
├─analysis
│  │  AnalysisPage.vue
│  │
│  └─components
│  │       IncidentChecklist.vue
│  │       StepAgentTrust.vue
│  │       StepBuildingHistory.vue
│  │       StepCheckRegistryInfo.vue
│  │       StepRiskAnalysis.vue
│  │
│  └─ composables
│          useAnalysisStep.js
│          usePostcode.js
├─auth
│  │  ChangePasswordPage.vue
│  │  LoginPage.vue
│  │  ResetPasswordPage.vue
│  │  ResetPasswordSentPage.vue
│  │  SignupAgreementPage.vue
│  │  SignupFormPage.vue
│  │
│  └─components
│          AuthTitle.vue
│          InputEmail.vue
│
├─checklist
│  │  ChecklistPage.vue
│  │
│  └─components
│  │       ChecklistBtn.vue
│  │       ChecklistNavBar.vue
│  │       ChecklistQuestion.vue
│  │       ChecklistStagePage.vue
│  │       CircleButton.vue
│  │
│  └─components
│          useChecklistStep.js
│ 
├─dangerResult
│  │  DangerResultPage.vue
│  │
│  └─components
│          DangerResultButtons.vue
│          DangerResultCard.vue
│          DangerResultSummery.vue
│
├─home
│  │  Calculator.vue
│  │  HomePage.vue
│  │
│  └─components
│          ApartBtn.vue
│          CalOption.vue
│          HomeBtn80px.vue
│          HomeBtnLg.vue
│          HomeBtnMed.vue
│          HomeBtnSmall.vue
│          OptionBtnSmall.vue
│
├─map
│  │  DetailPage.vue
│  │  FixMapPage.vue
│  │  MapAgencyPage.vue
│  │  MapCompoTest.vue
│  │  MapPage.vue
│  │
│  └─components
│          AreaSlider.vue
│          BottomSheet.vue
│          DetailAgency.vue
│          DetailLocation.vue
│          FilterBar.vue
│          FilterButton.vue
│          FilterOptionList.vue
│          FloatingButtonStack.vue
│          HomeFilter.vue
│          ListingMarkers.vue
│          ListingToggle.vue
│          LocationSearch.vue
│          MarketPrice.vue
│          MarketPriceDetail.vue
│          Slider.vue
│
├─mypage
│  │  AgencyBookmark.vue
│  │  ListingBookmark.vue
│  │  MyPage.vue
│  │  PrivacyNotice.vue
│  │
│  └─components
│          AgencyBookmarkCard.vue
│          CurrentPwModal.vue
│          ListingBookmarkCard.vue
│          MyMenu.vue
│
└─wordquiz
│   │  QuizHomePage.vue
│   │  QuizPage.vue
│   │
│   └─components
│           AnswerModal.vue
│           OXBtn.vue
│           OXQuizBox.vue
│           QuizHeader.vue
│           SelectBtn.vue
│           SelectQuizBox.vue
│
└─router
└─stores
```
</details>

<details>
<summary><b>📂  Back-End/ 구조 보기</b></summary>
  
```
ai
├─kobert.py
├─server.py
│
main/java/org.scoula
├─agent
│  ├─controller
│  │      AgentController.java
│  │
│  ├─domain
│  │      AgentBookmarkVO.java
│  │      AgentDetailVO.java
│  │      AgentReviewVO.java
│  │      OfficeGeographyVO.java
│  │
│  ├─dto
│  │      AgentBookmarkDTO.java
│  │      AgentDetailDTO.java
│  │      AgentReviewDTO.java
│  │      OfficeGeographyDTO.java
│  │      TrustScoreDTO.java
│  │
│  ├─mapper
│  │      AgentMapper.java
│  │
│  ├─model
│  │      Office.java
│  │      OpenApiResponse.java
│  │
│  └─service
│          AgentService.java
│
├─ai
│  ├─controller
│  │      AIController.java
│  │
│  └─service
│          AIServiceImpl.java
│
├─checklist
│  ├─controller
│  │      ChecklistController.java
│  │
│  ├─domain
│  │      ChecklistTemplateVO.java
│  │      ChecklistUserAnswerVO.java
│  │      ChecklistVO.java
│  │
│  ├─dto
│  │      ChecklistDTO.java
│  │      ChecklistResponseDTO.java
│  │      ChecklistTemplateDTO.java
│  │      ChecklistUserAnswerDTO.java
│  │
│  ├─mapper
│  │      ChecklistMapper.java
│  │      ChecklistTemplateMapper.java
│  │      ChecklistUserAnswerMapper.java
│  │
│  └─service
│          ChecklistService.java
│          ChecklistServiceImpl.java
│          ChecklistUserAnswerService.java
│          ChecklistUserAnswerServiceImpl.java
│
├─common
│  └─util
│          UploadFileName.java
│          UploadFiles.java
│
├─config
│  │  CorsConfig.java
│  │  RootConfig.java
│  │  ServletConfig.java
│  │  SpaController.java
│  │  SwaggerConfig.java
│  │  WebConfig.java
│  │
│  └─db
│          RdsConnectionCleaner.java
│
├─dangerResult
│  ├─controller
│  │      DangerResultController.java
│  │
│  ├─domain
│  │      DangerAnswerVO.java
│  │      DangerResultVO.java
│  │
│  ├─dto
│  │      DangerResultDTO.java
│  │
│  ├─mapper
│  │      DangerResultMapper.java
│  │
│  └─service
│          DangerResultService.java
│          DangerResultServiceImpl.java
│
├─documentAnalysis
│  ├─controller
│  │      DocumentAnalysisController.java
│  │
│  ├─domain
│  │      IllegalBuildingCheckVO.java
│  │      MonthlyRentVO.java
│  │
│  ├─dto
│  │      DocumentAgentDTO.java
│  │      DocumentAnalysisDTO.java
│  │      DocumentAnalysisResultDTO.java
│  │      DocumentSthRiskDTO.java
│  │      IllegalBuildingCheckDTO.java
│  │
│  ├─mapper
│  │      DocumentAnalysisMapper.java
│  │
│  └─service
│          DocumentAnalysisService.java
│          DocumentAnalysisServiceImpl.java
│
├─exception
│      ApiExceptionAdvice.java
│      CommonExceptionAdvice.java
│
├─listing
│  ├─controller
│  │      ListingApiController.java
│  │
│  ├─domain
│  │      ListingVO.java
│  │
│  ├─mapper
│  │      ListingMapper.java
│  │
│  └─service
│          ListingService.java
│          ListingServiceImpl.java
│
├─pricetrend
│  ├─controller
│  │      PriceTrendApiController.java
│  │
│  ├─domain
│  │      PriceTrendVO.java
│  │
│  ├─dto
│  │      MaxPriceDTO.java
│  │
│  ├─mapper
│  │      PriceTrendMapper.java
│  │
│  └─service
│          PriceTrendService.java
│          PriceTrendServiceImpl.java
│
├─quiz
│  ├─controller
│  │      QuizController.java
│  │      UserQuizStatusController.java
│  │
│  ├─domain
│  │      QuizVO.java
│  │      UserQuizStatusVO.java
│  │
│  ├─dto
│  │      QuizDTO.java
│  │      SubmitQuizRequest.java
│  │
│  ├─mapper
│  │      QuizMapper.java
│  │      UserQuizStatusMapper.java
│  │
│  └─service
│          QuizService.java
│          UserQuizStatusService.java
│          UserQuizStatusServiceImpl.java
│
├─sectionGeo
│  ├─controller
│  │      SectionGeoController.java
│  │
│  ├─dto
│  │      SectionGeoDTO.java
│  │
│  ├─mapper
│  │      SectionGeoMapper.java
│  │
│  └─service
│          SectionGeoService.java
│
├─security
│  ├─account
│  │  ├─domain
│  │  │      AuthVO.java
│  │  │      CustomUser.java
│  │  │      UserVO.java
│  │  │
│  │  ├─dto
│  │  │      AuthResultDTO.java
│  │  │      LoginDTO.java
│  │  │      UserInfoDTO.java
│  │  │
│  │  └─mapper
│  │          UserDetailsMapper.java
│  │
│  ├─config
│  │      SecurityConfig.java
│  │      SecurityInitializer.java
│  │
│  ├─filter
│  │      AuthenticationErrorFilter.java
│  │      JwtAuthenticationFilter.java
│  │      JwtUsernamePasswordAuthenticationFilter.java
│  │
│  ├─handler
│  │      CustomAccessDeniedHandler.java
│  │      CustomAuthenticationEntryPoint.java
│  │      LoginFailureHandler.java
│  │      LoginSuccessHandler.java
│  │
│  ├─service
│  │      CustomUserDetailsService.java
│  │      
│  └─util
│          JsonResponse.java
│          JwtProcessor.java
│
└─user
    ├─config
    │      MailConfig.java
    │
    ├─controller
    │      MemberController.java
    │
    ├─domain
    │      PasswordResetTokenVO.java
    │      PasswordRewriteVO.java
    │
    ├─dto
    │      ChangePasswordDTO.java
    │      PasswordResetTokenDTO.java
    │      PasswordRewriteDTO.java
    │      UserDTO.java
    │      UserJoinDTO.java
    │      UserUpdateDTO.java
    │      VerifyPasswordDTO.java
    │
    ├─exception
    │      PasswordMissmatchException.java
    │
    ├─mapper
    │      UserMapper.java
    │
    └─service
            PasswordResetService.java
            UserService.java
            UserServiceImpl.java
```
</details>

<br />

## 📸 스크린샷

<br />

## 🧑🏻‍💻 개발자
| [김유빈](https://github.com/ubeeni) | [노경현](https://github.com/Kyunghyun1121) |
|:---:|:---:|
| 팀장 / 체크리스트 / 서류, AI 계약서 분석 / 부동산 용어 해석 / 부동산 지식 퀴즈 | 체크리스트 / 서류 분석 / 인프라 및 배포 환경 구성 |

| [이다연](https://github.com/Leeday11) | [황동민](https://github.com/Dongmin-Hwang715) |
|:---:|:---:|
| 디자인 / 중개사무소 / 홈, 로그인, 회원가입, 마이페이지 / 부동산 지식 퀴즈 / 중개수수료 계산기 | 중개사무소 / 로그인, 회원가입, 마이페이지 / 부동산 지식 퀴즈 | 

| [김려린](https://github.com/ryeorin) | [이의민](https://github.com/min4034415) |
|:---:|:---:|
| 지도 / 매물, 시세 상세 페이지 / AI 계약서 분석 / 사용자 기반 매물 추천 | 지도 / 부동산 맵 필터 / 매물, 시세 상세 페이지 |
