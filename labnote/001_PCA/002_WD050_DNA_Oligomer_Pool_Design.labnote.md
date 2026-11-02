---
title: WD050 DNA Oligomer Pool Design
experimenter: 문지민
created_date: 2026-09-08
last_updated_date: 2026-09-10
end_date: ''
---

## [WD050 DNA Oligomer Pool Design]

> 본 workflow는 총 8,929 bp 길이의 RSM3 서열을 oligo 기반으로 합성하고 최종 조립하는 과정을 포함한다. 전체 RSM3 서열은 약 1.8 kb 크기의 5개 block으로 분할하였으며, block 간 최종 조립은 Golden Gate Assembly를 이용하도록 설계하였다. Block 분할 및 assembly junction 설계에는 GenomeAssembly Tool과 NEBridge SplitSet Tool을 활용하였다.
분할된 5개 block 중 Block 1은 PTDS method, Block 2는 MOSAIC method, Block 5는 two-step PCA method를 적용하여 oligo 기반 합성을 수행하였다. 각 합성 방법을 통해 제작된 block은 이후 primer amplification을 통해 충분한 양의 DNA fragment를 확보하도록 하였다.
각 block의 amplification primer는 DVA vector와의 Gibson Assembly가 가능하도록 vector overlap sequence를 포함하도록 설계하였으며, 동시에 최종 Golden Gate Assembly를 위해 BsaI recognition site와 각 block에 해당하는 assembly overhang sequence가 포함되도록 구성하였다. 이를 통해 각 block을 개별적으로 DVA vector에 cloning한 후 sequence를 확인하고, 최종적으로 BsaI 기반 Golden Gate Assembly를 수행하여 전체 8,929 bp RSM3 서열을 하나의 construct로 조립하도록 workflow를 구성하였다.

## Related Unit Operations

- [USW010 DNA Oligomer Pool Design](#usw010-dna-oligomer-pool-design)
- [USW020 Primer Design](#usw020-primer-design)

---

### [USW010 DNA Oligomer Pool Design]

> A software package that designs DNA oligomers which are pooled in a single tube. It optimizes the selection and combination of oligomers for efficient DNA assembly and synthesis.

#### Meta
- Experimenter: '문지민'
- Start_date: '2026-08-06'
- End_date: '2026-08-13'
- Software: 'Snapgene, ChatGPT-5.6 Sol'

#### Input
[RSM3_mutated_fullseq_Align.gb](RSM3_mutated_fullseq_Align.gb)

#### Output
[RSM3 DNA, complete genome_mutated_1788935258178.fasta](RSM3%20DNA,%20complete%20genome_mutated_1788935258178.fasta)[RSM3 Fragment block design.docx](RSM3%20Fragment%20block%20design.docx)
[RSM3 Block2.txt](RSM3%20Block2.txt)[RSM_Block1-5.txt](RSM_Block1-5.txt)
[PCA_GPTOligo1-5.xlsx](PCA_GPTOligo1-5.xlsx)
[260820_RSM3_PCABlock1_Macrogen_tube.xls](260820_RSM3_PCABlock1_Macrogen_tube.xls)

#### Parameters
- (options, hyperparameters, seed)

#### QC Metrics
Tm 우선 설계(Tm-priority design)
- Overlap Tm: 59–63°C 범위를 엄격하게 적용
- GC content: 대부분 35-70% 범위 내 분포
- 최소 overlap 길이: GC 영역에서는 모든 블록에 20 bp 이상의 동일 기준을 적용하기 어려워, 블록별로 19/20/17/18 bp로 조정
- 이차구조 평가: 서열 간 상보성을 기반으로 한 스크리닝 지표를 사용하여, 잠재적인 이차구조 형성 가능성을 상대적으로 최소화하는 방향으로 설계

#### Method
1. RSM3 서열에 대한 DNA sequence를 gb (GeneBank DNA) file로 준비하였다.
2. RSM3(8.9kb) 서열에서 GenomeAssembly (https://esunni.github.io/GenomeAssembler/) 사이트를 이용하여 서열을 약 1.8kb 5개의 block으로 나눈 후, BsaI 인식 서열 4곳에 대해 silent mutation을 진행하였으며 파일명은 'RSM3 DNA, complete genome_mutated.fasta'로 저장하였다.
3. NEBridge SplitSet Tool 이용해 5개의 block에 대한 4bp overhang fragment를 얻어 block sequence를 제작했다. Sequence는 'RSM3 Fragment block design.docx'에 저장하였다.
4. Block은 400-500bp로 나누어 각각 4개의 소블럭 형성하여 'RSM_Block1-5.txt'로 저장하였다.
5. 각 소블럭은 GPT-5.6 Sol을 이용하여 Oligo를 제작하였으며 설정값은 다음과 같다.
    1) Coverage: assembly oligos cover every target base
    2) Orientation: First oligo +, Final oligo -
    3) Overlap length: 19-25bp
    4) Overlap Tm: 58-63°C
    5) Oligo length: 55-70bp
    6) Oligo GC%: 30-70%
    7) Secondary structure 최소화 (Hairpin, Self-dimer, Hetero-dimer)
