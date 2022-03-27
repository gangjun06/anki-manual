# 검색

<!-- toc -->

Anki의 `탐색` 화면과 `뭉치 필터` 기능은 일반적인 방법으로 특정 카드/노트를 검색합니다.

## 간단한 검색

검색 상자에 텍스트를 입력하면 Anki가 일치하는 노트를 찾아 해당 카드를 표시합니다. Anki는 노트의 모든 필드를 검색하지만 태그를 검색하지는 않습니다(태그를 검색하는 방법은 이 섹션의 뒷부분을 참조하십시오). 
몇 가지 예:

`dog`  
"dog"를 포함하고 있는 노트를 찾습니다. (예: "dog", "doggy", "underdog")

`dog cat`  
"dog"와 "cat" 을 둘다 포함하고 있는 노트를 찾습니다. (예: "raining cats and dogs")

`dog or cat`  
"dog"또는 "cat"이 포함된 노트를 찾습니다.

`dog (cat or mouse)`  
"dog"와 "cat"이 포함된 노트 또는 "dog"와 "mouse"가 포함된 노트를 찾습니다.

`-cat`  
"cat"이 포함되지 않은 노트를 찾습니다.

`-cat -mouse`  
"cat"과 "mouse"가 포함되지 않은 노트를 찾습니다.

`-(cat or mouse)`  
"-cat -mouse"와 동일함

`"a dog"`  
"atta dog", "a dog"와 같이 정확한 순서를 가진 노트를 찾습니다. ("dog a", "adog"등은 찾지 않습니다.)

`-"a dog"`  
"a dog"라는 정확한 문구가 없는 노트를 찾습니다.

`d_g`  
d,&lt;아무 문자(한글자),&gt;,g 와 같은 노트를 찾습니다. (예: "dog", "dig", "dug")

`d*g`  
d,&lt;아무 문자(한글자 이상)또는 공백,&gt;,g 와 같은 노트를 찾습니다. (예: "dg", "dog", "dung")

`w:dog`  
단어에서 "dog"를 찾습니다. ("dog"는 검색되지만, "doggy", "underdog"등은 검색되지 않습니다)
Anki 2.1.24+ 또는 AnkiMobile 2.1.61+ 버전이 필요합니다.

`w:dog*`  
"dog"와 "doggy"는 검색되지만 "underdog"는 안됩니다.

`w:*dog`  
"dog"와 "underdog"는 검색되지만 "doggy"는 안됩니다.

상기 내용에 대한 설명:

- 검색어는 공백으로 구분됩니다.

- 여러 검색어가 제공되는 경우 Anki는 모든 용어와 일치하는 노트를 찾습니다. 각 용어 사이에 암묵적인 'and'가 삽입됩니다. Anki 2.1.24+ 및 Anki Mobile 2.0.60+에서는 "cat and dog"는 "dog cat"과 동일하지만 오래된 Anki 버전은 "and"를 검색해야 하는 다른 단어로 취급합니다.

- 여러개중 하나만 일치해도 되는 경우 "or"을 사용할 수 있습니다.

- 검색어에 마이너스 기호를 추가하여 일치하지 않는 노트를 찾을 수 있습니다..

- `cat(cat or mouse)`와 같이 괄호 안에 검색어를 넣어 그룹화할 수 있습니다. 이것은 OR과 AND 검색을 조합할 때 중요합니다. 예를 들어 괄호 안에 'dog cat' 또는 'dog mouse'가 있으면 'dog and cat' 또는 'mouse'와 일치합니다.

