---
title: MOSAIC RSM3-Block2
author: 문지민
experiment_type: labnote
sample_tracking: yes
status: planned
project:
created_date: 2026-10-12
last_updated_date: 2026-10-30
---

## 🎯 Experiment Objective
본 실험은 RSM3 Block2의 One-step 및 Two-step MOSAIC 합성 과정과 QC·서열 검증 결과를 기록하고 비교하는 것을 목적으로 한다. 각 단계의 입력·출력 시료, 처리 이력, QC 결과를 연결하여 합성 방식별 결과를 추적한다.

이번 002–008 작성 기준: [MOSAIC_Block2protocol.docx](../../../../Protocol/Mosaic/MOSAIC_Block2protocol.docx), 작성일 2026-09-29, Version 1. 일반 MOSAIC 문서는 사용하지 않았다.

기존 참고 링크: [MOSAIC - T4 ligase & E.coli (Notion)](https://app.notion.com/p/400eb16dbc8280cc98cec438cb658293). 이번 전사의 조건 근거로 사용하지 않았다.

아래 workflow는 실험 예정 항목이다. 002–005에는 Block2 원문의 조건을 unit operation별로 배치하였다. 006–008은 원문에 있는 단계만 연결하고 상세 조건이 없는 부분은 미확정으로 표시했다. 수행일과 실제 결과는 비워 두었다. 001은 이번 수정 대상에서 제외하였다.

## 🗂️ Related Workflows

- [ ] [WD050 DNA Oligomer Pool Design - MOSAIC oligo pool 구성 및 준비](./001_WD050_DNA_Oligomer_Pool_Design_MOSAIC_oligo_pool_preparation.labnote.md)
  - Unit operations: USW010 DNA Oligomer Pool Design — One-step 및 A/B pool 구성 확인 → UHW010 Liquid Handling — pool 준비
  - 예정 산출물: pool 구성표, One-step pool 및 A/B pool 시료 정보

- [ ] [WB010 DNA Oligomer Assembly - One-step MOSAIC self-assembly](./002_WB010_DNA_Oligomer_Assembly_MOSAIC_One-step_self-assembly.labnote.md)
  - Unit operations: UHW010 Liquid Handling — 반응 준비 → UHW100 Thermocycling — annealing → UHW230 Nucleic Acid Fragment Analysis — gel QC → UHW400 Manual — Qubit 정량
  - 예정 산출물: One-step assembly 산물, gel 이미지, 농도 측정 기록

- [ ] [WB010 DNA Oligomer Assembly - Two-step MOSAIC A/B self-assembly](./003_WB010_DNA_Oligomer_Assembly_MOSAIC_Two-step_AB_self-assembly.labnote.md)
  - Unit operations: UHW010 Liquid Handling — A/B 1차 반응 준비 → UHW100 Thermocycling — 1차 annealing → UHW230 Nucleic Acid Fragment Analysis — 1차 QC(개요만 기재) → UHW010 Liquid Handling — 2차 혼합 → UHW100 Thermocycling — 2차 annealing → UHW230 Nucleic Acid Fragment Analysis — 2차 gel QC → UHW250 Nucleic Acid Purification — gel extraction → UHW400 Manual — Qubit 정량(정제 전/후 시점 미정)
  - 예정 산출물: A/B 1차 및 2차 assembly 산물, 정제한 2차 산물, gel 이미지, 농도 측정 기록
  - 확인 사항: 3.3 입력 명칭과 1차 산물의 대응, QC 후 각 15 µL 확보 여부, 정량·정제 시점 및 후속 Gibson 연결

- [ ] [WG010 Blank Workflow - MOSAIC nick repair](./004_WG010_Blank_Workflow_MOSAIC_nick_repair.labnote.md)
  - Unit operations: UHW010 Liquid Handling — phosphorylation 반응 준비 → UHW180 Incubation — phosphorylation → UHW010 Liquid Handling — ligase 첨가 → UHW180 Incubation — ligase 처리 → UHW230 Nucleic Acid Fragment Analysis — gel QC
  - 예정 산출물: nick repair 처리 산물과 처리 이력. 후처리 gel QC는 원문에 별도 기재가 없어 실시 여부 미정
  - 확인 사항: One-step 및 A/B 산물 중 적용 대상과 적용 시점

- [ ] [WB150 PCR-based Target Amplification - DVA vector PCR 및 정제](./005_WB150_PCR-based_Target_Amplification_MOSAIC_DVA_vector_preparation.labnote.md)
  - Unit operations: UHW010 Liquid Handling — PCR 반응 준비 → UHW100 Thermocycling — PCR → UHW010 Liquid Handling / UHW180 Incubation — DpnI 처리 → UHW230 Nucleic Acid Fragment Analysis — gel 확인 → UHW250 Nucleic Acid Purification — 정제 → UHW400 Manual — 농도 측정(기존 Qubit 제목 보존, 정량법 미확정)
  - 예정 산출물: 정제한 linear DVA vector, gel 이미지, 농도 측정 기록

- [ ] [WB030 DNA Assembly - MOSAIC insert–DVA Gibson assembly](./006_WB030_DNA_Assembly_MOSAIC_Gibson_assembly.labnote.md)
  - Unit operations: USW340 Computation — 투입량 계산 → UHW010 Liquid Handling — 반응 준비 → UHW180 Incubation — Gibson assembly
  - 예정 산출물: Gibson assembly 산물과 투입량 기록(상세 조건 미정). 기존 vector-only control은 원문 근거가 없어 적용 미확정
  - 확인 사항: 투입 fragment 구성·길이·몰비·조성·반응 조건 및 대조군. 원문에는 상세 Gibson 절차가 없음

- [ ] [WB150 PCR-based Target Amplification - MOSAIC 확인용 PCR](./007_WB150_PCR-based_Target_Amplification_MOSAIC_verification_PCR.labnote.md)
  - Unit operations: UHW010 Liquid Handling — PCR 반응 준비 → UHW100 Thermocycling — PCR → UHW230 Nucleic Acid Fragment Analysis — gel QC
  - 예정 산출물: 확인용 PCR 산물, gel 이미지, 확인 대상 시료 기록
  - 확인 사항: Block2 원문에는 확인용 PCR 절차가 없음. 실시 여부·template·primer·조건·실시 위치를 별도 확인하며, vector PCR의 DVA template를 옮겨 적지 않는다.

- [ ] [WG010 Blank Workflow - Transformation 및 sequencing 기록](./008_WG010_Blank_Workflow_MOSAIC_follow-up_verification_records.labnote.md)
  - 예정 작업: 별도 프로토콜을 연결하고, transformation 및 sequencing 기록과 결과를 해당 시료에 연결한다.
  - Unit operations: UHW400 Manual — Transformation 기록 → UHW400 Manual — Sequencing 기록 (기록용 입력 폼, 실제 방법은 별도 확인)
  - 예정 산출물: transformation 기록, sequencing 결과, 목표 서열과의 비교 기록

001에서 준비할 pool은 002(One-step)와 003(Two-step)으로 분기하며, 005의 vector 준비는 별도로 진행한다. 원문 개요에 따라 003에는 1차 QC와 2차 혼합·annealing을 배치하였다. 004의 적용 분기·시점과 006의 상세 조건은 미확정이다. 007은 원문에 절차가 없는 기존 입력 폼이고, 008은 개요에 있는 후속 단계의 기록 폼이다. 정제·QC·정량의 세부 순서가 불명확한 곳은 노트 블록 배치만으로 실제 순서를 확정하지 않는다.

### Unit operation 기록 기준

개별 workflow 작성 시 unit operation은 Meta → Input → Reagent → Labware and Consumables → Equipment → Method → Output → Results & Discussions 순서로 기록한다. Input과 Output에는 시료 ID를 연결하고, 합성 방식(One-step/Two-step), pool 구분, 조건, 반복 번호를 유지한다. 미실시 단계의 결과는 비워 둔다.

현재 unit operation 목록에는 Qubit 전용 항목이 없어 UHW400 Manual로 기록한다. Nick repair는 WG010 Blank Workflow로 구성한다. 위 체크리스트는 생성한 workflow 노트 8개에 연결되어 있으며, 002–005에는 원문 조건과 확인 사항을 채우고, 006–008에는 근거가 없는 상세 조건을 미확정으로 표시하였다. Qubit은 002·003에는 명시되어 있으나 005 vector 절에는 정량법이 없어 기존 제목만 보존하였다. 소프트웨어 작업은 Parameters, QC Metrics, Environment, Discussion을 포함한 소프트웨어용 양식으로 기록한다.

### 확인 필요 사항

> [!warning] Block2 Word 원문 기준 확인 사항
> - 002: 2.1의 2.5 µL pool 열은 기재 부피 합계 6.5 µL, 표기 총부피 20 µL로 누락 성분/부피가 있다. 2.3 뒤 Onepot 표는 조건 1–5 모두 20 µL로 합계가 맞으므로 기존 ‘조건 5 불일치’ 메모를 대체한다. 적용할 조성표를 확인한다.
> - 002·003: 원문 표제의 11 h 40 min은 냉각 시간이다. 초기 5 min을 포함한 총 시간과 구분하고, One-step End point 공란·4°C Hold 메모 및 Two-step Hold 미기재를 구분한다.
> - 003: 3.3의 ‘Oligo pool (A/B)’가 1차 assembly 산물인지, 1차 QC 후 A/B 각 15 µL가 확보되는지 확인한다. 3.4 제목의 ‘1st’는 2차 assembly 뒤 배치와 불일치한다. Qubit 정량 시점과 gel extraction 상세 조건도 미확정이다.
> - 004: One-step/Two-step의 T4 사용 여부와 처리 시점을 확인한다. Nick repair 후 gel QC는 원문에 별도 명시되지 않았다.
> - 005: 프라이머 이름 RSM3_Block1_DVA-F/R은 원문 그대로 보존하며 실제 사용 대상을 확인한다. DpnI 처리 PCR 양, 정제 방식·QC 선후 및 농도 측정법은 미확정이다.
> - 006: 원문 길이 Block2 1,892 bp + vector 2,001 bp의 단순 합계는 3,893 bp이고, 원문 예상 완성 plasmid는 약 3,797 bp이다. Overlap 반영 여부는 미기재이다. Gibson 조성·몰비·반응 조건과 vector-only control 적용 여부를 확인한다.
> - 007: 확인용 PCR은 선택한 원문에 절차가 없다. DVA plasmid template는 원문의 vector PCR 입력이며 확인용 PCR 입력으로 확정하지 않는다.
> - 008: Transformation·sequencing은 원문 개요에만 있어 실제 방법을 별도 확인한다. 일반 MOSAIC 문서의 조건은 보충하지 않았다.


## Summary and Discussion


