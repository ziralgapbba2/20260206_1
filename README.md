# 서비스 접수 대시보드

## 📁 파일 구성

```
📁 리포지토리/
  ├── index.html              (메인 대시보드)
  ├── data_service.js         (데이터 파일 - 2MB)
  ├── symptom_analysis.html   (증상 분석 대시보드)
  ├── processing_analysis.html (처리 분석 대시보드)
  └── README.md
```

## 🚀 GitHub Pages 배포 방법

### 1. 리포지토리 생성
- GitHub에서 새 리포지토리 생성
- Private 또는 Public 선택 (데이터 보안 고려)

### 2. 파일 업로드
```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/사용자명/리포지토리명.git
git push -u origin main
```

### 3. GitHub Pages 활성화
1. 리포지토리 Settings 클릭
2. 왼쪽 메뉴에서 "Pages" 클릭
3. Source: "Deploy from a branch" 선택
4. Branch: "main" 선택, 폴더: "/ (root)" 선택
5. Save 클릭

### 4. 접속
- 약 1-2분 후 자동 배포
- URL: `https://사용자명.github.io/리포지토리명/`

## ⚠️ 중요 사항

### 인터넷 연결 필요
이 대시보드는 다음 CDN을 사용합니다:
- Chart.js (차트 라이브러리)
- pako (데이터 압축 해제)

→ **오프라인에서는 작동하지 않습니다**

### 데이터 보안
- `data_service.js`에는 **193,937건의 실제 서비스 데이터**가 포함됨
- Public 리포지토리 사용 시 **누구나 데이터 접근 가능**
- 민감한 데이터인 경우 **Private 리포지토리** 사용 권장

### 브라우저 호환성
- Chrome, Edge, Firefox, Safari 최신 버전 권장
- Internet Explorer는 미지원

## 🔧 문제 해결

### 데이터가 로딩되지 않음
1. 브라우저 콘솔(F12) 확인
2. `data_service.js` 파일이 같은 폴더에 있는지 확인
3. 인터넷 연결 확인 (CDN 로딩 필요)

### GitHub Pages에서 404 에러
1. 파일명 대소문자 확인 (`index.html`, `data_service.js`)
2. GitHub Pages 설정 확인 (Branch: main)
3. 배포 완료까지 1-2분 대기

### 차트가 표시되지 않음
1. 콘솔에서 Chart.js 로딩 에러 확인
2. CDN 접속 확인 (방화벽/프록시 차단 여부)

## 📊 데이터 정보

- **기간**: 2025년 12월 vs 2026년 1월
- **데이터 건수**: 193,937건
- **압축 방식**: gzip + base64
- **원본 크기**: 31MB → 압축 후: 2MB

## 🔒 보안 권장사항

### Private 리포지토리 사용 시
```
✅ 팀원만 접근 가능
✅ 검색엔진 노출 없음
✅ 데이터 보호
```

### .gitignore 설정 (데이터 제외)
```
# .gitignore
data_service.js
*.xlsx
```

## 📞 문의

문제 발생 시:
1. 브라우저 콘솔(F12) 스크린샷
2. GitHub Pages URL
3. 에러 메시지

위 정보를 함께 제공해주세요.
