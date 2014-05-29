# Vim x Shell

* 이응준
* 서버사이드 웹 프로그래머 at NAVER LABS
* semtlenori@gmail.com
* twitter: @semtlnori


```markdown

• 인생은 짧고 툴은 많다.
```


```markdown

• 인생은 짧고 툴은 많다.

• 몇개만 (깊이) 배워서 많이 써먹자.

```


# Orthogonality


# Orthogonality

* find
* grep
* wc


# Orthogonality

```
find grep  wc
 |    |    |
-*----*----*--- find
 |    |    |
-*----*----*--- grep
 |    |    |
-*----*----*--- wc
 |    |    |
```


# GUI vs CLI

"특정 디렉토리의 중복된 파일들이 어떤 것이 있는지 찾아보고 싶다."

```markdown
1. 좋은 툴을 찾는다.
2. 설치한다.
3. 사용법을 배운다.
4. 사용해서 해결한다.
```


# GUI vs CLI

"특정 디렉토리의 중복된 파일들이 어떤 것이 있는지 찾아보고 싶다."

```markdown
1. 좋은 툴을 찾는다.          find . -type f | xargs -i sha1sum {} | rev\
2. 설치한다.                  | uniq -d -f 1 | rev
3. 사용법을 배운다.
4. 사용해서 해결한다.
```


# GUI vs CLI

"특정 디렉토리의 중복된 파일들이 어떤 것이 있는지 찾아보고 싶다."
"크기가 1MiB 이상인 경우에 한해서만"

```markdown
1. 그 기능을 지원하는지 알아본다.
2. 지원한다면 해결!
3. 지원하지 않는다면 새로운 툴을 찾아본다.
```


# GUI vs CLI

"특정 디렉토리의 중복된 파일들이 어떤 것이 있는지 찾아보고 싶다."
"크기가 1MiB 이상인 경우에 한해서만"

```markdown
1. 그 기능을 지원하는지 알아본다.         find . -type f -size +1M | xargs -i sha1sum {} | rev\
2. 지원한다면 해결!                       | uniq -d -f 1 | rev
3. 지원하지 않는다면 새로운 툴을 찾아본다.
```


# CLI: Pros and Cons

* Cons: 어렵다. 잘 하려면 수련해야한다.
* Pros: 수련하면서 사용자가 점점 더 똑똑해진다.


# Shell On Vim How-To


# Shell On Vim How-To

* :!
* :r!
* :w !
* 몇몇 prg들


# Shell On Vim How-To

* :!{cmd}
* 쉘에서 {cmd}를 실행한다.
* 범위를 선택하면, 지정된 줄을 외부 프로그램을 실행해서 필터링한다.
* :help filter


# Shell On Vim How-To

* :r!{cmd}
* {cmd}를 실행해서 표준출력을 현재 커서 아래 줄에 붙인다.


# Shell On Vim How-To

* :w !{cmd}
* 선택한 줄을 표준입력으로 {cmd}를 실행한다.
* 선택한 줄이 없으면 현재 window의 내용 전체를 표준입력으로 받음
* :help w_c


# Shell On Vim How-To

* :grep / :set grepprg
* :make / :set makeprg
* ^\s / :set cscopepprg
* = / :set equalprg
* gq / :set formatprg
* K / :set keywordprg


# Vim x Shell x Knowledge

Demo
