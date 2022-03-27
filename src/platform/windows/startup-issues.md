# 윈도우 셋업 문제

<!-- toc -->

## 에러는 없지만, 앱이 켜지지 않음

최근 Anki가 에러메시지를 표시하지 않고 나타나지 않는다는 제보가 있었습니다.
이러한 상황이 발생하면 다음 중 하나를 시도할 수 있습니다:

- [최신 windows-qt6 beta](https://apps.ankiweb.net/downloads/beta/?C=N&O=D) (애드온 호환성 문제가 있는 경우 qt5를 사용해 보세요)
- 또는 [adjusting your decimal separator](https://forums.ankiweb.net/t/windows-update-broke-anki/1822/75)
- 또는 이전 버전인 `2.1.35-alternate`를 사용할 수 있습니다.

## 윈도우 업데이트

Anki를 실행할때, 다음과 같은 메세지가 표시되는 경우가 있습니다.

- _Error loading Python DLL_
- _The program can't start because api-ms-win.... is missing_
- _Failed to execute script runanki_
- _Failed to execute script pyi_rth_multiprocessing_
- _Failed to execute script pyi_rth_win32comgenpy_

일반적으로 이러한 오류는 컴퓨터에 Windows 업데이트 또는 Windows 라이브러리가 없기 때문입니다.

Windows 업데이트를 열고 시스템에 모든 업데이트가 설치되어 있는지 확인하세요.
설치가 필요한 경우는, 설치 후에 컴퓨터를 재시작하여 주세요.

## 윈도우 7/8

윈도우 7/8 에서는, 추가 업데이트를 수동으로 설치해야 할 수 있습니다.

- <https://www.microsoft.com/en-us/download/details.aspx?id=48234>
- <https://aka.ms/vs/15/release/vc_redist.x64.exe>
- <http://www.catalog.update.microsoft.com/Search.aspx?q=kb4474419>
- <http://www.catalog.update.microsoft.com/Search.aspx?q=kb4490628>

## 비디오 드라이버 문제

[드라이버 문제](./display-issues.md) 글을 확인하여 주세요.

## 다중 디스플레이

_LoadLibrary failed with error 126_ 이 표시되면 Anki가 [다중 디스플레이](https://forums.ankiweb.net/t/error-126-on-open-anki-desktop/13967)에 문제가 있는 툴킷이 원인일 수 있습니다.

## 백신 / 방화벽 프로그램

컴퓨터에 써드파티 소프트웨어가 있으면 Anki가 로드되지 않을 수 있습니다.
Anki를 예외에 추가하거나 백신/방화벽을 일시적으로 비활성화하여 작동하는지 확인할 수 있습니다.

## 관리자 접근

일부 사용자는 Anki 아이콘을 마우스 오른쪽 버튼으로 클릭하고 `관리자로 실행`을 선택할 때 Anki가 실행되지 않았다고 제보했습니다.
Anki는 모든 데이터를 사용자 폴더에 저장하므로 관리자 권한이 필요하지 않습니다.
그러나 다른 방법을 전부 해 보았을땐 시도할 수 있습니다.

## 업데이트후 여러개의 Anki

업데이트 프로세스로 인해 여러개의 Anki가 설치된 경우 (`C:\Program Files\Anki` 및 `C:\Program Files (x86)\Anki`)
동작하지 않는 상태가 되어, Anki가 에러 메세지의 없이 작동하지 않는 경우가 있습니다.

설치된 모든 Anki를 제거해 보세요. Windows의 `앱 & 기능` 설정 메뉴를 사용하거나
각 Anki 프로그램 폴더에서 `uninstall.exe`를 실행하여 제거할 수 있습니다.
그 후 새로운 Anki를 다시 설치합니다.

## 디버깅

콘솔에서 Anki 를 실행하면, 에러에 관한 더욱 상세한 정보가 표시됩니다.
최신 버전의 Anki를 설치하고 모든 Windows 업데이트가 설치되어 있는지 확인한 후
Anki를 직접 실행하는 대신 `Win+R`을 사용하여 cmd.exe를 입력합니다. 콘솔 창이 뜨면

```bat
cd \program files\anki & anki-console
```

아마 Anki는 이전처럼 열리지 않을 것이지만, 문제의 원인을 분석할 수 있습니다.

## 다른 모든 것이 실패했을 경우

위의 방법들을 시도해도 Anki를 실행할 수 없는 경우에는, 2가지 옵션이 있습니다:

- [파이썬으로 실행](https://faqs.ankiweb.net/running-from-python.html) 을 시도하여 보세요.
- 2.1.35-alternate 또는 2.1.15 과 같은 이전 버전을 사용하여 보세요.
