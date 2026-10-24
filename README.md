# High/Low Resistance Auto Probe Station

반도체 웨이퍼 **고저항 / 저저항 자동 측정** Full-Auto Probe Station 제어 SW
C# · WinForms · .NET Framework | MSTECH

<!-- 여기에 영상 드래그 → 자동 생성된 링크가 이 자리에 들어감 -->

![overview](images/01_overview.png)

## Overview
웨이퍼 로딩부터 Vision Align, 좌표 이동, 프로브 컨택, 측정까지 전 공정을 자동화한 장비 제어 소프트웨어.

## Features
- **EFEM** : LoadPort(FOUP) → Robot → Pre-Align → Stage 웨이퍼 자동 반송
- **Motion** : Ajin AXL, Ezi-SERVO 다축 모션 제어, Homing / 좌표계 / Positioner
- **Vision** : HIKROBOT 카메라 + 마크 매칭 기반 XY/θ 자동 보정
- **Auto Measure** : Wafer Map 기반 좌표 이동 → 프로브 컨택 → 고/저저항 측정
- **Instrument** : VISA/GPIB 계측기 연동, 측정 Raw Data 관리
- **Device** : 온도 컨트롤러, Load Cell, OCR(Wafer ID), IO/Interlock
- **UI** : Control Hub, Recipe 관리/Lock, EMO Recovery, 실시간 통신 로그

## Screenshots
| Vision Align | Auto Measure |
|---|---|
| ![](images/02_vision_align.png) | ![](images/03_auto_measure.png) |

![measure](images/04_measure_result.png)

## Architecture
```
UI (MainForm / ControlHub / EFEM / Wafer Map)
        │
Sequence (Auto Run · Resume · Interlock)
        │
Device Layer
 ├─ Motion : Ajin / Ezi-SERVO / Positioner
 ├─ Robot / LoadPort / Pre-Align
 ├─ Vision (HIKROBOT)
 ├─ Instrument (VISA / GPIB)
 └─ Temp / LoadCell / OCR / IO
```

## Tech Stack
C#, WinForms, .NET Framework, OpenCvSharp, Ajin AXL, Ezi-SERVO, HIKROBOT MVS, VISA/GPIB, RS-232C/TCP

## Role
- 기간 : 20XX.XX ~ 20XX.XX
- 장비 제어 SW 전체 설계 및 개발

> 고객사 납품 장비 소스로 전체 코드는 비공개입니다.
