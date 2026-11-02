---
title: WB010 DNA Oligomer Assembly - RSM3 Block1 PCA assembly
experimenter: 문지민
created_date: 2026-09-08
last_updated_date: 2026-09-10
end_date: ''
---

## [WB010 DNA Oligomer Assembly] RSM3 Block1 PCA assembly

> This workflow focuses on assembling DNA oligomers into sequences that are several kilobases in length. The procedure typically begins with an oligomer pool and involves precise techniques to ensure accurate assembly of the desired DNA sequence.

## Related Unit Operations

- [UHW010 Liquid Handling | Oligo, Primer Resuspension](#uhw010-liquid-handling-oligo-primer-resuspension)
- [UHW010 Liquid Handling | 1st PCA Oligo pool & KOD assembly](#uhw010-liquid-handling-1st-pca-oligo-pool-kod-assembly)
- [UHW255 Centrifuge | 1st PCA Oligo pool & KOD Spindown](#uhw255-centrifuge-1st-pca-oligo-pool-kod-spindown)
- [UHW100 Thermocycling | 1st PCA Thermocycling](#uhw100-thermocycling-1st-pca-thermocycling)
- [UHW230 Nucleic Acid Fragment Analysis | 1st PCA product QC](#uhw230-nucleic-acid-fragment-analysis-1st-pca-product-qc)
- [UHW250 Nucleic Acid Purification | 1st PCA product purification](#uhw250-nucleic-acid-purification-1st-pca-product-purification)

---

### [UHW010 Liquid Handling] Oligo, Primer Resuspension

> This unit operation involves basic and fundamental liquid sample operations in laboratory processes, such as reagent preparation, sample distribution, dilution, mixing, and washing. It ensures precision and efficiency in handling liquid samples across various experimental setups.

#### Meta
- Experimenter: '문지민'
- Start_date: '2026-08-31 09:00'
- End_date: '2026-08-31 10:30'

#### Input
[260820_RSM3_PCABlock1_Macrogen_tube.xls](260820_RSM3_PCABlock1_Macrogen_tube.xls)- (samples from the previous step)
- 배송 받은 oligo pool vial tube (RSM3 Block1 oligo & Primers)

#### Reagent
- @reagent;Reagent-1789026237667;UltraPure™ DNase/RNase-Free Distilled Water;Invitrogen™_10977015

#### Labware and Consumables
- @labware;Labware-1789020548121;Yellow Tip_2-200 μL;Eppendorf_0030073436

#### Equipment
- @equip;Equip-1789020568019;Pipett_200p;Eppendorf- Pipett_200p (Eppendorf)
- 
- @equip;Equip-1789024045341;Vortex-Genie 2 mixer;Scientific Industries

#### Method
1. Oligo pool 42개와 Outer primer 8개, Gibson primer 4개에 Nuclease-free water를 첨가하여 100 pmol/μL (100 μM) 농도로 resuspension하였다.
2. Oligo가 충분히 용해되도록 5 min 동안 vortexing하였다.
3. Resuspension된 100 μM oligo를 1:10으로 희석하여 10 μM working solution을 제조하였다.
4. Resuspension된 oligo는 −20°C에서 보관하였다.

#### Output
100 μM Oligo 42개, 10 μM Oligo 42개, 100 μM Outer primer 8개, 10 μM Outer primer 8개, 100 μM Gibson primer 4개, 10 μM Gibson primer 4개

#### Results & Discussions
- 본 실험에서는 마크로젠으로부터 vial 형태로 제공된 oligo pool을 manual로 resuspension한 후 실험에 사용하였다. 그러나 vial 단위의 개별 분주 및 희석 과정이 필요하여 처리 시간이 길고, 반복적인 수작업으로 인해 분주 오차 및 sample handling error가 발생할 가능성이 있다. 향후에는 oligo를 96-well plate 형태로 공급받아 liquid handler를 이용해 resuspension 및 working solution 제조 과정을 자동화함으로써 작업 시간을 단축하고, 분주 정확도와 실험 재현성을 향상시킬 수 있을 것으로 판단된다.

---

### [UHW010 Liquid Handling] 1st PCA Oligo pool & KOD assembly

> This unit operation involves basic and fundamental liquid sample operations in laboratory processes, such as reagent preparation, sample distribution, dilution, mixing, and washing. It ensures precision and efficiency in handling liquid samples across various experimental setups.

#### Meta
- Experimenter: '문지민'
- Start_date: '2026-08-31 10:30'
- End_date: '2026-08-31 11:30'

#### Input
- 10 μM Oligo 42개

#### Reagent
- Reagent-1788851665659;KOD- KOD One PCR Master Mix (Toyobo_KMM-101)
- Reagent-1789026237667;UltraPure™ DNase/RNase-Free Distilled Water

#### Labware and Consumables
- Labware-1789020678475;White Tip_0.1-10 μL;Eppendorf_0030073371
- Labware-1789020548121;Yellow Tip_2-200 μL
- PCR 8 strip (??)

#### Equipment
- Equip-1789020711244;Pipett_10p;Eppendorf
- Equip-1789020568019;Pipett_200p

#### Method
1. 각 assembly oligo의 pool 내 최종 농도는 0.15 µM(150 nM)가 되도록 정규화하였다.
  - Pool 1/2/4는 각각 10개의 10 µM oligo working solution을 1.5 µL씩 혼합하고 nuclease-free water 85 µL를 첨가하여 최종 부피가 100 µL가 되도록 제조하였다.
  - Pool 3은 12개의 10 µM oligo working solution을 1.5 µL씩 혼합하고 nuclease-free water 82 µL를 첨가하여 최종 부피가 100 µL가 되도록 제조하였다.
2. 1차 PCA assembly 반응 혼합물 구성은 아래와 같다.
| Component              | Working conc. | Volume  | Final conc. |
| ---------------------- | ------------- | ------- | ----------- |
| KOD One PCR Master Mix | 2X            | 20.0 µL | 1X          |
| PCA oligo pool         | 0.15 µM each  | 8.0 µL  | 30nM each   |
| Nuclease-free water    | -             | 12.0 µL | -           |
| Total                  | -             | 40.0 µL |             |

| Component              | Working conc. | Volume  | Final conc. |
| ---------------------- | ------------- | ------- | ----------- |
| KOD One PCR Master Mix | 2X            | 20.0 µL | 1X          |
| PCA oligo pool         | 0.15 µM each  | 16.0 µL | 60nM each   |
| Nuclease-free water    | -             | 4.0 µL  | -           |
| Total                  | -             | 40.0 µL |             |

#### Output
- RSM3_Block1 Oligo pool 1/2/3/4 30nM
- RSM3_Block1 Oligo pool 1/2/3/4 60nM

#### Results & Discussions
- Assembly oligo pool은 모든 oligo가 150 nM의 동일한 농도가 되도록 제조하여 oligo 수에 따른 농도 편차를 최소화하였다. 
- 제조된 pool 8.0 µL를 40.0 µL PCA 반응에 첨가함으로써 각 oligo의 최종 농도는 각각 30 nM과 60 nM이 되었다.

---

### [UHW255 Centrifuge] 1st PCA Oligo pool & KOD Spindown

> Separating components of different densities within a liquid sample by applying centrifugal force. Used for pelleting cells, clarifying solutions, separating precipitates, and sample preparation steps in various workflows.

#### Meta
- Experimenter: '문지민'
- Start_date: '2026-08-31 11:30'
- End_date: '2026-08-31 11:31'

#### Input
- RSM3_Block1 Oligo pool 1/2/3/4 30nM
- RSM3_Block1 Oligo pool 1/2/3/4 60nM

#### Reagent
- (None)

#### Labware and Consumables
- (None)

#### Equipment
- @equip;Equip-1789024617432;Centrifuge 5425;Eppendorf_5405000310

#### Method
1. PCR tube를 balane 맞추어 장착한다.
2. 뚜껑을 닫고 5-10s 동안 반응액이 tube 바닥으로 모이도록 spin down한다.
3. 원심분리가 완료되면 뚜껑을 열고 tube를 꺼낸다.

#### Output
- Centrifuged RSM3_Block1 Oligo pool 1/2/3/4 30nM
- Centrifuged RSM3_Block1 Oligo pool 1/2/3/4 60nM

#### Results & Discussions
- 1st PCA assembly를 위한 Oligo pool을 spin down하였다.

---

### [UHW100 Thermocycling] 1st PCA Thermocycling

> The process of repeatedly heating and cooling through defined temperature cycles to facilitate reactions. It is used in workflows such as DNA assembly and DNA/RNA amplification, including PCR.

#### Meta
- Experimenter: '문지민'
- Start_date: '2026-08-31 11:31'
- End_date: '2026-08-31 12:20'

#### Input
- Centrifuged RSM3_Block1 Oligo pool 1/2/3/4 30nM
- Centrifuged RSM3_Block1 Oligo pool 1/2/3/4 60nM

#### Reagent
- (None)

#### Labware and Consumables
- (None)

#### Equipment
- Equip-1789020746727;AllInOneCycler™ PCR system;BIONEER, A-2041

#### Method
- 1st PCA assembly를 위해 Centrifuged RSM3_Block1 Oligo pool 1/2/3/4를 합성하는 단계이다.
1. 아래와 같이 Thermocycling을 진행한다.
| Phase             | Temperature | Time  | Cycles |
| ----------------- | ----------- | ----- | ------ |
| Pre-denaturation  | 98°C        | 2 min | 1      |
| Denaturation      | 98°C        | 10 s  | 25     |
| Overlap annealing | 56°C        | 15 s  |        |
| Extension         | 68°C        | 30 s  |        |
| Final extension   | 68°C        | 2 min | 1      |
| Hold              | 4°C         | hold  | —      |

2. 반응이 완료된 tube는 Purification 단계를 진행한다.
  - 즉시 진행하지 않을 경우 -20°C에 보관한다.

#### Output
- 1st PCA assembled Oligo pool 1/2/3/4 30nM
- 1st PCA assembled Oligo pool 1/2/3/4 60nM

#### Results & Discussions
- 1차 PCA assembly에서는 KOD를 이용한 PCR을 통해 서로 상보적인 oligo가 결합하고 연장되어 RSM3_Block1의 4개 소블럭이 조립되도록 하였다. 
- Overlap annealing 시간은 oligo 간 결합과 후속 연장이 충분히 이루어질 수 있도록 15 s로 설정하였다. 다만 최적의 annealing 조건은 oligo의 수와 길이, overlap 영역의 Tm 및 GC 함량 등에 따라 달라질 수 있으므로, assembly 효율이 낮은 경우 annealing temperature와 시간을 추가로 최적화할 필요가 있다.
- 즉시 정제하지 않는 경우에는 산물의 안정성을 유지하기 위해 반응물을 −20°C에 보관하였다.

---

### [UHW230 Nucleic Acid Fragment Analysis] 1st PCA product QC

> To separate, identify, and characterize fragments of nucleic acids based on their size. This unit operation is crucial for genetic analysis and quality control.

#### Meta
- Experimenter: '문지민'
- Start_date: '2026-08-31 13:00'
- End_date: '2026-08-31 13:20'

#### Input
- 1st PCA assembled Oligo pool 1/2/3/4 30nM
- 1st PCA assembled Oligo pool 1/2/3/4 60nM

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
2. Sample을 다음과 같이 혼합한다.
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
4. 충분히 혼합한 후 13min동안 loading을 진행한다.
5. 장치를 이용해 Gel 사진을 찍는다.

#### Output
![KakaoTalk_20260901_154415454_01.jpg](KakaoTalk_20260901_154415454_01.jpg)
- 우측 4개는 30nM Oligo pool 합성 결과이며, 좌측 4개는 60nM Oligo pool 합성 결과이다.

#### Results & Discussions
- 1차 PCA 결과, 예상 크기인 약 500 bp보다 높은 위치에서 band가 관찰되었으며, 전반적으로 smear한 양상을 보였다.
- 반면, purification 후 E-Gel 분석에서는 약 400–500 bp 위치에서 band가 확인되었다. 이를 고려할 때 초기 gel에서 관찰된 smear 및 예상보다 높은 위치의 band는 PCR 반응액 내 부산물의 영향 또는 전기영동 과정에서 gel의 휘어짐 등에 의해 나타난 현상일 가능성이 있다.
- Oligo pool 농도에 따른 결과를 비교한 결과, 60 nM 조건에서 30 nM 조건보다 전반적으로 더 진한 band intensity가 관찰되었다. 따라서 본 실험 조건에서는 60 nM oligo pool을 사용했을 때 상대적으로 더 많은 PCA 산물이 생성된 것으로 판단된다.

---

### [UHW250 Nucleic Acid Purification] 1st PCA product purification

> The process of purifying DNA or RNA from biological samples using an automated device. It ensures high purity and yield for downstream applications.

#### Meta
- Experimenter: '문지민'
- Start_date: '2026-08-31 13:20'
- End_date: '2026-08-31 14:00'

#### Input
- 1st PCA assembled Oligo pool 1/2/3/4 30nM
- 1st PCA assembled Oligo pool 1/2/3/4 60nM

#### Reagent
- Reagent-1789020476790;Wizard® SV Gel and PCR Clean-Up System;Promega A9282
- Reagent-1789026237667;UltraPure™ DNase/RNase-Free Distilled Water

#### Labware and Consumables
- Labware-1789020945985;Blue Tip_50-1000 μL;Eppendorf_0030073479
- Labware-1789020548121;Yellow Tip_2-200 μL

#### Equipment
- Equip-1789024617432;Centrifuge 5425

#### Method
PCR 산물은 **Wizard® SV Gel and PCR Clean-Up System (Promega, A9282)을 이용하여 정제하였다.
  1. PCR 반응액에 40 µL(1:1)의 Membrane Binding Solution을 첨가
  2. 혼합액을 SV Minicolumn에 옮기고 실온에서 1분 incubation
  3. 16,000 × g에서 1분간 원심분리 후 flow-through를 제거
  4. 700 µL Membrane Wash Solution을 첨가하고 16,000 × g에서 1분간 원심분리
  5. Flow-through를 제거한 후 500 µL Membrane Wash Solution을 추가하고 16,000 × g에서 5분간 원심분리
  6. column을 추가로 1분간 원심분리
  7. Column을 새로운 1.5 mL tube로 옮기고 40 µL Nuclease-Free Water를 membrane에 첨가
  8. 실온에서 1분간 incubation한 후 16,000 × g에서 1분간 원심분리하여 DNA를 elution
  9. DNA Nanodrop 측정 후 이후 실험 진행, 나머지는 -20°C 보관

#### Output
- Purified 1st PCA assembled Oligo pool 1/2/3/4 30nM
- Purified 1st PCA assembled Oligo pool 1/2/3/4 60nM

#### Results & Discussions
- 1차 PCA를 통해 조립된 Block1-1~1-4 산물을 정제한 후 농도를 측정한 결과는 다음과 같다.
|      | Sample   | conc (ng/µL) |
| ---- | -------- | ------------ |
| 30nM | Block1-1 | 32.3         |
|      | Block1-2 | 43.1         |
|      | Block1-3 | 76.8         |
|      | Block1-4 | 80.2         |
| 60nM | Block1-1 | 31.5         |
|      | Block1-2 | 37.1         |
|      | Block1-3 | 76.6         |
|      | Block1-4 | 60.4         |
- 30 nM과 60 nM 조건의 정제 후 DNA 농도를 비교한 결과, 60 nM 조건에서 농도가 일관되게 증가하는 경향은 나타나지 않았으며, 일부 sample에서는 오히려 30 nM 조건에서 더 높은 농도가 측정되었다.
- 그러나 앞선 gel 분석에서는 60 nM 조건에서 30 nM 조건보다 전반적으로 더 진한 band intensity가 관찰되었으므로, Nanodrop 측정값과 gel 결과가 완전히 일치하지 않았다.
- Nanodrop은 목표 크기의 PCA 산물뿐만 아니라 잔존 oligo 및 비특이적 DNA 등도 함께 측정될 수 있기 때문에, 측정 농도만으로 실제 PCA 조립 효율이나 목표 산물의 양을 판단하기에는 한계가 있다.

## Conclusions and Discussion

