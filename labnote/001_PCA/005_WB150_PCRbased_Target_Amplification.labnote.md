---
title: WB150 PCR-based Target Amplification - Gibson assembly
experimenter: 문지민
created_date: 2026-09-08
last_updated_date: 2026-09-14
end_date: ''
---

## [WB150 PCR-based Target Amplification] Gibson assembly

> This workflow utilizes designed primers and Polymerase Chain Reaction (PCR) to specifically amplify a target gene sequence from complex templates such as genomic DNA or metagenomic samples, enabling gene screening and retrieval.

## Related Unit Operations

- [UHW010 Liquid Handling | DVA vector PCR 혼합조성](#uhw010-liquid-handling-dva-vector-pcr)
- [UHW100 Thermocycling | DVA vector PCR](#uhw100-thermocycling-dva-vector-pcr)
- [UHW010 Liquid Handling | DpnI 처리](#uhw010-liquid-handling-dpni)
- [UHW250 Nucleic Acid Purification | DVA vector PCR product purification](#uhw250-nucleic-acid-purification-dva-vector-pcr-product-purification)
- [UHW230 Nucleic Acid Fragment Analysis | DVA vector PCR QC](#uhw230-nucleic-acid-fragment-analysis-dva-vector-pcr-qc)
- [UHW010 Liquid Handling | Gibson assembly 혼합조성](#uhw010-liquid-handling-gibson-assembly)
- [UHW100 Thermocycling | Gibson assembly](#uhw100-thermocycling-gibson-assembly)
- [UHW310 Transformation | Gibson assembly product transformation](#uhw310-transformation-gibson-assembly-product-transformation)
- [UHW010 Liquid Handling | DVA-RSM3 Block1 colony inoculation](#uhw010-liquid-handling-dva-rsm3-block1-colony-inoculation)

---

### [UHW010 Liquid Handling] DVA vector PCR 혼합조성

#### Meta
- Experimenter: 문지민
- Start_date: ''
- End_date: ''

#### Input
- DVA_AE_MoClo plasmid template
- RSM3_Block1_DVA-F and RSM3_Block1_DVA-R

#### Reagent
- Reagent-1788851665659;KOD- KOD One PCR Master Mix (Toyobo_KMM-101)
- Reagent-1789026237667;UltraPure™ DNase/RNase-Free Distilled Water
- RSM3_Block1_DVA-F;10 µM working stock
- RSM3_Block1_DVA-R;10 µM working stock

#### Labware and Consumables
- Labware-1789020678475;White Tip_0.1-10 µL;Eppendorf_0030073371
- Labware-1789020548121;Yellow Tip_2-200 µL
- PCR tube

#### Equipment
- Equip-1789020711244;Pipett_10p;Eppendorf
- Equip-1789020568019;Pipett_200p

#### Method
1. DVA vector를 증폭하기 위한 50.0 µL PCR 반응을 다음과 같이 준비하였다.
| Component              | Working concentration | Volume  | Final concentration |
| ---------------------- | --------------------- | ------- | ------------------- |
| KOD One PCR Master Mix | 2X                    | 25.0 µL | 1X                  |
| RSM3_Block1_DVA-F      | 10 µM                 | 1.5 µL  | 0.30 µM             |
| RSM3_Block1_DVA-R      | 10 µM                 | 1.5 µL  | 0.30 µM             |
| DVA plasmid template   | -                     | 1 µL    |                     |
| Nuclease-free water    | -                     | 21 µL   | -                   |
| Total                  | -                     | 50.0 µL | -                   |

#### Output
- DVA vector PCR reaction mixture

#### Results & Discussions
- Gibson assembly에 사용할 linear DVA vector를 확보하기 위해 DVA plasmid를 template로 사용하였다.
- Vector primer는 DVA vector의 양 말단에 assembly overlap을 포함하도록 설계되었으며, PCR product가 PCA fragment와 Gibson assembly될 수 있도록 하였다.
- 또한 vector primer에는 이후 Golden Gate Assembly에 사용할 BsaI recognition site와 1-bp spacer 및 assembly overhang 서열을 함께 포함하였다. 따라서 DVA vector PCR product는 현재 단계에서 RSM3 Block1 PCA fragment와 Gibson assembly하는 데 사용될 뿐 아니라, 이후 BsaI digestion을 통해 정의된 overhang을 생성하여 최종 block assembly에도 활용할 수 있도록 설계되었다.
- 이와 같은 primer 설계를 통해 Gibson cloning과 후속 Golden Gate Assembly를 위해 별도의 서열 변형이나 추가적인 primer 재설계 없이 동일한 construct를 연속적으로 사용할 수 있다.

---

### [UHW100 Thermocycling] DVA vector PCR

#### Meta
- Experimenter: 문지민
- Start_date: ''
- End_date: ''

#### Input
- DVA vector PCR reaction mixture

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
| Denaturation          | 98°C        | 10 s  | 30     |
| Annealing (Tm = 67°C) | 62°C        | 5 s   | 30     |
| Extension             | 68°C        | 15 s  | 30     |
| Final extension       | 68°C        | 30 s  | 1      |
| Hold                  | 4°C         | hold  | -      |

#### Output
- PCR-amplified DVA vector product

#### Results & Discussions
- 30 cycles의 PCR을 통해 Gibson assembly에 필요한 linear DVA vector를 증폭하였다.
- DVA vector의 예상 PCR product 크기는 약 2,004 bp이며, 이후 gel QC에서 full-length band 형성 여부를 확인하였다.

---

### [UHW010 Liquid Handling] DpnI 처리

#### Meta
- Experimenter: 문지민
- Start_date: ''
- End_date: ''

#### Input
- PCR-amplified DVA vector product

#### Reagent
- Reagent-1789112329669;DpnI;NEB_R0176L

#### Labware and Consumables
- PCR tube
- Labware-1789020678475;White Tip_0.1-10 µL;Eppendorf_0030073371

#### Equipment
- Equip-1789020711244;Pipett_10p;Eppendorf

#### Method
1. PCR product에 DpnI 1.0 µL(20 U)를 첨가하였다.
2. 37°C에서 30분간 반응시켜 methylated parental DVA plasmid template를 제거하였다.
3. DpnI 처리 후 PCR product cleanup 및 QC를 진행하였다.

#### Output
- DpnI-treated linear DVA vector product

#### Results & Discussions
- DpnI 처리를 통해 PCR template로 사용된 원형 parental plasmid의 잔존 가능성을 줄이고, PCR로 증폭된 linear DVA vector를 후속 Gibson assembly에 사용하도록 준비하였다.

---

### [UHW250 Nucleic Acid Purification] DVA vector PCR product purification

#### Meta
- Experimenter: 문지민
- Start_date: ''
- End_date: ''

#### Input
- DpnI-treated linear DVA vector product

#### Reagent
- Reagent-1789020476790;Wizard® SV Gel and PCR Clean-Up System;Promega A9282
- Reagent-1789026237667;UltraPure™ DNase/RNase-Free Distilled Water

#### Labware and Consumables
- Labware-1789020945985;Blue Tip_50-1000 μL;Eppendorf_0030073479
- Labware-1789020548121;Yellow Tip_2-200 μL
- 1.5 mL microcentrifuge tube

#### Equipment
- Equip-1789024617432;Centrifuge 5425

#### Method
PCR 산물은 Wizard® SV Gel and PCR Clean-Up System (Promega, A9282)을 이용하여 정제하였다.
1. DpnI 처리된 PCR 산물에 동일 부피(1:1)인 50 µL Membrane Binding Solution을 첨가하고 충분히 혼합하였다.
2. 혼합액을 SV Minicolumn에 옮기고 실온에서 1분간 incubation하였다.
3. 16,000 × g에서 1분간 원심분리한 후 flow-through를 제거하였다.
4. 700 µL Membrane Wash Solution을 첨가하고 16,000 × g에서 1분간 원심분리하였다.
5. Flow-through를 제거한 후 500 µL Membrane Wash Solution을 추가하고 16,000 × g에서 5분간 원심분리하였다.
6. Column을 추가로 1분간 원심분리하여 membrane을 건조하였다.
7. Column을 새로운 1.5 mL tube로 옮기고 20 µL Nuclease-free Water를 membrane 중앙에 첨가하였다.
8. 실온에서 1분간 incubation한 후 16,000 × g에서 1분간 원심분리하여 DNA를 elution하였다.
9. Eluted DNA의 농도를 Nanodrop으로 측정하고, 이후 실험 전까지 시료는 -20°C에 보관하였다.

#### Output
- Purified DVA vector PCR product

#### Results & Discussions
-  Gibson assembly에 적합한 linear DVA vector로 정제하였으며 농도는 다음과 같다.
|       | Sample  | conc (ng/µL) |
| ----- | ------- | ------------ |
| Outer | DVA_PCR | 47.6         |
- 후속 gel QC에서 약 2,004 bp의 full-length band가 유지되는지 확인하였다.

---

### [UHW230 Nucleic Acid Fragment Analysis] DVA vector PCR QC

#### Meta
- Experimenter: 문지민
- Start_date: ''
- End_date: ''

#### Input
- Purified DVA vector PCR product

#### Reagent
- Agarose gel, DNA ladder, DNA stain, gel running buffer
- Reagent-1789026237667;UltraPure™ DNase/RNase-Free Distilled Water

#### Labware and Consumables
- PCR tube or gel loading tips

#### Equipment
- Gel electrophoresis system

#### Method
1. 정제된 DVA vector PCR product sample을 다음과 같이 혼합하여 총 20 µL로 준비하였다.
| Component                       | Volume (µL) |
| ------------------------------- | ----------- |
| Purified DVA vector PCR product | 5           |
| 10× Loading dye                 | 2           |
| Nuclease-free water             | 13          |
| Total                           | 20          |
2. DNA marker는 다음과 같이 혼합하여 총 20 µL로 준비하였다.
| Component           | Volume (µL) |
| ------------------- | ----------- |
| DNA Marker          | 3           |
| Nuclease-free water | 17          |
| Total               | 20          |
3. Sample과 marker를 agarose gel에 loading하여 약 2,004 bp의 full-length band를 확인하였다.
4. Gel image를 기록하고 Nanodrop으로 DNA 농도를 측정하였다.

#### Output
![DVA_PCR.jpg](DVA_PCR.jpg)

#### Results & Discussions
- Gel image의 lane은 왼쪽부터 1번 lane에 정제 전 DVA vector PCR product, 2번 lane에 정제 후 DVA vector PCR product를 loading하여 비교하였다.
- 1번 lane과 2번 lane 모두 약 2,004 bp 위치에서 예상 크기와 일치하는 full-length band가 확인되었다. 이를 통해 DpnI 처리 및 purification 이후에도 DVA vector PCR product의 목표 크기가 유지되었음을 확인하였다.
- 정제 전후 모두 목표 band가 확인되었으며, 정제 후 산물을 후속 Gibson assembly에 사용할 linear DVA vector로 선별하였다.

---

### [UHW010 Liquid Handling] Gibson assembly 혼합조성

#### Meta
- Experimenter: 문지민
- Start_date: ''
- End_date: ''

#### Input
- Purified 2nd PCA RSM3 Block1 product

#### Reagent
- Reagent-1789114476169;Gibson Assembly® Master Mix;NEB_E2611L
- Reagent-1789026237667;UltraPure™ DNase/RNase-Free Distilled Water

#### Labware and Consumables
- e-tube
- Labware-1789020678475;White Tip_0.1-10 µL;Eppendorf_0030073371

#### Equipment
- Equip-1789020711244;Pipett_10p;Eppendorf

#### Method
1. 총 20 µL Gibson assembly 반응을 ice 위에서 준비하였다.
| Component                    | Total amount       | Volume        |
| ---------------------------- | ------------------ | ------------- |
| Gibson Assembly Master Mix   | 2X                 | 10.0 µL       |
| Linear DVA vector (2,004 bp) | 0.05 pmol / 65 ng  | 1.37 µL       |
| PCA fragment (1,870 bp)      | 0.15 pmol / 182 ng | 2.09 µL       |
| Nuclease-free water          | -                  | 6.54 µL       |
| Total                        | -                  | 20.0 µL       |
2. Linear DVA vector와 PCA fragment의 농도를 기준으로 목표 질량에 해당하는 투입 부피를 계산하였다.
| Component                | Measured conc | Target amount | Calculated volume |
| ------------------------ | ------------- | ------------- | ----------------- |
| DVA-1 vector (2,004 bp)  | 47.6 ng/µL    | 65 ng         | 1.37 µL           |
| RSM3 Block1 PCA fragment | 87.1 ng/µL    | 182 ng        | 2.09 µL           |
| Nuclease-free water      | -             | -             | 6.54 µL           |
| Total                    | -             | -             | 10.00 µL          |

#### Output
- Gibson assembly reaction mixture: DVA vector + RSM3 Block1 PCA fragment
- Vector-only Gibson control

#### Results & Discussions
- 약 2,004 bp의 linear DVA vector와 약 1,870 bp의 RSM3 Block1 PCA fragment를 각각 0.05 pmol과 0.15 pmol로 투입하여, vector와 insert의 molar ratio를 1:3으로 설정하였다.
- 실제 반응에서는 DVA-1 vector 농도 47.6 ng/µL와 RSM3 Block1 PCA fragment 농도 87.1 ng/µL를 기준으로 각각 65 ng(1.37 µL)과 182 ng(2.09 µL)을 투입하여 목표 molar ratio를 맞추었다.
- Vector-only Gibson control도 함께 준비하여, insert가 없는 조건에서 발생하는 background와 assembly 반응에 의한 colony 형성을 비교할 수 있도록 하였다.

---

### [UHW100 Thermocycling] Gibson assembly

#### Meta
- Experimenter: 문지민
- Start_date: ''
- End_date: ''

#### Input
- Gibson assembly reaction mixture
- Vector-only Gibson control

#### Reagent
- (None)

#### Labware and Consumables
- e-tube

#### Equipment
- Heatblock

#### Method
1. Gibson assembly reaction mixture를 ice 위에서 준비한 후 50°C에서 60분간 반응시켰다.
2. NEB protocol에 따라 반응 시간을 15분으로 단축할 수 있으나, 본 protocol에서는 60분 조건을 적용하였다.
3. 반응 직후 transformation을 진행하거나, 필요 시 ice 위에 두고 단시간 보관하였다.

#### Output
- Gibson-assembled DVA-RSM3 Block1 construct
- Vector-only Gibson control product

#### Results & Discussions
- 60분 반응 조건은 vector와 insert의 overlap 형성 및 nick sealing이 충분히 진행되도록 적용한 조건이다. 
- 반응 후 생성된 assembly product는 단순한 linear DNA mixture가 아니라, DVA vector backbone과 RSM3 Block1 insert가 연결된 circular plasmid로 전환될 수 있는 형태로 준비하였다.
- 이후 competent cell transformation을 통해 assembly product를 세포 내에서 증폭하고, 형성된 colony를 colony PCR 및 plasmid sequencing으로 분석하여 RSM3 Block1 insert의 삽입 여부, 크기 및 염기서열 정확성을 검증한다.

---

### [UHW310 Transformation] Gibson assembly product transformation

#### Meta
- Experimenter: 문지민
- Start_date: ''
- End_date: ''

#### Input
- Gibson-assembled DVA-RSM3 Block1 construct
- Vector-only Gibson control product
- DH5α competent cells

#### Reagent
- LB broth without antibiotic
- LB agar plate with Ampicillin

#### Labware and Consumables
- 1.5 mL tube
- LB broth tube
- LB agar plate (+Amp)
- Spreader

#### Equipment
- 37°C shaking incubator

#### Method
1. Competent cell을 ice 위에서 5분간 해동하였다.
2. Gibson assembly product를 competent cell에 첨가하고 gently mixing하였다.
3. Ice에서 30분간 incubation하였다.
4. 42°C에서 45초간 heat shock한 후 ice에서 2분간 incubation하였다.
5. 1 mL LB broth를 첨가하고 37°C shaking incubator에서 1시간 recovery하였다.
6. Recovery culture 20 µL를 LB agar plate (+Amp)에 도말하였다.
7. 37°C incubator에서 overnight 배양하여 colony 형성을 확인하였다.

#### Output
- Transformed DVA-RSM3 Block1 colonies
- Vector-only control colonies

#### Results & Discussions
![Colony_1.jpg](Colony_1.jpg)![Colony_2.jpg](Colony_2.jpg)
- Gibson assembly product를 competent cell에 transformation하여 DVA vector 기반 RSM3 Block1 clone을 확보하도록 하였다.
- Colony_2은 1mL 배양액에 대해 50 µL spreading 하였고, Colony_1은 1 mL을 전체 spreading하였다. Colony_2 결과 Gibson assembly가 잘 진행된 것을 확인할 수 있다.
- 형성된 colony는 colony PCR 및 plasmid sequencing을 통해 RSM3 Block1 insert의 크기와 정확한 서열을 확인해야 한다.

---

### [UHW010 Liquid Handling] DVA-RSM3 Block1 colony inoculation

#### Meta
- Experimenter: 문지민
- Start_date: ''
- End_date: ''

#### Input
- Transformed DVA-RSM3 Block1 colonies

#### Reagent
- LB broth with Ampicillin

#### Labware and Consumables
- Sterile inoculation loop or pipette tip
- Sterile culture tube

#### Equipment
- 37°C shaking incubator

#### Method
1. Ampicillin selection plate에서 isolated colony를 선택하였다.
2. 선택한 colony를 Ampicillin이 포함된 LB broth 5 mL에 접종하였다.
3. Vector-only control plate에서 colony가 확인된 경우, control colony를 별도의 LB broth에 접종하였다.
4. 접종한 culture를 37°C shaking incubator에서 overnight 배양하였다.
5. 배양 후 culture를 plasmid preparation, colony PCR 또는 sequencing용 template 준비에 사용하였다.

#### Output
- Overnight DVA-RSM3 Block1 culture
- Overnight vector-only control culture

#### Results & Discussions
- Ampicillin 선택 배지에서 형성된 single colony를 액체 배양으로 확장하여 후속 plasmid 분석에 사용할 충분한 세포량을 확보하였다.
- Assembly sample과 vector-only control을 각각 분리 배양하여 insert를 포함한 clone과 vector background를 구분할 수 있도록 하였다.
- 배양된 clone은 plasmid preparation 후 colony PCR 또는 restriction analysis로 insert의 존재 여부와 예상 크기를 확인하고, 최종적으로 sequencing을 통해 RSM3 Block1 서열의 정확성을 검증한다.

## Conclusions and Discussion

- DVA plasmid를 PCR로 증폭하고 DpnI 처리하여 약 2,004 bp의 linear DVA vector를 준비하였다.
- 약 1,870 bp RSM3 Block1 PCA fragment와 linear DVA vector를 0.15 pmol:0.05 pmol 비율로 Gibson assembly하여 DVA-RSM3 Block1 construct 제작을 시도하였다.
- Assembly product는 competent cell transformation 후 colony 단위로 확보하고, colony PCR 및 sequencing을 통해 insert의 정확한 크기와 염기서열을 검증한다.

