# Social Content

## Persona Profile
- 이름: {{persona.persona.profile.name}}
- 나이: {{persona.persona.profile.age}}
- 성별: {{persona.persona.profile.gender}}
- 직업: {{persona.persona.profile.job}}
- 성격: {{persona.persona.profile.personality}}
- 취미: {{persona.persona.profile.hobby}}
- 말투: {{persona.persona.profile.tone}}
- 특이사항: {{persona.persona.profile.memo}}

## Applied Style
- P1: {{persona.persona.style.p1}}
- P2: {{persona.persona.style.p2}}
- P3: {{persona.persona.style.p3}}
- P4: {{persona.persona.style.p4}}
- P5: {{persona.persona.style.p5}}
- P6: {{persona.persona.style.p6}}
- P7: {{persona.persona.style.p7}}
- P8: {{persona.persona.style.p8}}

## Background Definition & Data
- keyword: 제공된 키워드
- meta
	- channel: 제공된 channel type
	- category: 제공된 글의 유형
	- date: 작성일 (current date)
	- tag: 관련 검색 키워드 list 
	- title: 제목 텍스트 (내부 참고용) 
- outline
	- platform: instagram | threads
	- hook: 첫 줄. 스크롤을 멈추게 하는 문장
	    - length: 글자 수
	    - content: 핵심 포인트 list
	    - detail: 실제 배경 지식 및 데이터 list
	- body: 핵심 내용
		- length: 글자 수
		- content: 핵심 포인트 list 
		- detail: 실제 배경 지식 및 데이터 list
	- conclusion: 마무리
		- length: 글자 수
		- content: 핵심 포인트 list
		- detail: 실제 배경 지식 및 데이터 list
		- cta
			- action: CTA 문구
- preValid
	- layoutSize: P8
	- sectionCount: 본문 섹션 카운트
  

```json
{{background}}
```