- Anki는 설정한 [필드 정렬](editing.md#customizing-fields)의 포맷 내에서만 검색할 수 있습니다. 예를 들어 필드 중 하나에 `exa*mple"`을 추가하면 해당 필드가 정렬 필드가 아닌 경우 "example"을 검색할 때 일치하지 않습니다. 단어의 형식이 지정되지 않았거나 단어의 중간 형식이 변경되지 않으면 Anki는 모든 필드에서 해당 단어를 찾을 수 있습니다.

- 표준 검색에서는 대소문자를 구분하지 않습니다.a-z는 A-Z와 일치하며, 그 반대도 마찬가지입니다. 키릴 문자와 같은 다른 문자는 표준 검색에서는 대소문자를 구분하지만 단어 검색이나 정규 표현식(`w:`,`re:`)을 사용하면 대소문자를 구분하지 않습니다.

## 필드로 제한

특정 필드에 일부 텍스트가 포함된 경우에만 Anki에게 일치하도록 요청할 수 있습니다. 위의 검색과 달리 필드를 검색하려면 기본적으로 '정확한 일치'가 필요합니다.

`front:dog`  
Front 필드가 정확히 "dog"인 노트를 찾습니다. "a dog"라고 하는 필드는 일치하지 않습니다.

`front:*dog*`  
Front 필드 내에서 "dog"가 포함된 노트를 찾습니다.

`front:`  
전면 필드가 비어 있는 노트를 찾습니다.

`front:_*`  
전면 필드가 비어 있지 않은 노트를 찾습니다.

`front:*`  
전면 필드가 비어 있는지 여부에 관계없이 노트를 찾습니다.

`fr*:text`
"fr"로 시작하는 필드에서 노트를 찾습니다.  Anki 2.1.24+ 또는 AnkiMobile 2.1.60+ 의 버전이 필요합니다.

## 태그, 뭉치, 카드 및 노트

`tag:animal`  
"animal" 또는 "animal::"과 같은 하위 태그가 있는 노트를 찾습니다.

`tag:none`  
태그가 붙어 있지 않은 노트를 찾습니다.

`tag:ani*`  
"ani"로 시작하는 태그가 있는 노트를 찾습니다.

`deck:french`  
"french" 뭉치 또는 "french::Vocab"와 같은 하위 뭉치에서 카드를 찾습니다.

`deck:french -deck:french::*`  
"french" 뭉치에 있는 카드를 찾지만 하위 뭉치는 찾지 않습니다.

`deck:"french vocab"`  
뭉치에 띄어쓰기가 있을경우 쌍따움표를 사용합니다.

`"deck:french vocab"`  
이러한 방식도 위와 같습니다.

`deck:filtered`  
필터링된 뭉치만 찾습니다.

`-deck:filtered`  
필터링되지 않은 뭉치만 찾습니다.

`card:forward`  
Forward 카드를 찾습니다.

`card:1`  
템플릿 번호로 카드 검색 - 예를 들어 노트의 두 번째 삭제 부분을 찾으려면 `card:2`를 사용합니다.

`note:basic`  
"basic"노트타입을 가진 카드를 찾습니다.

## 악센트 무시/문자 조합

Anki 2.1.24 또는 AnkiMobile 2.0.60 이상의 버전이 필요함.

You can use `nc:` to remove combining characters ("no combining"). For example:

`nc:uber`  
matches notes with "uber", "über", "Über" and so on.

`nc:は`  
matches "は", "ば", and "ぱ"

Searches that ignore combining characters are slower than regular searches.

## 정규식

Anki 2.1.24+ and AnkiMobile 2.0.60+ support searching in notes with "regular expressions",
a standard and powerful way of searching in text.

Start a search with `re:` to search by regular expression. To make things easier, Anki will
treat the following as [raw input](#raw-input), so bear in mind the rules listed there.

Some examples:

`"re:(some|another).*thing"`  
find notes that have "some" or "another" on them, followed by 0 or more characters, and then "thing"

`re:\d{3}`  
find notes that have 3 digits in a row

Regular expressions can also be limited to a specific field. Please note that unlike the normal searches
in a specific field, regular expressions in fields don't require an exact match. Eg:

`front:re:[a-c]1`  
matches uppercase or lowercase a1, B1 or c1 that occurs anywhere in the "Front" field

`front:re:^[a-c]1$`  
like the above, but will not match if any other text falls before or after a1/b1/c1.

Anki 2.1.50 added regex support for tags:

`tag:re:^parent$`  
find notes with the exact tag "parent", disregarding any child tags like "parent::child"

`"tag:re:lesson-(1[7-9]|2[0-5])"`  
find notes with tags "lesson-17" through "lesson-25"

You can learn more about regular expressions here: <https://regexone.com/lesson/introduction_abcs>

Some things to be aware of:

- The search is case-insensitive by default; use `(?-i)` at the start to turn on case sensitivity.
- Some text like spaces and newlines may be represented differently in HTML - you can
  use the HTML editor in the editing screen to see the underlying HTML contents.
- For the specifics of Anki's regex support, please see the regex crate documentation: <https://docs.rs/regex/1.3.9/regex/#syntax>

## 카드 상태

`is:due`  
review cards and learning cards waiting to be studied

`is:new`  
new cards

`is:learn`  
cards in learning

`is:review`  
reviews (both due and not due) and lapsed cards

`is:suspended`  
cards that have been manually suspended

`is:buried`  
cards that have been buried, either [automatically](studying.md#siblings-and-burying) or
manually

Note that with the [new scheduler](https://faqs.ankiweb.net/the-anki-2.1-scheduler.html),
Anki now distinguishes between manually and automatically buried cards so you can
unbury one set without the other.

Cards that have lapsed fall into several of these categories, so it may
be useful to combine them to get more precise results:

`is:learn is:review`  
cards that have lapsed and are awaiting relearning

`-is:learn is:review`  
review cards, not including lapsed cards

`is:learn -is:review`  
cards that are in learning for the first time

`flag:1`  
cards with a red flag

`flag:2`  
cards with an orange flag

`flag:3`  
cards with a green flag

`flag:4`  
cards with a blue flag

`flag:5`  
cards with a pink flag

`flag:6`  
cards with a turquoise flag

`flag:7`  
cards with a purple flag

## Card properties

`prop:ivl>=10`  
cards with interval of 10 days or more

`prop:due=1`  
cards due tomorrow

`prop:due=-1`  
cards due yesterday that haven’t been answered yet

`prop:due>-1 prop:due<1`  
cards due between yesterday and tomorrow

`prop:reps<10`  
cards that have been answered less than 10 times

`prop:lapses>3`  
cards that have moved into relearning more than 3 times

`prop:ease!=2.5`  
cards easier or harder than default

## Recent Events

### 추가됨

`added:1`  
오늘 추가된 카드

`added:7`  
지난 1주일간 추가된 카드

노트 추가 시간이 아닌 카드 추가 시간에 대해 체크하기 때문에 오래 전에 노트를 추가했더라도 기간 내에 생성된 카드가 포함됩니다.

### 수정됨

`edited:n`  
지난 n일 동안 노트 텍스트가 추가/삭제된 카드.

Anki 2.1.28 / AnkiMobile 2.0.64 이상의 버전이 필요함.

### Answered

`rated:1`  
cards answered today

`rated:1:2`  
cards answered Hard (2) today

`rated:7:1`  
cards answered Again (1) over the last 7 days

`rated:31:4`  
cards answered Easy (4) in the last month

Rating searches had been limited to 31 days before version 2.1.39.

### First Answered

On version 2.1.45+, you can also search for the very first review only:

`introduced:1`  
cards answered for the first time today

`introduced:365`  
cards answered for the first time within the last 365 days

## Matching special characters

This section was written for Anki 2.1.36+ - earlier versions did not support escaping
characters in certain situations.

As shown in the previous section, some characters like `*`, `_` and `"` have a
special meaning in Anki. If you need to locate those characters in a search,
you need to tell Anki not to treat them specially.

- _Space_  
  To match something including spaces, enclose the `"entire term"` in double
  quotes. If it is a colon search, you also have the option to only quote the
  `part:"after the colon"`.

- `"`, `*` and `_`  
  Add a backslash before these characters to treat them literally. For example,
  `_` will match any single character, but `\_` matches only an actual underscore.

- `\`  
  Because a backlash is used to remove the special meaning from other characters,
  it too is treated specially. If you need to search for an actual backslash,
  use `\\` instead of `\`.

- `(` and `)`  
  You can search for parentheses either by enclosing the full term in quotes,
  and/or by using a backslash. That is, `"some(text)"`, `some\(text\)` and
  `"some\(text\)"` are all equivalent, but `some(text)` is not.

- `-`  
  Starting a search term with `-` usually inverts it: `-dog` matches everything
  except dog for example. If you instead wish to include an actual hyphen,
  you can either use a backslash, or include the text in quotes, such as
  `\-.-` or `"-.-"`.

- `:`  
  Colons have to be escaped unless they are preceded by another, unescaped colon.
  So `w:e:b` is a word boundary search for `e:b`, `w\:e\:b` searches literally for
  `w:e:b` and `w\:e:b` searches the field `w:e` for `b` (see
  [field searches](#limiting-to-a-field)).

- `&`, `<`, and `>`  
  `&`, `<`, and `>` are treated as HTML when searching in Anki, and as such searches
  containing them don't work as expected. However, you can search for them by using their
  corresponding HTML entity names (`&amp;` for `&`, `&lt;` for `<`, and `&gt;` for `>`).
  For example, searching `&lt;&amp;text&gt;` searches for a card with `<&text>` in a field.

### Raw input

Text preceded by certain keywords (like `re:`) will be treated as raw input. That is,
the characters listed above largely lose their special meaning. In such a context, only
a minimum of escaping is required to prevent ambiguity:

- `"` must be escaped.

- Spaces and unescaped parentheses require the search term to be quoted.

- The search term must not end in an odd number of backslashes.

## Object IDs

`nid:123`  
the note with note id 123

`cid:123,456,789`  
all cards with card ids 123, 456 or 789

Note and card IDs can be found in the [card info](stats.md) dialog in the
browser. These searches may also be helpful when doing add-on
development or otherwise working closely with the database.
