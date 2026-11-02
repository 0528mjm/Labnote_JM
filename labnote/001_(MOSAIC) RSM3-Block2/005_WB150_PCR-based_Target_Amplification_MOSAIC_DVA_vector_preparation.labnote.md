---
title: "WB150 PCR-based Target Amplification - DVA vector PCR 및 정제"
experimenter: "문지민"
created_date: 2026-10-29
last_updated_date: 2026-10-30
end_date: ''
---

## [WB150 PCR-based Target Amplification] MOSAIC DVA vector preparation

> This workflow utilizes designed primers and Polymerase Chain Reaction (PCR) to specifically amplify a target gene sequence from complex templates such as genomic DNA or metagenomic samples, enabling gene screening and retrieval.

실험 개요: [[labnote/001_(MOSAIC) RSM3-Block2/README.labnote|MOSAIC RSM3-Block2]]

작업 범위: DVA vector PCR 및 정제

Block2 Word 프로토콜을 기존 unit operation에 배치한 예정 workflow이다. 수행일·시료 ID·실제 결과는 미기록 상태이다.

프로토콜 기준: [MOSAIC_Block2protocol.docx](../../../../Protocol/Mosaic/MOSAIC_Block2protocol.docx), 작성일 2026-09-29, Version 1. 일반 MOSAIC 문서의 조건은 사용하지 않았다.

> [!warning] 원문 확인 필요
> 원문 예상 vector PCR 산물은 약 2,001 bp이다. 프라이머 이름은 Block2 문서 안에서도 RSM3_Block1_DVA-F/R로 적혀 있어 그대로 보존하고 실제 사용 프라이머를 확인한다. 개요의 Block2 1,892 bp + vector 2,001 bp 단순 합계는 3,893 bp로 예상 완성 plasmid 3,797 bp와 다르며, overlap 반영 여부는 미기재이다. 정제와 QC의 정확한 순서, loading dye의 최종 농도도 확인한다.

## Related Unit Operations

