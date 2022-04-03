# 설정

<!-- toc -->

설정은 Windows/Linux의 도구 메뉴 또는 Mac의 Anki 메뉴에서 사용할 수 있습니다.

## 기본

**그래픽 드라이버**  
Ank는 화면에 앱을 띄우기 위한 그래픽 드라이버가 필요합니다.
하드웨어 및 소프트웨어 구성에 따라 사용하시는 컴퓨터에 가장 적합한 드라이버는 다를 수 있습니다.
ANGLE 및 OpenGL은 소프트웨어 옵션보다는 성능이 우수하지만 일부 시스템에서는 올바르게 작동하지 않을 수 있습니다.
Mac에서는 OpenGL사용을 권장합니다.

**오디오 재생버튼 보이기**  
오디오가 있는 카드의 학습 화면에 클릭 가능한 재생 버튼이 표시되는지 여부.

**응답할 때 오디오 중단**  
카드에 답 보기를 할 때 현재 재생 중인 오디오파일을 정지할지를 설정합니다.

**클립보드 이미지 PNG로 붙여넣기**  
기본적으로 Anki는 클립보드 이미지를 JPG 파일로 붙여넣어 디스크 공간을 절약합니다.
하지만 원하는 경우 이 옵션을 사용하여 PNG 이미지로 붙여넣을 수 있습니다.
PNG 이미지는 투명한 배경을 지원하며 무손실이지만 일반적으로 파일 크기가 훨씬 커집니다.

**Paste without Shift strips formatting**  
기본적으로는 <kbd>Shift</kbd> 키를 누르지 않는 한 붙여넣을 때 굵은 글씨 및 색상과 같은 형식이 유지됩니다.
이 옵션은 사용할 시 반대로 작동합니다.

**야간 모드**  
야간 모드에서는 Anki가 검은 배경에 카드를 흰색 텍스트로 표시합니다.
일부 카드 템플릿은 이 옵션을 활성화한 상태에서 올바르게 작동하기 위해 수정해야 할 수 있습니다.
자세한 내용은 [야간 보드 템플릿 스타일링](styling.html#야간-모드))을 참조하십시오.

**카드를 추가할 때, 현재 뭉치에 넣음**  
Controls how note types and decks interact. The default of "When adding, default to current deck" means that Anki saves the last-used note type for each deck and selects it again then next time you choose the deck (and, in addition, will start with the current deck selected when choosing Add from anywhere). The other option, "Change deck depending on note type," saves the last-used deck for each note type (and opens the add window to the last-used note type when you choose Add). This may be more convenient if you always use a single note type for each deck.

노트 유형과 뭉치가 상호 작용하는 방식을 제어합니다.
기본 설정인 "카드를 추가할 때, 현재 뭉치에 넣음"은 Anki가 각 뭉치에 대해 마지막으로 사용한 노트 유형을 저장한 다음
카드 추가 선택창에서 뭉치를 선택하면, 해당 노트 유형을 불러옵니다(또한 어디에서나 추가를 할 때 현재 덱이 선택됩니다).
다른 옵션인 "노트 유형에 따라 뭉치 바꾸기"는 각 노트 유형에 대해 마지막으로 사용한 뭉치를 저장합니다
(그리고 추가를 선택하면 마지막으로 사용한 노트 유형에 대한 추가 창이 열립니다).
이 방법은 각 덱에 대해 항상 하나의 노트 유형을 사용하는 경우에 더 편리할 수 있습니다.

**Default search text (기본 검색 텍스트)**
Allows you to customize the starting search text in the browser (eg, to start with "deck:current").
탐색에서의 기본 검색 입력어를 설정할 수 있습니다. (예시: "deck:current")

**User interface size (UI 크기)**
인터페이스 크기가 작으면 이 설정을 통하여 확대하여 볼 수 있습니다.

## 일정 재조정

**답 버튼 위에 다음 복습시점 표시**  
얼마나 후에 카드를 다시 학습한지 알고 싶을때 유용합니다.

**남은 카드 개수를 복습 화면에 표시**  
이 옵션을 꺼서 화면 아래의 남은 카드 카드 개수를 없엘 수 있습니다.

**복습하지 않은 긴 주기의 배운 카드 보기**  
2.1 스케줄러가 유효한 경우에만 표시됩니다.
보통은 1일 이상의 주기를 가진 학습 카드는 일반 학습 후 표시됩니다. 체크하면 Anki가 일반 리뷰 전에 보여 줍니다.

**Legacy timezone handling**  
이 문서를 확인해주세요:
<https://faqs.ankiweb.net/timezone-handling-changes.html>

**V3 Scheduler**  
Anki V3 스케쥴러:  
<https://faqs.ankiweb.net/the-2021-scheduler.html>

**새 카드와 복습 카드 섞기**:
v1/v2 스케줄러가 작동하는 경우에만 표시됩니다.
이 옵션에서 새로운 카드가 표시되는 타이밍(모든 복습과와 학습 전, 후)을 제어합니다.

**하루가 시작되는 시각**
Anki가 다음 날 카드를 언제 표시해야 하는지 제어합니다.
기본 설정인 '4시간 뒤'는 자정 무렵에 학습하는 경우 한 세션에 이틀 분량의 카드가 표시되지 않도록 합니다.
만약 매우 늦게 일어나거나 매우 일찍 일어난다면, 이 설정을 사용하여 학습 시간을 조정할 수 있습니다.
또한 1일의 경계를 넘는 카드는 리뷰 카드와 같이 [예정된 날짜](./deck-options.md#day-boundaries)에 표시됩니다.

**앞당겨 공부하기 제한**  
현재 뭉치에서 학습 중인 카드 외에 더 이상 학습할 것이 없을 때 Anki가 어떻게 작동할지 설정합니다.
기본 설정인 20분에서는 학습할 카드가 더이상 없을때, 학습까지 남은 시간이 20분 미만인 카드를 표시합니다.
이 값을 0으로 설정하면 Anki는 항상 카드의 학습시간이 돌아올때까지 기다리며
나머지 카드를 복습할 시간이 될 때까지 축하 화면을 표시합니다.

**시간 제한**  
타임박스는 30분간의 학습 세션과 같이 긴 학습을 더 작은 조각으로 분할하여 집중할 수 있도록 도와주는 기술입니다.
타임박스 시간 제한을 0분이 아닌 분수로 설정하면 Anki는 지정된 시간 제한 동안 학습할 수 있는 카드 수를 주기적으로 표시합니다.

## 테트워크

네트워크 탭에는 AnkiWeb과의 동기화 관련 옵션이 있습니다.

- 로그인 되어 있을때, 이곳에서 로그아웃을 할 수 있습니다.
- '다음 동기화할 떄, 한 방향으로만 변경사항 적용' 옵션이 활성화되면 다음 동기화에서 업로드 또는 다운로드 여부를 묻습니다.
  이 기능은 실수로 일부 변경을 한 경우 AnkiWeb에 있는 이전 버전으로 덮어쓰기를 원할 때 유용합니다.
