# Generate Background

실제 글 생성 전에, Outline에 'Actual Fact Content'를 추가 정리합니다.

## Goal
- 글의 본문 내용 구체화

## Input
- Persona: P3(정보밀도), P6(전문용어)
- Outline JSON
- Document (Markdown Data)

```
{
  "persona": {
	  "style": {
		  "p3": 5,
		  "p6": "high"
	    }
  }
}
```
## Prompt
- [시스템 프롬프트](https://github.com/lemoncloud-io/eureka-blog/blob/docs/blog/areas/prompts/background-system.md)
- [유저 프롬프트](https://github.com/lemoncloud-io/eureka-blog/blob/docs/blog/areas/prompts/background-user.md)
