# 바로방 (House Recommendation project)

- 발품 팔기 전에 바로방에서 찾아보자!
- 2030 세대를 위해 서울시 전월세 매물을 추천해주는 웹 사이트를 구현했습니다.
- 실거래가 기반 집 추천과 현재 부동산 매물 정보까지 같이 제공합니다.

### python, QGIS, PostgreSQL, Django 프로그램을 사용하였으며, 진행 순서는 다음과 같습니다.

### 1. 데이터 수집 및 전처리
- 국토교통부 실거래가 공개시스템에서 5년치 부동산 실거래가 데이터 수집
- 공공 데이터 포털에서 각종 편의시설 데이터 수집
- 서울 열린 데이터 광장에서 편의시설 및 지하철역 데이터 수집
- 카카오 API 로 위도, 경도, 편의시설 데이터 수집
- 네이버 부동산 매물 데이터 크롤링 (BeautifulSoup, selenium)

### 2. 데이터 저장
- QGIS 로 공간 정보 데이터 가시화
- PostgreSQL에 데이터 저장

### 3. Django 로 웹 사이트 구현
- 사용자가 부동산 유형, 전/월세, 예산, 직장주소, 편의시설 조건 선택
- SQL 구문으로 조건에 따른 부동산 매물별 점수 계산
- 점수가 높은 매물 상위 10개 추천, 주변 편의시설 정보, 관련 네이버 매물을 지도상에 표시