# Content Meta

글의 메타 정보로, 생성 방향성을 위해 적용됩니다.

## Common

| Key           | Description | Type   | Required |
| ------------- | ----------- | ------ | -------- |
| topic.keyword | 글의 핵심 키워드   | string | Y        |

## Blog

keyword를 기반하며 입력되지 않은 값은 이후 단계에서 LLM이 생성합니다.

### Topic

글의 핵심 주제와 방향을 정의합니다.

| Key     | Description | Type   | Required |
| ------- | ----------- | ------ | -------- |
| keyword | 글의 핵심 키워드   | string | Y        |
| title   | 글 제목        | string | N        |
| target  | 타겟 독자       | string | N        |

### Backlink

백링크는 본문 내의 첫 키워드에 삽입되며 ,적용 시 모든 값은 필수입니다.

| Key     | Description | Type   | Required |
| ------- | ----------- | ------ | -------- |
| keyword | 링크를 삽입할 키워드 | string | N        |
| link    | 연결할 URL     | string | N        |

### CTA

글 하단에 독자의 행동을 유도하는 문구와 링크를 설정합니다.
적용 시 target · serviceName · link는 필수입니다.

| Key         | Description     | Type   | Required |
| ----------- | --------------- | ------ | -------- |
| target      | CTA 타겟 독자       | string | N        |
| serviceName | 연결할 서비스 또는 글 제목 | string | N        |
| link        | 연결할 URL         | string | N        |
| action      | CTA 문구          | string | N        |

```json
{
	"blog": {
		"topic": {
		    "keyword": "LLM이란 무엇인가?",
		    "title": "LLM이란 무엇인가? 2026년 실무자를 위한 대규모 언어 모델 완벽 가이드",
		    "target": "LLM 도입을 고민중인 개인 또는 기업"
		  },
		  "backlink": {
		    "keyword": "Transformer",
		    "link": "https://docs.eureka.codes/blog/what-is-transformer/"
		  },
		  "cta": {
		    "target": "LLM을 실무에 도입하고 싶은 개인 또는 기업",
		    "serviceName": "Eureka Codes",
		    "link": "https://eureka.codes/",
		    "action": "딱 맞는 AI 모델을 찾고 계신가요? 지금 바로 Eureka Codes에서 맞춤형 LLM 도입 가이드를 확인해보세요!"
		}
	}
}
```

```json
{
	"blog": {
		"topic": {
		    "keyword": "LLM이란 무엇인가?",
		    "title": "LLM(Large Language Model)이란?",
		    "target": "LLM"
		  },
		  "backlink": {
		    "keyword": "LLM",
		    "link": "https://docs.eureka.codes/blog/what-is-large-language-model/"
		  },
		  "cta": {
		    "target": "",
		    "serviceName": "",
		    "link": "",
		    "action": ""
		}
	}
}
```

---

## Social

### Topic

글의 주제와 방향을 잡기 위해 정의합니다.

| Key     | Description | Type   | Required |
| ------- | ----------- | ------ | -------- |
| keyword | 글의 핵심 키워드   | string | Y        |

### CTA

글 마지막 줄에 독자의 행동을 유도하는 문구를 설정합니다.
action이 없으면 빈 문자열로 처리되며 LLM이 임의로 생성하지 않습니다.

| Key    | Description | Type   | Required  |
| ------ | ----------- | ------ | --------- |
| action | CTA 문구      | string | N (적용 권장) |

```json
{
	"social": {
		"topic": {
		    "keyword": "LLM이란 무엇인가?"
		},
		"cta": {
		    "action": "자세한 기록은 프로필 링크"
		}
	}
}
```

