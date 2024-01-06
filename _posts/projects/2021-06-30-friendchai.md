---
layout: post
title: "FriendChise"
date: 2021-06-30
category: projects
---

## 개요

정부에서 제공하는 데이터를 활용한 프랜차이즈 추천 웹 서비스

## 기간

2021년 3월 15일 ~ 2021년 6월 30일 (약 4개월)

## 상세 내용

대학 졸업 프로젝트로 정부에서 제공하는 OpenAPI를 활용하여 프랜차이즈 정보, 전국 가맹점 점포 등의 데이터를 필터링과 클러스터링하여 프랜차이즈 창업 희망자들에게 테마별로 추천해주는 웹 서비스입니다.

- 데이터 수집 및 전처리
- RESTful API django 서버 구축
- Vue.js에 카카오 맵 API 연동

### 데이터 수집 및 전처리

파이썬을 이용해 정부 공정거래위원회에서 제공하는 정보공개서를 바탕으로 전국에 있는 요식업 관련 프랜차이즈를 수집했습니다. 유효하지 않다고 판단되는 몇몇 데이터에 대해선 전처리를 수행했습니다. 그리고 전국 가맹점 점포 데이터를 csv 파일로 받아서 사용할 수 있는 유요한 데이터로 전처리를 수행했습니다.

[공공데이터 포털](https://www.data.go.kr/index.do)

[가맹사업거래 > 정보공개서 > 정보공개서 열람](https://franchise.ftc.go.kr/mnu/00013/program/userRqst/list.do)

[파이썬 웹 크롤링](https://github.com/PioneerRedwood/CrawlingData)

### RESTful API django 서버 구축

프론트엔드 서버에서 요청하는 특정 자원의 요청을 수행하기 위한 RESTful API 서버를 django를 통해 구축했습니다. 1) 자바 Spring framework 2) 파이썬 django 3) JS nodeJS 세 개 후보군 중에서 팀원들과 의논하여 다소 같이 이해하기 쉽고 빠르게 제작할 수 있다고 판단한 django 프레임워크를 채택했습니다.

[FriendChai/Django서버 at main · PioneerRedwood/FriendChai](https://github.com/PioneerRedwood/FriendChai/tree/main/Django%EC%84%9C%EB%B2%84)

### django 관리자 데이터 테이블 화면

![관리자 계정 정보 조회.png](/assets/FriendChise/admin-select-brand-info.png)

![관리자 본사 정보 조회.png](/assets/FriendChise/admin-select-headquater-info.png)

![관리자 브랜드 정보 조회.png](/assets/FriendChise/admin-select-brand-info.png)

![관리자 인구수 정보 조회.png](/assets/FriendChise/admin-select-population-info.png)

![관리자 전국 점포 주소 조회.png](/assets/FriendChise/admin-select-store-info.png)

### Vue.JS 카카오맵 API 연동

카카오맵 API를 통해 생성한 맵에 업종, 프랜차이즈 이름, 지역 등을 검색하여 가게명, 업종 등을 한눈에 지도 형태로 보여줍니다. 맵을 확대하고 축소하는데 어느 부분까지 가게들을 보이게 할 지에 대해 많은 의논이 오갔던 부분이었습니다. 전국 가게 점포의 위치는 시군구/읍면동 형태와 경위도 좌표가 있어서 카카오 맵 API 함수를 이용해 지도에 보여줄 수 있었습니다.

![맵.png](/assets/FriendChise/app-main.png)

## 후기

프로젝트의 기획부터 완성까지 12주 안에 끝내는 수업이었습니다.  기존의 프로젝트의 무산과 4명 모두 웹 서비스 개발은 처음이라는 부분이 더해져 책임감 있게 개발에 임해서 기간 내 완성이 가능했습니다. 

주에 적어도 3번 이상 온/오프라인으로 미팅을 가졌습니다. 데이터를 수집하고 전처리하는 과정에서 많은 시간이 소요됐고 끝에 다다랐을 때 수집된 데이터를 테마에 맞게 추출하기 위해 클러스터링하는 과정과 프론트엔드로 화면을 구성하고 사용자 프로세스를 구성하는 부분에 많은 시간을 투자할 수 없어서 아쉬웠습니다. 

## 링크
[Github 링크](https://github.com/PioneerRedwood/FriendChai)