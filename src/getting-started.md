# 시작하기

<!-- toc -->

## 설치 및 업그레이드

본인의 OS에 맞는 문서를 참고하여 주세요:

- [Windows](./platform/windows/installing.md)
- [Mac](./platform/mac/installing.md)
- [Linux](./platform/linux/installing.md)

## 영상

Anki에 대하여 빠른 설명을 보고 싶으시면, 아래의 영상들을 참고하여 주세요.
몇몇 영상은 이전 버전의 Anki를 기준으로 제작되었지만, 개념은 같습니다.

- [공유뭉치 및 기본기능](http://www.youtube.com/watch?v=QS2G-k2hQyg&yt:cc=on)

- [동기화](https://www.youtube.com/watch?v=YkiM4DPzSVc&list=PLGgmaKOIHykFoomqkBJAyGiDQ2kyiuTao&yt:cc=on)

- [카드 순서 바꾸기](http://www.youtube.com/watch?v=DnbKwHEQ1mA&yt:cc=on)

- [카드 꾸미기](http://www.youtube.com/watch?v=F1j1Zx0mXME&yt:cc=on)

- [카드 답 타이핑](http://www.youtube.com/watch?v=5tYObQ3ocrw&yt:cc=on)

만약 현재 국가에서 유튜브를 사용할 수 없으면, [영상 다운로드](https://apps.ankiweb.net/downloads/archive/screencasts/2.0/)
를 대신 이용할 수 있습니다.

## 주요 개념

### 카드

질문과 답의 쌍을 `카드` 라고 부릅니다. 이것은, 한쪽에는 질문이, 뒷면에는 답이 있는
종이 플래시 카드에 근거하고 있습니다. Anki에서 카드는 실제 카드처럼 보이지 않습니다.
기본적으로 질문을 표시한 상태로 답을 같이 보여줍니다. 예를 들어,
기초 화학을 공부하고 있을 때 이런 질문을 볼 수 있을 겁니다.

    Q: 산소의 원소 기호는?

생각해 보고 답을 `O`로 정한 후 `답 보기` 버튼을 누르면,
Anki는 다음과 같이 표시해줄 것입니다:

    Q: 산소의 원소 기호는?
    A: O

그것이 옳다는 것을 확인한 후 Anki에게 얼마나 잘 기억하고 있는지 말하면,
Anki는 다음에 보여줄 시간을 선택할 것입니다.

### 뭉치(Decks)

`뭉치` 는 카드의 그룹입니다.  카드를 다른 뭉치에 배치하여, 모든 카드를 공부하는 대신
카드 뭉치의 일부를 학습합니다. 각각의 뭉치는 새로 학습할 카드수, 얼마나 후에 카드를
다시 학습할 것인지 등을 설정할 수 있습니다.

뭉치는 다른 뭉치를 포함할 수 있으며, Anki는 `::`을 통하여 뭉치안의 뭉치를 구별합니다. 
예시로, `영어::일상영단어`라는 뭉치는 `영어`뭉치안에 포함된 `일상영단어`뭉치를 뜻합니다.
`영어::일상영단어`를 선택하면 일상영단어에 포함된 단어만 학습할 수 있고,
`영어`를 선택하면 영어뭉치내의 모든 단어(일상영단어를 포함하는) 단어를 학습할 수 있습니다.

위와같이 뭉치를 사용하고 싶으면, 뭉치의 이름을 `::`을 사용하여 표현하거나, 뭉치목록에서
드래그&드롭으로 중첩시킬 수 있습니다. 이와같이 중첩된 뭉치를 `자식뭉치` 라고 하고, 자식뭉치의
상위에 있는 뭉치를 `부모뭉치`라고 부릅니다.

Anki는 `기본`이라는 뭉치로 시작합니다. 어떠한 뭉치에도 속하지 않은 카드는, 이곳으로 들어갑니다.
기본뭉치에 카드가 없거나 다른 뭉치가 추가된 경우에는 Anki는 기본뭉치를 숨깁니다.
또는 이 뭉치의 이름을 바꾸어 다른 카드에 사용할 수도 있습니다.

뭉치는 "음식 단어" 나 "레슨 1"과 같은 다양한 카테고리의 카드를 정리하는데 적합합니다.
이에 대한 자세한 내용은 [뭉치를 적절하게 사용하기](editing.md#using-decks-appropriately) 섹션을 참고하여 주세요.

덱이 표시되는 카드 순서에 미치는 영향에 대해서는, [표기 순서](studying.md#display-order) 섹션을 참조하십시오.

### 노트 & 필드

플래시 카드를 만들때는, 하나의 카드보다는 여러장의 카드를 만드는 것이 바람직합니다.
예를들어 일본어를 배우고 있을때 `こんにちわ(곤니치와)`가 `안녕`을 뜻하는 것을 학습하기 위해
`こんにちわ(곤니치와)`를 보여주고 `안녕`을 기억하도록 하는 카드와, 
`안녕`을 보여주고 `こんにちわ(곤니치와)`를 기억하도록 하는 카드를 만들 수 있습니다.
하나는 외국어를 인식하는 능력을 테스트하고, 다른 하나는 외국어 단어를 생성하는 능력을
테스트하는 것입니다.

종이 플래시카드를 이용하는 경우에는 이를 위해서 카드마다 한번씩 총 2번을 작성하는 방법밖에
없습니다. 하지만 플래시 카드 프로그램은 앞면과 뒷면을 뒤집는 기능을 제공함으로써 더욱 쉽게
만들도록 도와줍니다. 이는 종이 플래시카드를 개선한 것이지만, 두가지 단점이 존재합니다.

- 이러한 프로그램은 인식과 생성의 성과를 개별적으로 추적하지 않기 때문에 카드는 최적의
시간에 표시되지 않는 경향이 있습니다. 즉, 원하는 것보다 더 많은 것을 잊거나 필요한 것보다
더 많이 공부하게 됩니다.

- 이러한 방식은 질문과 대답이 완전히 동일할때만 정상적으로 동작합니다. 예를 들어 각 카드의 뒷면에 추가 정보를 표시할 수 없습니다.

Anki는 카드를 분활함으로써 이러한 문제를 해결하였습니다. Anki에 각 카드의 형태를 설정하면,
카드 추가 및 업데이트시 Anki 는 자동으로 학습할 카드목록을 업데이트 합니다.

우리가 일본어 단어를 학습하고 있고 각 카드의 뒷면에 해당하는 페이지 번호를 포함하고 싶다고
다음과 같이 상상하여 보세요:

    Q: こんにちわ
    A: 안녕
       페이지 #12

외국어 단어를 생성하는 능력을 테스트하는 카드:

    Q: 안녕
    A: こんにちわ
       페이지 #12

이 예제에서는 3개의 정보가 있습니다: 일본어, 한국어, 페이지. 만약 이 정보를 합치면
다음과 같이 됩니다:

    일본어: こんにちわ
    한국어: 안녕
    페이지: 12

Anki에서는 이러한 정보를 `노트`라고 하며 각각의 정보를 `필드`라고 합니다.
이 노트에는 3가지 필드가 있습니다: 일본어, 한국어, 페이지

필드를 추가 및 편집하려면 노트를 추가하거나 편집하는 동안 `필드...`버튼을 클릭합니다.
필드에 관한 자세한 설명은 [필드 커스터마이징](editing.md#필드-커스터마이징) 섹션을 참고하세요.

### 카드 타입

In order for Anki to create cards based on our notes, we need to give it
a blueprint that says which fields should be displayed on the front or
back of each card. This blueprint is called a 'card type'. Each type of
note can have one or more card types; when you add a note, Anki will
create one card for each card type.

Each card type has two 'templates', one for the question and one for the
answer. In the above French example, we wanted the recognition card to
look like this:

    Q: Bonjour
    A: Hello
       Page #12

To do this, we can set the question and answer templates to:

    Q: {{French}}
    A: {{English}}<br>
       Page #{{Page}}

By surrounding a field name in double curly brackets, we tell Anki to
replace that section with the actual information in the field. Anything
not surrounded by curly brackets remains the same on each card. (For
instance, we don’t have to type “Page \#” into the Page field when
adding material – it’s added automatically to every card.) &lt;br&gt; is
a special code that tells Anki to move to the next line; more details
are available in the [templates](templates/intro.md) section.

The production card templates work in a similar way:

    Q: {{English}}
    A: {{French}}<br>
       Page #{{Page}}

Once a card type has been created, every time you add a new note, a card
will be created based on that card type. Card types make it easy to keep
the formatting of your cards consistent and can greatly reduce the
amount of effort involved in adding information. They also mean Anki can
ensure related cards don’t appear too close to each other, and they
allow you to fix a typing mistake or factual error once and have all the
related cards updated at once.

To add and edit card types, click the “Cards…​” button while adding or
editing notes. For more information on card types, please see the [Cards
and Templates](templates/intro.md) section.

### Note Types

Anki allows you to create different types of notes for different
material. Each type of note has its own set of fields and card types.
It’s a good idea to create a separate note type for each broad topic
you’re studying. In the above French example, we might create a note
type called “French” for that. If we wanted to learn capital cities, we
could create a separate note type for that as well, with fields such as
“Country” and “Capital City”.

When Anki checks for duplicates, it only compares other notes of the
same type. Thus if you add a capital city called “Orange” using the
capital city note type, you won’t see a duplicate message when it comes
time to learn how to say “orange” in French.

When you create a new collection, Anki automatically adds some standard
note types to it. These note types are provided to make Anki easier for
new users, but in the long run it’s recommended you define your own note
types for the content you are learning. The standard note types are as
follows:

**Basic**
Has Front and Back fields, and will create one card. Text you enter in
Front will appear on the front of the card, and text you enter in Back
will appear on the back of the card.

**Basic (and reversed card)**  
Like Basic, but creates two cards for the text you enter: one from
front→back and one from back→front.

**Basic (optional reversed card)**
This is a front→back card, and optionally a back→front card. To do this,
it has a third field called “Add Reverse.” If you enter any text into
that field, a reverse card will be created. More information about this
is available in the [Cards and Templates](templates/intro.md) section.

**Basic (type in the answer)**
This is essentially Basic, with an extra text box on the front where you
can type your answer in, after flipping to the back your input would be
checked and compared with the answer. More information is available in the
[Checking Your Answer](templates/fields.md#checking-your-answer) section.

**Cloze**  
A note type which makes it easy to select text and turn it into a cloze
deletion (e.g., “Man landed on the moon in \[…​\]” → “Man landed on the
moon in 1969”). More information is available in the [cloze
deletion](editing.md#cloze-deletion) section.

To add your own note types and modify existing ones, you can use Tools →
Manage Note Types from the main Anki window.

Notes and note types are common to your whole collection rather than
limited to an individual deck. This means you can use many different
types of notes in a particular deck, or have different cards generated
from a particular note in different decks. When you add notes using the
Add window, you can select what note type to use and what deck to use,
and these choices are completely independent of each other. You can also
change the note type of some notes [after you’ve already created
them](browsing.md).

### Collection

Your 'collection' is all the material stored in Anki – your cards,
notes, decks, note types, deck options, and so on.

## Shared Decks

You can watch [a video about Shared Decks and Review
Basics](http://www.youtube.com/watch?v=QS2G-k2hQyg&yt:cc=on) on YouTube.

The easiest way to get started with Anki is to download a deck of cards
someone has shared:

1. Click the “Get Shared” button at the bottom of the deck list.

2. When you’ve found a deck you’re interested in, click the “Download”
   button to download a deck package.

3. Double-click on the downloaded package to load it into Anki, or
   File→Import it.

Please note that it’s not currently possible to add shared decks
directly to your AnkiWeb account. You need to import them with the
desktop program, then synchronize to upload them to AnkiWeb.

Creating your own deck is the most effective way to learn a complex
subject. Subjects like languages and the sciences can’t be understood
simply by memorizing facts — they require explanation and context to
learn effectively. Furthermore, inputting the information yourself
forces you to decide what the key points are, leading to a better
understanding.

If you are a language learner, you may be tempted to download a long
list of words and their translations, but this won’t teach you a
language any more than memorizing scientific equations will teach you
astrophysics. To learn properly, you need textbooks, teachers, or
exposure to real-world sentences.

    Do not learn if you do not understand.
    --SuperMemo

Most shared decks are created by people who are learning material
outside of Anki – from textbooks, classes, TV, etc. They select the
interesting points from what they learn and put them into Anki. They
make no effort to add background information or explanations to the
cards, because they already understand the material. So when someone
else downloads their deck and tries to use it, they’ll find it very
difficult as the background information and explanations are missing.

That is not to say shared decks are useless – simply that for complex
subjects, they should be used as a 'supplement' to external material,
not as a 'replacement' for it. If you’re studying textbook ABC and
someone has shared a deck of ideas from ABC, that’s a great way to save
some time. And for simple subjects that are basically a list of facts,
such as capital city names or pub quiz trivia, you probably don’t need
external material. But if you attempt to study complex subjects without
external material, you will probably meet with disappointing results.
