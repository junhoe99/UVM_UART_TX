# 🌐 UVM_UART

SystemVerilog 기반 UVM을 활용해 UART IP의 TX 모듈을 Verification하는 프로젝트입니다.

---

## 🔎 Overview

본 프로젝트는 UART IP의 TX 모듈을 대상으로 UVM Testbench를 설계하고 Verification을 수행하여 안정적 동작을 검증합니다.

---

## 📌 DUT Spec Analysis

### 1. System Block Diagram
![System Block](https://github.com/user-attachments/assets/f35191cc-3701-4830-ada3-a31a89ce559e)

### 2. Protocol
![Protocol](https://github.com/user-attachments/assets/0bf95832-7a3f-4a1a-8e93-271f4bd011b7)


### 3. Timing Diagram / FSM / ASM
**FSM**  
![FSM](https://github.com/user-attachments/assets/b4991daa-326d-4f95-9840-c5816e181085)

**ASM**  
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