6. 제작된 Oligo 'PCA_GPTOligo1-5.xlsx'는 Snapgene alignment를 이용하여 재검증하였다.
7. RSM3 서열 중 Block1에 대하여 Macrogen에서 60bp 이상 서열에 대해 PAGE 정제로 oligo를 주문하였다.

#### Environment
- (conda / poetry / container / OS / HW)

#### Discussion
- 초기 oligo 설계에는 Dsembler2를 활용하고자 하였으나, 설계 결과가 + strand로 시작하는 경우 마지막 oligo 역시 + strand로 배치되는 등 본 실험에서 요구하는 oligo 배치 방식과 일치하지 않는 경우가 확인되었다. 이에 따라 Dsembler2 결과를 직접 적용하기에는 제한이 있다고 판단하였으며, 최종적으로 GPT 기반의 oligo 설계를 진행하였다.

- 전체 RSM3 서열 합성에 필요한 oligo는 총 212개로, 모든 oligo에 대해 secondary structure 및 oligo 간 상호작용을 개별적으로 검토하는 데에는 현실적인 한계가 있었다. 따라서 oligo length, GC content, overlap length 및 overlap Tm 등의 주요 설계 조건을 기준으로 QC를 수행하였다. 일부 oligo에서 GC content 또는 overlap length가 초기 설정 범위를 벗어나는 경우가 확인되었으나, 전체적인 서열 특성과 assembly 가능성을 고려하여 허용 가능한 범위로 판단하였다. Oligo별 상세 설계 및 QC 결과는 `PCA_GPTOligo1-5.xlsx`의 관련 sheet에 정리하였다.

- Block 1 합성에는 총 54개의 oligo가 필요하여 개별 tube 형태로 주문하였다. 그러나 향후 다른 block까지 합성 범위를 확대할 경우 필요한 oligo 수가 크게 증가하므로, 개별 tube 방식은 비용뿐만 아니라 oligo preparation 및 sample handling 측면에서도 비효율적일 수 있다. 따라서 다수의 block을 동시에 합성하는 경우에는 96-well plate scale로 oligo를 주문하는 것이 실험 준비 및 oligo 관리의 효율성을 높이는 데 적합할 것으로 판단된다.

---

### [USW020 Primer Design]

> Designing primers regarding melting temperature and structure. The primers are used for mutant generation, PCR primers, and other molecular biology applications, ensuring specificity and efficiency in amplification.

#### Meta
- Experimenter: '문지민'
- Start_date: '2026-08-12 17:58'
- End_date: '2026-08-13'
- Software: 'Snapgene'

#### Input
[RSM3 Block2.txt](RSM3%20Block2.txt)[RSM_Block1-5.txt](RSM_Block1-5.txt)

#### Output
[RSM3Block_OuterPrimer.xlsx](RSM3Block_OuterPrimer.xlsx)
[260820_RSM3_PCABlock1_Macrogen_tube.xls](260820_RSM3_PCABlock1_Macrogen_tube.xls)

