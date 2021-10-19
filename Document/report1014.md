### 주간 보고서

#### 박찬우
- 플레이어 씬의 노트3줄 구현, 어려운 부분이 있어 유튜브 및 깃 자료 검색, 공부
프로젝트 안드로이드 빌드 및 빌드 환경에서 오류 확인 및 수정할 점 정리
- 21일 발표를 위한 발표 내용에 들어갈 부분에 대해 논의 및 지난 발표를 토대로 피드백
- 21일 전까지의 구현 내용과 계획에 대해 논의

#### 박세진
- 점수 시스템 구현 (ScoreManager 스크립트생성)
기본스코어:currentScore=0, 스코어증가량: increaseScore=10으로 생성
노트 판정(perfect,good,bad,miss)에 따라 다른 점수가 증가하도록 increaseScore에 weight[판정]을 곱함 
t_currentScore에 지속적으로 increaseScore를 더하고 text로 변환
점수가 증가할때마다 간단한 크기조절을 통한 애니메이션추가
- 콤보 쌓기 구현.(ComboManager 스크립트 생성)
기본콤보:currentCombo=0으로 생성
콤보이미지와 오브젝트를 시작시에 비활성화
IncreaseCombo(int p_num=1) 생성
currentCombo에 p_num을 지속적으로 더하고 텍스트로 변환
currentCombo가 3일 때부터 콤보이미지,오브젝트를 활성화
currentCombo를 0으로 만들고 비활성화하는 ResetCombo() 생성
ScoreManager 스크립트에서 ComboManager를 참조함
IncreaseScore(int p_JudgementScore)함수에 콤보증가, 콤보 점수계산 기능 추가
int t_increaseScore = increaseScore + t_bonusComboScore;
t_increseScore부분 수정

#### 박예진
- 타이틀 씬과 곡 선택 씬에 쓰일 임시 BGM 추가.
https://assetstore.unity.com/packages/audio/music/casual-game-bgm-5-135943
- 간단한 기능만 구현되어 있던 UI들에 그래픽 파트가 제작한 이미지 넣기.
- 플레이에 쓰일 4곡 수집 후 버튼 선택 시 미리듣기 가능하도록 구현.
버튼 선택 시 곡 선택 씬의 원래 BGM과 충돌하여 버튼 선택 시 - >오디오 소스 play(), 곡 선택 BGM stop().
다른 노래 미리듣기 재생 시에도 다른 버튼을 누르면 현재 재생되던 곡이 멈추고 다른 곡의 미리듣기가 재생되도록 함. 모든 오디오소스의 인스펙터 창에서 곡 선택 BGM이 멈출 수 있도록 On Click에 추가.


#### 김정민
- 플레이 씬 구성요소인 노트와 노트 버튼, 노트 컨테이너(임시), 판정 이펙트 이미지 제작.
노트, 긴노트(꼬리), 노트 버튼, 노트 컨네이터 이미지(배경 포함), 판정 이펙트 제작.
플레이 씬 예시 이미지 3가지.( 노트 컨네이너에 기울기 적용, 미적용)
- 곡 선택 씬의 곡 정보창 틀과 배경 이미지를 제작하고 저번 주에 만든 곡선택 버튼의 색감을 수정.
배경 이미지 (알파벳 패턴), 수정된 곡 선택 버튼 전체적인 색 채도를 올리고 , 글씨 색을 배경보다 조금 더 밝게 수정, 곡 선택 씬 예시 이미지 제작.
