---
title: "WB010 DNA Oligomer Assembly - One-step MOSAIC self-assembly"
experimenter: "문지민"
created_date: 2026-10-29
last_updated_date: 2026-10-30
end_date: ''
---

## [WB010 DNA Oligomer Assembly] MOSAIC One-step self-assembly

> This workflow focuses on assembling DNA oligomers into sequences that are several kilobases in length. The procedure typically begins with an oligomer pool and involves precise techniques to ensure accurate assembly of the desired DNA sequence.

실험 개요: [[labnote/001_(MOSAIC) RSM3-Block2/README.labnote|MOSAIC RSM3-Block2]]
## Related Unit Operations

- [UHW010 Liquid Handling | Oligo pool 생성](#uhw010-liquid-handling-oligo-pool-생성)
- [UHW010 Liquid Handling | One-step reaction preparation](#uhw010-liquid-handling-one-step-reaction-preparation)
- [UHW100 Thermocycling | One-step annealing](#uhw100-thermocycling-one-step-annealing)
- [UHW230 Nucleic Acid Fragment Analysis | One-step gel QC](#uhw230-nucleic-acid-fragment-analysis-one-step-gel-qc)
- [UHW400 Manual | One-step Qubit quantification](#uhw400-manual-one-step-qubit-quantification)



---

### [UHW010 Liquid Handling] Oligo pool 생성

> This unit operation involves basic and fundamental liquid sample operations in laboratory processes, such as reagent preparation, sample distribution, dilution, mixing, and washing. It ensures precision and efficiency in handling liquid samples across various experimental setups.

#### Meta
- Experimenter: 문지민
- Start_date: '2026-10-30 17:54'
- End_date: ''

#### Input
- DNA-1793350383655;RSM3-Block2-Oligo-96well plate

#### Reagent
- Reagent-1789026237667;UltraPure™ DNase/RNase-Free Distilled Water

#### Labware and Consumables
- Labware-1789020548121;Yellow Tip_2-200 μL

#### Equipment
- Equip-1789020568019;Pipett_200p

#### Method
1. Oligo pool 46개와 Outer primer 2개, Gibson primer 2개에 Nuclease-free water를 첨가하여 100 pmol/μL (100 μM) 농도로 resuspension하였다.
2. Oligo가 충분히 용해되도록 5 min 동안 vortexing하였다.
3. Gibson primer에 대해 100 μM oligo를 1:10으로 희석하여 10 μM working solution을 제조하였다.
4. Resuspension된 oligo는 −20°C에서 보관하였다.

#### Output
- DNA-1793090183678;RSM3-Block2-Oligopool-46
- DNA-1793090292018;RSM3-Block2-OligopoolA-23
- DNA-1793090350017;RSM3-Block2-OligopoolB-23

#### Results & Discussions
- (Any results and discussions. Link file path if needed)

---

### [UHW010 Liquid Handling] One-step reaction preparation

> 작업명: Oligo pool 제작

#### Meta

- Experimenter: "문지민"
- Start_date: ''
- End_date: ''

#### Input
DNA-1793090183678;RSM3-Block2-Oligopool-46
DNA-1793090292018;RSM3-Block2-OligopoolA-23
DNA-1793090350017;RSM3-Block2-OligopoolB-23

#### Reagent

- TE buffer (1X)
- MgCl₂ (100 mM) in TE

#### Labware and Consumables

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Equipment

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Method

**2.1 반응 조성 — 원문 표기 보존**

| 성분 | 2.5 µL pool 조건 | 3.0 / 4.0 µL pool 조건 |
| --- | --- | --- |
| Oligo pool | 2.5 µL; 250 nM; Total 6.1 µg | 3.0 / 4.0 µL; 300 nM / 400 (단위 원문 생략); Total 7.32 / 9,76 µg (원문 표기) |
| TE buffer (1X) | 2.0 µL; 1× final | 15 / 14 µL; 1× final |
| MgCl₂ (100 mM) in TE | 2.0 µL; 10 mM final | 2.0 µL; 10 mM final |
| Total | 20 µL | 20 µL |

> [!warning] 조성 확인 필요
> 2.5 µL pool 열의 부피 합계는 6.5 µL이다. 원문에는 나머지 13.5 µL에 해당하는 성분이 없다. Two-step의 물 첨가 조건을 이 표에 옮겨 넣지 않는다.

**2.3 뒤 Onepot 조건표 — 원문 열 순서 유지**

| 성분 | 조건 1 | 조건 2 | 조건 3 | 조건 4 | 조건 5 |
| --- | --- | --- | --- | --- | --- |
| Oligo pool (µL) | 1 | 2 | 2.5 | 3 | 4 |
| TE buffer (1X) (µL) | 17 | 16 | 15.5 | 15 | 14 |
| MgCl₂ (100 mM) in TE (µL) | 2 | 2 | 2 | 2 | 2 |
| Total | 20 µL | 20 µL | 20 µL | 20 µL | 20 µL |

원문 표의 개별 부피 숫자는 µL 기준으로 정리하였다. 각 조건을 별도 기록하며, 선택 조건·반복 번호·pool 시료 ID는 실제 실험 시 입력한다. 앞쪽 2.1 표와 혼합해 새 조성을 만들지 않는다.

#### Output
DNA-1793090183678;RSM3-Block2-Oligopool-46
DNA-1793090292018;RSM3-Block2-OligopoolA-23
DNA-1793090350017;RSM3-Block2-OligopoolB-23

#### Results & Discussions

---

### [UHW100 Thermocycling] One-step annealing

> 작업명: Annealing
> The process of repeatedly heating and cooling through defined temperature cycles to facilitate reactions. It is used in workflows such as DNA assembly and DNA/RNA amplification, including PCR.

#### Meta

- Experimenter: "문지민"
- Start_date: ''
- End_date: ''

#### Input

직전 One-step reaction preparation의 조건별 반응액.

#### Reagent

원문에 이 단계의 별도 추가 시약이 기재되어 있지 않다.

#### Labware and Consumables

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Equipment

Thermocycler 사용 장비·모델은 원문에 별도 명시되지 않아 실험 시 기록한다.

#### Method

출처: 원문 2.2 Annealing program.

| 단계 | 온도 | 시간/속도 |
| --- | --- | --- |
| Initial denaturation | 95°C | 5 min |
| Slow cooling | 95°C → 25°C | 1°C씩 10 min마다 감소 |
| End point | 원문 표의 온도 숫자 공란 | 미기재 |
| Hold | 4°C | 원문 메모: ‘Hold 온도는 얼마? 4도’; 시간 미기재 |

원문 제목은 11 h 40 min이다. 70°C를 1°C/10 min으로 냉각하는 시간만 11 h 40 min이고, 초기 5 min을 포함하면 11 h 45 min이므로 총 프로그램 시간은 확인한다. End point 표의 공란과 냉각 종료 25°C 표기를 구분해 보존한다.

#### Output

예정 산출물: 조건별 One-step assembly 산물 → gel QC·Qubit 정량용 분취. 후속 nick repair 적용 여부는 [[labnote/001_(MOSAIC) RSM3-Block2/004_WG010_Blank_Workflow_MOSAIC_nick_repair.labnote|004]]에서 확인. 실제 생성 여부·시료 ID·회수량은 실험 시 기록한다.

#### Results & Discussions

---

### [UHW230 Nucleic Acid Fragment Analysis] One-step gel QC

> 작업명: Gel QC
> To separate, identify, and characterize fragments of nucleic acids based on their size. This unit operation is crucial for genetic analysis and quality control.

#### Meta

- Experimenter: "문지민"
- Start_date: ''
- End_date: ''

#### Input

One-step annealing 산물에서 조건별 5 µL 분취분.

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

출처: 원문 2.3 PCA QC. 시료 5 µL를 사용한 gel QC를 기록한다. Agarose 농도, buffer 조성, stain 제품, 전압·시간은 원문 미기재이며 다른 문서의 조건을 보충하지 않는다. 조건별 lane과 원시 이미지 연결은 실제 수행 시 입력한다.

#### Output

예정 산출물: 조건별 gel 이미지와 band 관찰 기록. Gel에 사용한 분취분과 후속 반응용 잔여 산물을 구분한다. 실제 생성 여부·시료 ID·회수량은 실험 시 기록한다.

#### Results & Discussions

---

### [UHW400 Manual] One-step Qubit quantification

> 작업명: Qubit 정량
> Any general process of experiment including preparation of reagents, labware, and manual operations. It encompasses traditional laboratory techniques and procedures.

#### Meta

- Experimenter: "문지민"
- Start_date: ''
- End_date: ''

#### Input

One-step assembly 산물의 정량용 분취분. Gel에 사용한 분취분과 구분한다.

#### Reagent

Qubit dsDNA 정량용 시약. Assay 종류·제품·시료 및 시약 투입량은 원문 미기재.

#### Labware and Consumables

원문에 상세 정보 없음. 실제 사용 내역은 실험 시 기록한다.

#### Equipment

Qubit; 모델은 원문 미기재.

#### Method

출처: 원문 2.3 ‘Qubit dsDNA 농도 측정’. 정량 대상의 조건·반복 번호·시료 ID와 측정 농도를 연결한다. 구체적인 assay 절차·분취량·희석배수는 원문에 없어 임의로 채우지 않는다.

#### Output

예정 산출물: 조건별 농도 측정 기록과 잔여 assembly 산물 정보 → [[labnote/001_(MOSAIC) RSM3-Block2/006_WB030_DNA_Assembly_MOSAIC_Gibson_assembly.labnote|006]]의 투입량 확인 자료. 004 적용 여부는 미확정. 실제 생성 여부·시료 ID·회수량은 실험 시 기록한다.

#### Results & Discussions

## Conclusions and Discussion