#### Parameters
- (options, hyperparameters, seed)

#### QC Metrics
Outer primer
각 block의 말단 서열을 변경하지 않는 것을 기본 조건으로 하여 primer를 설계하였다. Forward/Reverse primer의 Tm은 각각 60–64°C, primer pair 간 ΔTm ≤2°C를 우선적인 QC 기준으로 적용하였다. 해당 조건을 만족하는 범위에서 안정적인 amplification을 위해 적절한 길이의 primer를 선정하였다.

Gibson Assembly primer
Gibson Assembly primer는 각 block의 증폭과 DVA vector와의 assembly가 가능하도록 설계된 전체 primer sequence를 기준으로 QC를 수행하였다. 특히 vector overlap sequence, BsaI recognition site, 1-bp spacer 및 4-bp Golden Gate overhang이 설계된 위치와 방향으로 정확하게 포함되어 있는지 확인하였다. 또한 overlap 부분의 Tm값을 비슷하게 설정하여, 이후 Gibson Assembly 및 Golden Gate Assembly에 사용할 수 있도록 설계하였다.

#### Method
1. Outer primer 및 Gibson Assembly primer 설계
각 RSM3 block의 증폭을 위한 outer primer와 DVA vector cloning을 위한 Gibson Assembly primer는 SnapGene을 이용하여 설계하였으며, 설계 결과는 RSM3Block_OuterPrimer에 정리하였다.

2. Gibson Assembly primer 구성
Gibson Assembly primer는 각 block과 DVA vector 간의 Gibson Assembly가 가능하도록 vector와 상동성을 갖는 overlap sequence를 포함하여 설계하였다. 또한 이후 5개 block의 Golden Gate Assembly를 고려하여 BsaI recognition site, 1-bp spacer 및 block 간 연결을 위한 4-bp overhang sequence를 primer에 포함하였다. 이를 통해 각 block을 DVA vector에 개별적으로 cloning한 후, BsaI digestion을 통해 정의된 overhang을 생성하여 최종 5-block assembly에 사용할 수 있도록 설계하였다.

#### Environment
- (conda / poetry / container / OS / HW)

#### Discussion
- (comments for the next step)

## Conclusions and Discussion

Oligo assembly를 통해 합성된 각 block을 바로 최종 Golden Gate Assembly에 사용하는 대신, DVA vector에 개별적으로 Gibson Assembly하여 cloning하는 전략을 적용하였다. Oligo 기반 DNA 합성 과정에서는 substitution, insertion 및 deletion 등의 sequence error가 발생할 가능성이 있으므로, 각 block을 개별 clone으로 확보한 후 sequencing을 통해 정확한 서열을 선별하는 과정이 필요하다고 판단하였다.

각 block을 DVA vector에 개별적으로 cloning함으로써 약 1.8 kb 단위에서 sequence QC가 가능하며, 문제가 확인된 경우 전체 RSM3 서열을 다시 합성하지 않고 해당 block만 재합성 또는 재선별할 수 있다는 장점이 있다. 특히 서로 다른 oligo assembly 방법으로 제작된 block의 정확도를 개별적으로 평가하고 비교하는 데에도 적합한 전략으로 판단된다.

또한 Gibson Assembly용 vector overlap과 최종 조립을 위한 BsaI recognition site 및 overhang을 primer에 함께 포함시킴으로써, oligo assembly 이후 별도의 서열 변형 과정 없이 동일한 block을 DVA vector cloning과 최종 Golden Gate Assembly에 연속적으로 활용할 수 있도록 하였다.

반면 각 block에 대해 cloning, transformation, colony selection 및 sequencing 과정이 추가되므로 직접적인 multi-fragment assembly에 비해 전체 실험 시간이 증가하는 한계가 있다. 그러나 최종적으로 5개의 block을 이용하여 8,929 bp의 긴 RSM3 서열을 조립해야 한다는 점을 고려하면, 최종 assembly 이전에 각 block의 sequence 정확도를 확보하는 것이 전체 construct의 조립 성공률과 신뢰성을 높이는 데 유리할 것으로 판단된다.

