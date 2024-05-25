
# Git의 `origin`과 `main`(master) 브랜치 개념 이해하기

이전에 Git을 제대로 공부하지 않고 GitHub에 디렉토리를 Push하려다가 내가 Branch 개념을 제대로 이해하지 못 하고 있다고 느꼈고, 이를 이해하기 위해 ChatGPT를 통해 Branch에 대해 다시 공부를 하면서 `origin`과 `main`(master)의 차이를 확실히 알게 됐다.

나와 같이 `origin`과 `main`의 개념이 헷갈리는 분들을 위해 기록을 남겨본다.

## 1. origin
`origin`은 branch가 아닌 원격 저장소(GitHub의 Git 저장소)의 기본 이름이다. 그렇기 때문에 원격 저장소와 로컬 저장소를 연결할 때 `origin`을 사용한다.

**예:**
```bash
git clone origin <원격 저장소 repository 주소>
# 이 명령어는 로컬 저장소 디렉토리를 origin이라는 원격 저장소의 repository에 클론한다는 것을 뜻한다.
# 하지만 origin을 생략하고 이 명령어를 실행할 수도 있는데,
# 이 경우 자동으로 원격 저장소의 이름을 origin으로 설정한다.
```

## 2. main(master)
Git에서 사용하는 브랜치(branch) 이름 중 하나로, 일반적으로 프로젝트의 기본 브랜치로 사용된다. 새로운 저장소를 만들 때 기본 브랜치로 생성되며, 주로 배포 가능한 안정적인 버전을 포함한다. 이 때, 주의할 점은 로컬 저장소의 기본 브랜치(`main`)와 원격 저장소의 기본 브랜치(`origin/main`)가 각각 다르다는 점이다.

### 로컬 저장소의 `main` 브랜치
로컬 저장소의 `main` 브랜치는 아래와 같이 사용할 수 있다.
```bash
git checkout main
# 로컬 저장소의 main 브랜치에서 작업하겠다는 뜻이다.
```

### 원격 저장소의 `origin/main` 브랜치
원격 저장소의 `origin/main` 브랜치는 아래와 같이 사용할 수 있다.

**예:**
```bash
git push origin main
# 해당 명령어는 origin(원격 저장소)의 main(브랜치)에 로컬 저장소의 main 브랜치에 있는 커밋 및 변경 사항을 push한다는 것을 의미한다.
```
