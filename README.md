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
 </details>
