⚠️ 이전 This-is-my-study-archive는 공사중..

📜: Paper link 🧑🏻‍💻: Developer blog & Github link 🤗: HuggingFace 🗞️: News

---
# 2025
## 🌱 March
<details>
    <summary>1st week</summary>
    
- 🤗 [kakaocorp] [kanana-nano-2.1b-instruct](https://huggingface.co/kakaocorp/kanana-nano-2.1b-instruct)
    - **Kanana**: 카카오에서 개발한 한국어-영어 이중 언어 모델
    - **Kanana-Nano-2.1B**: 기본, 지시, 임베딩, 함수 호출, RAG 등
        - 최첨단 모델과 유사한 크기 대비 낮은 연산 비용
        - 고품질 데이터 필터링, 단계적 사전 훈련, 심층 업스케일링, 가지치기 및 증류 등의 기술을 사용해 효율적인 학습 진행
        - 후속 학습 과정에서 지도식 미세 조정 및 선호도 최적화를 통해 사용자와의 원활한 상호 작용 향상
        - 사전 학습 및 후속 학습 과정에서 Kakao 사용자 데이터는 포함되지 않음

- 🧑🏻‍💻 [OpenAI] [Introducing GPT-4.5](https://openai.com/index/introducing-gpt-4-5/)
    - 비지도 학습을 확장하여 지식 정확도, 직관력 향상
    - 주요 기능: function calling, Structured Outputs, streaming, system messages
    - 사실성 + 감성지능(EQ) ↑, hallucination(환각) 발생률 ↓
      <details>
          <summary>비교</summary>
          
        - **비추론 모델**(GPT-4o)과 비교했을 때: 성능이 좋음
        - **추론 모델**(OpenAI o1, o3-mini)과 비교했을 때: 일반 지식과 창의적 작업에서는 더 좋지만, 논리적 추론과 복잡한 문제 해결에서는 떨어짐
      </details>

- 🧑🏻‍💻 [ANTHROPIC] [Claude 3.7 Sonnet and Claude Code](https://www.anthropic.com/news/claude-3-7-sonnet)
    - **Claude 3.7 Sonnet**: 빠른 응답과 심층적 사고(step-by-step thinking)를 결합한 하이브리드 추론 모델로, API를 통해 thinking time 조절 가능
    - SWE-bench, TAU-bench에서 최고 성능 기록(코드 이해/수정/테스트 자동화 능력 강화)
    - **Claude Code** 출시: 코드 검색, 편집, 테스트 실행, GitHub 커밋/푸시 가능, 대규모 리팩토링 및 디버깅 지원
    - API 활용: 모델이 사고에 사용할 토큰 수(N)를 직접 설정하여 속도/비용/정확도 간 최적화

- 🧑🏻‍💻 [langgenius] [dify](https://github.com/langgenius/dify/releases/tag/1.0.0)
    - **Dify v1.0.0**출시: AI 애플리케이션 확장을 위한 플러그인 시스템 도입
    - 미니맵의 팬 및 줌 기능, 통합 추론 모델, Docker SSRF 설정 개선, HNSW 벡터 색인 등
    - `.difypkg` 포맷 지원, 워크플로우 에이전트 노드 추가로 사용자 정의 기능 강화
    - Docker 배포 → `docker-compose.yaml`
    - **Dify 마켓플레이스** 출시, 플러그인 공유 및 다운로드 가능
 
- 🧑🏻‍💻 [LandingAI] [Agentic Document Extraction](https://landing.ai/agentic-document-extraction)
    - **Agentic Document Extraction**: 시각적 맥락을 활용하여 복잡한 문서(의료 서식, 재무 보고서 등)에서 데이터를 정확하게 추출하는 인공지능 기반 솔루션
    - 표, 차트, 체크박스 등 다양한 시각적 요소를 정확하게 인식
    - 시각적 근거를 제시 → 추출 결과의 신뢰성을 높임, 다양한 산업 분야(의료, 물류, 금융, 법률 등)에 적용 가능
    - API를 통해 레이아웃 인식, 이미지 해석 등의 기능을 제공하여 효율적인 문서 처리 및 의사결정 지원을 가능하게 함
    - [Test Link](https://va.landing.ai/demo/doc-extraction)

- 🤗 [Qwen] [QwQ-32B](https://huggingface.co/Qwen/QwQ-32B)
    - **QwQ-32B**: 추론 능력을 갖춘 중간 규모의 언어 모델로, 기존 모델보다 어려운 문제 해결에 강점을 보임
    - RoPE, SwiGLU, RMSNorm, QKV bias 적용된 Transformer 기반, 64층 구조와 32.5B 파라미터 보유
    - 최대 131,072 토큰의 긴 컨텍스트 지원, Supervised Fine-tuning 및 RL 기반 후처리 수행
    - 최적화된 성능을 위해 **온도(0.6), TopP(0.95), TopK(20~40) 설정** 및 특정 태그 활용 권장
    - 배포 시 vLLM 사용 추천, 긴 컨텍스트 필요 시 `rope_scaling` 설정 추가 가능
    - [블로그](https://qwenlm.github.io/blog/qwq-32b/)

- 🤗 [dragonkue] [snowflake-arctic-embed-l-v2.0-ko](https://huggingface.co/dragonkue/snowflake-arctic-embed-l-v2.0-ko)
    - **snowflake-arctic-embed-l-v2.0**: 한국어 검색 성능을 향상시키기 위해 추가 학습된 SentenceTransformer 모델
    - 최대 토큰 길이 8192, 1024차원 임베딩을 생성하며 코사인 유사도를 사용하며 AI Hub의 다양한 한국어 기계독해 데이터로 학습됨
    - MTEB 벤치마크에서 SOTA 성능을 기록, MIRACL, AutoRAGRetrieval 등 여러 한국어 검색 평가에서 우수한 성능을 보임
    - 최대 토큰 길이가 1300개로 제한되어 있어 긴 문서 검색 시 한계가 있으며, 더 긴 문서는 gte-multilingual-base, KURE-v1 등의 모델 활용 권장

- 🤗 [dnotitia] [DNA-R1](https://huggingface.co/dnotitia/DNA-R1)
    - **DNA-R1**: Microsoft Phi-4 기반 한국어 최적화 모델로, DeepSeek-R1 방식의 강화학습을 적용하여 수학, 코딩, 논리적 사고에서 뛰어난 성능 발휘
    - 한국어 비논리 데이터 → DeepSeek-R1 방식의 한국어 논리 데이터 → GRPO 강화학습을 통한 최적화 3단계 진행
    - 14B 모델임에도 KMMLU, KoBEST, GSM8K 등의 벤치마크에서 대형 모델과 경쟁하는 높은 성능 기록
    - 한국어 중심 CoT 추론, 자기 검증, 다단계 문제 해결, <think>, <answer> 태그 활용 가능

- 📜 [HKUST(GZ)] [Atom of Thoughts for Markov LLM Test-Time Scaling](https://arxiv.org/pdf/2502.12018)
    - **Atom of Thoughts (AOT)**: LLM의 추론 성능 향상을 위한 테스트 시간 확장 기법, 불필요한 과거 정보 처리 없이 순수한 추론에 계산 자원 집중
    - 마르코프 프로세스와 유사한 메모리리스 전이 방식 사용 → 문제를 독립적인 atomic questions으로 분해 후 해결
    - 질문을 Directed Acyclic Graph 로 표현하고, 독립적인 하위 질문으로 축소하는 과정을 반복하여 직접 해결 가능한 상태로 변환
    - 장점: 기존 방법과 달리 history 축적 없이 현재 상태만 활용해 불필요한 연산 낭비 방지 및 추론 성능 극대화
    - HotpotQA에서 GPT-4o-mini 적용 시 F1 80.6% 기록, o3-mini 대비 3.4%, DeepSeek-R1 대비 10.6% 향상
</details>
