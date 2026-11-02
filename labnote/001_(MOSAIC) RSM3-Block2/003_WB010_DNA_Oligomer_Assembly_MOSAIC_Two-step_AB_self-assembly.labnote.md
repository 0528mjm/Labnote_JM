---
title: "WB010 DNA Oligomer Assembly - Two-step MOSAIC A/B self-assembly"
experimenter: "문지민"
created_date: 2026-10-29
last_updated_date: 2026-10-30
end_date: ''
---

## [WB010 DNA Oligomer Assembly] MOSAIC Two-step AB self-assembly

> This workflow focuses on assembling DNA oligomers into sequences that are several kilobases in length. The procedure typically begins with an oligomer pool and involves precise techniques to ensure accurate assembly of the desired DNA sequence.

실험 개요: [[labnote/001_(MOSAIC) RSM3-Block2/README.labnote|MOSAIC RSM3-Block2]]

작업 범위: Two-step MOSAIC A/B self-assembly

Block2 Word 프로토콜을 기존 unit operation에 배치한 예정 workflow이다. 수행일·시료 ID·실제 결과는 미기록 상태이다.

프로토콜 기준: [MOSAIC_Block2protocol.docx](../../../../Protocol/Mosaic/MOSAIC_Block2protocol.docx), 작성일 2026-09-29, Version 1. 일반 MOSAIC 문서의 조건은 사용하지 않았다.

> [!warning] 원문 확인 필요
> 원문 3.3·3.4에 2차 혼합·annealing 절차가 있다. 3.3의 ‘Oligo pool (A/B)’가 1차 assembly 산물을 뜻하는지, 1차 QC 분취 후 각 15 µL가 확보되는지, Qubit 정량의 정제 전/후 시점을 확인한다. 원문의 gel extraction 상세 절차와 후속 Gibson 연결은 미기재이다.

## Related Unit Operations

