---
title: "WB030 DNA Assembly - MOSAIC insert–DVA Gibson assembly"
experimenter: "문지민"
created_date: 2026-10-29
last_updated_date: 2026-10-30
end_date: ''
---

## [WB030 DNA Assembly] MOSAIC Gibson assembly

> This workflow is dedicated to assembling double-stranded DNA fragments into sequences that are several kilobases or larger. It includes the assembly of multiple DNA fragments, such as parts or operon-level sequences, in a specific order to achieve the desired genetic construct.

실험 개요: [[labnote/001_(MOSAIC) RSM3-Block2/README.labnote|MOSAIC RSM3-Block2]]

작업 범위: MOSAIC insert–DVA Gibson assembly

Block2 Word 프로토콜을 기존 unit operation에 배치한 예정 workflow이다. 수행일·시료 ID·실제 결과는 미기록 상태이다.

프로토콜 기준: [MOSAIC_Block2protocol.docx](../../../../Protocol/Mosaic/MOSAIC_Block2protocol.docx), 작성일 2026-09-29, Version 1. 일반 MOSAIC 문서의 조건은 사용하지 않았다.

> [!warning] 원문 확인 필요
> Block2 원문에는 개요의 Gibson Assembly만 있고 몰비·조성·반응 조건은 없다. 기존 A/B 개별 투입 및 vector-only control은 원문 근거가 확인되지 않아 미확정이다. 길이 표기의 불일치와 nick repair 연결은 확인 후 결정한다.

## Related Unit Operations

- [USW340 Computation Gibson input calculation](#usw340-computation-gibson-input-calculation)
- [UHW010 Liquid Handling Gibson reaction preparation](#uhw010-liquid-handling-gibson-reaction-preparation)
- [UHW180 Incubation Gibson incubation](#uhw180-incubation-gibson-incubation)

---

### [USW340 Computation] Gibson input calculation

> 작업명: 투입량 계산
> A general process of data collection, preprocessing, and analysis steps. This software supports a wide range of bioinformatics and computational biology applications.

#### Meta

- Experimenter: "문지민"
- Start_date: ''
- End_date: ''
- Software: ''

#### Input

원문 실험 개요의 Block2 1,892 bp 및 DVA vector PCR 산물 2,001 bp. 실제 insert·vector 농도와 overlap 정보는 미기재.

#### Output

예정 산출물: 입력 정보 확인 후의 투입량 계산 기록. 현재 계산값은 미확정. 실제 생성 여부·시료 ID·회수량은 실험 시 기록한다.

#### Parameters

원문 예상 완성 plasmid: 약 3,797 bp. 몰비·투입 질량·반응 부피·overlap 길이는 원문 미기재.

#### QC Metrics

1,892 + 2,001 = 3,893 bp(단순 합계). 원문 예상 3,797 bp와의 차이는 96 bp이나 overlap 차감에 의한 것인지는 확인되지 않았다.

#### Method

Block2 문서는 개요에 Gibson Assembly를 명시하지만 상세 조성·계산식은 제공하지 않는다. 원문 길이와 실제 농도·overlap이 확인되기 전 투입량을 계산하거나 몰비를 가정하지 않는다.

#### Environment

원문 미기재. 실제 계산 도구는 사용 시 기록한다.

#### Discussion

기존 노트에 있던 A/B 개별 투입 구성과 vector-only control은 이번 원문에서 확인되지 않았다. 적용할 입력 구성·대조군은 미확정으로 남긴다.

---

### [UHW010 Liquid Handling] Gibson reaction preparation

> 작업명: 반응 준비
> This unit operation involves basic and fundamental liquid sample operations in laboratory processes, such as reagent preparation, sample distribution, dilution, mixing, and washing. It ensures precision and efficiency in handling liquid samples across various experimental setups.

#### Meta

- Experimenter: "문지민"
- Start_date: ''
- End_date: ''

#### Input

[[labnote/001_(MOSAIC) RSM3-Block2/002_WB010_DNA_Oligomer_Assembly_MOSAIC_One-step_self-assembly.labnote|002]] One-step 산물 또는 [[labnote/001_(MOSAIC) RSM3-Block2/003_WB010_DNA_Oligomer_Assembly_MOSAIC_Two-step_AB_self-assembly.labnote|003]] Two-step 산물과 [[labnote/001_(MOSAIC) RSM3-Block2/005_WB150_PCR-based_Target_Amplification_MOSAIC_DVA_vector_preparation.labnote|005]] vector 산물 후보. [[labnote/001_(MOSAIC) RSM3-Block2/004_WG010_Blank_Workflow_MOSAIC_nick_repair.labnote|004]] 처리 여부와 insert 구성은 미정.

#### Reagent

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Labware and Consumables

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Equipment

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Method

원문에 상세 조건 없음. 별도 프로토콜 확인 전에는 조건을 확정하지 않는다.

#### Output

예정 산출물: Gibson 반응액. 원문에는 조성이 없어 현재 준비 조건은 미확정. 실제 생성 여부·시료 ID·회수량은 실험 시 기록한다.

#### Results & Discussions

---

### [UHW180 Incubation] Gibson incubation

> 작업명: Gibson incubation
> Maintaining specific conditions for cells or chemical reactions to promote growth or desired reactions. It is essential for cell culture and biochemical assays.

#### Meta

- Experimenter: "문지민"
- Start_date: ''
- End_date: ''

#### Input

Gibson reaction preparation의 반응액 후보. 조성 확정 전 미실시.

#### Reagent

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Labware and Consumables

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Equipment

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Method

원문에 상세 조건 없음. 별도 프로토콜 확인 전에는 조건을 확정하지 않는다.

#### Output

예정 산출물: Gibson assembly 산물 → [[labnote/001_(MOSAIC) RSM3-Block2/008_WG010_Blank_Workflow_MOSAIC_follow-up_verification_records.labnote|008]] 후속 단계 후보. [[labnote/001_(MOSAIC) RSM3-Block2/007_WB150_PCR-based_Target_Amplification_MOSAIC_verification_PCR.labnote|007]] 확인용 PCR의 적용 여부는 미정. 실제 생성 여부·시료 ID·회수량은 실험 시 기록한다.

#### Results & Discussions

## Conclusions and Discussion
