---
title: WG010 Blank Workflow - T7E1 treatment
experimenter: 문지민
created_date: 2026-09-01 14:00
last_updated_date: 2026-09-11
end_date: ''
---

## [WG010 Blank Workflow] T7E1 treatment

> A general-purpose blank workflow template. Use this when the workflow does not fit into Design, Build, Test, or Learn categories.

## Related Unit Operations

- [UHW010 Liquid Handling | 1st PCA product Heteroduplex 형성을 위한 혼합물](#uhw010-liquid-handling-1st-pca-product-heteroduplex)
- [UHW100 Thermocycling | 1st PCA product Heteroduplex 형성 PCR](#uhw100-thermocycling-1st-pca-product-heteroduplex-pcr)
- [UHW010 Liquid Handling | Heteroduplex 1st PCA product에 T7E1 추가](#uhw010-liquid-handling-heteroduplex-1st-pca-product-t7e1)
- [UHW100 Thermocycling | Heteroduplex 1st PCA product에 T7E1 반응](#uhw100-thermocycling-heteroduplex-1st-pca-product-t7e1)
- [UHW250 Nucleic Acid Purification | T7E1 treated product purification](#uhw250-nucleic-acid-purification-t7e1-treated-product-purification)
- [UHW230 Nucleic Acid Fragment Analysis | T7E1 treated product QC](#uhw230-nucleic-acid-fragment-analysis-t7e1-treated-product-qc)

---

### [UHW010 Liquid Handling] 1st PCA product Heteroduplex 형성을 위한 혼합물

> This unit operation involves basic and fundamental liquid sample operations in laboratory processes, such as reagent preparation, sample distribution, dilution, mixing, and washing. It ensures precision and efficiency in handling liquid samples across various experimental setups.

#### Meta
- Experimenter: '문지민'
- Start_date: '2026-09-01 10:00'
- End_date: '2026-09-01 10:10'

#### Input
- Purified 1st PCA assembled Oligo pool 1/2/3/4 30nM

#### Reagent
- Reagent-1789028119644;NEBuffer2;NEB_M0302
- Reagent-1789026237667;UltraPure™ DNase/RNase-Free Distilled Water

#### Labware and Consumables
- Labware-1789020548121;Yellow Tip_2-200 μL
- Labware-1789020678475;White Tip_0.1-10 μL
- PCR tube??

#### Equipment
- Equip-1789020568019;Pipett_200p
- Equip-1789020711244;Pipett_10p

#### Method
1. 1st oligo에 대해 Heteroduplex를 형성하기 위해 PCR tube로 다음과 같이 혼합물을 준비한다.
| Component                     | Block1-1 | Block1-2 | Block1-3 | Block1-4 |
| ----------------------------- | -------: | -------: | -------: | -------: |
| Assembly PCR product (200 ng) | 6.19 µL  | 4.64 µL  | 2.60 µL  | 2.49 µL  |
| NEBuffer 2, 10X               | 2.00 µL  | 2.00 µL  | 2.00 µL  | 2.00 µL  |
| Nuclease-free water           | 10.81 µL | 12.36 µL | 14.40 µL | 14.51 µL |
| Subtotal                      | 19.00 µL | 19.00 µL | 19.00 µL | 19.00 µL |

- Assembly PCR product의 농도는 30 nM 1st PCA product 정제 결과를 사용하였다.
- Block1-1: 32.3 ng/µL, Block1-2: 43.1 ng/µL, Block1-3: 76.8 ng/µL, Block1-4: 80.2 ng/µL
- 각 투입 부피는 200 ng을 목표로 계산하였다.

#### Output
- Heteroduplex 혼합 1st PCA product 1/2/3/4

#### Results & Discussions
- Assembly PCR product 200 ng을 이용하여 heteroduplex 형성 반응을 진행하였다.
- Heteroduplex 형성을 통해 정상 서열과 mismatch를 포함하는 DNA 간의 불일치 구조를 형성하고, 이후 T7 Endonuclease I 처리에 의한 error correction이 가능하도록 하였다.

---

### [UHW100 Thermocycling] 1st PCA product Heteroduplex 형성 PCR

> The process of repeatedly heating and cooling through defined temperature cycles to facilitate reactions. It is used in workflows such as DNA assembly and DNA/RNA amplification, including PCR.

#### Meta
- Experimenter: '문지민'
- Start_date: '2026-09-01 10:10'
- End_date: '2026-09-01 11:20'

#### Input
- Heteroduplex 혼합 1st PCA product 1/2/3/4

#### Reagent
- (None)

#### Labware and Consumables
- (None)

#### Equipment
- Equip-1789020746727;AllInOneCycler™ PCR system

#### Method
1. 준비된 19 µL heteroduplex 반응액을 PCR 장비에 넣고 아래 조건으로 denaturation 및 reannealing을 진행하였다.
| Phase            | Condition         |
| ---------------- | ----------------- |
| Denaturation     | 98°C, 5 min       |
| Rapid cooling    | 98→85°C, −2°C/s   |
| Slow reannealing | 85→16°C, −1°C/10s |
| Hold             | 4°C               |
2. 반응이 완료된 시료는 T7 Endonuclease I 처리에 사용하였다.

#### Output
- Heteroduplex 1st PCA product 1/2/3/4

#### Results & Discussions
- 고온에서 DNA를 denaturation한 후 단계적으로 reannealing하여 정상 서열과 mismatch를 포함하는 DNA 사이에 heteroduplex가 형성되도록 유도하였다.
- 형성된 mismatch-containing heteroduplex는 이후 T7 Endonuclease I 처리 단계에서 인식될 수 있도록 준비하였다.

---

### [UHW010 Liquid Handling] Heteroduplex 1st PCA product에 T7E1 추가

> This unit operation involves basic and fundamental liquid sample operations in laboratory processes, such as reagent preparation, sample distribution, dilution, mixing, and washing. It ensures precision and efficiency in handling liquid samples across various experimental setups.

#### Meta
- Experimenter: '문지민'
- Start_date: '2026-09-01 11:20'
- End_date: '2026-09-01 11:21'

#### Input
- Heteroduplex 1st PCA product 1/2/3/4

#### Reagent
- Reagent-1789028139931;T7 Endonuclease I

#### Labware and Consumables
- Labware-1789020678475;White Tip_0.1-10 μL

#### Equipment
- Equip-1789020711244;Pipett_10p

#### Method
1. Heteroduplex 형성이 완료된 19 µL DNA sample에 T7 Endonuclease I (10 U/µL) 1.0 µL를 첨가하였다.

#### Output
- T7E1 treated 1st PCA product 1/2/3/4

#### Results & Discussions
- T7E1 처리를 통해 heteroduplex에 형성된 mismatch 부위를 인식하여 절단하고자 한다.

---

### [UHW100 Thermocycling] Heteroduplex 1st PCA product에 T7E1 반응

> The process of repeatedly heating and cooling through defined temperature cycles to facilitate reactions. It is used in workflows such as DNA assembly and DNA/RNA amplification, including PCR.

#### Meta
- Experimenter: '문지민'
- Start_date: '2026-09-01 11:21'
- End_date: '2026-09-01 11:40'

#### Input
- Heteroduplex 1st PCA product 1/2/3/4

#### Reagent
- (None)

#### Labware and Consumables
- (None)

#### Equipment
- Equip-1789020746727;AllInOneCycler™ PCR system

#### Method
1. 37°C에서 15분간 반응시켰다.
2. 반응 후 즉시 DNA cleanup을 진행하였다.

#### Output
- T7E1 reacted 1st PCA product 1/2/3/4

#### Results & Discussions
- T7E1 처리를 통해 heteroduplex에 형성된 mismatch 부위를 인식하여 절단하였다.
- 처리 후 DNA를 정제하고 후속 amplification을 진행하여 상대적으로 정확한 서열을 가진 DNA를 증폭하고자한다.

---

### [UHW250 Nucleic Acid Purification] T7E1 treated product purification

> The process of purifying DNA or RNA from biological samples using an automated device. It ensures high purity and yield for downstream applications.

#### Meta
- Experimenter: '문지민'
- Start_date: '2026-09-01 11:40'
- End_date: '2026-09-01 12:20'

#### Input
- T7E1 reacted 1st PCA product 1/2/3/4

#### Reagent
- Reagent-1789020476790;Wizard® SV Gel and PCR Clean-Up System;Promega A9282
- Reagent-1789026237667;UltraPure™ DNase/RNase-Free Distilled Water

#### Labware and Consumables
- Labware-1789020945985;Blue Tip_50-1000 μL;Eppendorf_0030073479
- Labware-1789020548121;Yellow Tip_2-200 μL

#### Equipment
- Equip-1789024617432;Centrifuge 5425

#### Method
PCR 산물은 Wizard® SV Gel and PCR Clean-Up System (Promega, A9282)을 이용하여 정제하였다.
  1. T7E1 반응액에 20 µL(1:1)의 Membrane Binding Solution을 첨가
  2. 혼합액을 SV Minicolumn에 옮기고 실온에서 1분 incubation
  3. 16,000 × g에서 1분간 원심분리 후 flow-through를 제거
  4. 700 µL Membrane Wash Solution을 첨가하고 16,000 × g에서 1분간 원심분리
  5. Flow-through를 제거한 후 500 µL Membrane Wash Solution을 추가하고 16,000 × g에서 5분간 원심분리
  6. column을 추가로 1분간 원심분리
  7. Column을 새로운 1.5 mL tube로 옮기고 20 µL Nuclease-Free Water를 membrane에 첨가
  8. 실온에서 1분간 incubation한 후 16,000 × g에서 1분간 원심분리하여 DNA를 elution
  9. DNA Nanodrop 측정 후 이후 실험 진행, 나머지는 -20°C 보관

#### Output
- Purified T7E1 reacted 1st PCA product 1/2/3/4

#### Results & Discussions
- T7E1을 처리한 1st PCA 산물을 정제한 후 농도를 측정한 결과는 다음과 같다.
|         | Sample   | conc (ng/µL) |
| ------- | -------- | ------------ |
| T7E1    | Block1-1 | 10           |
| Treated | Block1-2 | 4.6          |
|         | Block1-3 | 5.2          |
|         | Block1-4 | 7.1          |
2. 

---

### [UHW230 Nucleic Acid Fragment Analysis] T7E1 treated product QC

> To separate, identify, and characterize fragments of nucleic acids based on their size. This unit operation is crucial for genetic analysis and quality control.

#### Meta
- Experimenter: 문지민
- Start_date: '2026-09-10 17:12'
- End_date: '2026-09-10 17:35'

#### Input
- Purified T7E1 reacted 1st PCA product 1/2/3/4

#### Reagent
- Reagent-1789027092951;E-Gel™ EX Agarose Gels, 1%;Invitrogen_G401001
- Reagent-1789027106924;E-Gel™ 1 Kb Plus Express DNA Ladder;Invitrogen_10488091
- Reagent-1789027142713;E-Gel™ Sample Loading Buffer (1X);Invitrogen_10482055
- Reagent-1789026237667;UltraPure™ DNase/RNase-Free Distilled Water

#### Labware and Consumables
- Labware-1789020678475;White Tip_0.1-10 μL
- Labware-1789020548121;Yellow Tip_2-200 μL

#### Equipment
- Equip-1789020711244;Pipett_10p;eppendorf
- Equip-1789020568019;Pipett_200p;eppendorf
- Equip-1789027063130;E-Gel™ Power Snap Electrophoresis System;Invitrogen_G8300

#### Method
1. E-Gel™ EX Agarose Gel을 E-Gel™ Power Snap Electrophoresis System에 장착한다.
2. T7E1 처리된 각 sample(Block1-1~4)을 다음과 같이 혼합한다.
| Component      | Volume (µL) |
| -------------- | ----------- |
| PCR product    | 5           |
| 1× Loading dye | 15          |
| Total          | 20          |
3. Marker는 다음과 같이 혼합한다.
| Component  | Volume (µL) |
| ---------- | ----------- |
| DNA Marker | 3           |
| D.W.       | 17          |
| Total      | 20          |
4. 충분히 혼합한 후 13 min 동안 loading을 진행한다.
5. 장치를 이용해 Gel 사진을 찍는다.

#### Output
![KakaoTalk_20260901_154415454_02.jpg](KakaoTalk_20260901_154415454_02.jpg)

#### Results & Discussions
- T7E1 처리 후 purification된 1st PCA 산물들을 E-Gel 분석하였다.
- T7E1 처리를 한 왼쪽 4개의 sample에 대해서 band가 관찰되지 않아, T7E1 처리에 대한 평가가 불가능하였다.
- T7E1 처리된 산물의 pure한 정상 서열을 포함하는 DNA는 이후 2차 amplification 단계로 진행하여 충분한 양의 DNA를 확보할 수 있도록 하였다.

## Conclusions and Discussion

