# Deepfake / Face Forgery Detection (Type 2 — Digital / Injection Attacks)

Part of [Awesome Face Authentication Security](./README.md). This page collects resources for detecting **digitally manipulated faces** — face-swap, face reenactment, attribute editing, and entire-face synthesis (GAN/diffusion). In the authentication-security taxonomy these are **Type 2 (digital / injection) attacks**, complementary to [Type 1 presentation attacks](./Face-Anti-Spoofing.md).

Scope: CCF-A venues (CVPR, ICCV, ECCV, T-PAMI, T-IFS, AAAI, IJCAI, NeurIPS, ICLR, ACM MM), 2022–2026, plus major datasets and surveys. For papers that detect **both** Type 1 and Type 2 attacks, see the [Unified Attack Detection](./README.md#unified-type-1--type-2-attack-detection) section in the overview.

# Contents
- [Datasets](#datasets)
- [Surveys](#surveys)
- [Detection Methods](#detection-methods)
  - [Year 2026](#year-2026)
  - [Year 2025](#year-2025)
  - [Year 2024](#year-2024)
  - [Year 2023](#year-2023)
  - [Year 2022](#year-2022)
- [Notes](#notes)

# Datasets
|  Name   | Release year | Manipulations / Attacks | Scale |
|:--------|:--------:|:--------|:--------|
|[FaceForensics++](https://github.com/ondyari/FaceForensics)|2019|Deepfakes, Face2Face, FaceSwap, NeuralTextures (3 compression levels)|1,000 real + 4,000 fake videos|
|[DeepfakeTIMIT](https://www.idiap.ch/en/scientific-research/data/deepfaketimit)|2018|GAN face-swap on VidTIMIT (LQ + HQ)|640 fake videos, 32 subjects|
|[DFFD (Diverse Fake Face Dataset)](http://cvlab.cse.msu.edu/dffd-dataset.html)|2020|Identity swap, expression/attribute edit, entire-face synthesis (ProGAN, StyleGAN)|~58.7k real + ~240k fake images|
|[DFDC Preview](https://arxiv.org/abs/1910.08854)|2019|2 face-swap methods|~5,000 videos, 66 actors|
|[DFDC (full)](https://ai.meta.com/datasets/dfdc/)|2020|Multiple face-swap/GAN methods + augmentations/distractors|~128k clips, ~3,426 actors|
|[Celeb-DF (v2)](https://github.com/yuezunli/celeb-deepfakeforensics)|2020|High-quality improved face-swap synthesis|590 real + 5,639 fake videos, 59 celebrities|
|[DeeperForensics-1.0](https://github.com/EndlessSora/DeeperForensics-1.0)|2020|End-to-end face-swap (DF-VAE) + 7 real-world perturbations|60,000 videos (~17.6M frames), 100 actors|
|[WildDeepfake](https://github.com/OpenTAI/wild-deepfake)|2020|Real-world in-the-wild deepfakes (mixed software)|7,314 face sequences from 707 videos|
|[KoDF](https://deepbrainai-research.github.io/kodf/)|2021|FaceSwap, DeepFaceLab, FSGAN, FOMM, ATFHP, Wav2Lip|62,166 real + 175,776 fake clips, 403 subjects|
|[FakeAVCeleb](https://github.com/DASH-Lab/FakeAVCeleb)|2021|Audio-visual: face-swap (FSGAN), lip-sync (Wav2Lip), voice cloning|500 real + 19,500 fake videos|
|[ForgeryNet](https://github.com/yinanhe/ForgeryNet)|2021|7 image-level + 8 video-level manipulations; 36 perturbations|2.9M images + 221,247 videos|
|[DF-Platter](https://iab-rubric.org/df-platter-database)|2023|Multi-face heterogeneous deepfakes, low/high-res, multiple methods|133,260 videos|
|[DiFF (Diffusion Facial Forgery)](https://github.com/xaCheng1996/DiFF)|2024|Diffusion-generated faces, 13 methods (T2I, I2I, face-swap, face-edit)|500,000+ images, 30,000 prompts|
|[DF40](https://github.com/YZY-stack/DF40)|2024|40 techniques: 10 face-swap, 13 reenactment, 12 synthesis, 5 editing|Million-level images + videos|
|[AV-Deepfake1M](https://github.com/ControlNet/AV-Deepfake1M)|2024|LLM-driven audio-visual deepfakes (content-driven)|1M+ videos|
|[DeepFaceGen](https://github.com/HengruiLou/DeepFaceGen)|2024|35 generation techniques (face-swap, reenactment, synthesis)|~1.5M real/forged samples|
|[ILLUSION](https://www.iab-rubric.org/illusion-database)|2025|Multi-modal, multi-lingual audio-visual deepfakes|~1.3M samples|

# Surveys
|  Title  | Venue | Note |
|:--------|:--------:|:--------|
|[Deepfake Generation and Detection: A Benchmark and Survey](https://arxiv.org/abs/2403.17881)|ACM CSUR 2025|Face swap, reenactment, talking-face, attribute editing + detection benchmarks|
|[Deepfake Detection: A Comprehensive Survey from the Reliability Perspective](https://dl.acm.org/doi/full/10.1145/3699710)|ACM CSUR 2024|Transferability, interpretability, robustness|
|[DeepFake Detection in the AIGC Era: A Survey, Benchmarks, and Future Perspectives](https://www.sciencedirect.com/science/article/abs/pii/S1566253525008024)|Information Fusion 2025|Cue-based vs data-driven; diffusion/AIGC-era focus|
|[Deep Learning for Deepfakes Creation and Detection: A Survey](https://arxiv.org/abs/1909.11573)|CVIU 2022|Foundational survey of creation + detection|
|[A Survey on Speech Deepfake Detection](https://dl.acm.org/doi/10.1145/3714458)|ACM CSUR 2025|Audio-only (200+ papers); relevant for audio-visual deepfakes|

# Detection Methods

## Year 2026
|  Title  | Venue | Note |
|:--------|:--------:|:--------|
|[DiffusionFF: A Diffusion-based Framework for Joint Face Forgery Detection and Fine-Grained Artifact Localization](https://arxiv.org/abs/2508.01873)|CVPR 2026|DiffusionFF; diffusion decoder synthesizes fine-grained artifact-localization maps; detection + explainability|
|[Unleashing Vision-Language Semantics for Deepfake Video Detection](https://arxiv.org/abs/2603.24454)|CVPR 2026|VLAForge; CLIP cross-modal semantics + identity-aware VLA score; cross-forgery generalization, [Code](https://github.com/mala-lab/VLAForge)|
|[Revisiting Face Forgery Detection: From Facial Representation to Forgery Detection](https://arxiv.org/abs/2409.16945)|T-PAMI 2026|FFD-specific self-supervised pretrained backbone + competitive fine-tuning, [Code](https://github.com/zhenglab/FFDBackbone)|
|[SSD: Making Face Forgery Clues Evident Again With Self-Steganographic Detection](https://doi.org/10.1109/TPAMI.2026.3667180)|T-PAMI 2026|SSD; proactive self-steganographic detection embedding a learnable face to expose clues|
|[MAP-Mamba: Multi-Artifacts Perception Mamba for Generalizable Face Forgery Detection](https://doi.org/10.1109/TIFS.2026.3651948)|T-IFS 2026|MAP-Mamba; Mamba multi-artifact perception; generalization|
|[Dual-Granularity Contrastive Learning for DeepFake Detection](https://doi.org/10.1109/TIFS.2026.3653569)|T-IFS 2026|Dual-granularity contrastive learning; generalization|
|[Toward Generalizable Deepfake Detection via Forgery-Aware Audio-Visual Adaptation: A Variational Bayesian Approach](https://doi.org/10.1109/TIFS.2026.3673104)|T-IFS 2026|FoVB; variational Bayesian forgery-aware audio-visual adaptation|
|[FauForensics: Boosting Audio-Visual Deepfake Detection With Facial Action Units](https://doi.org/10.1109/TIFS.2026.3674401)|T-IFS 2026|Facial action units + frame-wise AV similarity fusion; audio-visual|
|[Component-Specific Prompt Tuning for Deepfake Detection](https://doi.org/10.1109/TIFS.2026.3678021)|T-IFS 2026|CSPT; component-specific prompt tuning of CLIP|
|[Precise Temporal Forgery Localization via Quantified Audio-Visual Asynchrony](https://doi.org/10.1109/TIFS.2026.3683280)|T-IFS 2026|Quantifies audio-visual asynchrony to localize forged segments|
|[Adaptive Affinity Memorization With Layer Mutation for Multimodal Deepfake Continual Detection](https://doi.org/10.1109/TIFS.2026.3707760)|T-IFS 2026|Affinity memorization + layer mutation; multimodal continual learning|
|[Open-World Deepfake Attribution via Confidence-Aware Asymmetric Learning](https://arxiv.org/abs/2512.12667)|AAAI 2026|CAL; open-world attribution of known + unknown forgeries|
|[Fine-Grained DINO Tuning with Dual Supervision for Face Forgery Detection](https://arxiv.org/abs/2511.12107)|AAAI 2026|DFF-Adapter; DINOv2 multi-head LoRA + dual supervision|
|[Veritas: Generalizable Deepfake Detection via Pattern-Aware Reasoning](https://arxiv.org/abs/2508.21048)|ICLR 2026|Oral; MLLM pattern-aware reasoning; transparent generalizable detection; HydraFake benchmark|
|[Exploring Specular Reflection Inconsistency for Generalizable Face Forgery Detection](https://openreview.net/forum?id=KwXkLYmZvR)|ICLR 2026|SRI-Net; physics cue (specular/illumination inconsistency); targets diffusion faces|
|[A Rich Knowledge Space for Scalable Deepfake Detection](https://openreview.net/forum?id=hNd5L7WnjC)|ICLR 2026|SD²; refines CLIP with type-specific text labels; MMI-DD dataset|

## Year 2025
|  Title  | Venue | Note |
|:--------|:--------:|:--------|
|[Forensics Adapter: Adapting CLIP for Generalizable Face Forgery Detection](https://openaccess.thecvf.com/content/CVPR2025/html/Cui_Forensics_Adapter_Adapting_CLIP_for_Generalizable_Face_Forgery_Detection_CVPR_2025_paper.html)|CVPR 2025|Lightweight CLIP adapter + masked blending-boundary learning; cross-dataset, [Code](https://github.com/OUC-VAS/ForensicsAdapter)|
|[Rethinking Vision-Language Model in Face Forensics: Multi-Modal Interpretable Forged Face Detector](https://openaccess.thecvf.com/content/CVPR2025/papers/Guo_Rethinking_Vision-Language_Model_in_Face_Forensics_Multi-Modal_Interpretable_Forged_Face_CVPR_2025_paper.pdf)|CVPR 2025|M2F2-Det (Oral); CLIP+LLM; detection score + textual explanation, [Code](https://github.com/CHELSEA234/M2F2_Det)|
|[Towards General Visual-Linguistic Face Forgery Detection](https://openaccess.thecvf.com/content/CVPR2025/html/Sun_Towards_General_Visual-Linguistic_Face_Forgery_Detection_CVPR_2025_paper.html)|CVPR 2025|VLFFD; face-forgery text generator + vision-language tri-branch, [Code](https://github.com/skjack/vlffd)|
|[D3: Scaling Up Deepfake Detection by Learning from Discrepancy](https://openaccess.thecvf.com/content/CVPR2025/papers/Yang_D3_Scaling_Up_Deepfake_Detection_by_Learning_from_Discrepancy_CVPR_2025_paper.pdf)|CVPR 2025|Discrepancy deepfake detector; deconstructs universal artifacts; OOD generalization|
|[FreqDebias: Towards Generalizable Deepfake Detection via Consistency-Driven Frequency Debiasing](https://openaccess.thecvf.com/content/CVPR2025/papers/Kashiani_FreqDebias_Towards_Generalizable_Deepfake_Detection_via_Consistency-Driven_Frequency_Debiasing_CVPR_2025_paper.pdf)|CVPR 2025|FreqDebias; breaks frequency shortcut bias; cross-dataset|
|[Generalizing Deepfake Video Detection with Plug-and-Play: Video-Level Blending and Spatiotemporal Adapter Tuning](https://openaccess.thecvf.com/content/CVPR2025/papers/Yan_Generalizing_Deepfake_Video_Detection_with_Plug-and-Play_Video-Level_Blending_and_Spatiotemporal_CVPR_2025_paper.pdf)|CVPR 2025|Video-level blending + spatiotemporal adapter; plug-and-play video generalization|
|[Towards a Universal Synthetic Video Detector: From Face or Background Manipulations to Fully AI-Generated Content](https://openaccess.thecvf.com/content/CVPR2025/html/Kundu_Towards_a_Universal_Synthetic_Video_Detector_From_Face_or_Background_CVPR_2025_paper.html)|CVPR 2025|UNITE; SigLIP + attention-diversity loss; face-swap/background/fully-AI video, [Code](https://github.com/Rohit-Kundu/UNITE)|
|[SIDA: Social Media Image Deepfake Detection, Localization and Explanation with Large Multimodal Models](https://openaccess.thecvf.com/content/CVPR2025/html/Huang_SIDA_Social_Media_Image_Deepfake_Detection_Localization_and_Explanation_with_CVPR_2025_paper.html)|CVPR 2025|SIDA; LMM joint detection + region localization + explanation|
|[Stacking Brick by Brick: Aligned Feature Isolation for Incremental Face Forgery Detection](https://openaccess.thecvf.com/content/CVPR2025/papers/Cheng_Stacking_Brick_by_Brick_Aligned_Feature_Isolation_for_Incremental_Face_CVPR_2025_paper.pdf)|CVPR 2025|Incremental/continual detection; aligned feature isolation|
|[DeepShield: Fortifying Deepfake Video Detection with Local and Global Forgery Analysis](https://openaccess.thecvf.com/content/ICCV2025/html/Cai_DeepShield_Fortifying_Deepfake_Video_Detection_with_Local_and_Global_Forgery_ICCV_2025_paper.html)|ICCV 2025|DeepShield; CLIP-ViT + local patch guidance + global forgery diversification; video generalization|
|[FakeRadar: Probing Forgery Outliers to Detect Unknown Deepfake Videos](https://openaccess.thecvf.com/content/ICCV2025/html/Li_FakeRadar_Probing_Forgery_Outliers_to_Detect_Unknown_Deepfake_Videos_ICCV_2025_paper.html)|ICCV 2025|FakeRadar; CLIP forgery-outlier probing; targets unknown manipulations|
|[Vulnerability-Aware Spatio-Temporal Learning for Generalizable and Interpretable Deepfake Video Detection](https://arxiv.org/abs/2501.01184)|ICCV 2025|FakeSTormer; multi-task spatiotemporal + subtle-artifact synthesis; generalizable & interpretable, [Code](https://github.com/10Ring/FakeSTormer)|
|[Beyond Spatial Frequency: Pixel-wise Temporal Frequency-based Deepfake Video Detection](https://arxiv.org/abs/2507.02398)|ICCV 2025|PwTF-DVD; per-pixel temporal-frequency inconsistency, [Code](https://github.com/rama0126/PwTF-DVD)|
|[Generalization-Preserved Learning: Closing the Backdoor to Catastrophic Forgetting in Continual Deepfake Detection](https://openaccess.thecvf.com/content/ICCV2025/papers/Zhang_Generalization-Preserved_Learning_Closing_the_Backdoor_to_Catastrophic_Forgetting_in_Continual_ICCV_2025_paper.pdf)|ICCV 2025|GPL; continual detection preserving cross-domain generalization|
|[MFCLIP: Multi-Modal Fine-Grained CLIP for Generalizable Diffusion Face Forgery Detection](https://doi.org/10.1109/TIFS.2025.3576577)|T-IFS 2025|MFCLIP; language-guided image+noise CLIP; diffusion-face generalization, [Code](https://github.com/Jenine-321/MFCLIP)|
|[SAGNet: Decoupling Semantic-Agnostic Artifacts From Limited Training Data for Robust Generalization in Deepfake Detection](https://doi.org/10.1109/TIFS.2025.3581726)|T-IFS 2025|SAGNet; decouples semantic-agnostic artifacts; cross-domain|
|[Customized Transformer Adapter With Frequency Masking for Deepfake Detection](https://doi.org/10.1109/TIFS.2025.3574983)|T-IFS 2025|Transformer adapter + frequency masking; generalization|
|[Semantic Token Transformer for Face Forgery Detection](https://doi.org/10.1109/TIFS.2025.3567110)|T-IFS 2025|STT; facial-semantic adaptive tokens|
|[Gradient-Aware Adaptive Meta-Prompt Learner for Generalizable Face Forgery Detection](https://doi.org/10.1109/TIFS.2025.3622981)|T-IFS 2025|GAMPL; gradient-aware meta-prompt learning|
|[Bi-Stream Coteaching Network for Weakly-Supervised Deepfake Localization in Videos](https://doi.org/10.1109/TIFS.2025.3533906)|T-IFS 2025|Bi-stream co-teaching; weakly-supervised video forgery localization|
|[Standing on the Shoulders of Giants: Reprogramming Visual-Language Model for General Deepfake Detection](https://ojs.aaai.org/index.php/AAAI/article/view/32559)|AAAI 2025|RepDFD; reprograms frozen CLIP with visual + text prompts; cross-dataset|
|[C2P-CLIP: Injecting Category Common Prompt in CLIP to Enhance Generalization in Deepfake Detection](https://ojs.aaai.org/index.php/AAAI/article/view/32772)|AAAI 2025|C2P-CLIP; category-common prompt into CLIP; cross-generator, [Code](https://github.com/chuangchuangtan/C2P-CLIP-DeepfakeDetection)|
|[Multi-modal Deepfake Detection via Multi-task Audio-Visual Prompt Learning](https://ojs.aaai.org/index.php/AAAI/article/view/32042)|AAAI 2025|Audio-visual multi-task prompt learning + cross-modal consistency|
|[GLCF: A Global-Local Multimodal Coherence Analysis Framework for Talking Face Generation Detection](https://ojs.aaai.org/index.php/AAAI/article/view/31982)|AAAI 2025|Audio-visual talking-face detection + MSTF benchmark|
|[ODDN: Addressing Unpaired Data Challenges in Open-World Deepfake Detection on Online Social Networks](https://ojs.aaai.org/index.php/AAAI/article/view/32063)|AAAI 2025|Oral; compression-robust open-world detection, [Code](https://github.com/ManyiLee/Open-world-Deepfake-Detection-Network)|
|[DevFD: Developmental Face Forgery Detection by Learning Shared and Orthogonal LoRA Subspaces](https://openreview.net/forum?id=Xpuci4SV06)|NeurIPS 2025|Continual learning; developmental MoE with Real-LoRA + orthogonal Fake-LoRAs|
|[Fair Deepfake Detectors Can Generalize](https://openreview.net/forum?id=p27bSdc3FS)|NeurIPS 2025|DAID; links fairness and generalization; demographic-aware rebalancing, [Code](https://github.com/xaCheng1996/DAID)|
|[From Specificity to Generality: Revisiting Generalizable Artifacts in Detecting Face Deepfakes](https://arxiv.org/abs/2504.04827)|NeurIPS 2025|Face-inconsistency + up-sampling artifacts; pseudo-fakes via super-resolution + self-blending|
|[Through the Lens: Benchmarking Deepfake Detectors Against Moiré-Induced Distortions](https://openreview.net/forum?id=HtGOaraQEH)|NeurIPS 2025|DeepMoiréFake benchmark; detector failure under screen-recapture Moiré|
|[HAMLET-FFD: Hierarchical Adaptive Multi-modal Learning Embeddings Transformation for Face Forgery Detection](https://arxiv.org/abs/2507.20913)|ACM MM 2025|HAMLET-FFD; CLIP bidirectional cross-modal reasoning; cross-domain|
|[WMamba: Wavelet-based Mamba for Face Forgery Detection](https://arxiv.org/abs/2501.09617)|ACM MM 2025|WMamba; wavelet/frequency + Mamba long-range modeling|
|[RAIDX: A Retrieval-Augmented Generation and GRPO Reinforcement Learning Framework for Explainable Deepfake Detection](https://arxiv.org/abs/2508.04524)|ACM MM 2025|RAIDX; RAG + GRPO RL; MLLM explainability with rationales + saliency|
|[Learning Real Facial Concepts for Independent Deepfake Detection](https://arxiv.org/abs/2505.04460)|IJCAI 2025|RealID; models the "real face" concept; independent dual-decision classifier|
|[CorrDetail: Visual Detail Enhanced Self-Correction for Face Forgery Detection](https://arxiv.org/abs/2507.05302)|IJCAI 2025|Interpretable detection; visual-detail self-correction (MLLM)|
|[ILLUSION: Unveiling Truth with a Comprehensive Multi-Modal, Multi-Lingual Deepfake Dataset](https://openreview.net/forum?id=qnlG3zPQUy)|ICLR 2025|Benchmark; ~1.3M audio-visual multi-lingual deepfake samples|

## Year 2024
|  Title  | Venue | Note |
|:--------|:--------:|:--------|
|[Transcending Forgery Specificity with Latent Space Augmentation for Generalizable Deepfake Detection](https://openaccess.thecvf.com/content/CVPR2024/html/Yan_Transcending_Forgery_Specificity_with_Latent_Space_Augmentation_for_Generalizable_Deepfake_CVPR_2024_paper.html)|CVPR 2024|LSDA; latent-space augmentation enlarges forgery space; cross-dataset|
|[LAA-Net: Localized Artifact Attention Network for Quality-Agnostic and Generalizable Deepfake Detection](https://openaccess.thecvf.com/content/CVPR2024/html/Nguyen_LAA-Net_Localized_Artifact_Attention_Network_for_Quality-Agnostic_and_Generalizable_Deepfake_CVPR_2024_paper.html)|CVPR 2024|LAA-Net; localized artifact attention + self-blended images, [Code](https://github.com/10Ring/LAA-Net)|
|[Exploiting Style Latent Flows for Generalizing Deepfake Video Detection](https://openaccess.thecvf.com/content/CVPR2024/html/Choi_Exploiting_Style_Latent_Flows_for_Generalizing_Deepfake_Video_Detection_CVPR_2024_paper.html)|CVPR 2024|StyleGRU; temporal anomalies in style-latent flows; video generalization|
|[AVFF: Audio-Visual Feature Fusion for Video Deepfake Detection](https://openaccess.thecvf.com/content/CVPR2024/html/Oorloff_AVFF_Audio-Visual_Feature_Fusion_for_Video_Deepfake_Detection_CVPR_2024_paper.html)|CVPR 2024|AVFF; cross-modal AV correspondence learning + fusion|
|[Preserving Fairness Generalization in Deepfake Detection](https://arxiv.org/abs/2402.17229)|CVPR 2024|Disentangles demographic vs forgery features + flat loss landscape; fairness, [Code](https://github.com/Purdue-M2/Fairness-Generalization)|
|[Contrasting Deepfakes Diffusion via Contrastive Learning and Global-Local Similarities](https://arxiv.org/abs/2407.20337)|ECCV 2024|CoDE; diffusion-image detection; contrastive global-local; D3 dataset, [Code](https://github.com/aimagelab/CoDE)|
|[Learning Natural Consistency Representation for Face Forgery Video Detection](https://arxiv.org/abs/2407.10550)|ECCV 2024|NACO; self-supervised spatiotemporal natural-consistency; generalization|
|[Common Sense Reasoning for Deepfake Detection](https://link.springer.com/chapter/10.1007/978-3-031-73223-2_22)|ECCV 2024|Vision-language common-sense reasoning; explainable (DD-VQA framing)|
|[Real Appearance Modeling for More General Deepfake Detection](https://link.springer.com/chapter/10.1007/978-3-031-72943-0_23)|ECCV 2024|RAM; recover real face from disturbed face (reconstruction); generalization|
|[Detecting and Grounding Multi-Modal Media Manipulation and Beyond](https://doi.org/10.1109/TPAMI.2024.3367749)|T-PAMI 2024|DGM4 / HAMMER++; multimodal manipulation detection + fine-grained grounding, [Code](https://github.com/rshaojimmy/MultiModal-DeepFake)|
|[Fully Unsupervised Deepfake Video Detection via Enhanced Contrastive Learning](https://doi.org/10.1109/TPAMI.2024.3356814)|T-PAMI 2024|Unsupervised contrastive learning over inter-frame correlation, [Code](https://github.com/bestalllen/Unsupervised_DF_Detection)|
|[Beyond the Prior Forgery Knowledge: Mining Critical Clues for General Face Forgery Detection](https://doi.org/10.1109/TIFS.2023.3332218)|T-IFS 2024|Mines manipulation-agnostic critical clues; generalization|
|[Exploring Bi-Level Inconsistency via Blended Images for Generalizable Face Forgery Detection](https://doi.org/10.1109/TIFS.2024.3417266)|T-IFS 2024|Blended-image self-supervision; bi-level inconsistency|
|[GenFace: A Large-Scale Fine-Grained Face Forgery Benchmark and Cross Appearance-Edge Learning](https://doi.org/10.1109/TIFS.2024.3461958)|T-IFS 2024|GenFace benchmark (incl. diffusion faces) + CAEL detector, [Code](https://github.com/Jenine-321/GenFace)|
|[DomainForensics: Exposing Face Forgery Across Domains via Bi-Directional Adaptation](https://doi.org/10.1109/TIFS.2024.3426317)|T-IFS 2024|Bi-directional domain adaptation; generalization, [Code](https://github.com/OUC-VAS/DomainForensics)|
|[MINTIME: Multi-Identity Size-Invariant Video Deepfake Detection](https://doi.org/10.1109/TIFS.2024.3409054)|T-IFS 2024|MINTIME; multi-identity, size-invariant video detection, [Code](https://github.com/davide-coccomini/MINTIME-Multi-Identity-size-iNvariant-TIMEsformer-for-Video-Deepfake-Detection)|
|[Constructing New Backbone Networks via Space-Frequency Interactive Convolution for Deepfake Detection](https://doi.org/10.1109/TIFS.2023.3324739)|T-IFS 2024|SFIConv; space-frequency interactive convolution backbone, [Code](https://github.com/EricGzq/SFIConv)|
|[MMNet: Multi-Collaboration and Multi-Supervision Network for Sequential Deepfake Detection](https://doi.org/10.1109/TIFS.2024.3361151)|T-IFS 2024|MMNet; detects sequential/multi-step face manipulations|
|[Frequency-Aware Deepfake Detection: Improving Generalizability through Frequency Space Domain Learning](https://ojs.aaai.org/index.php/AAAI/article/view/28310)|AAAI 2024|FreqNet; frequency-domain, source-agnostic features, [Code](https://github.com/chuangchuangtan/FreqNet-DeepfakeDetection)|
|[Exposing the Deception: Uncovering More Forgery Clues for Deepfake Detection](https://ojs.aaai.org/index.php/AAAI/article/view/27829)|AAAI 2024|Multiple non-overlapping local forgery clues + information bottleneck, [Code](https://github.com/QingyuLiu/Exposing-the-Deception)|
|[DF40: Toward Next-Generation Deepfake Detection](https://openreview.net/forum?id=UZpySDOwvZ)|NeurIPS 2024|DF40 benchmark; 40 forgery techniques, [Code](https://github.com/YZY-stack/DF40)|
|[DiffusionFake: Enhancing Generalization in Deepfake Detection via Guided Stable Diffusion](https://openreview.net/forum?id=FNzpVTpNbN)|NeurIPS 2024|Reverses forgery generation; Stable Diffusion disentangles source/target identity, [Code](https://github.com/skJack/DiffusionFake)|
|[FreqBlender: Enhancing DeepFake Detection by Blending Frequency Knowledge](https://proceedings.neurips.cc/paper_files/paper/2024/hash/4f92d2f498b88f1bd43732312272967a-Abstract-Conference.html)|NeurIPS 2024|FreqBlender; blends frequency distributions to synthesize pseudo-fakes|
|[Lips Are Lying: Spotting the Temporal Inconsistency between Audio and Visual in Lip-Syncing DeepFakes](https://openreview.net/forum?id=yMS7ansbr6)|NeurIPS 2024|LipFD; audio-visual lip-sync inconsistency; AVLips dataset, [Code](https://github.com/AaronComo/LipFD)|
|[Identity-Driven Multimedia Forgery Detection via Reference Assistance](https://dl.acm.org/doi/10.1145/3664647.3680622)|ACM MM 2024|R-MFDN (Oral); reference/identity-assisted cross-modal inconsistency; IDForge dataset, [Code](https://github.com/xyyandxyy/IDForge)|
|[Diffusion Facial Forgery Detection](https://dl.acm.org/doi/10.1145/3664647.3680797)|ACM MM 2024|DiFF; diffusion-synthesized face detection + benchmark, [Code](https://github.com/xaCheng1996/DiFF)|
|[Delocate: Detection and Localization for Deepfake Videos with Randomly-Located Tampered Traces](https://arxiv.org/abs/2401.13516)|IJCAI 2024|Video detection + localization of randomly-located tampered regions|

## Year 2023
|  Title  | Venue | Note |
|:--------|:--------:|:--------|
|[Implicit Identity Leakage: The Stumbling Block to Improving Deepfake Detection Generalization](https://openaccess.thecvf.com/content/CVPR2023/html/Dong_Implicit_Identity_Leakage_The_Stumbling_Block_to_Improving_Deepfake_Detection_CVPR_2023_paper.html)|CVPR 2023|CADDM; identity leakage harms generalization; artifact detection + multi-scale face swap, [Code](https://github.com/megvii-research/CADDM)|
|[Implicit Identity Driven Deepfake Face Swapping Detection](https://openaccess.thecvf.com/content/CVPR2023/html/Huang_Implicit_Identity_Driven_Deepfake_Face_Swapping_Detection_CVPR_2023_paper.html)|CVPR 2023|Explicit + implicit identity contrast; face-swap detection|
|[AltFreezing for More General Video Face Forgery Detection](https://openaccess.thecvf.com/content/CVPR2023/html/Wang_AltFreezing_for_More_General_Video_Face_Forgery_Detection_CVPR_2023_paper.html)|CVPR 2023|Alternately freezes spatial/temporal 3D-CNN weights; video generalization|
|[AUNet: Learning Relations Between Action Units for Face Forgery Detection](https://openaccess.thecvf.com/content/CVPR2023/html/Bai_AUNet_Learning_Relations_Between_Action_Units_for_Face_Forgery_Detection_CVPR_2023_paper.html)|CVPR 2023|AUNet; facial action-unit relations; region-level inconsistency|
|[Self-Supervised Video Forensics by Audio-Visual Anomaly Detection](https://openaccess.thecvf.com/content/CVPR2023/html/Feng_Self-Supervised_Video_Forensics_by_Audio-Visual_Anomaly_Detection_CVPR_2023_paper.html)|CVPR 2023|Self-supervised A/V synchrony; deepfake as anomaly, [Code](https://github.com/cfeng16/audio-visual-forensics)|
|[Detecting and Grounding Multi-Modal Media Manipulation](https://openaccess.thecvf.com/content/CVPR2023/html/Shao_Detecting_and_Grounding_Multi-Modal_Media_Manipulation_CVPR_2023_paper.html)|CVPR 2023|DGM4; joint detection + grounding of face/text manipulation, [Code](https://github.com/rshaojimmy/MultiModal-DeepFake)|
|[UCF: Uncovering Common Features for Generalizable Deepfake Detection](https://openaccess.thecvf.com/content/ICCV2023/html/Yan_UCF_Uncovering_Common_Features_for_Generalizable_Deepfake_Detection_ICCV_2023_paper.html)|ICCV 2023|UCF; disentangle forgery-irrelevant/method-specific/common features|
|[Controllable Guide-Space for Generalizable Face Forgery Detection](https://openaccess.thecvf.com/content/ICCV2023/papers/Guo_Controllable_Guide-Space_for_Generalizable_Face_Forgery_Detection_ICCV_2023_paper.pdf)|ICCV 2023|Guide-Space; controllable forgery-domain separation; cross-domain|
|[TALL: Thumbnail Layout for Deepfake Video Detection](https://openaccess.thecvf.com/content/ICCV2023/html/Xu_TALL_Thumbnail_Layout_for_Deepfake_Video_Detection_ICCV_2023_paper.html)|ICCV 2023|TALL; thumbnail-layout frames + transformer; efficient video detection|
|[SeeABLE: Soft Discrepancies and Bounded Contrastive Learning for Exposing Deepfakes](https://openaccess.thecvf.com/content/ICCV2023/papers/Larue_SeeABLE_Soft_Discrepancies_and_Bounded_Contrastive_Learning_for_Exposing_Deepfakes_ICCV_2023_paper.pdf)|ICCV 2023|SeeABLE; one-class with synthetic local anomalies; unseen forgeries|
|[AVoiD-DF: Audio-Visual Joint Learning for Detecting Deepfake](https://doi.org/10.1109/TIFS.2023.3262148)|T-IFS 2023|Exploits temporal/intrinsic audio-visual inconsistency|
|[F2Trans: High-Frequency Fine-Grained Transformer for Face Forgery Detection](https://doi.org/10.1109/TIFS.2022.3233774)|T-IFS 2023|F2Trans; central-difference attention + high-frequency wavelet sampler|
|[FedForgery: Generalized Face Forgery Detection With Residual Federated Learning](https://doi.org/10.1109/TIFS.2023.3293951)|T-IFS 2023|Residual VAE features + federated learning; generalization, [Code](https://github.com/GANG370/FedForgery)|
|[ISTVT: Interpretable Spatial-Temporal Video Transformer for Deepfake Detection](https://doi.org/10.1109/TIFS.2023.3239223)|T-IFS 2023|ISTVT; interpretable video transformer; decomposed attention, [Code](https://github.com/Vill-Lab/2023-TIFS-ISTVT)|
|[Masked Relation Learning for DeepFake Detection](https://doi.org/10.1109/TIFS.2023.3249566)|T-IFS 2023|Spatiotemporal relation graph + masked relation learning|
|[Noise Based Deepfake Detection via Multi-Head Relative-Interaction](https://ojs.aaai.org/index.php/AAAI/article/view/26701)|AAAI 2023|NoiseDF; forensic noise traces (face vs background) + relative interaction, [Code](https://github.com/wangty1/NoiseDF)|
|[DeepfakeBench: A Comprehensive Benchmark of Deepfake Detection](https://proceedings.neurips.cc/paper_files/paper/2023/hash/0e735e4b4f07de483cbe250130992726-Abstract-Datasets_and_Benchmarks.html)|NeurIPS 2023|DeepfakeBench; unified benchmark/codebase, [Code](https://github.com/SCLBD/DeepfakeBench)|
|[UMMAFormer: A Universal Multimodal-adaptive Transformer Framework for Temporal Forgery Localization](https://dl.acm.org/doi/10.1145/3581783.3613767)|ACM MM 2023|UMMAFormer; audio-visual temporal forgery localization; TVIL dataset, [Code](https://github.com/ymhzyj/UMMAFormer)|
|[DFIL: Deepfake Incremental Learning by Exploiting Domain-invariant Forgery Clues](https://dl.acm.org/doi/10.1145/3581783.3612377)|ACM MM 2023|DFIL; incremental learning; domain-invariant features + distillation, [Code](https://github.com/DeepFakeIL/DFIL)|

## Year 2022
|  Title  | Venue | Note |
|:--------|:--------:|:--------|
|[Detecting Deepfakes With Self-Blended Images](https://openaccess.thecvf.com/content/CVPR2022/html/Shiohara_Detecting_Deepfakes_With_Self-Blended_Images_CVPR_2022_paper.html)|CVPR 2022|SBI; self-blended images reproduce generic blending artifacts; strong cross-dataset, [Code](https://github.com/mapooon/SelfBlendedImages)|
|[Self-Supervised Learning of Adversarial Example: Towards Good Generalizations for Deepfake Detection](https://openaccess.thecvf.com/content/CVPR2022/html/Chen_Self-Supervised_Learning_of_Adversarial_Example_Towards_Good_Generalizations_for_Deepfake_CVPR_2022_paper.html)|CVPR 2022|SLADD; adversarially synthesizes challenging forgeries; generalization, [Code](https://github.com/liangchen527/SLADD)|
|[Protecting Celebrities From DeepFake With Identity Consistency Transformer](https://openaccess.thecvf.com/content/CVPR2022/html/Dong_Protecting_Celebrities_From_DeepFake_With_Identity_Consistency_Transformer_CVPR_2022_paper.html)|CVPR 2022|ICT; inner/outer-face identity inconsistency transformer; robust, [Code](https://github.com/LightDXY/ICT_DeepFake)|
|[End-to-End Reconstruction-Classification Learning for Face Forgery Detection](https://openaccess.thecvf.com/content/CVPR2022/html/Cao_End-to-End_Reconstruction-Classification_Learning_for_Face_Forgery_Detection_CVPR_2022_paper.html)|CVPR 2022|RECCE; reconstruct genuine faces, use discrepancy; generalization, [Code](https://github.com/VISION-SJTU/RECCE)|
|[Leveraging Real Talking Faces via Self-Supervision for Robust Forgery Detection](https://openaccess.thecvf.com/content/CVPR2022/html/Haliassos_Leveraging_Real_Talking_Faces_via_Self-Supervision_for_Robust_Forgery_Detection_CVPR_2022_paper.html)|CVPR 2022|RealForensics; audio-visual self-supervision; robust to unseen, [Code](https://github.com/ahaliassos/RealForensics)|
|[Detecting and Recovering Sequential DeepFake Manipulation](https://arxiv.org/abs/2207.02204)|ECCV 2022|SeqFakeFormer; detect/recover multi-step manipulations; Seq-DeepFake dataset, [Code](https://github.com/rshaojimmy/SeqDeepFake)|
|[UIA-ViT: Unsupervised Inconsistency-Aware Method based on Vision Transformer for Face Forgery Detection](https://arxiv.org/abs/2210.12752)|ECCV 2022|UIA-ViT (Oral); unsupervised patch-consistency on ViT, [Code](https://github.com/wany0824/UIA-ViT)|
|[ForgeryNIR: Deep Face Forgery and Detection in Near-Infrared Scenario](https://doi.org/10.1109/TIFS.2022.3146766)|T-IFS 2022|NIR-domain GAN forgery benchmark + detection; cross-domain|
|[FakeLocator: Robust Localization of GAN-Based Face Manipulations](https://doi.org/10.1109/TIFS.2022.3141262)|T-IFS 2022|Full-resolution fakeness map; localization, robust to degradation|
|[Hierarchical Frequency-Assisted Interactive Networks for Face Manipulation Detection](https://doi.org/10.1109/TIFS.2022.3198275)|T-IFS 2022|HFI-Net; multi-level frequency-assisted interaction|
|[Improving Generalization by Commonality Learning in Face Forgery Detection](https://doi.org/10.1109/TIFS.2022.3146781)|T-IFS 2022|CFFExtractor; common forgery feature learning; generalization, [Code](https://github.com/botianzhe/CFFExtractor)|
|[Dual Contrastive Learning for General Face Forgery Detection](https://arxiv.org/abs/2112.13522)|AAAI 2022|DCL; dual inter-/intra-instance contrastive learning; generalization, [Code](https://github.com/Tencent/TFace/tree/master/security/tasks/Face-Forgery-Detection/DCL)|
|[Exploiting Fine-grained Face Forgery Clues via Progressive Enhancement Learning](https://arxiv.org/abs/2112.13977)|AAAI 2022|PEL; progressive enhancement of RGB + frequency clues|
|[ADD: Frequency Attention and Multi-View Based Knowledge Distillation to Detect Low-Quality Compressed Deepfake Images](https://arxiv.org/abs/2112.03553)|AAAI 2022|ADD; frequency attention + multi-view distillation; compressed deepfakes, [Code](https://github.com/Leminhbinh0209/AAAI22-ADD)|
|[Delving into Sequential Patches for Deepfake Detection](https://arxiv.org/abs/2207.02803)|NeurIPS 2022|Spotlight; LTTD; local-to-global temporal transformer|
|[Deepfake Video Detection with Spatiotemporal Dropout Transformer](https://dl.acm.org/doi/10.1145/3503161.3547913)|ACM MM 2022|Patch ViT + spatiotemporal dropout augmentation; robustness/generalization|

# Notes
+ Venue glossary (T-PAMI, T-IFS, CVPR, ICCV, ECCV, AAAI, IJCAI, NeurIPS, ICLR, ACM MM) is shared with the main [README](./README.md#notes).
+ ACM CSUR: ACM Computing Surveys · CVIU: Computer Vision and Image Understanding · Information Fusion: Elsevier journal.
+ This is a curated CCF-A selection (2022–2026), not exhaustive — proactive watermarking/defense, attacks on detectors, and audio-only speech-deepfake papers are mostly out of scope. For broader coverage see dedicated awesome-deepfake-detection lists.
