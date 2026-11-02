---
title: "WG010 Blank Workflow - MOSAIC nick repair"
experimenter: "문지민"
created_date: 2026-10-29
last_updated_date: 2026-10-30
end_date: ''
---

## [WG010 Blank Workflow] MOSAIC nick repair

> A general-purpose blank workflow template. Use this when the workflow does not fit into Design, Build, Test, or Learn categories.

실험 개요: [[labnote/001_(MOSAIC) RSM3-Block2/README.labnote|MOSAIC RSM3-Block2]]

작업 범위: MOSAIC nick repair

Block2 Word 프로토콜을 기존 unit operation에 배치한 예정 workflow이다. 수행일·시료 ID·실제 결과는 미기록 상태이다.

프로토콜 기준: [MOSAIC_Block2protocol.docx](../../../../Protocol/Mosaic/MOSAIC_Block2protocol.docx), 작성일 2026-09-29, Version 1. 일반 MOSAIC 문서의 조건은 사용하지 않았다.

> [!warning] 원문 확인 필요
> 원문에는 T4 미사용·T4 사용·Yeast 분기가 있으나, 이번 One-step/Two-step 중 적용 분기와 nick repair 시점은 명시되지 않았다. 아래 PNK·T4 조건은 T4 사용 분기의 예정 절차이며 적용 결정을 뜻하지 않는다. Nick repair 후 gel QC는 원문 4절에 별도로 명시되지 않았다.

## Related Unit Operations

