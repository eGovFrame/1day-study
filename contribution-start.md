### 전자정부 표준프레임워크 GitHub Contribution 시작 가이드

Git을 처음 사용해도 괜찮아요. <br>
이번 목표는 Git 명령어를 모두 외우는 것이 아닙니다. <br>
직접 문서를 수정하고 **표준프레임워크에 Pull Request(PR)를 보내는 것**이 목표입니다.


## 전체 흐름
1. GitHub 계정 만들기
2. 개발 환경 준비하기 (VS Code + Git + Codex)
3. Git 사용자 정보 설정하기
4. 대상 Repository Fork 하기
5. 내 PC에 Clone 하기
6. AI를 활용해 Contribution 대상 찾기
7. 문서 수정하기
   * 기존 파일 수정
   * 새로운 파일 만들기
8. 변경사항 확인하기
9. Commit 하기
10. 내 GitHub Repository로 Push 하기
11. Pull Request 보내기 → 표준프레임워크 원본 Repository

---
### GitHub이란?
GitHub은 여러 사람이 소스코드와 문서를 함께 관리하고 협업하는 공간입니다.<br>
이번에는 표준프레임워크 문서를 수정하고, 그 결과를 GitHub를 통해 기여해 봅니다.

---

### 작업은
개발가이드를 https://www.egovframe.go.kr/wiki/doku.php?id=egovframework:%EA%B3%B5%ED%86%B5%EC%BB%B4%ED%8F%AC%EB%84%8C%ED%8A%B8%EA%B0%80%EC%9D%B4%EB%93%9C <br>
github repository - https://github.com/eGovFramework/egovframe-docs 에 markdown 변환 / 보완 / 현행화 작업하는 것 

---

## 1. GitHub 계정 만들기

먼저 GitHub에서 계정을 만들고 로그인합니다.
가입이 끝나면 나만의 GitHub 주소가 생깁니다.

```text
https://github.com/내아이디
```

예를 들면 다음과 같습니다.

```text
https://github.com/example-user
```

이후 표준프레임워크 Repository를 Fork하면 내 GitHub 계정 아래에 Repository 복사본이 만들어집니다.

---

## 2. 개발 환경 준비하기

이번 실습에서는 세 가지 도구를 사용합니다.

* Git
* VS Code
* Codex

### 준비할 것

* Git 설치
* VS Code 설치
* Codex 설치 및 로그인

준비가 끝났다면 이제 Contribution을 시작할 수 있습니다.

---

## 3. Git 사용자 정보 설정하기

Git은 Commit을 만들 때 누가 작업했는지 함께 기록합니다.

VS Code에서 터미널을 열고 아래 명령어를 실행합니다.

```bash
git config --global user.name "본인 이름"
git config --global user.email "본인 이메일"
```

잘 설정됐는지 확인하려면 다음 명령어를 실행합니다.

```bash
git config --global --list
```

---

## 4. Repository Fork 하기

이번에 Contribution할 Repository입니다.

https://github.com/eGovFramework/egovframe-docs

Repository 오른쪽 위에 있는 **Fork** 버튼을 클릭합니다.

Fork는 간단히 말하면 **원본 Repository를 내 GitHub 계정으로 복사하는 것**입니다.

```text
원본 Repository
eGovFramework/egovframe-docs
        ↓ Fork
내 GitHub Repository
내아이디/egovframe-docs
```

원본을 바로 수정하는 것이 아니라, 내 Repository에서 먼저 작업한다고 생각하면 됩니다.

---

## 5. 내 PC로 Clone 하기

이제 GitHub에 있는 내 Repository를 내 PC로 가져옵니다.

Fork한 Repository에서 주소를 복사한 후 터미널에서 실행합니다.

```bash
git clone https://github.com/내아이디/egovframe-docs.git
```

폴더로 이동.

```bash
cd egovframe-docs
```

그리고 VS Code로 엽니다.

```bash
code .
```

이제 내 PC에서 문서를 수정할 준비가 끝났습니다.

---

## 6. AI와 함께 Contribution 대상 찾기

여기서 이런 고민이 생길 수 있습니다.

> "그래서 어떤 문서를 수정하지?"

이럴 때 AI에게 물어보면 됩니다.

Codex에게 다음 프롬프트를 입력해 보세요.

```text
기존 개발가이드와 GitHub Repository의 문서를 비교하여
아직 Markdown으로 전환되지 않았거나 현행화가 필요한
공통컴포넌트 가이드를 찾고,
실제 Pull Request로 기여하기 좋은 대상 5개를
우선순위와 함께 추천해주세요.

대상 Repository:
https://github.com/eGovFramework/egovframe-docs

기존 개발가이드:
https://www.egovframe.go.kr/wiki/doku.php?id=egovframework:공통컴포넌트가이드
```

AI가 추천한 대상 중 하나를 골라 작업을 시작합니다.
처음이라면 너무 큰 작업보다는 **작은 문서 하나를 제대로 완성하는 것**을 추천합니다.

---

## 7. 문서 수정하기
바로 "수정해줘"라고 하기보다는 먼저 무엇을 수정할지 확인해 보는 것이 좋습니다.

먼저 AI에게 다음 내용을 확인합니다.

1. 어떤 파일을 수정해야 하는지
2. 왜 수정이 필요한지
3. 무엇을 변경할 것인지
4. 작업 범위가 어디까지인지

확인한 후 AI와 함께 문서를 수정합니다.

작업 방법은 크게 두 가지입니다.

* 기존 Markdown 파일 수정하기
* 새로운 Markdown 파일 만들기

> AI가 작성한 내용도 한 번은 직접 읽고 확인하는 것이 좋습니다.

---

## 8. 변경사항 확인하기

문서를 수정했다면 무엇이 바뀌었는지 확인합니다.

```bash
git status
```

조금 더 자세한 내용을 보고 싶다면 다음 명령어를 사용합니다.

```bash
git diff
```

```text
파일 수정
   ↓
git status로 확인
   ↓
git diff로 변경 내용 확인
```

---

## 9. Commit 하기

수정한 파일을 먼저 Git에 추가합니다.

```bash
git add .
```

그리고 작업 내용을 하나의 기록으로 저장합니다.

```bash
git commit -m "docs: update common component guide"
```

Commit 메시지는 어렵게 생각하지 않아도 됩니다.

**"내가 무엇을 수정했는지 짧게 설명한다"** 정도로 생각하면 됩니다.

---

## 10. 내 GitHub Repository로 Push 하기

내 PC에서 작업한 내용을 GitHub에 올립니다.

```bash
git push
```

```text
내 PC
  ↓ git push
내 GitHub Repository
```

---

## 11. Pull Request 보내기

이제 마지막 단계입니다.

GitHub에서 **Compare & Pull Request** 버튼을 클릭합니다.

```text
내 Repository
내아이디/egovframe-docs
        ↓ Pull Request
원본 Repository
eGovFramework/egovframe-docs
```

어떤 내용을 수정했는지 간단하게 작성하고 Pull Request를 생성합니다.

그리고 끝! 
        ↓
🎉 첫 번째 Contribution 완료!
```

> Git을 완벽하게 이해한 다음 시작할 필요는 없습니다.
> 직접 한 번 Fork하고, 수정하고, Commit하고, Pull Request를 보내보면 Git과 GitHub가 훨씬 쉽게 이해됩니다.

