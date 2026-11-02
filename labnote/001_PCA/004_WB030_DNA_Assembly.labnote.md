---
title: WB030 DNA Assembly - Outer primer amplification & 2nd PCA assembly
experimenter: 문지민
created_date: 2026-09-08
last_updated_date: 2026-09-11
end_date: ''
---

## [WB030 DNA Assembly] Outer primer amplification & 2nd PCA assembly

> This workflow is dedicated to assembling double-stranded DNA fragments into sequences that are several kilobases or larger. It includes the assembly of multiple DNA fragments, such as parts or operon-level sequences, in a specific order to achieve the desired genetic construct.

## Related Unit Operations

- [UHW010 Liquid Handling | Outer primer 혼합조성](#uhw010-liquid-handling-outer-primer)
- [UHW100 Thermocycling | Outer-primer recovery PCR](#uhw100-thermocycling-outer-primer-recovery-pcr)
- [UHW250 Nucleic Acid Purification | Recovery PCR product purification](#uhw250-nucleic-acid-purification-recovery-pcr-product-purification)
- [UHW230 Nucleic Acid Fragment Analysis | Recovery PCR product QC](#uhw230-nucleic-acid-fragment-analysis-recovery-pcr-product-qc)
- [UHW010 Liquid Handling | 2nd PCA Gibson assembly 혼합조성](#uhw010-liquid-handling-2nd-pca-gibson-assembly)
- [UHW100 Thermocycling | 2nd PCA Gibson assembly](#uhw100-thermocycling-2nd-pca-gibson-assembly)
- [UHW250 Nucleic Acid Purification | 2nd PCA product purification](#uhw250-nucleic-acid-purification-2nd-pca-product-purification)
- [UHW230 Nucleic Acid Fragment Analysis | 2nd PCA product QC](#uhw230-nucleic-acid-fragment-analysis-2nd-pca-product-qc)

---

### [UHW010 Liquid Handling] Outer primer 혼합조성

> This unit operation involves basic and fundamental liquid sample operations in laboratory processes, such as reagent preparation, sample distribution, dilution, mixing, and washing. It ensures precision and efficiency in handling liquid samples across various experimental setups.

#### Meta
- Experimenter: 문지민
- Start_date: '2026-09-11 13:46'
- End_date: ''

#### Input
- Purified T7E1 reacted 1st PCA product 1/2/3/4

#### Reagent
- Reagent-1788851665659;KOD- KOD One PCR Master Mix (Toyobo_KMM-101)
- Reagent-1789026237667;UltraPure™ DNase/RNase-Free Distilled Water
- RSM3_Block1-1/2/3/4_Out-F and Out-R;10 µM working stock

#### Labware and Consumables
- Labware-1789020678475;White Tip_0.1-10 µL;Eppendorf_0030073371
- Labware-1789020548121;Yellow Tip_2-200 µL
- PCR tube

#### Equipment
- Equip-1789020711244;Pipett_10p;Eppendorf
- Equip-1789020568019;Pipett_200p

#### Method
1. 각 block의 T7E1-treated product에 대응하는 outer primer pair를 다음과 같이 배정하였다.
| Block     | Forward primer         | Reverse primer          |
| --------- | ---------------------- | ----------------------- |
| Block 1-1 | RSM3_Block1-1_Out-F    | RSM3_Block1-1_Out-R     |
| Block 1-2 | RSM3_Block1-2_Out-F    | RSM3_Block1-2_Out-R     |
| Block 1-3 | RSM3_Block1-3_Out-F    | RSM3_Block1-3_Out-R     |
| Block 1-4 | RSM3_Block1-4_Out-F    | RSM3_Block1-4_Out-R     |
2. 각 반응은 40.0 µL가 되도록 아래와 같이 혼합하였다.
| Component               | Working concentration| Volume    | Final concentration |
| ----------------------- | -------------------- | --------- | ------------------- |
| KOD One PCR Master Mix  | 2X                   | 20.0 µL   | 1X                  |
| T7E1-treated product    | -                    | x µL      | 50 ng               |
| Forward primer          | 10 µM                | 2.0 µL    | 0.5 µM              |
| Reverse primer          | 10 µM                | 2.0 µL    | 0.5 µM              |
| Nuclease-free water     | -                    | 16 - x µL | -                   |
| Total                   | -                    | 40.0 µL   | -                   |

- 각 block의 DNA 농도값을 기준으로 50 ng의 T7E1-treated product를 투입하는 경우의 부피는 다음과 같이 계산하였다.
| Block     | DNA conc (ng/µL) | T7E1-treated product | Nuclease-free water |
| --------- | ---------------- | -------------------- | ------------------- |
| Block 1-1 | 66.6             | 0.75                 | 15.25               |
| Block 1-2 | 60.2             | 0.83                 | 15.17               |
| Block 1-3 | 88.7             | 0.56                 | 15.44               |
| Block 1-4 | 93.4             | 0.54                 | 15.46               |

#### Output
- Outer-primer amplified 1st PCA product 1/2/3/4

#### Results & Discussions
- T7E1 처리 산물에 outer primer를 추가하여 후속 2nd PCA assembly에 사용할 recovery PCR 산물을 확보하였다.
- 각 block의 template 농도에 따라 투입 부피를 조정하여 모든 반응에 동일한 양의 DNA(50 ng)가 들어가도록 하였다. 이를 통해 template 양의 차이로 인해 발생할 수 있는 block별 amplification 편차를 줄이고자 하였다.
- Forward primer와 Reverse primer는 각각 0.5 µM의 동일한 최종 농도로 설정하여 primer pair 간 농도 불균형을 방지하였다.

---

### [UHW100 Thermocycling] Outer-primer recovery PCR

#### Meta
- Experimenter: 문지민
- Start_date: '2026-09-11'
- End_date: ''

#### Input
- Outer-primer PCR reaction mixture 1/2/3/4

#### Reagent
- (None)

#### Labware and Consumables
- PCR tube

#### Equipment
- Equip-1789020746727;AllInOneCycler™ PCR system

#### Method
| Phase            | Temperature | Time  | Cycles |
| ---------------- | ----------- | ----- | ------ |
| Pre-denaturation | 98°C        | 2 min | 1      |
| Denaturation     | 98°C        | 10 s  | 30     |
| Annealing        | 56°C        | 5 s   | 30     |
| Extension        | 68°C        | 5 s   | 30     |
| Final extension  | 68°C        | 30 s  | 1      |
| Hold             | 4°C         | hold  | -      |

#### Output
- Outer-primer amplified 1st PCA product 1/2/3/4

#### Results & Discussions
- 각 subblock의 outer primer를 이용해 후속 assembly에 필요한 말단 서열을 포함하는 recovery PCR을 수행하였다.
- 30 cycle의 증폭을 통해 T7E1 처리 후 상대적으로 적은 양으로 남아 있을 수 있는 1st PCA 산물을 2nd PCA에 사용할 수 있는 양까지 증폭하고자 하였다.
- 56°C annealing과 68°C extension 조건은 outer primer의 결합과 polymerase에 의한 DNA 합성이 연속적으로 이루어지도록 설정한 조건이다.
- 이 단계의 성공 여부는 이후 agarose gel에서 각 subblock에 해당하는 473, 470, 483, 458 bp band가 단일하고 선명하게 관찰되는지로 확인하였다.

---

### [UHW250 Nucleic Acid Purification] Recovery PCR product purification

#### Meta
- Experimenter: 문지민
- Start_date: ''
- End_date: ''

#### Input
- Outer-primer amplified 1st PCA product 1/2/3/4

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
1. Recovery PCR 산물에 동일 부피(1:1)의 Membrane Binding Solution을 첨가하고 충분히 혼합하였다.
2. 혼합액을 SV Minicolumn에 옮기고 실온에서 1분간 incubation하였다.
3. 16,000 × g에서 1분간 원심분리한 후 flow-through를 제거하였다.
4. 700 µL Membrane Wash Solution을 첨가하고 16,000 × g에서 1분간 원심분리하였다.
5. Flow-through를 제거한 후 500 µL Membrane Wash Solution을 추가하고 16,000 × g에서 5분간 원심분리하였다.
6. Column을 추가로 1분간 원심분리하여 membrane을 건조하였다.
7. Column을 새로운 1.5 mL tube로 옮기고 40 µL Nuclease-free Water를 membrane 중앙에 첨가하였다.
8. 실온에서 1분간 incubation한 후 16,000 × g에서 1분간 원심분리하여 DNA를 elution하였다.
9. Eluted DNA의 농도를 Nanodrop으로 측정하고, 이후 실험 전까지 나머지 시료는 -20°C에 보관하였다.

#### Output
- Purified outer-primer amplified 1st PCA product 1/2/3/4

#### Results & Discussions
- Recovery PCR 산물을 정제하여 2nd PCA assembly의 fragment로 사용할 준비를 하였다.
- 정제된 산물의 농도는 다음과 같다.
|       | Sample   | conc (ng/µL) |
| ----- | -------- | ------------ |
| Outer | Block1-1 | 66.6         |
|       | Block1-2 | 60.2         |
|       | Block1-3 | 88.7         |
|       | Block1-4 | 93.4         |

- 모든 fragment에서 60 ng/µL 이상의 농도가 확인되어, 2nd PCA assembly에 필요한 각 fragment 50 ng을 충분히 확보할 수 있었다.
- Fragment별 농도 차이를 보정하기 위해 각 시료의 농도를 기준으로 투입 부피를 계산하여 동일한 DNA 질량이 반응에 들어가도록 하였다.
- 정제된 recovery PCR 산물은 농도 측정 후 -20°C에 보관하였으며, QC 결과를 확인한 뒤 2nd PCA Gibson assembly에 사용하였다.

---

### [UHW230 Nucleic Acid Fragment Analysis] Recovery PCR product QC

#### Meta
- Experimenter: 문지민
- Start_date: ''
- End_date: ''

#### Input
- Purified outer-primer amplified 1st PCA product 1/2/3/4

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
1. E-Gel™ EX Agarose Gel을 E-Gel™ Power Snap Electrophoresis System에 장착하였다.
2. 각 recovery PCR product(Block1-1~4) 5 µL에 E-Gel™ Sample Loading Buffer (1X) 15 µL를 첨가하여 총 20 µL의 sample을 준비하였다.
| Component     | Volume (µL) |
| ------------- | ----------- |
| PCR product   |           5 |
| 1× Loading dye|          15 |
| Total         |          20 |
3. DNA marker는 다음과 같이 혼합하여 준비하였다.
| Component           | Volume (µL) |
| ------------------- | ----------- |
| DNA Marker          |           3 |
| Nuclease-free water |          17 |
| Total               |          20 |
4. Sample과 marker를 E-Gel™에 loading하고 13분간 전기영동하였다.
5. E-Gel™ Power Snap 장비로 gel image를 촬영하고, 각 sample에서 예상 크기의 band가 나타나는지 확인하였다.

#### Output
![KakaoTalk_20260901_154415454_06.jpg](KakaoTalk_20260901_154415454_06.jpg)

#### Results & Discussions
- E-Gel™ 분석 결과, Block1-1, Block1-2, Block1-3, Block1-4 recovery PCR product 모두 400-500 bp 범위에서 band가 확인되었다.
- 각 산물의 예상 크기는 Block1-1 473 bp, Block1-2 470 bp, Block1-3 483 bp, Block1-4 458 bp이며, 관찰된 band가 해당 예상 크기 범위와 일치하였다.
- 따라서 네 개 subblock 모두 원하는 크기의 full-length PCR product가 증폭된 것으로 판단하였으며, 정제 후 농도 측정 결과와 함께 확인하여 2nd PCA assembly용 fragment로 사용하였다.

---

### [UHW010 Liquid Handling] 2nd PCA Gibson assembly 혼합조성

#### Meta
- Experimenter: 문지민
- Start_date: ''
- End_date: ''

#### Input
- Purified outer-primer amplified 1st PCA product 1/2/3/4

#### Reagent
- Reagent-1788851665659;KOD- KOD One PCR Master Mix (Toyobo_KMM-101)
- Reagent-1789026237667;UltraPure™ DNase/RNase-Free Distilled Water
- RSM3_Block1_Gib-F and RSM3_Block1_Gib-R;10 µM working stock

#### Labware and Consumables
- Labware-1789020678475;White Tip_0.1-10 µL;Eppendorf_0030073371
- Labware-1789020548121;Yellow Tip_2-200 μL
- PCR tube

#### Equipment
- Equip-1789020711244;Pipett_10p;Eppendorf
- Equip-1789020568019;Pipett_200p

#### Method
1. 2nd PCA Gibson assembly 반응을 50.0 µL로 준비하였다.
| Component                 | Working conc | Volume    | Final conc       |
| ------------------------- | ------------ | --------- | ---------------- |
| KOD One PCR Master Mix    | 2X           | 25.0 µL   | 1X               |
| RSM3_Block1_Gib-F         | 10 µM        | 1.5 µL    | 0.30 µM          |
| RSM3_Block1_Gib-R         | 10 µM        | 1.5 µL    | 0.30 µM          |
| Purified fragment 1/2/3/4 | -            | x µL      | 50 ng or 100 ng  |
| Nuclease-free water       | -            | 23 - x µL | -                |
| Total                     | -            | 50.0 µL   | -                |

- Block별 purified fragment 투입량과 Nuclease-free water 보충량은 다음과 같이 계산하였다.
- 50 ng condition

| Block    | Fragment conc (ng/µL) | Purified fragment | Nuclease-free water |
| -------- | --------------------- | ----------------- | ------------------- |
| Block1-1 | 66.6                  | 0.75 µL           | 22.25 µL            |
| Block1-2 | 60.2                  | 0.83 µL           | 22.17 µL            |
| Block1-3 | 88.7                  | 0.56 µL           | 22.44 µL            |
| Block1-4 | 93.4                  | 0.54 µL           | 22.46 µL            |

- 100 ng condition

| Block    | Fragment conc (ng/µL) | Purified fragment | Nuclease-free water |
| -------- | --------------------- | ----------------- | ------------------- |
| Block1-1 | 66.6                  | 1.50 µL           | 21.50 µL            |
| Block1-2 | 60.2                  | 1.66 µL           | 21.34 µL            |
| Block1-3 | 88.7                  | 1.13 µL           | 21.87 µL            |
| Block1-4 | 93.4                  | 1.07 µL           | 21.93 µL            |

#### Output
- 2nd PCA Gibson assembly reaction mixture 1/2/3/4 (50 ng condition)
- 2nd PCA Gibson assembly reaction mixture 1/2/3/4 (100 ng condition)

#### Results & Discussions
- Outer-primer recovery PCR로 확보한 fragment를 Gibson primer pair와 함께 2nd PCA assembly 반응에 투입하였다.
- 각 fragment는 50 ng과 100 ng 두 조건으로 투입하고, fragment 농도에 따라 부피를 조정하여 각 조건 내에서 4개 subblock 간 DNA 질량 차이를 최소화하였다.
- 100 ng 조건에서는 50 ng 조건보다 fragment 투입량을 두 배로 조정하고, 반응 총량 50 µL를 유지하도록 Nuclease-free water의 양을 줄였다.
- Gibson primer pair는 assembly 과정에서 fragment의 말단과 결합하여 후속 증폭 및 연결이 일어나도록 하며, primer의 최종 농도는 각각 0.30 µM으로 동일하게 설정하였다.

---

### [UHW100 Thermocycling] 2nd PCA Gibson assembly

#### Meta
- Experimenter: 문지민
- Start_date: ''
- End_date: ''

#### Input
- 2nd PCA Gibson assembly reaction mixture 1/2/3/4 (50 ng condition)
- 2nd PCA Gibson assembly reaction mixture 1/2/3/4 (100 ng condition)

#### Reagent
- (None)

#### Labware and Consumables
- PCR tube

#### Equipment
- Equip-1789020746727;AllInOneCycler™ PCR system

#### Method
| Phase                 | Temperature | Time  | Cycles |
| --------------------- | ----------- | ----- | ------ |
| Pre-denaturation      | 98°C        | 2 min | 1      |
| Denaturation          | 98°C        | 10 s  | 25     |
| Annealing (Tm = 56°C) | 53°C        | 15 s  | 25     |
| Extension             | 68°C        | 20 s  | 25     |
| Final extension       | 68°C        | 2 min | 1      |
| Hold                  | 4°C         | hold  | -      |

#### Output
- 2nd PCA assembled RSM3 Block1 product 1/2/3/4 (50 ng condition)
- 2nd PCA assembled RSM3 Block1 product 1/2/3/4 (100 ng condition)

#### Results & Discussions
- 2nd PCA assembly를 통해 각 purified fragment를 연결하고 약 1,870 bp의 assembled product를 생성하였다.
- 50 ng과 100 ng의 두 input 조건에서 동일한 thermocycling program을 적용하여 input DNA 양에 따른 assembly product 형성 결과를 비교하였다.
- 2nd PCA product의 예상 크기는 프로토콜 기준 약 1,870 bp이며, fragment 간 연결이 정상적으로 이루어졌는지는 이 크기의 full-length band로 확인한다.
- 25 cycle 동안 denaturation, annealing, extension을 반복하여 fragment 간 결합과 assembled product의 증폭을 유도하였다. 
- 53°C annealing 조건은 Gibson primer의 Tm(56°C)을 고려해 설정한 조건이다.
- 최종 product의 정확한 형성 여부는 후속 purification 후 agarose gel에서 약 1,870 bp의 full-length band가 확인되는지와 농도 측정 결과를 함께 비교하여 판단한다.

---

### [UHW250 Nucleic Acid Purification] 2nd PCA product purification

#### Meta
- Experimenter: 문지민
- Start_date: ''
- End_date: ''

#### Input
- 2nd PCA assembled RSM3 Block1 product 1/2/3/4 (50 ng condition)
- 2nd PCA assembled RSM3 Block1 product 1/2/3/4 (100 ng condition)

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
	1. 2nd PCA 산물에 동일 부피(1:1)의 Membrane Binding Solution을 첨가하고 충분히 혼합하였다.
	2. 혼합액을 SV Minicolumn에 옮기고 실온에서 1분간 incubation하였다.
	3. 16,000 × g에서 1분간 원심분리한 후 flow-through를 제거하였다.
	4. 700 µL Membrane Wash Solution을 첨가하고 16,000 × g에서 1분간 원심분리하였다.
	5. Flow-through를 제거한 후 500 µL Membrane Wash Solution을 추가하고 16,000 × g에서 5분간 원심분리하였다.
	6. Column을 추가로 1분간 원심분리하여 membrane을 건조하였다.
	7. Column을 새로운 1.5 mL tube로 옮기고 30-50 µL Nuclease-free Water를 membrane 중앙에 첨가하였다.
	8. 실온에서 1분간 incubation한 후 16,000 × g에서 1분간 원심분리하여 DNA를 elution하였다.
	9. Eluted DNA의 농도를 Nanodrop으로 측정하고, 이후 실험 전까지 나머지 시료는 -20°C에 보관하였다.

#### Output
- Purified 2nd PCA assembled RSM3 Block1 product 1/2/3/4 (50 ng conditions)
- Purified 2nd PCA assembled RSM3 Block1 product 1/2/3/4 (100 ng conditions)

#### Results & Discussions
- 정제된 2nd PCA product의 농도를 Nanodrop으로 측정하여, 50 ng 및 100 ng input 조건에서 생성된 산물의 회수량을 비교하였다.
- 'Purified 2nd PCA assembled RSM3 Block1 product 1/2/3/4'의 농도는 다음과 같다.
| Sample       | conc (ng/µL) |
| ------------ | ------------ |
| Block1-50ng  | 194.6        |
| Block1-100ng | 85.2         |

- Block1-50ng 조건에서는 194.6 ng/µL, Block1-100ng 조건에서는 85.2 ng/µL가 측정되었다. 두 조건 모두 정제 후 DNA가 회수되었으며, 50 ng input 조건에서 100 ng input 조건보다 약 2.3배 높은 농도가 확인되었다.
- 두 조건 모두 후속 cloning 또는 Gibson assembly에 사용할 수 있는 충분한 양의 2nd PCA product를 확보한 것으로 판단하였다.
- 최종 사용 시에는 input DNA 양만으로 산물량을 판단하지 않고, 농도 측정 결과와 약 1,870 bp full-length band 확인 결과를 함께 고려하여 적절한 조건의 product를 선택하였다.

---

### [UHW230 Nucleic Acid Fragment Analysis] 2nd PCA product QC

#### Meta
- Experimenter: 문지민
- Start_date: ''
- End_date: ''

#### Input
- Purified 2nd PCA assembled RSM3 Block1 product 1/2/3/4 (50 ng conditions)
- Purified 2nd PCA assembled RSM3 Block1 product 1/2/3/4 (100 ng conditions)

#### Reagent
- Agarose gel, DNA ladder, DNA stain, gel running buffer
- Reagent-1789026237667;UltraPure™ DNase/RNase-Free Distilled Water

#### Labware and Consumables
- PCR tube or gel loading tips

#### Equipment
- Gel electrophoresis system

#### Method
1. 각 2nd PCA product를 다음과 같이 혼합하여 총 20 µL의 sample을 준비하였다.
| Component           | Volume (µL) |
| ------------------- | ----------- |
| PCR product         | 5           |
| 10× Loading dye     | 2           |
| Nuclease-free water | 13          |
| Total               | 20          |
2. DNA marker는 다음과 같이 혼합하여 준비하였다.
| Component           | Volume (µL) |
| ------------------- | ----------- |
| DNA Marker          | 3           |
| Nuclease-free water | 17          |
| Total               | 20          |
3. Sample과 marker를 agarose gel에 100V 30min loading하였다.
4. Gel을 사진찍었다.

#### Output
![RSM3_Block1.png](RSM3_Block1.png)

#### Results & Discussions
- Gel image의 lane은 왼쪽부터 다음과 같이 구성하였다.
  1. 정제 전 50 ng input으로 수행한 2nd PCA product
  2. 정제 후 50 ng input으로 수행한 2nd PCA product
  3. 정제 전 100 ng input으로 수행한 2nd PCA product
  4. 정제 후 100 ng input으로 수행한 2nd PCA product
- 정제 전후 sample을 각각 비교하고 50 ng과 100 ng input 조건을 나누어 분석해, input DNA 양과 purification이 2nd PCA product의 band pattern에 미치는 영향을 확인하였다.
- 각 lane에서 약 1.8 kb 위치에 band가 확인되어 2nd PCA assembly product가 형성된 것으로 판단하였으며, 정제 후 sample에서도 목표 크기의 band가 유지되었다.
- 50 ng과 100 ng input 조건의 band intensity를 비교한 결과 뚜렷한 차이는 관찰되지 않았으며, input DNA 양을 두 배로 증가시켜도 산물의 band intensity에는 큰 변화가 없는 것으로 확인하였다.

## Conclusions and Discussion

- T7E1-treated 1st PCA product에 outer primer를 적용하여 각 subblock의 말단 서열을 포함하는 recovery PCR fragment를 확보하였다. 
- Recovery PCR product는 예상 크기인 약 458-483 bp 범위의 band가 확인되어 2nd PCA assembly에 사용할 수 있는 품질로 판단하였다.
- 확보한 네 개의 fragment를 Gibson primer pair와 함께 2nd PCA assembly에 투입하여, 약 1,870 bp의 RSM3 Block1 assembled product를 제작하였다. 
- Gel 분석에서 50 ng과 100 ng input 조건 모두 약 1.8 kb 위치의 band가 확인되었으며, 두 조건 간 band intensity의 뚜렷한 차이는 관찰되지 않았다.
- 2nd PCA product를 정제한 후 50 ng input 조건에서는 194.6 ng/µL, 100 ng input 조건에서는 85.2 ng/µL의 DNA 농도가 측정되었다. 두 조건 모두 후속 cloning 또는 Gibson assembly에 사용할 수 있는 충분한 양의 DNA가 확보되었으며, 이후 단계에서는 목표 크기 band와 농도 결과를 함께 고려하여 사용할 산물을 선정한다.
- 다만 100 ng input 조건이 50 ng 조건보다 더 높은 최종 농도로 이어지지는 않았으며, 이러한 차이는 input DNA 양뿐 아니라 PCR 효율, purification 회수율 및 Nanodrop 측정 오차의 영향을 받을 수 있다. 따라서 본 결과만으로 input DNA 양과 최종 산물량의 직접적인 상관관계를 판단하기는 어렵다.
- 또한 약 1.8 kb band의 확인은 assembled product의 크기를 확인하는 데 유용하지만, gel 결과만으로는 fragment의 정확한 연결 순서와 염기서열의 오류 여부를 확정할 수 없다. 
- 최종 RSM3 Block1 construct의 정확성을 확인하기 위해서는 후속 sequencing 검증이 필요하다.