- [UHW010 Liquid Handling Phosphorylation preparation](#uhw010-liquid-handling-phosphorylation-preparation)
- [UHW180 Incubation Phosphorylation incubation](#uhw180-incubation-phosphorylation-incubation)
- [UHW010 Liquid Handling Ligase addition](#uhw010-liquid-handling-ligase-addition)
- [UHW180 Incubation Ligase incubation](#uhw180-incubation-ligase-incubation)
- [UHW230 Nucleic Acid Fragment Analysis Nick repair gel QC](#uhw230-nucleic-acid-fragment-analysis-nick-repair-gel-qc)

---

### [UHW010 Liquid Handling] Phosphorylation preparation

> 작업명: Phosphorylation 반응 준비
> This unit operation involves basic and fundamental liquid sample operations in laboratory processes, such as reagent preparation, sample distribution, dilution, mixing, and washing. It ensures precision and efficiency in handling liquid samples across various experimental setups.

#### Meta

- Experimenter: "문지민"
- Start_date: ''
- End_date: ''

#### Input

원문 4-2-1의 Assembled fragment 17 µL. [[labnote/001_(MOSAIC) RSM3-Block2/002_WB010_DNA_Oligomer_Assembly_MOSAIC_One-step_self-assembly.labnote|002]] 또는 [[labnote/001_(MOSAIC) RSM3-Block2/003_WB010_DNA_Oligomer_Assembly_MOSAIC_Two-step_AB_self-assembly.labnote|003]] 중 출처와 처리 시점은 미정.

#### Reagent

- 10× T4 DNA ligase buffer: 2 µL
- Polynucleotide kinase: 1 µL

#### Labware and Consumables

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Equipment

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Method

출처: 원문 4-2-1. T4 사용 분기를 적용하기로 한 경우의 반응 준비이다.

| 성분 | 부피 |
| --- | --- |
| Assembled fragment | 17 µL |
| 10× T4 DNA ligase buffer | 2 µL |
| Polynucleotide kinase | 1 µL |
| Total | 20 µL |

원문에 enzyme 제품·활성 단위와 적용 대상 시료는 없다. 분기 선택과 시료 출처를 확인한 뒤 해당 반응으로 기록한다.

#### Output

예정 산출물: 20 µL phosphorylation 반응액 → Phosphorylation incubation. 실제 생성 여부·시료 ID·회수량은 실험 시 기록한다.

#### Results & Discussions

---

### [UHW180 Incubation] Phosphorylation incubation

> 작업명: Phosphorylation incubation
> Maintaining specific conditions for cells or chemical reactions to promote growth or desired reactions. It is essential for cell culture and biochemical assays.

#### Meta

- Experimenter: "문지민"
- Start_date: ''
- End_date: ''

#### Input

직전 Phosphorylation preparation의 20 µL 반응액.

#### Reagent

원문에 이 단계의 별도 추가 시약이 기재되어 있지 않다.

#### Labware and Consumables

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Equipment

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Method

출처: 원문 4-2-1. 37°C에서 1 h incubation. 반응 날짜·사용 장비·실제 투입 시료는 수행 시 기록한다.

#### Output

예정 산출물: Phosphorylation 처리 반응액 → Ligase addition. 실제 생성 여부·시료 ID·회수량은 실험 시 기록한다.

#### Results & Discussions

---

### [UHW010 Liquid Handling] Ligase addition

> 작업명: Ligase 첨가
> This unit operation involves basic and fundamental liquid sample operations in laboratory processes, such as reagent preparation, sample distribution, dilution, mixing, and washing. It ensures precision and efficiency in handling liquid samples across various experimental setups.

#### Meta

- Experimenter: "문지민"
- Start_date: ''
- End_date: ''

#### Input

직전 Phosphorylation incubation의 반응액.

#### Reagent

T4 DNA ligase: 1 µL; 제품·활성 단위는 원문 미기재.

#### Labware and Consumables

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Equipment

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Method

출처: 원문 4-2-2. 위 phosphorylation 반응에 T4 DNA ligase 1 µL를 추가한다. 명시 성분의 단순 부피 합계는 21 µL이며, 이는 원문에 따로 기재된 총부피가 아니라 계산값이다. 추가 희석·정제는 원문에 없다.

#### Output

예정 산출물: T4 DNA ligase 첨가 반응액 → Ligase incubation. 실제 생성 여부·시료 ID·회수량은 실험 시 기록한다.

#### Results & Discussions

---

### [UHW180 Incubation] Ligase incubation

> 작업명: Ligase incubation
> Maintaining specific conditions for cells or chemical reactions to promote growth or desired reactions. It is essential for cell culture and biochemical assays.

#### Meta

- Experimenter: "문지민"
- Start_date: ''
- End_date: ''

#### Input

직전 Ligase addition의 반응액.

#### Reagent

원문에 이 단계의 별도 추가 시약이 기재되어 있지 않다.

#### Labware and Consumables

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Equipment

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Method

출처: 원문 4-2-2. 25°C에서 1 h, 이어서 52°C에서 1 h 처리한다. 원문은 52°C 단계의 목적을 설명하지 않으므로 불활성화 등의 의미를 임의로 부여하지 않는다.

#### Output

예정 산출물: T4 처리 산물. [[labnote/001_(MOSAIC) RSM3-Block2/006_WB030_DNA_Assembly_MOSAIC_Gibson_assembly.labnote|006]] 또는 [[labnote/001_(MOSAIC) RSM3-Block2/008_WG010_Blank_Workflow_MOSAIC_follow-up_verification_records.labnote|008]]와의 연결 및 처리 시점은 미확정. 실제 생성 여부·시료 ID·회수량은 실험 시 기록한다.

#### Results & Discussions

---

### [UHW230 Nucleic Acid Fragment Analysis] Nick repair gel QC

> 작업명: Gel QC
> To separate, identify, and characterize fragments of nucleic acids based on their size. This unit operation is crucial for genetic analysis and quality control.

#### Meta

- Experimenter: "문지민"
- Start_date: ''
- End_date: ''

#### Input

Nick repair 산물 후보. QC 실시 여부·분취량은 미정.

#### Reagent

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Labware and Consumables

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Equipment

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Method

Block2 원문 4절에는 nick repair 후 gel QC가 별도 기재되어 있지 않다. 기존 UHW 입력 폼은 보존하되, 002/003의 QC 조건을 자동 복사하지 않는다. 별도 확인 후 실시 여부와 방법을 기록한다.

#### Output

예정 산출물: 실시하기로 한 경우의 nick repair 후 gel QC 기록. 현재는 미확정. 실제 생성 여부·시료 ID·회수량은 실험 시 기록한다.

#### Results & Discussions

## Conclusions and Discussion
