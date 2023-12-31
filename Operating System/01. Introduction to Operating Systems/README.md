- [운영체제 1. INTRO](#운영체제-1-intro)
- [✨운영체제(OS)란?✨](#운영체제os란)
- [✨운영 체제의 목적✨](#운영-체제의-목적)
  - [✔️컴퓨터 시스템의 자원을 효율적으로 관리](#️컴퓨터-시스템의-자원을-효율적으로-관리)
  - [✔️컴퓨터 시스템을 편리하게 사용할 수 있는 환경을 제공](#️컴퓨터-시스템을-편리하게-사용할-수-있는-환경을-제공)
- [✨운영 체제의 분류✨](#운영-체제의-분류)
  - [📌 동시 작업 가능 여부](#-동시-작업-가능-여부)
    - [✔️단일 작업(single tasking)](#️단일-작업single-tasking)
    - [✔️다중 작업(multi tasking)](#️다중-작업multi-tasking)
  - [📌 사용자의 수](#-사용자의-수)
    - [✔️단일 사용자(single user)](#️단일-사용자single-user)
    - [✔️다중 사용자(multi user)](#️다중-사용자multi-user)
  - [📌 처리 방식](#-처리-방식)
    - [✔️일괄 처리(batch processing)](#️일괄-처리batch-processing)
    - [✔️시분할(time sharing)](#️시분할time-sharing)
    - [✔️실시간(Realtime OS)](#️실시간realtime-os)
  - [📌 몇 가지 용어](#-몇-가지-용어)
- [✨운영 체제의 예✨](#운영-체제의-예)
  - [📌 유닉스(UNIX)](#-유닉스unix)
  - [📌 Microsoft](#-microsoft)
    - [✔️DOS(Disk Operating System)](#️dosdisk-operating-system)
    - [✔️MS windows](#️ms-windows)
    - [✔️ Handheld deviece를 위한 OS](#️-handheld-deviece를-위한-os)
- [✨운영 체제의 구조✨](#운영-체제의-구조)

# 운영체제 1. INTRO

# ✨운영체제(OS)란?✨

- 컴퓨터 하드웨어 바로 위에 설치되어 사용자 및 다른 모든 소프트웨어와 하드웨어를 연결하는 소프트웨어 계층
- 협의의 운영체제(커널)
  - 운영체제 핵심 부분으로 메모리에 상주하는 부분
- 커널 뿐 아니라 각종 주변 시스템 유틸리티를 포함한 개념

# ✨운영 체제의 목적✨

### ✔️컴퓨터 시스템의 자원을 효율적으로 관리

- 프로세서, 기억장치, 입출력 장치 등의 효율적 관리
  - (컴퓨터 시스템의 자원: 프로세서, 기억장치, 입출력 장치 등)
  - (하드웨어 자원은 이미 있는 거임)
  - 사용자간의 형평성 있는 자원 분배
  - 주어진 자원으로 최대한의 성능을 내도록
- 사용자 및 운영체제 자신의 보호
- 프로세스, 파일, 메시지 등을 관리

### ✔️컴퓨터 시스템을 편리하게 사용할 수 있는 환경을 제공

- 운영체제는 동시 사용자/프로그램들이 각각 독자적 컴퓨터에서 수행되는 것 같은 환상을 제공
- 하드웨어를 직접 다루는 복잡한 부분을 운영체제가 대행

# ✨운영 체제의 분류✨

## 📌 동시 작업 가능 여부

### ✔️단일 작업(single tasking)

- 한 번에 하나의 작업만 처리
- ex) MS-DOS 프롬포트 상에서는 한 명령의 수행을 끝내기 전에 다른 명령을 수행시킬 수 없음

### ✔️다중 작업(multi tasking)

- 동시에 두 개 이상의 작업 처리
- ex) UNIX, MS Windows 등에서는 한 명령의 수행이 끝나기 전에 다른 명령이나 프로그램을 수행할 수 있음

## 📌 사용자의 수

여러 사용자의 계정을 만들어서 동시 접근할 수 있는지 없는지에 대한 분류.

### ✔️단일 사용자(single user)

- ex) MS-DOS, MS Windows

### ✔️다중 사용자(multi user)

- ex) UNIX, NT server

## 📌 처리 방식

### ✔️일괄 처리(batch processing)

- 작업을 모아서 한꺼번에 처리
- 작업이 오나전 종료될 때까지 기다려야 함
- ex) 초기 Punch Card 처리 시스템

### ✔️시분할(time sharing)

- 여러 작업을 수행할 때 컴퓨터 처리 능력을 일정한 시간 단위로 분할하여 사용
- 일괄 처리 시스템에 비해 짧은 응답 시간을 가짐
  ex) UNIX
- interactive한 방식 (컴퓨터 키보드 두드렸을 때 바로 결과가 나오는)

### ✔️실시간(Realtime OS)

- 정해진 시간 안에 어떠한 일이 반드시 종료됨이 보장되어야 하는 실시간 시스템을 위한 OS
- 데드라인이 있어서 _시간 내에 반드시!!!!_ 종료가 되어야 함
- ex) 원자로/공장 제어, 미사일 제어, 반도체 장비, 로보트 제어

- **실시간 시스템의 개념 확장**
  - Hard realtime system(경성 실시간 시스템)
    - 데드라인 안 지키면 치명적인 시스템
    - ex) 미사일 이상한 곳 날아감
  - Soft realtime system(연성 실시간 시스템)
    - 데드라인 못 지켜도 치명적이진 않음
    - ex) 영화 끊김 현상

## 📌 몇 가지 용어

1. <u>Multitasking</u>
   : 하나의 프로그램이 종료되기 전에 다른 프로그램 실행
2. <u>Multiprogramming</u>
   : 여러 프로그램이 메모리에 올라가 있음을 강조
3. <u>Timesahring</u>
   : CPU의 시간을 분할하여 나누어 쓴다는 의미
4. <u>Multiprocess</u>

- 위 용어들 모두 컴퓨터에서 여러 작업을 동시에 수행하는 것을 뜻함

- cf) Multiprocessor: 하나의 컴퓨터에 CPU(processor)가 여러 개 붙어 있음을 의미

# ✨운영 체제의 예✨

## 📌 유닉스(UNIX)

- 코드의 대부분을 C언어로 작성
- 높은 이식성
  - 하나의 컴퓨터에서 돌아가는 유닉스를 전혀 다른 컴퓨터에 이식하기 쉽다는 뜻
  - 그 컴퓨터에서만 돌아가게 하는 건 낮은 이식성
- 최소한의 커널 구조
- 복잡한 시스템에 맞게 확장 용이
- 소스 코드 공개
- 프로그램 개발에 용이
- 다양한 버전
  - System V, FreeBSD, SunOS, Solaris
  - Linux

## 📌 Microsoft

### ✔️DOS(Disk Operating System)

- MS사에서 1981년 IBM-PC를 위해 개발
- 단일 사용자용 운영체제, 메모리 관리 능력의 한계(주 기억 장치: 640KB)

### ✔️MS windows

- MS사의 다중 작업용 GUI 기반 운영체제
- Plug and Play, 네트워크 환경 강화
- DOS용 응용 프로그램과 호환성 제공
- 불안정성
- 풍부한 지원 소프트웨어

### ✔️ Handheld deviece를 위한 OS

- PalmOS, Pocket PC (WinCE), Tiny OS

# ✨운영 체제의 구조✨

CPU <-> memory <-> Disk, I/O device

- 누구한테 CPU를 줄까? : CPU 스케줄링
- 한정된 메모리를 어떻게 쪼개 써? : 메모리 관리
- 디스크에 파일을 어떻게 보관하지? : 파일 관리
- 각기 다른 입출력장치와 컴퓨터 간에 어떻게 정보를 주고 받게 하지? : 입출력 관리
- 프로세스 관리: 프로세스의 생성과 삭제, 자원 할당 및 반환, 프로세스 간 협력
- 그 외: 보호 시스템, 네트워킹, 명령어해석기 (command line interpreter)
