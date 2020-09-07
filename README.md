# openvim tutorial 필기 저장소

## 목차

* [OpenVim 사이트](#OpenVim-사이트)
* [1. 두 가지 모드, 'Insert' & 'Normal'](#1.-두-가지-모드,-'Insert'-&-'Normal')
* [2. 기본 움직임: h, j, k, l](#2.-기본-움직임:-h,-j,-k,-l-(Basic-movement-:-h,-j,-k,-l))
* [3. 단어 움직임: w, e, b](#3.-단어-움직임:-w,-e,-b-(Word-movement:-w,-e,-b))
* [4. 숫자 만큼 이동하기](#4.-숫자-만큼-이동하기-(Number-powered-movement))
* [5. 반복 문자 삽입](#5.-반복-문자-삽입-(Insert-text-repeatedly))
* [6. 글자 찾기, 'f' 또는 'F'](#6.글자-찾기,-'f'-또는-'F'-(Find-a-character,-f-and-F))
* [7. 짝 지어져 있는 괄호로 이동하기, '%'](#7.-짝-지어져-있는-괄호로-이동하기-'%'-(Go-to-matching-parentheses,-%))
* [8. 줄의 처음 또는 끝으로 이동하기, '0' 또는 '$'](#8.-줄의-처음-또는-끝으로-이동하기,-'0'-또는-'$'-(Go-to-start/end-of-line))
* [9. 커서에 있는 글자 찾기, '*' 또는 '#'](#9.-커서에-있는-글자-찾기,-'*'-또는-'#'-(Find-word-under-cursor,-*-and-#))
* [10. 제일 첫 번째 줄 또는 제일 마지막 번째 줄, 특정 줄로 이동, 'g' 또는 'G'](#10.-제일-첫-번째-줄-또는-제일-마지막-번째-줄,-특정-줄로-이동,-'g'-또는-'G'-(Goto-line,-g-and-G))
* [11. 단어 또는 글자 찾기, 'n' 또는 'N'](#11.-단어-또는-글자-찾기,-'n'-또는-'N'-(Search,-/text-with-n-and-N))
* [12. 새로운 줄 넣기, 'o' 또는 'O'](#12.-새로운-줄-넣기,-o-또는-O-(Insert-new-line,-o-and-O))
* [13. 글자 지우기, 'x' 또는 'X'](#13.-글자-지우기,-x-또는-X-(Removing-a-character,-x-and-X))
* [14. 글자 바꾸기, 'r'](#14.-글자-바꾸기,-'r'-(Replacing-letter-under-cursor,-r))
* [15. 단어의 오른쪽 글자들 지우기, 'd'](#15.-단어의-오른쪽-글자들-지우기,-'d'-(Deleting,-d))
* [16. 이전 명령어 반복하기, '.'](#16.-이전-명령어-반복하기,-'.'-(Repetition-with-.))
* [17. 비쥬얼 모드 이용하기, 'v'](#17.-비쥬얼-모드-이용하기,-'v'-(Visual-mode,-v))
* [18. Real Vim awaits](#18.-Real-Vim-awaits)

</br>

## OpenVim 사이트

[[ OpenVim 바로가기 ]](#https://openvim.com/)

---
</br>

## 1. 두 가지 모드, 'Insert' & 'Normal'

### Insert mode

텍스트를 입력할 수 있는 모드

#### Insert mode로 전환

    normal 모드에서 'i' 키 누르기

### Normal mode

이동하거나 텍스트를 조작할 수 있는 모드

#### Normal mode로 전환

    Insert 모드에서 'ESC' 키 누르기

---
</br>

## 2. 기본 움직임: h, j, k, l (Basic movement : h, j, k, l)

h : 왼쪽, j : 아래쪽, k : 위쪽, l : 오른쪽

         k  

    h    j    l

---
</br>

## 3. 단어 움직임: w, e, b (Word movement: w, e, b)

### w

다음 단어의 첫 글자로 이동

### e

다음 단어의 마지막 글자로 이동

### b

이전 단어의 첫 글자로 이동

---
</br>

## 4. 숫자 만큼 이동하기 (Number powered movement)

텍스트 내에서 이동하는 것은 키를 조합할 수 있다.

### 순서

    normal mode 에서 이동할 글자 숫자 입력 -> 'w' 키 누르기

### 예

#### 다음 세 번째 단어의 첫 글자로 이동 하기

(normal mode) '3' 키 누르기 -> 'w' 키 누르기

---
</br>

## 5. 반복 문자 삽입 (Insert text repeatedly)

반복되는 글자를 여러번 입력할 필요 없이 키 조합을 통해서 간단하게 입력할 수 있다.

### 순서

    normal mode 에서 반복 횟수 입력 -> Insert mode 로 전환 -> 입력할 글자 입력 -> normal mode 로 전환

### 예

#### '-' 30 글자 입력하기

(normal mode 에서) '30' 입력 -> 'i' 키 누르기 -> '-' 입력 -> 'esc' 키 누르기

---
</br>

## 6. 글자 찾기 (Find a character, f and F)

### 순서

    normal mode 에서 몇 번째 글자 찾을지 숫자 입력 (1 은 생략 가능)-> 소문자는 'f' / 대문자는 'F' 키 누르기 -> 찾을 글자 입력

### 예

### ''Insert' & 'Normal' (Two modes, insert and normal)' 문장에서 세 번째 'm' 찾기

(normal mode 에서) '3' 입력 -> 'f' 키 누르기 -> 'm' 입력

---
</br>

## 7. 짝 지어져 있는 괄호로 이동하기 (Go to matching parentheses, %)

코딩하다 보면 (), {}, [] 로 묶여 있는 것을 많이 볼 수 있다. 각 괄호의 시작 또는 끝으로 이동하고 싶을 때 사용하면 편리하다. '%' 를 입력하면 된다.

### 방법

    normal mode 에서 묶여 있는 괄호 문장 안에서 '%' 입력

### 예

#### '(i am in here) [i am in here2] {i am in here3}' [ ] 괄호로 이동하기

(normal mode 에서) 커서가 '[i am in here2]' 에 있을 경우 '%' 입력하기

---
</br>

## 8. 줄의 처음 또는 끝으로 이동하기, 0 또는 $ (Go to start/end of line)

줄의 처음 또는 끝으로 이동하고 싶을 때, normal mode 에서 '0' 또는 '$'를 입력하면 된다. **'0'** 은 맨 앞으로, **'$'** 는 맨 뒤로 이동한다.

### 예

#### 'For the end of a line, there's' 문장 맨 앞으로 이동

(normal mode 에서) '0' 입력

---
</br>


## 9. 커서에 있는 단어 찾기 (Find word under cursor, * and #)

현재 위치해 있는 커서의 단어를 빨리 찾기 위해서 사용한다.

'*' 현재 커서 후에 있는 단어, '#' 현재 커서 전에 있는 단어 찾는다.

### 예

#### 'Nothing new under the cursor. Monkey loves the banana.' 첫 번째 'the'에 커서가 위치 했을 때 다음 'the' 빨리 찾기

(normal mode 에서) 첫 번째 'the' 에 커서를 위치 -> '*' 입력

---
</br>

## 10. 제일 첫 번째 줄 또는 제일 마지막 번째 줄, 특정 줄로 이동, g 또는 G (Goto line, g and G)

### gg

  가장 첫 번째 줄로 이동

### G

  가장 마지막 번째 줄로 이동

### '숫자' + G

  입력한 숫자 줄로 이동

---
</br>

## 11. 단어 또는 글자 찾기, n 또는 N (Search, /text with n and N)

### 순서

        '/' 키 누르기 -> 찾꼬 싶은 단어 또는 글자 입력

        'n' 또는 'N' 을 눌러 다음 및 이전 단어 또는 글자를 검색할 수 있다.

---
</br>

## 12. 새로운 줄 넣기, o and O (Insert new line, o and O)

새로운 줄에 텍스트를 입력하려면, normal 모드에서 o 또는 O 를 입력하면 된다. 입력하고 나면 insert 모드로 전환됨.

'o' 는 현재 커서 아래에 새로운 줄이 추가된다. 'O' 는 현재 커서 위에 새로운 줄이 추가된다.   

---
</br>

## 13. 글자 지우기, x 또는 X (Removing a character, x and X)

현재 커서에 있는 글자를 지우는 방법은, normal 모드에서 x 또는 X 를 입력하면 된다.

'x' 는 현재 커에 있는 글자를 지운다. 'X' 는 현재 커서의 왼쪽에 있는 글자를 지운다.

---
</br>

## 14. 글자 바꾸기, 'r' (Replacing letter under cursor, r)

현재 커서에 있는 글자 하나를 바꾸기 위해서, normal 모드에서 'r' 을 입력하고 바꿀 글자를 입력하면 된다.

### 예

#### 'Replace my' -> 'Replace me' 로 변경하기

'y' 글자로 커서를 옮기기 -> (normal mode 에서) 'r' 입력 -> 'e' 입력

---
</br>

## 15. 단어의 오른쪽 글자들 지우기, 'd' (Deleting, d)

normal 모드에서 현재 커서에 있는 단어의 오른쪽에 있는 글자들을 한꺼번에 지우기는 방법은, 'd'+'w' 를 입력하면 된다.

현재 커서부터 n개의 단어를 지우기 위해서는, 'd' + '(숫자)' + 'e' 를 입력하면 된다.

### 예

#### '나는 자랑스러운 태극이 앞에' -> '나는 자랑 태극이 앞에' 로 수정하기

(normal mode 에서) '스' 커서로 옮기기 -> 'd' + 'w' 입력

---
</br>

## 16. 이전 명령어 반복하기, '.' (Repetition with .)

이전 명령어를 반복 실행하는 방법은, '.' 을 입력하면 된다.

### 예

#### '가나다 라마바 사아자 차카 타' -> '사아자 차카 타' -> '타' 로 지우기

(normal mode 에서) 커서를 '가'로 옮긴다 -> 'd' + '2' + 'w' -> '라' 위에서 '.' 입력

---
</br>

## 17. 비쥬얼 모드 이용하기, 'v' (Visual mode, v)

'insert mode', 'normal mode' 외 **'visual mode'** 가 존재한다. **'visual mode'** 는 움직임 명령어를 이용해 단어를 선택할 수 있고, 다른 명령어를 조합해 선택한 단어에 한번에 명령을 실행할 수 있다.

'v' 를 입력하고 'h', 'j', 'k', 'l', 'w', 'e', 'b' 등을 입력하면 현재 커서부터 블록이 설정된다.

### 예

#### 'This sentence has seen the light.' -> 'This has seen the light.' 블록을 설정해 한번에 지워라

(normal mode에서) 'sentence'의 's'로 커서 이동 -> 'v' 입력해 visiual mode 로 전환 -> 'l' 입력해 'sentence ' 까지 블록을 설정하던지 / 's' 에서 'e' 를 입력해 한번에 블록을 설정 -> 'd' 를 입력해 지우기

---
</br>

## 18. Real Vim awaits

### 중요한 명령어들!!

#### ':' + 'w'

저장

#### ':' + 'ㅂ'

그만두기

#### ':' + 'q' + '!'

저장하지 않고 그만두기

#### ':' + 'w' + 'q'

저장하고 그만두기

#### 'u'

복원하기 (undo)

#### 'ctrl' + 'R'

복구하기 (redo)

#### ':' + 'help'

더 많은 vim 설명 보기