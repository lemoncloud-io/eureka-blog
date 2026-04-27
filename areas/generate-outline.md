# Generate Outline

실제 글 생성 전에,  글의 논리적인 흐름 및 구조를 정리합니다.

## Goal
- 글의 개요 템플릿 생성

## Input
- Persona: P7(구조유형), P8(Layout size), Channel
- content-meta: Topic, CTA
- Document (Markdown Data)

```json
{
	"persona": {
	    "style": {
			"p7": "mixed",
		    "p8": "large"
	    },
	    "channel": {
			"type": "blog",
			"category": "expert_knowledge"
	    }
	},
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
	"persona": {
		"channel": {
			"type": "blog",
			"category": "expert_knowledge"
		},
		"style": {
			"p7": "mixed",
			"p8": "medium"
		}
	},
	"blog": {
		"topic": {
		    "keyword": "LLM이란 무엇인가?",
		    "title": "",
		    "target": ""
		  }
	}
}
```

## Prompt
- [시스템 프롬프트](https://github.com/lemoncloud-io/eureka-blog/blob/docs/blog/areas/prompts/outline-system.md)
- [유저 프롬프트](https://github.com/lemoncloud-io/eureka-blog/blob/docs/blog/areas/prompts/outline-user.md)


## Output
- 제목 -> 서론 -> 본문 -> FAQ -> 마무리 순으로 정리됩니다.

```json
{
  "keyword": "LLM이란 무엇인가?",
  "meta": {
    "channel": "blog",
    "category": "expert_knowledge",
    "date": "2026-04-13",
    "tag": [
      "LLM",
      "거대언어모델",
      "인공지능",
      "트랜스포머",
      "생성형AI",
      "딥러닝"
    ]
  },
  "outline": {
    "title": {
      "content": "LLM(Large Language Model)이란? 정의부터 작동 원리까지 완벽 정리"
    },
    "intro": {
      "length": 250,
      "content": [
        "최근 IT 산업의 핵심 키워드인 LLM의 정의와 부상 배경",
        "ChatGPT와 같은 생성형 AI의 근간이 되는 기술적 중요성",
        "본 글에서 다룰 LLM의 구조, 작동 원리 및 미래 전망 안내"
      ]
    },
    "section": [
      {
        "structureType": "mixed",
        "length": 400,
        "content": [
          "LLM은 방대한 데이터를 사전 학습한 초대형 딥러닝 모델",
          "트랜스포머(Transformer) 아키텍처: 셀프 어텐션 기능을 통한 문맥 이해",
          "기존 RNN과의 차이: 병렬 처리를 통한 학습 시간 단축 및 효율성 증대",
          "수천억 개의 파라미터를 통한 고도화된 언어 처리 능력"
        ],
        "title": "1. 대규모 언어 모델(LLM)의 정의와 기술적 특징"
      },
      {
        "structureType": "mixed",
        "length": 450,
        "content": [
          "질문 답변, 요약, 번역 등 다재다능한 작업 수행 능력",
          "적은 프롬프트만으로도 높은 예측 성능을 보이는 제너레이티브 AI의 핵심",
          "주요 글로벌 LLM 모델들의 파라미터 규모 및 특징 비교"
        ],
        "title": "2. LLM이 중요한 이유와 주요 모델 사례"
      },
      {
        "structureType": "mixed",
        "length": 400,
        "content": [
          "워드 임베딩(Word Embedding): 단어를 다차원 벡터로 표현하여 관계 파악",
          "인코더와 디코더의 역할: 텍스트 수치화 및 고유 출력 생성 과정",
          "모델 파라미터(가중치와 편향)의 규모가 성능에 미치는 영향"
        ],
        "title": "3. LLM은 어떻게 작동하나요? (핵심 원리)"
      },
      {
        "structureType": "numbered",
        "length": 400,
        "content": [
          "1. 카피라이팅: 원본 문구 작성 및 스타일 개선",
          "2. 지식 기반 답변(KI-NLP): 디지털 아카이브를 활용한 전문 정보 제공",
          "3. 텍스트 분류: 감정 분석 및 문서 클러스터링",
          "4. 코드 생성: 자연어 프롬프트를 활용한 프로그래밍 언어 작성"
        ],
        "title": "4. LLM의 실무 응용 분야"
      },
      {
        "structureType": "mixed",
        "length": 350,
        "content": [
          "제로샷 학습(Zero-shot): 별도 훈련 없이 프롬프트에 응답",
          "퓨샷 학습(Few-shot): 소수의 예시를 통한 성능 최적화",
          "미세 조정(Fine-tuning): 특정 도메인 데이터를 활용한 파라미터 조정"
        ],
        "title": "5. LLM의 학습 모델 및 훈련 방식"
      }
    ],
    "faq": {
      "title": "LLM에 대해 자주 묻는 질문(FAQ)",
      "length": 300,
      "content": [
        "Q: LLM과 일반 챗봇의 가장 큰 차이점은 무엇인가요? / A: LLM은 트랜스포머 구조와 거대 파라미터를 통해 단순 규칙이 아닌 문맥의 의미를 깊이 있게 이해합니다.",
        "Q: LLM의 할루시네이션(환각) 현상은 왜 발생하나요? / A: 모델이 확률적으로 다음 단어를 예측하는 과정에서 사실과 다른 정보를 생성할 수 있으며, 이는 미세 조정을 통해 개선 중입니다."
      ]
    },
    "conclusion": {
      "length": 300,
      "content": [
        "LLM은 업무 환경 혁신과 대화형 AI의 진화를 이끄는 파괴적 기술",
        "시청각 교육 및 자율주행 등 새로운 영역으로의 확장 가능성",
        "기술적 한계를 극복하며 인간의 성능에 가까워지는 LLM의 미래 주목"
      ],
      "cta": {
        "action": "",
        "link": "",
        "serviceName": "",
        "target": ""
      }
    }
  },
  "preValid": {
    "layoutSize": "large",
    "sectionCount": 5
  }
}
```