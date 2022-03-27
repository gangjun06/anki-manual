# 글자 크기

텍스트 크기가 올바르지 않은 경우 다음 두 가지 환경 변수를 사용할 수 있습니다.:

- ANKI_NOHIGHDPI=1 QT의 High DPI 지원의 일부가 꺼집니다

- ANKI_WEBSCALE=1 는 메뉴바등의 인터페이스 요소는 그대로 두고, Anki 의 Web 뷰(뭉치 리스트, 스터디 화면등)의 크기을 변경합니다. 1을 1.5 또는 0.75와 같은 원하는 비율로 변경합니다.

Windows 에서는, Anki 를 보다 간단하게 시작할 수 있도록 배치 파일에 이러한 내용을 추가할 수 있습니다.
예를 들어 바탕 화면에 startanki.bat라는 이름의 파일을 다음 텍스트로 생성합니다:

    set ANKI_WEBSCALE=0.75
    start "Anki" "C:\Program Files\Anki\anki"

저장 후 파일을 더블 클릭하여 Anki를 시작할 수 있습니다.
