# 🌐 UVM_UART

SystemVerilog 기반 UVM을 활용해 UART IP의 **TX 모듈**을 Verification하는 프로젝트입니다.

---

## 🔎 Overview
본 프로젝트는 UART IP의 TX 모듈을 대상으로 **UVM Testbench**를 설계하고, 시뮬레이션을 통해 **안정적 동작 검증**을 수행합니다.

---

## 📌 DUT Spec Analysis

### **1. Key Parameters / Features**
- **Data Bits** : 8bit  
- **Parity Bits** : 없음 → 단순성과 리소스 절약을 위해 parity bit 미사용
- **BAUD Rate** : 9600 bps
- **Oversampling** :  
  UART는 비동기 통신이므로 TX/RX 클럭이 완벽히 맞지 않아도 동작해야 함 → **16배 Oversampling**으로 타이밍 동기화 & 정확한 데이터 샘플링 구현

---

### **2. System Block Diagram**
![System Block](https://github.com/user-attachments/assets/9a877ee5-fb74-4b15-a695-0856ae47b962)

---

### **3. Protocol**
![Protocol](https://github.com/user-attachments/assets/0bf95832-7a3f-4a1a-8e93-271f4bd011b7)

#### **필수 Protocol 규칙(ASSERTION & COVERAGE로 검증할 예정)**
| 규칙 | 설명 |
|------|------|
| **START BIT** | 각 전송 frame은 반드시 **start bit = 0**으로 시작해야 함 |
| **STOP BIT**  | 전송 종료 시 반드시 **stop bit = 1**로 끝나야 함 |
| **BIT SEQUENCE** | 데이터 bit는 **LSB → MSB** 순서로 전송 |
| **BAUD RATE** | 각 비트의 지속 시간은 **baud rate**에 맞춰야 함 |

---

### **4. FSM / ASM**
**🎯 FSM**  
![FSM](https://github.com/user-attachments/assets/b4991daa-326d-4f95-9840-c5816e181085)

**🎯 ASM**  
![ASM](https://github.com/user-attachments/assets/4bb34b18-3029-4c76-a67c-f4e1cb682ad6)

---

## 🔁 Verification Plan
- Verification 목표 정의  
- Test Strategy 설계  
- Functional Coverage & Assertion 기반의 Coverage Plan 작성  

---

## 📚 TB Architecture
UVM Testbench 계층 구조:
- DUT  
- Interface  
- Driver & Sequencer  
- Monitor  
- Agent & Environment  
- Scoreboard & Coverage  

---

## 📋 Testcase & Scenario
- 기본 전송 테스트  
- 엣지 케이스 테스트  
- 랜덤 시나리오 기반 테스트  
- Coverage Hole 보완 Directed 테스트  

---

## ✨ Verification Results
- 시뮬레이션 파형  
- Functional Coverage 결과  
- Assertion Pass/Fail 현황  

---

## 🔥 Insights
- 검증 과정에서 발견된 이슈와 개선 포인트  
- 성능 및 안정성 향상 아이디어  
- 추후 확장 계획  
