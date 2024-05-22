# Git 초기 설정
git init                       # 새로운 Git 저장소 초기화
git clone [URL]                # 원격 저장소를 로컬로 복제

# 변경 내용 추적
git status                     # 작업 디렉토리의 상태 확인
git add [파일]                 # 변경 내용 스테이징
git commit -m "커밋 메시지"    # 스테이징된 변경 내용을 커밋

# 변경 내용 확인
git log                        # 커밋 기록 확인
git diff                       # 변경 내용 비교

# 원격 저장소 관리
git remote -v                  # 현재 설정된 원격 저장소 확인
git remote add [이름] [URL]    # 새로운 원격 저장소 추가
git push [원격 저장소] [브랜치] # 변경 내용을 원격 저장소로 푸시
git pull [원격 저장소] [브랜치] # 원격 저장소의 변경 내용을 가져와 병합

# 브랜치 관리
git branch                     # 현재 브랜치 목록 확인
git checkout [브랜치 이름]     # 특정 브랜치로 이동
git checkout -b [새로운 브랜치] # 새로운 브랜치 생성 및 이동
git merge [다른 브랜치]        # 다른 브랜치를 현재 브랜치로 병합
git branch -d [브랜치]         # 브랜치 삭제