- [UHW010 Liquid Handling AB reaction preparation](#uhw010-liquid-handling-ab-reaction-preparation)
- [UHW100 Thermocycling AB annealing](#uhw100-thermocycling-ab-annealing)
- [UHW230 Nucleic Acid Fragment Analysis AB first assembly QC](#uhw230-nucleic-acid-fragment-analysis-ab-first-assembly-qc)
- [UHW010 Liquid Handling AB second reaction preparation](#uhw010-liquid-handling-ab-second-reaction-preparation)
- [UHW100 Thermocycling AB second annealing](#uhw100-thermocycling-ab-second-annealing)
- [UHW230 Nucleic Acid Fragment Analysis AB gel QC](#uhw230-nucleic-acid-fragment-analysis-ab-gel-qc)
- [UHW250 Nucleic Acid Purification AB gel extraction](#uhw250-nucleic-acid-purification-ab-gel-extraction)
- [UHW400 Manual AB Qubit quantification](#uhw400-manual-ab-qubit-quantification)

---

### [UHW010 Liquid Handling] AB reaction preparation

> 작업명: A/B 반응 준비
> This unit operation involves basic and fundamental liquid sample operations in laboratory processes, such as reagent preparation, sample distribution, dilution, mixing, and washing. It ensures precision and efficiency in handling liquid samples across various experimental setups.

#### Meta

- Experimenter: "문지민"
- Start_date: ''
- End_date: ''

#### Input

001에서 준비할 Pool A와 Pool B(각 23 oligo). 원문 1.2의 각 oligo 농도 2 µM; A/B를 구분하고 시료 ID는 실험 시 입력한다.

#### Reagent

- TE buffer (1X)
- MgCl₂ (100 mM) in TE
- DEPC-treated water

#### Labware and Consumables

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Equipment

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Method

출처: 원문 3.1. A와 B를 각각 별도 반응으로 기록한다.

| 성분 | 각 반응 부피 | 원문 농도/질량 |
| --- | --- | --- |
| Oligo pool (A/B) | 2.5 µL | 250 nM; Total 3.04 µg |
| TE buffer (1X) | 2.0 µL | 1× final |
| MgCl₂ (100 mM) in TE | 2.0 µL | 10 mM final |
| DEPC-treated water | 13.5 µL | 미기재 |
| Total | 20 µL |  |

원문에 병기된 Total DNA 범위는 2–10 µg이다. TE buffer (1X) 2 µL와 1× final의 관계는 다른 성분 용매를 포함해 확인하며, 농도를 임의로 보정하지 않는다.

**2.3 뒤 Twopot (A/B) 별도 조건표**

| 성분 | 조건 1 | 조건 2 | 조건 3 | 조건 4 | 조건 5 |
| --- | --- | --- | --- | --- | --- |
| Oligo pool (µL) | 1 | 2 | 2.5 | 3 | 4 |
| TE buffer (1X) (µL) | 17 | 16 | 15.5 | 15 | 14 |
| MgCl₂ (100 mM) in TE (µL) | 2 | 2 | 2 | 2 | 2 |
| Total | 20 µL | 20 µL | 20 µL | 20 µL | 20 µL |

Twopot 표와 3.1은 구성 성분 표기가 다르므로 합치지 않는다. 적용할 조성표·조건·반복 번호는 실제 실험 전 확정한다.

#### Output

예정 산출물: A/B별 1차 반응액 → AB annealing Input. 실제 생성 여부·시료 ID·회수량은 실험 시 기록한다.

#### Results & Discussions

---

### [UHW100 Thermocycling] AB annealing

> 작업명: Annealing
> The process of repeatedly heating and cooling through defined temperature cycles to facilitate reactions. It is used in workflows such as DNA assembly and DNA/RNA amplification, including PCR.

#### Meta

- Experimenter: "문지민"
- Start_date: ''
- End_date: ''

#### Input

직전 AB reaction preparation의 A/B별 1차 반응액.

#### Reagent

원문에 이 단계의 별도 추가 시약이 기재되어 있지 않다.

#### Labware and Consumables

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Equipment

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Method

출처: 원문 3.2. A와 B를 구분해 1차 annealing을 기록한다.

| 단계 | 온도 | 시간/속도 |
| --- | --- | --- |
| Initial denaturation | 95°C | 5 min |
| Slow cooling | 95°C → 25°C | 1°C씩 10 min마다 감소 |
| End point | 25°C | 원문 3.2·3.4 표기 |

원문에는 11 h 40 min으로 기재되어 있으나 초기 5 min을 포함한 총 시간과 구분해야 한다. Hold 조건은 이 절에 없다.

#### Output

예정 산출물: A/B별 1차 assembly 산물 → 1차 QC 및 2차 혼합 입력. 실제 생성 여부·시료 ID·회수량은 실험 시 기록한다.

#### Results & Discussions

---

### [UHW230 Nucleic Acid Fragment Analysis] AB first assembly QC

#### Meta

- Experimenter: "문지민"
- Start_date: ''
- End_date: ''

#### Input

A/B별 1차 assembly 산물의 QC용 분취분. 분취량 미정.

#### Reagent

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Labware and Consumables

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Equipment

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Method

출처: 원문 실험 개요의 ‘1st Mosaic self-assembly → Assembly QC → 2nd Mosaic self-assembly’. 1차 QC는 개요에만 있고 별도 상세 조건은 없다. 원문 후반 PCA QC의 5 µL를 이 단계의 분취량으로 확정하지 않는다. QC 방법·시료 소모량을 확인하고 잔여량과 2차 혼합에 사용할 A/B 산물을 구분한다.

#### Output

예정 산출물: 1차 QC 기록 및 잔여 A/B assembly 산물 정보 → AB second reaction preparation. 실제 시료 소모량은 미확정. 실제 생성 여부·시료 ID·회수량은 실험 시 기록한다.

#### Results & Discussions

---

### [UHW010 Liquid Handling] AB second reaction preparation

#### Meta

- Experimenter: "문지민"
- Start_date: ''
- End_date: ''

#### Input

A/B별 1차 assembly 산물 후보. 원문 3.3의 입력 명칭은 ‘Oligo pool (A/B)’로, 개요와의 대응을 확인해야 한다.

#### Reagent

원문에 이 단계의 별도 추가 시약이 기재되어 있지 않다.

#### Labware and Consumables

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Equipment

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Method

출처: 원문 3.3 ‘2nd Mosaic assembly’.

| 성분 — 원문 명칭 | 부피 | 원문 농도/질량 |
| --- | --- | --- |
| Oligo pool (A/B) | 15 + 15 µL | 250 nM; Total 3.04 µg |
| Total | 30 µL |  |

개요는 1차 산물을 이용하는 2차 assembly를 가리키지만 표는 Oligo pool로 적혀 있다. 따라서 입력 정체를 미확정으로 표시한다. A/B의 회수량·QC 분취량을 확인하기 전 각 15 µL 확보를 단정하지 않는다. 추가 buffer·효소·물은 원문에 없다. 농도·질량도 원문 표기로 보존한다.

#### Output

예정 산출물: 2차 assembly용 30 µL 혼합액(입력 정체 확인 필요) → AB second annealing. 실제 생성 여부·시료 ID·회수량은 실험 시 기록한다.

#### Results & Discussions

---

### [UHW100 Thermocycling] AB second annealing

#### Meta

- Experimenter: "문지민"
- Start_date: ''
- End_date: ''

#### Input

AB second reaction preparation의 혼합액.

#### Reagent

원문에 이 단계의 별도 추가 시약이 기재되어 있지 않다.

#### Labware and Consumables

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Equipment

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Method

출처: 원문 3.4. 이 절의 제목은 ‘1st Annealing program’이지만, 3.3 ‘2nd Mosaic assembly’ 바로 뒤에 있어 2차 단계에 배치하되 원문 제목의 불일치를 남긴다.

| 단계 | 온도 | 시간/속도 |
| --- | --- | --- |
| Initial denaturation | 95°C | 5 min |
| Slow cooling | 95°C → 25°C | 1°C씩 10 min마다 감소 |
| End point | 25°C | 원문 3.2·3.4 표기 |

원문 표제의 11 h 40 min은 냉각 시간과 전체 시간을 구분해 확인한다. 이 절에는 Hold 조건이 없다.

#### Output

예정 산출물: 2차 assembly 산물 → AB gel QC. 후속 정량·gel extraction 대상과 연결한다. 실제 생성 여부·시료 ID·회수량은 실험 시 기록한다.

#### Results & Discussions

---

### [UHW230 Nucleic Acid Fragment Analysis] AB gel QC

> 작업명: Gel QC
> To separate, identify, and characterize fragments of nucleic acids based on their size. This unit operation is crucial for genetic analysis and quality control.

#### Meta

- Experimenter: "문지민"
- Start_date: ''
- End_date: ''

#### Input

2차 assembly 산물에서 QC용 5 µL 분취분.

#### Reagent

- Agarose
- DNA ladder
- DNA stain
- Gel running buffer

#### Labware and Consumables

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Equipment

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Method

출처: 원문 3.4 뒤 PCA QC ‘5 uL loading’. 시료 5 µL를 사용하는 gel QC를 기록한다. Gel 농도·buffer 조성·전압·시간은 원문 미기재이다. 개요의 2차 Assembly QC에 대응하여 배치했으며, 1차 QC의 조건을 대신 확정하지 않는다.

#### Output

예정 산출물: 2차 assembly gel 이미지·band 관찰 기록 및 gel extraction 대상 정보. 실제 생성 여부·시료 ID·회수량은 실험 시 기록한다.

#### Results & Discussions

---

### [UHW250 Nucleic Acid Purification] AB gel extraction

> 작업명: Gel extraction
> The process of purifying DNA or RNA from biological samples using an automated device. It ensures high purity and yield for downstream applications.

#### Meta

- Experimenter: "문지민"
- Start_date: ''
- End_date: ''

#### Input

2차 assembly 산물의 gel extraction 대상. 원문은 ‘Assembled product 전체’로 기재하며, 앞선 QC·정량 분취분과의 관계는 확인 필요.

#### Reagent

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Labware and Consumables

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Equipment

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Method

출처: 원문 3.4 뒤 ‘Gel extraction Assembled product 전체’. Kit, target band 범위, gel 절취·처리 조건, 용출량은 미기재이다. Vector용 Wizard kit를 이 단계에 자동 적용하지 않는다. 원문은 PCA QC·Qubit 뒤 gel extraction을 적고 있어, 현재 양식의 정제 → Qubit 배치는 기록 위치이며 실제 정량 시점을 확정한 순서가 아니다.

#### Output

예정 산출물: 정제한 2차 assembly 산물 → [[labnote/001_(MOSAIC) RSM3-Block2/006_WB030_DNA_Assembly_MOSAIC_Gibson_assembly.labnote|006]]의 insert 후보. [[labnote/001_(MOSAIC) RSM3-Block2/004_WG010_Blank_Workflow_MOSAIC_nick_repair.labnote|004]] 적용 시점 및 후속 연결은 확인 필요. 실제 생성 여부·시료 ID·회수량은 실험 시 기록한다.

#### Results & Discussions

---

### [UHW400 Manual] AB Qubit quantification

> 작업명: Qubit 정량
> Any general process of experiment including preparation of reagents, labware, and manual operations. It encompasses traditional laboratory techniques and procedures.

#### Meta

- Experimenter: "문지민"
- Start_date: ''
- End_date: ''

#### Input

A/B 또는 2차 assembly 산물 중 실제 정량 대상. 정제 전/후를 포함한 측정 시점은 원문에서 명확하지 않아 실험 전 확인한다.

#### Reagent

Qubit dsDNA 정량용 시약. Assay 종류와 투입량은 원문 미기재.

#### Labware and Consumables

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Equipment

Qubit; 모델은 원문 미기재.

#### Method

출처: 원문 3.4 뒤 PCA QC의 ‘Qubit dsDNA 농도 측정’. 측정 대상이 1차 A/B인지 2차 산물인지, gel extraction 전인지 후인지 구분해 기록한다. 측정 조건과 희석배수는 원문에 없다.

#### Output

예정 산출물: 대상·측정 시점이 명시된 농도 기록. 정제 산물의 농도로 확인되기 전 Gibson 투입량 계산에 확정값으로 사용하지 않는다. 실제 생성 여부·시료 ID·회수량은 실험 시 기록한다.

#### Results & Discussions

## Conclusions and Discussion
