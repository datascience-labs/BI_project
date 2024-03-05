---
layout: project
title: BI_project/
project: BI_project
repo: datascience-labs/BI_project
permalink: /:path/:basename:output_ext
---

# 전력 데이터 보안 강화를 위해 AI 반도체에 탑재 가능한 이상치 탐지 AMI 모듈 제안
## 프로젝트 수행 기간
2022.05.30 ~ 2022.08.08

## 핵심내용
![image01](https://github.com/y00ns/BI_project/assets/104632673/25319973-a446-4b15-bb9b-0e363bf846e2)


## 배경
### 확산 중인 AMI의 핵심, 스마트 미터
최근 정부는 세종시 등의 지역에서 스마트 그리드 사업을 시행 중임. 스마트 그리드는 전기의 생산, 운반, 소비 과정에 정보통신기술을 접목하여 공급자와 소비자가 상호작용함으로써 효율성을 높인 지능형 전력망 시스템임. 최근 기후 변화와 에너지 자원 고갈로 에너지 효율화가 중요해짐. 이에 따라 에너지 효율화에 크게 기여할 수 있는 스마트 그리드 사업이 주목받음

### 국내 스마트 미터, 정말로 안전한가
- 사이버 공격은 AMI 내의 각 구성요소와 구성요소 사이의 유무선 통신에서 일어남. 따라서, 스마트 미터도 사이버 공격의 타깃이 됨. 스마트 미터가 공격당하면 데이터 변조, 개인정보 유출, 금전 손해 등의 피해가 발생함.
- 우리나라의 스마트 미터는 인증서와 암호화 방식을 사용한 암호 모듈을 사용함. 난수를 생성하여 암호화된 개인키와 공개키를 만들고 메모리에 저장하는 인증서를 모든 스마트 미터에 발급하여 정보를 보호함. 해당 암호 모듈은 난수 생성기와 키를 저장하는 보안 메모리가 없음. 암호화된 키를 복호화하는 비밀키가 평범한 메모리에 저장되기 때문에 공격자에 의해 유출될 수 있음. 
- 공격자가 비밀키를 아는 경우, 복호화된 개인키와 공개키를 획득함. 신원을 증명해주는 개인키와 공개키를 소유한 경우, 공개키를 통해 저장된 정보를 유출하고 조작할 수 있음. 만약 공격자가 악성코드를 주입한다면, 주입된 악성코드가 DCU로 전송되어 다른 스마트 미터까지 감염시킴. 또한, 조작된 정보가 DCU에 전송되고 전력수요 예측에 어려움이 생김.

### FDIA(False Data Injection Attack) 피해를 줄이기 위한 이상치 데이터 탐지
![image04](https://github.com/y00ns/BI_project/assets/104632673/5ae4103d-89df-4829-8aa0-e78383d5592d)
공격자가 스마트 미터에 FDIA를 가한 경우, 주입된 이상치 데이터를 찾아 피해를 줄여야 함. 그러나 인증서와 암호화 방식은 들어오는 데이터가 정상인지 판단만 진행함. 인증된 데이터에 더 이상 관여하지 않음. 따라서, 사이버 공격을 사전에 막는 인증서와 암호화 방식과 함께, 해당 방식을 뚫고 침입한 이상치 데이터를 탐지하는 기술을 개발하여 함께 사용함으로써 보안을 강화해야 함. 

## 제안 아이디어 : AI 반도체에 탑재 가능한 이상치 탐지 AMI 모듈
### TCN (Temporal Convolutional Networks) 기반의 이상치 탐지 모델
![image08](https://github.com/y00ns/BI_project/assets/104632673/428736c0-df6a-49e9-a465-cd683e75e1b5)

### 탐지 과정
![image09](https://github.com/y00ns/BI_project/assets/104632673/8e6f9526-2649-413b-b4f1-cf8c55f9c33c)

### 사용 데이터
![그림5](https://github.com/y00ns/BI_project/assets/104632673/5606b6a4-85c5-4d22-8b4e-9f30c9d61296)

### 공격받은 데이터 생성
![image06](https://github.com/y00ns/BI_project/assets/104632673/2247609b-ae4d-4ca1-a713-466b70e250c2)


### 탐지 결과
![화면 캡처 2024-03-04 132121](https://github.com/y00ns/BI_project/assets/104632673/31ae52f3-753b-430b-b6a3-b885743f3917)
![그림1](https://github.com/y00ns/BI_project/assets/104632673/2a1a75b3-542c-49af-a087-6912eeb87590)

## 이상치 탐지 모델의 활용
### 인공지능 반도체를 활용한 탐지 소형화
![image12](https://github.com/y00ns/BI_project/assets/104632673/98cc37d4-2ff0-4026-86e1-2a451690dadf)

### 대시보드를 통한 알람 서비스
- 알람서비스 수행 과정
![image13](https://github.com/y00ns/BI_project/assets/104632673/c9b2e4d7-d1b5-4334-84ff-ba49c1b214ef)

- 알람 서비스 대시보드
![image14](https://github.com/y00ns/BI_project/assets/104632673/af254a9e-dd7c-4696-ad27-8812af8a4c37)

## 실현 가능성
![image15](https://github.com/y00ns/BI_project/assets/104632673/71fd6cf5-306a-4c83-9598-7c86caeca310)

## 기대 효과
![그림2](https://github.com/y00ns/BI_project/assets/104632673/819c92a0-ee70-4c11-941e-49ccb0e4c37c)


