# Social Background

## Input JSON structure description
* persona: 페르소나 정보
	* style: 어조 스타일 정보
		* p3: 정보밀도
			* 1: 핵심 요약 위주.
			* 2: 주요 포인트 설명.
			* 3: 상세 데이터 및 수치 포함.
			* 4: 심층 분석 및 비교 데이터 포함.
			* 5: 논문 수준의 방대한 정보와 레퍼런스 포함.
		* p6: 전문용어(log | medium | high)
			* low: 일반인 기준. 전문용어 최소화. 쉬운 설명 위주.
			* medium: 업계 종사자 기준. 통용 용어는 설명 없이 사용. 생소한 용어는 괄호 설명 또는 비유 추가.
			* high: 전문가 기준. 고급 용어 설명 없이 사용. 영문 원어 표기 적극 활용.
* outline: 생성된 outline JSON  
* document: Research Document by keyword
  
## Input

### Persona
```json
{
	"persona": {
	    "style": {
			"p3": {{persona.persona.style.p3}},
		    "p6": "{{persona.persona.style.p6}}"
	    }
}
```

### Outline
```json
{{outline}}
```

### Research Document
```md
{{document}}

{{document2}}
```