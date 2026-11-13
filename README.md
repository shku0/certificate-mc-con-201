# MC-Con-201 Flashcards App

Salesforce Marketing Cloud Next Consultant (MC-Con-201) 자격증 시험 대비를 위한 웹 기반 플래시카드 애플리케이션입니다. 별도의 설치 없이 브라우저 환경에서 즉시 실행 가능하며, 커스텀 문제 데이터를 쉽게 로드하여 학습할 수 있습니다.

## 주요 기능
* 학습 모드 지원
  * 테스트 모드: 클릭 시 정답과 해설을 확인할 수 있는 3D 플래시카드 모드
  * 학습 모드: 문제와 해설을 동시에 나열하여 빠르게 읽고 넘기는 스크롤 모드
* 인터페이스 제어
  * 모바일 환경: 좌우 스와이프 제스처를 통한 카드 이동 지원
  * 데스크톱 환경: 키보드 방향키(이동) 및 스페이스바(뒤집기) 지원
* 커스텀 데이터 로드
  * JSON 포맷의 문제 세트를 웹 화면에서 직접 입력하여 전체 학습 데이터 즉시 교체 가능

## 사용 방법
1. 우측 상단의 [데이터 불러오기] 버튼을 클릭합니다.
2. 텍스트 입력 창에 공유받은 문제 세트(JSON 포맷)를 붙여넣습니다.
3. [적용하기] 버튼을 누르면 입력한 데이터가 로드되어 학습을 시작할 수 있습니다.

### 데이터 포맷 양식
새로운 문제 데이터를 추가할 경우, 아래의 JSON 배열 형식을 준수하여 작성해야 합니다.

```json
[
  {
    "qNum": 1,
    "front": "How to generate a segment matching the campaign brief from Campaign Creation Agent?\n\nA. Create new\nB. Ask Agent in chat\nC. Review draft in Segment Creation",
    "answer": "정답: C. Review draft in Segment Creation",
    "explanation": "Agent가 캠페인 컨텍스트를 바탕으로 이미 세그먼트 초안을 자동 생성하므로, Segment Creation에서 검토 및 수정만 하면 됩니다."
  }
]
