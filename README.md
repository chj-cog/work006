# 원하는 포즈로 이미지 만드는 도구

## 도구 설명
- 참조 사진에서 OpenPose로 관절(골격) 정보를 뽑고, 이를 ControlNet 조건으로 넣어 Stable Diffusion이 같은 자세의 인물을 만듭니다.

## 사용법
1. GitHub의 `pose_tool.ipynb`를 Colab에서 엽니다.
2. GPU 런타임에서 모델 로드, 포즈 추출, 생성, 저장 셀을 순서대로 실행합니다.
# ---------- 실행: 프롬프트만 바꿔 가며 쓰면 됩니다 ---------- PROMPT = "" <- 이 안에 프롬프트 적기
3. `samples/`에서 참조 사진(`pose_XX.png`)과 결과 이미지(`output_XX.png`)를 확인합니다.

## 테스트 결과
<!-- 직접 실행하고 관찰한 결과로 채우세요. 사용한 프롬프트 전체는 prompts.md에 적습니다. -->
- 포즈 1: 슈퍼히어로랜딩 → 프롬프트: "a female barista" → 결과: (팔 위치는 맞음 / 팔이 네개, 발은 표현 안됨)
- 포즈 1: 슈퍼히어로랜딩 → 프롬프트: "a female athlete in a red and black tracksuit doing a superhero landing pose on a concrete rooftop" → 결과: (잘 나옴 / 한쪽 무릎이 떠있음)
- 포즈 2: 손하트 → 프롬프트: "worker at factory " → 결과: (두 팔과 머리는 맞음 / 손하트 부분이 잘 만들어지지 않음)
- 포즈 2: 손하트 → 프롬프트: "a female barista " → 결과: (두 팔과 머리는 맞음 / 손하트 부분이 잘 만들어지지 않음)

## 한계
<!-- 테스트 중 실제로 관찰한 한계를 적으세요. -->
- (관찰한 한계)
