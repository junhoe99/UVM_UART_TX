# UVM_UART

> SystemVerilog를 기반으로한 UVM을 활용해 UART IP를 검증하는 프로젝트입니다. 


## Overview
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/620fc099-ac59-4412-90ae-1c73ed47d597" />
**Brief and Link**는 개인화된 뉴스 요약을 제공하고 반도체 산업 분야의 기업 및 훈련 프로그램에 대한 종합적인 검색 기능을 제공합니다.


## Features

### 📰 News Brief System
- 키워드 기반 자동 뉴스 수집
- AI 기반 콘텐츠 요약
- 예약된 뉴스레터 발송
- 사용자 관심사 기반 맞춤형 콘텐츠

### 🔍 Feature 1 - Company Info. and Training course Search
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/d4a52b17-d21f-4f0d-8a50-a4daa8925325" />

- **Company Search**: 실시간 기업 정보 및 채용 공고
- **Training Search**: HRD-Net API 연동 훈련 프로그램 검색
- **Unified Results**: 여러 데이터 소스 통합 검색 결과

### 📧 Feature 2 - Email Automation
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/e7a946c2-ee8f-4084-b6eb-a781f37536a0" />

- **New Crawling & Brefieng** : 사용자가 선택한 키워드의 뉴스를 크롤링 및 내용 요약
- **Email Automation** :사용자가 선택한 시간대에 매일매일 뉴스레터를 전송

## Architecture

- **Backend**: Flask 웹 애플리케이션
- **Email**: 네이버 메일 SMTP
- **News**: 최신 뉴스 수집 및 요약(NAVER API, kss Package)
- **Search**: API 연동 (Work-net, HRD-Net)
- **Scheduler**: 내장 백그라운드 작업 스케줄러
- **Server 구축** : AWS EC2 가상서버를 활용해 서버 구축

## Result
- **Feature 1**
  - 이메일 발송:  
    <img width="1582" height="43" alt="image" src="https://github.com/user-attachments/assets/83adedfc-46c8-4194-99a5-9d1fa9ceb99c" />

  - 이메일 내용:  
    <img width="722" height="661" alt="image" src="https://github.com/user-attachments/assets/13941936-2f69-4801-91b9-a5d14c5248b0" />

- **Feature 2**
  - 이메일 발송:  
    <img width="1581" height="42" alt="image" src="https://github.com/user-attachments/assets/622f3dbd-65e4-4085-af6a-27e531cdf843" />

  - 이메일 내용:  
    <img width="757" height="698" alt="image" src="https://github.com/user-attachments/assets/821bfee4-0b8c-48ec-8131-082e4a5d3e79" />


