# 🌐 UVM_UART

SystemVerilog 기반 UVM을 활용해 UART IP의 TX 모듈을 Verification하는 프로젝트입니다.

---

## 🔎 Overview

본 프로젝트는 UART IP의 TX 모듈을 대상으로 UVM Testbench를 설계하고 Verification을 수행하여 안정적 동작을 검증합니다.

---

## 📌 DUT Spec Analysis

### **1. Key Parameters**
    - Data Bits : 8bit
    - NO Parity Bits : 멀티비트에서 정확성이 크지 않으므로, 단순성과 리소스 절약을 위해 parity bit를 사용하지 않았음.
    - **Oversampling : baud_tick**  UART는 비동기 통신이라, TX와 RX의 클럭이 완벽히 맞지 않아도 동작해야 함. 따라서 타이밍 동기화 & 정확한 data 샘플링을 위해 16배로 oversampling을 진행.

### **2. System Block Diagram**
![System Block](https://github.com/user-attachments/assets/f35191cc-3701-4830-ada3-a31a89ce559e)

### **3. Protocol**
![Protocol](https://github.com/user-attachments/assets/0bf95832-7a3f-4a1a-8e93-271f4bd011b7)
    - **필수 Protocol 규칙**
      1. **START BIT :** 각 전송 frame은 반드시 **start bit = 0**으로 시작해야 함.
      2. **STOP BIT :** 전송이 끝날때는, 반드시 **STOP but = 0**으로 끝나야 함.
      3. **BIT SEQUENCE :** 데이터 bit는 LSB부터 전송되어야 함.
      4. **BAUD RATE :** 각 비트의 지속 시간은 baud rate에 맞춰야 함. 
    

### **4. Timing Diagram / FSM / ASM**
**🎯FSM**  
![FSM](https://github.com/user-attachments/assets/b4991daa-326d-4f95-9840-c5816e181085)

**🎯ASM**  
![ASM](https://github.com/user-attachments/assets/4bb34b18-3029-4c76-a67c-f4e1cb682ad6)

---

## 🔁 Verification Plan

Verification 목표, test strategy, coverage plan을 상세히 기술합니다.

---

## 📚 TB Architecture

UVM Testbench의 계층적 구조(DUT, Interface, Driver, Sequencer, Monitor, Agent, Env 등)를 설명합니다.

---

## 📋 Testcase & Scenario

- 기본 전송 테스트
- 엣지 케이스 테스트
- 랜덤 시나리오 기반 테스트
- Coverage Hole 보완 테스트

---

## ✨ Verification Results

시뮬레이션 파형, functional coverage, assertion 결과 등을 포함합니다.

---

## 🔥 Insights

Verification 과정에서 도출된 주요 인사이트, 개선점, 추후 작업 방향 등을 정리합니다.
