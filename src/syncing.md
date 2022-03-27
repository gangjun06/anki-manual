# AnkiWeb 연동

<!-- toc -->

`AnkiWeb`은 콜렉션을 기기간 동기화해주고 온라인에서 학습할 수 있게 해주는
서비스 입니다. 아래의 단계를 따라하기전, [무료 회원가입](https://ankiweb.net/) 을 하여 주세요.

## 소개 영상
빠르게 동기화에 알고싶다면,  [동기화 소개 영상](https://www.youtube.com/watch?v=YkiM4DPzSVc&list=PLGgmaKOIHykFoomqkBJAyGiDQ2kyiuTao&yt:cc=on). 을 확인하세요.

## 셋업

장치간 동기화를 시작할려면 메인화면 오른쪽 상단의 동기화 버튼(단축키 `Y`)을 눌러주세요.
등록 과정에서 작성한 AnkiWeb 아이디와 비밀번호를 입력하는 창이 나타납니다.

컬렉션을 처음 동기화하면 Anki에서 업로드 또는 다운로드 여부를 묻습니다.
컴퓨터에 카드가 있고 AnkiWeb 계정이 비어 있는 경우 "업로드"를 선택하여
데이터를 AnkiWeb으로 보냅니다. 다른 장치에서 AnkiWeb에 카드가 있고 컴퓨터에
카드가 없는 경우 "다운로드"를 선택하여 빈 로컬 컬렉션을 AnkiWeb에 있는 카드로 대체합니다.
양쪽 디바이스에 다른 카드가 있는 경우 데이터 손실을 방지하기 위해 [추가 작업이 필요합니다](#병합-충돌)

초기 단방향 동기화가 완료되면 Anki는 몇 가지 예외를 제외하고 여러 기기에서의 변경 사항을
자동으로 병합할 수 있습니다.

1대의 기기으로 Anki를 사용하고 있는 여러명의 유저가 각각 유저의 프로필을 만들어 사용하는 경우, 각 유저는 동기화하는 독자적인 AnkiWeb 계정을 작성할 필요가 있습니다. 하나의 AnkiWeb 계정으로 여러 프로필을 동기화하려고 하면 데이터가 손실됩니다.

## 자동 동기화

동기화가 활성화되면 컬렉션이 닫히거나 열릴 때마다 Anki가 자동으로 동기화됩니다. 수동으로 동기화하려면 Anki 환경설정에서 자동 동기화를 사용 불가능으로 설정할 수 있습니다.

## 버튼 색

일반 동기화가 필요한 경우 동기화 버튼이 파란색으로, 전체 동기화가 필요한 경우 빨간색으로 변경됩니다.

## 미디어

관련 영상: <https://www.youtube.com/watch?v=phP9GGG-PxY>

Anki는 노트에 사용되는 소리와 이미지를 동기화합니다. 미디어 폴더에 미디어가 추가 또는 제거되었을 때는 알 수 있지만 기존 파일을 추가 또는 제거하지 않고 편집했는지 여부는 알 수 없습니다. 편집 내용을 확인하려면 파일 추가 또는 삭제도 필요합니다.

USB 플래시 드라이브에서 Anki를 실행하는 경우 NTFS 파일 시스템을 사용해야 합니다. Anki는 FAT32 파일 시스템에서 미디어 변경을 감지하지 못할 수 있습니다.

## 충돌

관련 영상: <https://www.youtube.com/watch?v=UEAcpfMQnjo>

통상적인 상황에서는 학습과 노트 편집을 병합할 수 있으므로 동기화하기 전에  2개의 다른 기기에서
학습 또는 편집하면 Anki가 두 위치 모두에서 변경 내용을 보존합니다. 같은 카드를 2개의 다른 기기에서
학습했을 경우, 양쪽의 학습가 리비전 이력에 표시되며, 카드는 최근 대답한 상태로 유지됩니다.

Anki가 병합할 수 없는 몇 가지 상황이 있습니다. 이는 주로 메모 형식과 관련이 있습니다. 새 필드 추가 또는 카드 템플릿 제거 등이 있습니다. 병합할 수 없는 작업을 수행하면 Anki가 경고를 표시하고 작업을 중단할 수 있는 옵션을 제공합니다. 계속하도록 선택할 경우 컬렉션을 다음에 동기화할 때 단방향 동기화가 강제됩니다.

또는 동기화 중에 특정 문제가 감지되면 단방향 동기화로 강제됩니다. 동기화 문제가 계속 발생할 경우 지원 사이트에 게시해 주십시오.

단방향 동기화가 필요한 경우 동기화 할 시 컬렉션을 AnkiWeb에서 다운받을지 AnkiWeb에 업로드할지를 선택해야 합니다. 양쪽에서 변경이 이루어진 경우 한쪽 기기의 변경만 보존할 수 있습니다.

`업로드`를 선택하면 로컬 디바이스의 콘텐츠가 AnkiWeb으로 전송됩니다. 그런 다음 다른 기기에서 동기화할 때에는 `다운로드`를 선택하여 해당 컨텐츠의 복사본을 가져오도록 해야 합니다.

`다운로드`를 선택하면 로컬 변경이 AnkiWeb에 있는 데이터로 대체됩니다.

모든 기기가 동기화되면 이후 동기화는 서로다른 기기의 변경을 자동으로 병합하는 일반 동작으로 돌아갑니다.

전체 업로드 또는 다운로드를 강제하는 경우 (예를 들어 실수로 한쪽 뭉치를 삭제하여 삭제를 동기화하는 것이 아니라 뭉치를 복원하는 경우), `툴` -&gt; `설정`-&gt; `네트워크` -&gt; `다음 동기화 때, 한 방향으로 변경 사항 적용하기` 체크박스를 켜고 정상적으로 동기화할 수 있습니다. (사용할 쪽을 선택할 수 있습니다.)

단방향 동기화를 강제하면 카드 동기화에만 영향을 줍니다. 미디어는 정상적으로 동기화됩니다. AnkiWeb에서 삭제할 파일이 있는 경우 먼저 클라이언트가 완전히 동기화되어 있는지 확인하십시오. 동기화가 최신 상태가 되면 (미디어 확인 기능을 통해) 삭제한 파일은 다음 동기화 시 AnkiWeb에서 제거됩니다.

## 병합 충돌

Because the [first sync](#setup) can only sync changes in one
direction, if you have added different content to different devices or
profiles before setting syncing up, content on one device will be lost
if you overwrite it with the content from the other device. With some
work, it is possible to manually merge data into a single collection.

Start by taking a backup on each device/profile, in case something goes
wrong. With the computer version you can use File&gt;Export to export
"all decks" with scheduling information and media files included, and
save the file somewhere safe. In AnkiMobile, the Add/Export button on
the decks list screen will let you export all decks with media.

Next, if one of your devices is a mobile device, synchronize it first.
If there’s a conflict, choose "upload" to overwrite any existing data on
AnkiWeb with the data from your mobile device. If both devices/profiles
are on your computer, synchronize the device/profile with the most
number of decks first.

Now return to the other device/profile. If automatic syncing is enabled,
a message may pop up asking if you want to upload or download. Click the
cancel button - we don’t want to sync yet.

Once you’re looking at the deck list, click the cog icon next to the
first deck, and choose "export". Export the content with scheduling
information and media included, and save the .apkg file somewhere. Now
you’ll need to repeat this for each top-level deck.

Once all top-level decks have been exported, click the sync button at
the top right, and choose "download", which will overwrite the local
content with the content you synced from your other device.

You can now use File&gt;Import to import the .apkg files you exported
earlier, which will merge the exported content with the existing
content, so everything will be in one place.

## 방화벽

Anki는 동기화할 떄에는 HTTPS 전송이 가능해야 하고 `ankiweb.net, ankiweb.net, sync2.ankiweb.net`에 접속하여 동기화할 수 있어야 합니다.
이러한 도메인은 시간이 지남에 따라 변경될 수 있으며 이들이 가리키는 IP 주소도 변경될 수 있습니다. 
따라서 향후 방화벽규칙을 갱신해야 할 가능성을 줄이기 위해 `*.ankiweb.net` 에 와일드카드접근을 허용하는 것을 권장합니다.

컴퓨터에 방화벽이 있는 경우 Anki에 대한 예외를 추가해야 합니다. 직장 또는 학교 네트워크에 접속하고 있는 경우는, 네트워크 관리자에게 문의해 주세요.

## 프록시

인터넷에 접속하기 위해 프록시가 필요한 경우 Windows 또는 MacOS에 있는 경우 Anki는 자동으로 시스템 프록시 설정을 선택하고 다른 플랫폼에 있는 경우 `HTTP_PROXY` 환경변수를 적용합니다.

Anki는 프록시가 수동으로 구성되고 암호가 필요하지 않은 경우에만 시스템 설정을 선택할 수 있습니다. 시스템에서 자동 프록시 설정을 사용하는 경우 또는 사용자 이름과 비밀번호가 필요한 프록시를 사용하는 경우 프록시 설정을 Anki에게 수동으로 알려야 합니다.

Anki에게 프록시 설정을 알리려면 프록시 서버를 가리키는 `HTTPS_PROXY` 환경변수를 정의합니다.
다음과 같이 표시됩니다:

    http://user:pass@proxy.company.com:8080

사용자 이름 또는 비밀번호에 특수문자 `@`(예를 들어 `user@workdomain.com`)가 포함되어 있는 경우
다음과 같이 `@`를 `%40`으로 변경해야 합니다.

    http://user%40workdomain.com:pass@proxy.company.com:8080

Anki 2.0에서는 `HTTPS_PROXY`가 아닌 `HTTP_PROXY`가 검색됩니다.

Windows에서 환경 변수를 설정하려면 [구글검색](https://www.google.com/search?q=윈도우%20환경변수%20설정) 을 참고하세요.

Mac에서 환경변수를 설정하려면 [이 링크](<http://stackoverflow.com/questions/135688/setting-environment-variables-in-os-x) 를 참고하세요.

보안 접속을 가로채거나 자체 인증서를 사용하여 네트워크가 잠기면, Anki가 SSL 에러를 발생시킬 가능성이 있습니다. 이러한 환경에서는 [에드온](https://ankiweb.net/shared/info/878367706)을 사용하여 오류를 회피할 수 있습니다.

대체 해결법은 로컬 프록시 서버를 설치하고 해당 프록시 서버를 일반 프록시 서버로 지정하는 것입니다. 그런 다음 Anki에게 로컬 프록시를 사용하도록 지시할 수 있습니다. 그러면 요청이 일반적으로 사용하는 프록시로 리디렉션됩니다.
