# Blog Outline

## Input description
  
* persona: 페르소나 정보
	* style: 어조 스타일 정보
		* p7: 구조 유형
			* flow: 문단 중심 전개. 소제목 없이 서술형 포인트 위주
			* heading: 소제목 중심. AEO 대응을 위한 질문형 H2/H3 적극 활용
			* numbered: 가이드나 절차 설명에 적합. 번호(1. 2. 3.)를 활용한 순차적 리스트
			* mixed: 대분류는 소제목(H2), 세부 내용은 리스트(번호형, 글머리 기호)로 계층화
		* p8: 레이아웃 사이즈
			* low: 한눈에 들어오는 짧은 분량. (400~600자 내외)
			* medium: 일반적인 블로그 포스팅의 표준 분량. (800~1,500자 내외)
			* large: 다수의 섹션을 포함한 방대한 분량. (2,000자 이상)
	* channel: 채널 정보
		* type: 채널 타입
			* blog: 블로그형
			* social: 소셜형
		* category: 글의 유형
			* personal_experience: 개인 경험
			* product_review: 리뷰
		    * expert_knowledge: 전문 지식
* blog: by channel type
	* topic
		* keyword: 글의 핵심 키워드
		* title: 글 제목
		* target: 타겟 독자
	* cta: 행동 유도 정보
		* target: cta 타겟 독자
		* serviceName: 연결할 서비스 또는 글 제목
		* link: 연결할 URL
		* action: cta 문구
* document: keyword로 검색된 정보 (markdown)

## Input

### Persona & Blog Meta
```json
{{persona}}
```

### Research Document
```md
{{document}}
```

### Current Date
{{datetime}}