- [UHW010 Liquid Handling Vector PCR preparation](#uhw010-liquid-handling-vector-pcr-preparation)
- [UHW100 Thermocycling Vector PCR](#uhw100-thermocycling-vector-pcr)
- [UHW010 Liquid Handling DpnI preparation](#uhw010-liquid-handling-dpni-preparation)
- [UHW180 Incubation DpnI incubation](#uhw180-incubation-dpni-incubation)
- [UHW230 Nucleic Acid Fragment Analysis Vector gel QC](#uhw230-nucleic-acid-fragment-analysis-vector-gel-qc)
- [UHW250 Nucleic Acid Purification Vector purification](#uhw250-nucleic-acid-purification-vector-purification)
- [UHW400 Manual Vector Qubit quantification](#uhw400-manual-vector-qubit-quantification)

---

### [UHW010 Liquid Handling] Vector PCR preparation

> 작업명: PCR 반응 준비
> This unit operation involves basic and fundamental liquid sample operations in laboratory processes, such as reagent preparation, sample distribution, dilution, mixing, and washing. It ensures precision and efficiency in handling liquid samples across various experimental setups.

#### Meta

- Experimenter: "문지민"
- Start_date: ''
- End_date: ''

#### Input

- DVA plasmid template: 1 µL, total 1–10 ng.
- 실제 template 시료 ID는 미정.

#### Reagent

- KOD One PCR Master Mix (2X)
- RSM3_Block1_DVA-F (10 µM)
- RSM3_Block1_DVA-R (10 µM)
- Nuclease-free water

#### Labware and Consumables

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Equipment

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Method

출처: 원문 5 DVA Vector PCR 아래 ‘7.1 반응 조성’.

| 성분 | Working concentration / 투입량 기준 | 부피 |
| --- | --- | --- |
| KOD One PCR Master Mix | 2X | 25.0 µL |
| RSM3_Block1_DVA-F | 10 µM | 1.5 µL |
| RSM3_Block1_DVA-R | 10 µM | 1.5 µL |
| DVA plasmid template | 1–10 ng total | 1 µL |
| Nuclease-free water | — | 21 µL |
| Total |  | 50.0 µL |

프라이머의 Block1 이름은 원문 그대로이며 Block2로 바꾸지 않는다. 실제 시료·primer 식별자는 확인 후 기록한다.

#### Output

예정 산출물: 50 µL vector PCR 반응액 → Vector PCR. 실제 생성 여부·시료 ID·회수량은 실험 시 기록한다.

#### Results & Discussions

---

### [UHW100 Thermocycling] Vector PCR

> 작업명: PCR
> The process of repeatedly heating and cooling through defined temperature cycles to facilitate reactions. It is used in workflows such as DNA assembly and DNA/RNA amplification, including PCR.

#### Meta

- Experimenter: "문지민"
- Start_date: ''
- End_date: ''

#### Input

Vector PCR preparation의 50 µL 반응액.

#### Reagent

원문에 이 단계의 별도 추가 시약이 기재되어 있지 않다.

#### Labware and Consumables

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Equipment

Thermocycler; 모델은 원문 미기재.

#### Method

출처: 원문 5의 Thermocycler program.

| Phase | Temperature | Time | Cycles |
| --- | --- | --- | --- |
| Pre-denaturation | 98°C | 2 min | 1 |
| Denaturation | 98°C | 10 s | 30 |
| Annealing (Tm = 67°C) | 62°C | 5 s | 30 |
| Extension | 68°C | 15 s | 30 |
| Final extension | 68°C | 30 s | 1 |
| Hold | 4°C | hold | — |

Denaturation → Annealing → Extension을 한 cycle로 하여 30회 수행하는 프로그램으로 기록한다. 원문 예상 PCR product는 약 2,001 bp이다. 원문에 있는 제조사 extension 참고 메모(기본 5 s/kb, low-copy 10 s/kb)는 별도 확인 전 프로그램 변경 근거로 사용하지 않고, 표의 15 s를 보존한다.

#### Output

예정 산출물: 예상 길이 약 2,001 bp의 vector PCR 산물 → DpnI preparation. 실제 증폭 성공은 미기록. 실제 생성 여부·시료 ID·회수량은 실험 시 기록한다.

#### Results & Discussions

---

### [UHW010 Liquid Handling] DpnI preparation

> 작업명: DpnI 처리 준비
> This unit operation involves basic and fundamental liquid sample operations in laboratory processes, such as reagent preparation, sample distribution, dilution, mixing, and washing. It ensures precision and efficiency in handling liquid samples across various experimental setups.

#### Meta

- Experimenter: "문지민"
- Start_date: ''
- End_date: ''

#### Input

Vector PCR 산물. 원문은 ‘PCR product’로만 표기하고 처리할 분취량은 별도 명시하지 않는다.

#### Reagent

DpnI: 1 µL (20 U).

#### Labware and Consumables

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Equipment

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Method

출처: 원문 5 아래 ‘7.2 DpnI 처리’. PCR product에 DpnI 1 µL (20 U)를 첨가한다. 전체 50 µL를 처리하는지 분취 처리인지 확인한다. 별도 buffer 첨가·총부피는 원문에 없어 확정하지 않는다.

#### Output

예정 산출물: DpnI 첨가 PCR 산물 → DpnI incubation. 실제 생성 여부·시료 ID·회수량은 실험 시 기록한다.

#### Results & Discussions

---

### [UHW180 Incubation] DpnI incubation

> 작업명: DpnI incubation
> Maintaining specific conditions for cells or chemical reactions to promote growth or desired reactions. It is essential for cell culture and biochemical assays.

#### Meta

- Experimenter: "문지민"
- Start_date: ''
- End_date: ''

#### Input

DpnI preparation의 반응액.

#### Reagent

원문에 이 단계의 별도 추가 시약이 기재되어 있지 않다.

#### Labware and Consumables

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Equipment

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Method

출처: 원문 7.2. 37°C에서 30 min 반응한다. 이후의 불활성화 조건은 원문에 없다.

#### Output

예정 산출물: DpnI 처리 vector PCR 산물 → Cleanup & QC. 정제와 gel 확인의 순서는 원문에서 확정되지 않았다. 실제 생성 여부·시료 ID·회수량은 실험 시 기록한다.

#### Results & Discussions

---

### [UHW230 Nucleic Acid Fragment Analysis] Vector gel QC

> 작업명: Gel 확인
> To separate, identify, and characterize fragments of nucleic acids based on their size. This unit operation is crucial for genetic analysis and quality control.

#### Meta

- Experimenter: "문지민"
- Start_date: ''
- End_date: ''

#### Input

Vector PCR product 5 µL. DpnI 처리·정제 전후 중 어느 시점의 시료인지 확인한다.

#### Reagent

- Agarose
- 10× dye: 2 µL
- D.W: 13 µL
- Ladder·stain·running buffer의 상세 정보는 이 절에 미기재.

#### Labware and Consumables

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Equipment

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Method

출처: 원문 Cleanup & QC.

| Loading 성분 | 부피 |
| --- | --- |
| PCR product | 5 µL |
| 10× dye | 2 µL |
| D.W | 13 µL |
| 합계 — 기재 성분 계산값 | 20 µL |

Agarose gel에 loading하며 예상 full-length band는 약 2 kb이다. Gel 농도·전압·시간은 미기재이다. Dye 표기는 10× 2 µL/총 20 µL로 계산상 최종 1×이나, 원문 의도와 사용 제품을 확인하며 농도나 부피를 임의로 수정하지 않는다.

#### Output

예정 산출물: Vector PCR gel 이미지·예상 약 2 kb band의 관찰 기록. 정제용 시료와 QC 분취분을 구분한다. 실제 생성 여부·시료 ID·회수량은 실험 시 기록한다.

#### Results & Discussions

---

### [UHW250 Nucleic Acid Purification] Vector purification

> 작업명: 정제
> The process of purifying DNA or RNA from biological samples using an automated device. It ensures high purity and yield for downstream applications.

#### Meta

- Experimenter: "문지민"
- Start_date: ''
- End_date: ''

#### Input

DpnI 처리 vector PCR 산물 후보. Gel 정제와 PCR cleanup 중 실제 적용 방식 및 QC와의 선후 관계는 확인 필요.

#### Reagent

Wizard® SV Gel and PCR Clean-Up System (Promega A9282). 개별 buffer·투입량은 원문 미기재.

#### Labware and Consumables

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Equipment

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Method

출처: 원문 Cleanup & QC. Wizard® SV Gel and PCR Clean-Up System (Promega A9282), elution 50 µL. Kit 안의 개별 처리 단계·원심 조건·용출액 종류는 원문에 없어 추가하지 않는다. 원문에 정제 방식이나 QC 선후가 확정되어 있지 않으므로 기존 블록 순서는 실제 수행 순서를 뜻하지 않는다.

#### Output

예정 산출물: 50 µL 용출로 계획한 정제 vector 산물 → 농도 측정 및 [[labnote/001_(MOSAIC) RSM3-Block2/006_WB030_DNA_Assembly_MOSAIC_Gibson_assembly.labnote|006]] 입력 후보. 실제 생성 여부·시료 ID·회수량은 실험 시 기록한다.

#### Results & Discussions

---

### [UHW400 Manual] Vector Qubit quantification

> 작업명: Qubit 정량
> Any general process of experiment including preparation of reagents, labware, and manual operations. It encompasses traditional laboratory techniques and procedures.

#### Meta

- Experimenter: "문지민"
- Start_date: ''
- End_date: ''

#### Input

정제 vector 산물의 정량용 분취분 후보. 측정 대상·시점 확인 필요.

#### Reagent

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Labware and Consumables

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Equipment

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Method

출처: 원문 Cleanup & QC의 ‘농도 측정’. Vector 절에는 Qubit이 명시되지 않았다. 기존 UHW400과 제목은 보존하지만 정량법을 Qubit으로 확정하지 않는다. 방법·장비·시약·분취량·희석배수는 실제 사용법 확인 후 기록한다.

#### Output

예정 산출물: 방법·대상·농도가 연결된 vector 농도 기록 → [[labnote/001_(MOSAIC) RSM3-Block2/006_WB030_DNA_Assembly_MOSAIC_Gibson_assembly.labnote|006]]의 투입량 확인 자료. 실제 생성 여부·시료 ID·회수량은 실험 시 기록한다.

#### Results & Discussions

## Conclusions and Discussion
