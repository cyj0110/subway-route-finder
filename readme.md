# Subway Route Finder

서울 지하철 최단 경로 길찾기 웹 프로젝트(연습)
카카오맵 지도 API를 사용하여 출발역과 도착역 사이 최적 경로 및 환승 정보를 표시합니다.

---

## 학습 목표

웹 개발 기초: HTML, CSS, JavaScript를 활용한 클라이언트 개발 경험.

프론트엔드 프레임워크: React/Vue 등으로 지도 기반 UI를 구축.

백엔드 개발: Node.js, Express를 사용하여 REST API 설계 및 DB 연동.

데이터베이스 모델링: 지하철 노선/역 데이터를 효율적으로 저장하고 질의.

알고리즘 적용: Dijkstra 알고리즘을 실제 서비스 로직에 구현.

API 연동: 카카오맵 API를 호출하고 지도/마커/경로 표시.

---

## 📌 주요 기능

- 지하철 역 검색 및 선택
- 최단 경로 계산 (환승 포함)
- 소요 시간 및 환승 정보 표시
- 지도 기반 경로 시각화 (카카오맵 API 사용)
- 백엔드: 최단 경로 계산 (다익스트라 알고리즘)
- DB: 지하철 노선, 역, 위치 정보 저장

---

## 🏗️ 프로젝트 구조
```
subway-route-finder/
│
├─ backend/ # 서버 코드 (Python Flask)
│ ├─ app.py
│ ├─ route.py
│ └─ database.db
│
├─ frontend/ # 웹 코드 (HTML, CSS, JS)
│ ├─ index.html
│ ├─ style.css
│ └─ script.js
│
├─ data/ # 지하철 노선/역 데이터 (CSV)
│ └─ subway_data.csv
│
└─ README.md # 프로젝트 설명
```
---

## ⚡ 사용 기술

- **Front-end**: HTML, CSS, JavaScript, 카카오맵 JS API
- **Back-end**: Python, Flask, SQLite
- **알고리즘**: 다익스트라 (최단 경로), 환승 처리
- **데이터베이스**: SQLite (지하철 노선 및 연결 정보)

---

## 🚀 설치 및 실행 방법

1. 리포지토리 클론
```bash
git clone https://github.com/username/subway-route-finder.git
cd subway-route-finder/backend
```
2. 가상환경 생성 (Python 3)
```
python -m venv venv
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows
```
3. 의존성 설치
```
pip install -r requirements.txt
```
4. 서버 실행
```
python app.py
```
5.  브라우저에서 frontend/index.html 열기

---

## 📊 데이터 구성

### station 테이블

| id | name   | line  | latitude | longitude |
|----|--------|-------|----------|-----------|
| 1  | 서울역 | 1호선 | 37.5665  | 126.9780  |
| 2  | 시청역 | 2호선 | 37.5700  | 126.9850  |

### connection 테이블

| from_station | to_station | travel_time |
|--------------|------------|-------------|
| 1            | 2          | 2           |
| 2            | 3          | 3           |


---

## 🎯 확장 아이디어

- 시간대별 소요 시간 비교

- 출발/도착역 자동완성

- 서울 지하철 + 버스 통합 경로

- 모바일 웹 및 지도 확대/축소 최적화

---

## 📝 참고

- 카카오맵 API 문서: https://developers.kakao.com/docs/latest/ko/local/dev-guide

- Python Flask 공식 문서: https://flask.palletsprojects.com/

---
