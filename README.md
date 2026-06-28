# Awesome-FAS (Face Authentication Security)

A curated list of Face Authentication Security (including face anti-spoofing/face presentation attack/face liveness detection, face attack models, etc.) and related resources. This is inspired by [Awesome-deep-vision](https://github.com/kjw0612/awesome-deep-vision), [Awesome-adversarial-machine-learning](https://github.com/yenchenlin/awesome-adversarial-machine-learning), [Awesome-deep-learning-papers](https://github.com/terryum/awesome-deep-learning-papers), [Awesome-NAS](https://github.com/D-X-Y/Awesome-NAS) and [Awesome-Pruing](https://github.com/he-y/Awesome-Pruning)


Please feel free to pull requests or open an issue to add papers.


  

# Contents
- [Awesome-FAS (Face Authentication Security)](#awesome-fas-face-authentication-security)
  - [Contents](#contents)
  - [Databases](#databases)
  - [Learning-based Methods](#learning-based-methods)
    - [Year 2026](##Year-2026)
    - [Year 2025](##Year-2025)
    - [Year 2024](##Year-2024)
    - [Year 2023](##Year-2023)
    - [Year 2022](##Year-2022)
    - [Year 2021](##Year-2021)
    - [Year 2020](##Year-2020)
    - [Year 2019-2018](##Year-2019-2018)
    - [Before 2018](##Before-2018)
  - [System / Mobile Applications](#system--mobile-applications)
  - [Attack](#attack)
  - [Notes](#Notes)
  



# Databases
|  Name   | Release year | Attacks | Modalities|#subjects|#videos| 
|:--------|:--------:|:--------:|:--------:|:--------:|:--------:|
|[Ambient-Flash](https://ieeexplore.ieee.org/document/9286821)|2021|2D attacks|VIS, additional light flashing|
|[3DMA](http://www.cbsr.ia.ac.cn/users/xiangyuzhu/papers/avss193dma.pdf)|2019|3D Mask|VIS,NIR|67 genuine + 48masks|920|
|[CASIA-SURF 3D HiFi Mask](https://arxiv.org/abs/2104.06148)|2020|3D Mask|VIS|
|[CASIA-SURF 3D Mask](http://www.cbsr.ia.ac.cn/users/jwan/database/3DMask.pdf), [paper](http://www.cbsr.ia.ac.cn/users/jwan/papers/TPAMI2020-spoof.pdf)|2020|3D Mask|VIS|
|[CUHK MMLab CelebA-Spoof](https://github.com/Davidzhangyuanhan/CelebA-Spoof)|2020|2D Print, Replay (Derived from CelbeA dataset)|VIS |
|[CASIA-SURF Cross-ethnicity Face Anti-spoofing (CeFA)](https://arxiv.org/abs/2003.05136), [paper](https://openaccess.thecvf.com/content/WACV2021/papers/Liu_CASIA-SURF_CeFA_A_Benchmark_for_Multi-Modal_Cross-Ethnicity_Face_Anti-Spoofing_WACV_2021_paper.pdf)|2019|2D Print, Replay; 3D print, silica gel mask| VIS, Depth, Infrared (IR)|8|192|
|[IDIAP WMCA](https://www.idiap.ch/dataset/wmca)|2019|2D Print, Replay and 3D Rigid Mask, Flexible Mask, Paper Mask attacks|VIS, depth, infrared and thermal|72|6716|
|[CASIA-SURF](https://www.researchgate.net/publication/329388462_CASIA-SURF_A_Dataset_and_Benchmark_for_Large-scale_Multi-modal_Face_Anti-spoofing), [paper](https://arxiv.org/pdf/1908.10654.pdf)|2018|2D Print/Cut|VIS, Depth, Infrared (IR)|1000|21000|
|[IDIAP CSMAD](https://www.idiap.ch/dataset/csmad), [paper](https://www.researchgate.net/profile/Sushil-Bhattacharjee/publication/329118426_Spoofing_Deep_Face_Recognition_with_Custom_Silicone_Masks/links/5bf68556a6fdcc3a8de9317e/Spoofing-Deep-Face-Recognition-with-Custom-Silicone-Masks.pdf)|2018|Custom Silicone Mask Attack|VIS, near-infrared (NIR), Thermal from long-wave infrared (LWIR), |
|[ROSE-YOUTU](http://rose1.ntu.edu.sg/datasets/faceLivenessDetection.asp)|2018|2D Replay, Print, Paper Mask|VIS|25|4225|
|~~MSU SiW-M~~（unavailable now）| 2019 | 2D Replay, Print & 3D Mask|VIS|
|[MSU SiW (Spoofing in the Wild)](http://cvlab.cse.msu.edu/spoof-in-the-wild-siw-face-anti-spoofing-database.html)| 2018 |2D Replay, Print|VIS|165|4620|
|[HKBU-MARs](http://rds.comp.hkbu.edu.hk/mars/)|2016|3D MASK|VIS|12|1008|
|[OULU-NPU](https://sites.google.com/site/oulunpudatabase/)|  2017 |2D Replay, Print|VIS|55|5940|
|[IDIAP Multispectral-Spoof Dataset](https://www.idiap.ch/dataset/msspoof)|2015|2D Print|VIS, Near-Infrared|21|4704 images|
|[IDIAP 3D Mask Attack Dataset (3DMAD)](https://www.idiap.ch/dataset/3dmad), [paper](https://ieeexplore.ieee.org/document/6712688)|2013|3D Mask|VIS, Depth|17|255|
|[IDIAP Replay Attack](https://www.idiap.ch/dataset/replayattack)|2012|2D Replay, Print|VIS|
|[CASIA MFSD (FASD)](http://www.cbsr.ia.ac.cn/english/FASDB_Agreement/Agreement.pdf)| 2012|2D Replay, Print|VIS|50|600||


# Learning-based methods
## Year 2026
|  Title  | Venue | Note |
|:--------|:--------:|:--------:|
|[FaceShield: Explainable Face Anti-Spoofing with Multimodal Large Language Models](https://ojs.aaai.org/index.php/AAAI/article/view/37945)|AAAI 2026|MLLM-based explainable FAS; outputs authenticity + attack type + reasoning + attack region, [Code](https://github.com/Why0912/FaceShield)|
|[PA-FAS: Towards Interpretable and Generalizable Multimodal Face Anti-Spoofing via Path-Augmented Reinforcement Learning](https://arxiv.org/abs/2511.17927)|AAAI 2026|MLLM + RL (path-augmented GRPO); multimodal; interpretable & domain-generalizable (Oral)|
|[HySpeFAS: A Hyperspectral Face Anti-Spoofing Dataset Based on Snapshot Compressive Imaging](https://doi.org/10.1109/TIFS.2025.3648158)|T-IFS 2026|New hyperspectral dataset; RGB/SSI/HSI (30 channels); 3D HiFi-mask / unknown attacks|
|[Fine-Grained Domain Alignment for Face Anti-Spoofing With Asymmetric Pseudo-Labels](https://doi.org/10.1109/TIFS.2026.3657032)|T-IFS 2026|Cross-domain adaptation; fine-grained alignment with asymmetric pseudo-labeling|

## Year 2025
|  Title  | Venue | Note |
|:--------|:--------:|:--------:|
|[FSFM: A Generalizable Face Security Foundation Model via Self-Supervised Facial Representation Learning](https://openaccess.thecvf.com/content/CVPR2025/papers/Wang_FSFM_A_Generalizable_Face_Security_Foundation_Model_via_Self-Supervised_Facial_CVPR_2025_paper.pdf)|CVPR 2025|FSFM; self-supervised ViT foundation model; cross-domain FAS + forgery detection, [Code](https://github.com/wolo-wolo/FSFM-CVPR25)|
|[Optimal Transport-Guided Source-Free Adaptation for Face Anti-Spoofing](https://arxiv.org/abs/2503.22984)|CVPR 2025|Source-free test-time domain adaptation; prototype model + optimal-transport adaptor|
|[Multi-View Slot Attention Using Paraphrased Texts for Face Anti-Spoofing](https://arxiv.org/abs/2509.06336)|ICCV 2025|MVP-FAS; CLIP/vision-language, multi-view slot attention for domain generalization, [Code](https://github.com/Elune001/MVP-FAS)|
|[Group-wise Scaling and Orthogonal Decomposition for Domain-Invariant Feature Extraction in Face Anti-Spoofing](https://arxiv.org/abs/2507.04006)|ICCV 2025|GD-FAS; domain generalization via feature orthogonal decomposition + group-wise scaling, [Code](https://github.com/SeungjinJung/GD-FAS)|
|[DADM: Dual Alignment of Domain and Modality for Face Anti-spoofing](https://arxiv.org/abs/2503.00429)|ICCV 2025|DADM; multi-modal (RGB/Depth/IR); dual domain + modality alignment, [Code](https://github.com/yjyddq/DADM)|
|[Rehearsal-Free and Efficient Continual Learning for Cross-Domain Face Anti-Spoofing](https://doi.org/10.1109/TPAMI.2025.3601053)|T-PAMI 2025|Rehearsal-free continual learning; central-difference conv adapter on ViT|
|[Reliable and Balanced Transfer Learning for Generalized Multimodal Face Anti-Spoofing](https://doi.org/10.1109/TPAMI.2025.3573785)|T-PAMI 2025|Multimodal (RGB/Depth/IR); reliable + modality-balanced transfer learning|
|[Fine-Grained Textual Guidance for Generalized Multi-Modal Face Anti-Spoofing](https://doi.org/10.1109/TIFS.2025.3613977)|T-IFS 2025|Multi-modal; fine-grained textual guidance (CLIP/vision-language); domain generalization|
|[ME-FAS: Multimodal Text Enhancement for Cross-Domain Face Anti-Spoofing](https://doi.org/10.1109/TIFS.2025.3571660)|T-IFS 2025|Cross-domain generalization; multimodal text/vision-language enhancement|
|[Hyperbolic Metric Learning for Generalizable Face Anti-Spoofing](https://doi.org/10.1109/TIFS.2025.3587917)|T-IFS 2025|Domain generalization; hyperbolic-space metric learning|
|[G2V2former: Graph Guided Video Vision Transformer for Face Anti-Spoofing](https://arxiv.org/abs/2408.07675)|T-IFS 2025|Video/temporal FAS; graph-guided spatiotemporal ViT (faces + landmarks)|
|[Confidence Aware Learning for Reliable Face Anti-Spoofing](https://arxiv.org/abs/2411.01263)|T-IFS 2025|Uncertainty-aware FAS; Gaussian + Mahalanobis confidence estimation|
|[Dual Consistency Regularization for Generalized Face Anti-Spoofing](https://doi.org/10.1109/TIFS.2025.3540659)|T-IFS 2025|Domain generalization; dual consistency regularization|
|[Cross-Optical Property Image Translation for Face Anti-Spoofing: From Visible to Polarization](https://doi.org/10.1109/TIFS.2024.3521323)|T-IFS 2025|Polarization modality; visible-to-polarization image translation|
|[Interpretable Face Anti-Spoofing: Enhancing Generalization with Multimodal Large Language Models](https://arxiv.org/abs/2501.01720)|AAAI 2025|I-FAS; FAS as interpretable VQA with MLLMs; cross-domain generalization|
|[SLIP: Spoof-Aware One-Class Face Anti-Spoofing with Language Image Pretraining](https://arxiv.org/abs/2503.19982)|AAAI 2025|SLIP; one-class FAS (live only); CLIP-style pretraining with spoof-aware prompts|
|[Mixture-of-Attack-Experts with Class Regularization for Unified Physical-Digital Face Attack Detection](https://arxiv.org/abs/2504.00458)|AAAI 2025|MoAE-CR; unified physical + digital attack detection; mixture-of-experts|
|[mmFAS: Multimodal Face Anti-Spoofing Using Multi-Level Alignment and Switch-Attention Fusion](https://arxiv.org/abs/2505.09484)|AAAI 2025|mmFAS; multimodal (RGB/Depth/IR); multi-level alignment + switch-attention fusion|
|[InstructFLIP: Exploring Unified Vision-Language Model for Face Anti-spoofing](https://arxiv.org/abs/2507.12060)|ACM MM 2025|InstructFLIP; instruction-tuned VLM; content-style decoupling + meta-domain generalization, [Code](https://github.com/kunkunlin1221/InstructFLIP)|

## Year 2024
|  Title  | Venue | Note |
|:--------|:--------:|:--------:|
|[CFPL-FAS: Class Free Prompt Learning for Generalizable Face Anti-spoofing](https://arxiv.org/abs/2403.14333)|CVPR 2024|CFPL; domain generalization; CLIP class-free prompt learning|
|[Gradient Alignment for Cross-Domain Face Anti-Spoofing](https://arxiv.org/abs/2402.18817)|CVPR 2024|GAC-FAS; domain generalization via sharpness-aware gradient alignment, [Code](https://github.com/Leminhbinh0209/CVPR24-FAS)|
|[Suppress and Rebalance: Towards Generalized Multi-Modal Face Anti-Spoofing](https://arxiv.org/abs/2402.19298)|CVPR 2024|MMDG; multi-modal (RGB/Depth/IR); U-Adapter + ReGrad; domain generalization, [Code](https://github.com/olgi9911/MMDG)|
|[Test-Time Domain Generalization for Face Anti-Spoofing](https://arxiv.org/abs/2403.19334)|CVPR 2024|TTDG; test-time style projection + diverse style shifts|
|[One-Class Face Anti-spoofing via Spoof Cue Map-Guided Feature Learning](https://openaccess.thecvf.com/content/CVPR2024/papers/Huang_One-Class_Face_Anti-spoofing_via_Spoof_Cue_Map-Guided_Feature_Learning_CVPR_2024_paper.pdf)|CVPR 2024|OC-SCMNet; one-class learning (live-only) with spoof cue map estimation|
|[DiffFAS: Face Anti-Spoofing via Generative Diffusion Models](https://arxiv.org/abs/2409.08572)|ECCV 2024|DiffFAS; diffusion-based cross-domain/cross-attack generation, [Code](https://github.com/murphytju/DiffFAS)|
|[TF-FAS: Twofold-Element Fine-Grained Semantic Guidance for Generalizable Face Anti-spoofing](https://www.ecva.net/papers/eccv_2024/papers_ECCV/papers/01098.pdf)|ECCV 2024|TF-FAS; CLIP fine-grained semantic prompts; domain generalization, [Code](https://github.com/xudongww/TF-FAS)|
|[Bottom-Up Domain Prompt Tuning for Generalized Face Anti-spoofing](https://link.springer.com/chapter/10.1007/978-3-031-72897-6_10)|ECCV 2024|BUDoPT; prompt tuning with adversarial domain-generalized prompts|
|[Towards Unified Representation of Invariant-Specific Features in Missing Modality Face Anti-spoofing](https://link.springer.com/chapter/10.1007/978-3-031-72670-5_6)|ECCV 2024|MMA-FAS; missing-modality; modality-disentangle adapters + LBP contrastive loss|
|[Source-Free Domain Adaptation With Domain Generalized Pretraining for Face Anti-Spoofing](https://ieeexplore.ieee.org/document/10449373/)|T-PAMI 2024|SDA-FAS; source-free DA with domain-generalized pretraining; PatchMix|
|[S-Adapter: Generalizing Vision Transformer for Face Anti-Spoofing With Statistical Tokens](https://arxiv.org/abs/2309.04038)|T-IFS 2024|S-Adapter; ViT adapter with statistical/Gram tokens; cross-domain generalization|
|[Surveillance Face Anti-Spoofing](https://arxiv.org/abs/2301.00975)|T-IFS 2024|CQIL; low-quality long-distance surveillance FAS; introduces SuHiFiMask dataset|
|[Cross-Scenario Unknown-Aware Face Anti-Spoofing With Evidential Semantic Consistency Learning](https://doi.org/10.1109/TIFS.2024.3356234)|T-IFS 2024|Open-set / unknown-attack; evidential deep learning + semantic consistency|
|[Dual Sampling Based Causal Intervention for Face Anti-Spoofing With Identity Debiasing](https://doi.org/10.1109/TIFS.2023.3326370)|T-IFS 2024|Causal intervention with dual sampling to remove identity bias; domain generalization|
|[MFAE: Masked Frequency Autoencoders for Domain Generalization Face Anti-Spoofing](https://doi.org/10.1109/TIFS.2024.3371266)|T-IFS 2024|MFAE; masked frequency-domain autoencoder (MAE-style); domain generalization|
|[IFAST: Weakly Supervised Interpretable Face Anti-Spoofing From Single-Shot Binocular NIR Images](https://doi.org/10.1109/TIFS.2024.3465930)|T-IFS 2024|IFAST; weakly supervised, interpretable; single-shot binocular NIR|
|[Category-Conditional Gradient Alignment for Domain Adaptive Face Anti-Spoofing](https://doi.org/10.1109/TIFS.2024.3486098)|T-IFS 2024|Category-conditional gradient alignment; cross-domain adaptation|
|[Multi-Domain Incremental Learning for Face Presentation Attack Detection](https://ojs.aaai.org/index.php/AAAI/article/view/28359)|AAAI 2024|MDIL; continual learning; ViT adaptive domain-specific experts|
|[Domain-Hallucinated Updating for Multi-Domain Face Anti-spoofing](https://ojs.aaai.org/index.php/AAAI/article/view/27992)|AAAI 2024|DHU; multi-domain FAS with domain hallucination for stable updating|
|[Unified Physical-Digital Face Attack Detection](https://arxiv.org/abs/2401.17699)|IJCAI 2024|UniAttackDetection; unified physical + digital; CLIP prompt learning; UniAttackData dataset|
|[FM-CLIP: Flexible Modal CLIP for Face Anti-Spoofing](https://dl.acm.org/doi/10.1145/3664647.3680856)|ACM MM 2024|FM-CLIP; multimodal flexible-modal; CLIP with cross-modal text guidance|
|[Style-conditional Prompt Token Learning for Generalizable Face Anti-spoofing](https://dl.acm.org/doi/10.1145/3664647.3680857)|ACM MM 2024|CLIP-based style-conditional prompt token learning; domain generalization|
|[Fine-Grained Prompt Learning for Face Anti-Spoofing](https://dl.acm.org/doi/abs/10.1145/3664647.3680855)|ACM MM 2024|FGPL; CLIP fine-grained prompt learning (domain-agnostic + domain-specific)|

## Year 2023
|  Title  | Venue | Note |
|:--------|:--------:|:--------:|
|[Instance-Aware Domain Generalization for Face Anti-Spoofing](https://arxiv.org/abs/2304.05640)|CVPR 2023|IADG; instance-level DG via asymmetric instance adaptive whitening (no domain labels), [Code](https://github.com/qianyuzqy/IADG)|
|[Rethinking Domain Generalization for Face Anti-spoofing: Separability and Alignment](https://openaccess.thecvf.com/content/CVPR2023/papers/Sun_Rethinking_Domain_Generalization_for_Face_Anti-Spoofing_Separability_and_Alignment_CVPR_2023_paper.pdf)|CVPR 2023|SA-FAS; domain separability + aligned live-to-spoof transition, [Code](https://github.com/sunyiyou/SAFAS)|
|[FLIP: Cross-domain Face Anti-spoofing with Language Guidance](https://openaccess.thecvf.com/content/ICCV2023/html/Srivatsan_FLIP_Cross-domain_Face_Anti-spoofing_with_Language_Guidance_ICCV_2023_paper.html)|ICCV 2023|FLIP; CLIP/vision-language ViT with language guidance; cross-domain, [Code](https://github.com/koushiksrivats/FLIP)|
|[Rehearsal-Free Domain Continual Face Anti-Spoofing: Generalize More and Forget Less](https://openaccess.thecvf.com/content/ICCV2023/html/Cai_Rehearsal-Free_Domain_Continual_Face_Anti-Spoofing_Generalize_More_and_Forget_Less_ICCV_2023_paper.html)|ICCV 2023|DCDCA; ViT dynamic central-difference conv adapter; rehearsal-free domain continual learning|
|[Towards Unsupervised Domain Generalization for Face Anti-Spoofing](https://openaccess.thecvf.com/content/ICCV2023/html/Liu_Towards_Unsupervised_Domain_Generalization_for_Face_Anti-Spoofing_ICCV_2023_paper.html)|ICCV 2023|Unsupervised DG from unlabeled multi-source data|
|[Deep Learning for Face Anti-Spoofing: A Survey](https://doi.org/10.1109/TPAMI.2022.3215850)|T-PAMI 2023|Comprehensive FAS survey; 2D/3D + digital attacks, multimodal, DG/DA|
|[Spoof Trace Disentanglement for Generic Face Anti-Spoofing](https://arxiv.org/abs/2012.05185)|T-PAMI 2023|Adversarial disentanglement of spoof traces; interpretable; improves generalization|
|[Domain Generalization for Face Anti-Spoofing via Negative Data Augmentation](https://doi.org/10.1109/TIFS.2023.3266138)|T-IFS 2023|NDA-FAS; DG trained with only synthesized negative samples, [Code](https://github.com/WeihangWANG/NDA-FAS)|
|[Consistency Regularization for Deep Face Anti-Spoofing](https://doi.org/10.1109/TIFS.2023.3235581)|T-IFS 2023|EPCR; embedding- + prediction-level consistency regularization (semi/self-supervised), [Code](https://github.com/clks-wzz/EPCR)|
|[FM-ViT: Flexible Modal Vision Transformers for Face Anti-Spoofing](https://doi.org/10.1109/TIFS.2023.3296330)|T-IFS 2023|FM-ViT; multimodal (RGB/Depth/IR) flexible-modal ViT; cross-modal transformer|
|[Attention-Aware Dual-Stream Network for Multimodal Face Anti-Spoofing](https://doi.org/10.1109/TIFS.2023.3293423)|T-IFS 2023|ADSNet; multimodal (RGB+Depth/IR); dual-stream attention fusion|
|[Polarized Image Translation From Nonpolarized Cameras for Multimodal Face Anti-Spoofing](https://doi.org/10.1109/TIFS.2023.3310348)|T-IFS 2023|Generates polarization cue from RGB via image translation; multimodal|
|[Unknown Face Presentation Attack Detection via Localized Learning of Multiple Kernels](https://doi.org/10.1109/TIFS.2023.3240841)|T-IFS 2023|Open-set / unknown-attack PAD; localized multiple-kernel learning|
|[Mask Attack Detection Using Vascular-Weighted Motion-Robust rPPG Signals](https://doi.org/10.1109/TIFS.2023.3293949)|T-IFS 2023|3D mask attacks; vascular-weighted motion-robust rPPG cues|
|[Cyclically Disentangled Feature Translation for Face Anti-spoofing](https://arxiv.org/abs/2212.03651)|AAAI 2023|CDFTN; domain adaptation via cyclic disentanglement of liveness vs. content|
|[Learning Polysemantic Spoof Trace: A Multi-Modal Disentanglement Network for Face Anti-spoofing](https://arxiv.org/abs/2212.03943)|AAAI 2023|Multimodal (RGB+Depth) disentanglement; polysemantic spoof traces|
|[Flow-Attention-based Spatio-Temporal Aggregation Network for 3D Mask Detection](https://arxiv.org/abs/2310.16569)|NeurIPS 2023|FASTEN; 3D mask PAD; RGB video + rPPG; flow-attention spatio-temporal aggregation, [Code](https://github.com/yuxincao22/FASTEN)|

## Year 2022
|  Title  | Venue | Note |
|:--------|:--------:|:--------:|
|[Learning Meta Pattern for Face Anti-Spoofing](https://arxiv.org/pdf/2110.06753.pdf)|TIFS 2022|MetaPattern, [Code](https://github.com/RizhaoCai/MetaPattern_FAS)|
|[Benchmarking Joint Face Spoofing and Forgery Detection with Visual and Physiological Cues](https://arxiv.org/abs/2208.05401)|ArXiv 2022|DeepFake and FAS | 
|[Adaptive Transformers for Robust Few-shot Cross-domain Face Anti-spoofing](https://arxiv.org/pdf/2203.12175.pdf)|ECCV 2022| - |
|[Face Anti-Spoofing Using Transformers with Relation-Aware Mechanism](https://ieeexplore.ieee.org/document/9817442)|T-BIOM 2022||
|[Domain Generalization via Shuffled Style Assembly for Face Anti-Spoofing](https://arxiv.org/pdf/2204.12685.pdf)|Preprint 2022|Probabilistic Modeling|
|[Robust Face Anti-Spoofing with Dual Probabilistic Modeling](https://arxiv.org/pdf/2203.05340.pdf)|CVPR 2022|Style transfer|
|[Feature Generation and Hypothesis Verification for Reliable Face Anti-Spoofing](https://arxiv.org/pdf/2112.14894.pdf)|AAAI 2022|Hypothesis Verification?|
|[MA-ViT: Modality-Agnostic Vision Transformers for Face Anti-Spoofing](https://arxiv.org/abs/2304.07549)|IJCAI 2022|MA-ViT; flexible single-/multi-modal single-branch ViT; modal-disentangle + cross-modal attention|
|[Adaptive Mixture of Experts Learning for Generalizable Face Anti-Spoofing](https://arxiv.org/abs/2207.09868)|ACM MM 2022|AMEL; domain generalization via domain-specific experts + dynamic aggregation|
|[Energy-Based Domain Generalization for Face Anti-Spoofing](https://dl.acm.org/doi/10.1145/3503161.3548073)|ACM MM 2022|Energy-based domain generalization|
|[Multi-domain Learning for Updating Face Anti-spoofing Models](https://arxiv.org/abs/2208.11148)|ECCV 2022|MD-FAS; spoof region estimator to update models without forgetting; SiW-Mv2 benchmark, [Code](https://github.com/chelsea234/multi-domain-learning-fas)|
|[Generative Domain Adaptation for Face Anti-Spoofing](https://arxiv.org/abs/2207.10015)|ECCV 2022|GDA; unsupervised DA by stylizing target to source with consistency constraints|
|[Source-Free Domain Adaptation with Contrastive Domain Alignment and Self-supervised Exploration for Face Anti-spoofing](https://link.springer.com/chapter/10.1007/978-3-031-19775-8_30)|ECCV 2022|SDA-FAS; source-free DA; contrastive domain alignment + self-supervised exploration, [Code](https://github.com/YuchenLiu98/ECCV2022-SDA-FAS)|
|[Learning Multi-Granularity Temporal Characteristics for Face Anti-Spoofing](https://doi.org/10.1109/TIFS.2022.3158062)|T-IFS 2022|Video/temporal FAS; multi-granularity temporal modeling|
|[Conv-MLP: A Convolution and MLP Mixed Model for Multimodal Face Anti-Spoofing](https://doi.org/10.1109/TIFS.2022.3183398)|T-IFS 2022|Conv-MLP; multimodal (RGB+Depth+IR); convolution + MLP-mixer hybrid|
|[Salience-Aware Face Presentation Attack Detection via Deep Reinforcement Learning](https://doi.org/10.1109/TIFS.2021.3135748)|T-IFS 2022|DRL to locate salient discriminative regions/patches|
|[One-Class Knowledge Distillation for Face Presentation Attack Detection](https://doi.org/10.1109/TIFS.2022.3178240)|T-IFS 2022|One-class / anomaly PAD; knowledge distillation; robust to unknown attacks|
|[Learning Temporal Similarity of Remote Photoplethysmography for Fast 3D Mask Face Presentation Attack Detection](https://doi.org/10.1109/TIFS.2022.3197335)|T-IFS 2022|3D mask attacks; rPPG temporal-similarity learning|

## Year 2021
|  Title  | Venue | Note |
|:--------|:--------:|:--------:|
|[Asymmetric Modality Translation For Face Presentation Attack Detection](https://arxiv.org/abs/2110.09108)|TMM 2021| |
|[Consistency Regularization for Deep Face Anti-Spoofing](https://arxiv.org/pdf/2111.12320.pdf)|ArXiv 2021| |
|[Dual-Branch Meta-learning Network with Distribution Alignment for Face Anti-spoofing](https://ieeexplore.ieee.org/document/9646915/keywords#keywords)|TIFS 2021| [Code](https://github.com/taylover-pei/DBMNet-TIFS)|
|[Dual Spoof Disentanglement Generation for Face Anti-spoofing with Depth Uncertainty Learning](https://arxiv.org/pdf/2112.00568.pdf)|ArXiv 2021||
|[Unified Detection of Digital and Physical Face Attacks](http://cvlab.cse.msu.edu/pdfs/deb_liu_jain_arxiv2021_unified.pdf)|ArXiv 2021||
|[Attention-Based Spatial-Temporal Multi-Scale Network for Face Anti-Spoofing](https://ieeexplore.ieee.org/iel7/8423754/9467110/09382387.pdf)|T-BIOM 2021||
|[Self-Domain Adaptation for Face Anti-Spoofing](https://arxiv.org/abs/2102.12129)|AAAI 2021|DA|
|[Detection and Continual Learning of Novel Face Presentation Attacks](https://arxiv.org/abs/2108.12081)|ICCV 2021|Continual Learning; New attack types|
|[Deep Learning for Face Anti-Spoofing: A Survey](https://arxiv.org/pdf/2106.14948.pdf)|ArXiv 2021|Survey; Under review|
|[Meta-teacher for Face Anti-Spoofing](https://ieeexplore.ieee.org/document/9462562)|T-PAMI 2021|MetaTeacher|
|[Dual-Cross Central Difference Network for Face Anti-Spoofing](https://arxiv.org/pdf/2105.01290.pdf)|IJCAI 2021|Based on CDCN|
|[Learning One Class Representations for Face Presentation Attack Detection Using Multi-Channel Convolutional Neural Networks](https://arxiv.org/abs/2007.11457)|T-IFS 2021| Multi-modality |
|[Face Anti-Spoofing via Adversarial Cross-Modality Translation](http://www.cbsr.ia.ac.cn/users/jwan/papers/TIFS2021-spoof.pdf)|T-IFS 2021| Multi-modality |
|[Cross Modal Focal Loss for RGBD Face Anti-Spoofing](https://arxiv.org/abs/2103.00948#:~:text=Automatic%20methods%20for%20detecting%20presentation,in%20generalizing%20to%20unseen%20attacks.)|CVPR 2021| Multi-modality |
|[Data Fusion based Two-stage Cascade Framework for Multi-Modality Face Anti-Spoofing](https://www.researchgate.net/publication/349901486_Data_Fusion_based_Two-stage_Cascade_Framework_for_Multi-Modality_Face_Anti-Spoofing)|T-DSC 2021| Multi-modality  |
|[Improved Detection of Face Presentation Attacks Using Image Decomposition](https://arxiv.org/pdf/2103.12201.pdf)| ArXiv 2021| Albedo  |
|[Contrastive Context-Aware Learning for 3D High-Fidelity Mask Face Presentation Attack Detection](https://arxiv.org/abs/2104.06148)|ArXiv 2021|CASIA-SURF 3DHiFi Dataset |
|[TransRPPG: Remote Photoplethysmography Transformer for 3D Mask Face Presentation Attack Detection](https://arxiv.org/abs/2104.07419)|ArXiv 2021|rPPG |
|[Structure Destruction and Content Combination for Face Anti-Spoofing](https://arxiv.org/pdf/2107.10628.pdf)|IJCB 2021| |
|[Adaptive Normalized Representation Learning for Generalizable Face Anti-Spoofing](https://arxiv.org/pdf/2108.02667.pdf)|ACM MM 2021| |
## Year 2020
|  Title  | Venue | Note |
|:--------|:--------:|:--------:|
|[Revisiting Pixel-Wise Supervision for Face Anti-Spoofing](https://www.researchgate.net/publication/346303022_Revisiting_Pixel-Wise_Supervision_for_Face_Anti-Spoofing)|T-BIOM 2020|-|
|[Cross-domain face presentation attack detection via multi-domain disentangled representation learning](https://arxiv.org/abs/2004.01959)|CVPR 2020|DG, Disentangledment learning|
|[Rethinking Shape From Shading for Spoofing Detection](https://ieeexplore.ieee.org/document/9286821)|T-IP 2020|-|
|[Camera Invariant Feature Learning for Generalized Face Anti-spoofing](https://arxiv.org/pdf/2101.10075.pdf)|T-IFS 2020| Domain generalization |
|[NAS-FAS: Static-Dynamic Central Difference Network Search for Face Anti-Spoofing](https://arxiv.org/abs/2011.02062)| T-PAMI 2020|NAS; Domain generalization;|
|[3DPC-Net: 3D Point Cloud Network for Face Anti-spoofing](http://www.cbsr.ia.ac.cn/users/jwan/papers/IJB2020-3DPCNet.pdf)|IJCB 2020|Pseudo Point Cloud|
|[DRL-FAS: A Novel Framework Based on Deep Reinforcement Learning for Face Anti-Spoofing](https://arxiv.org/pdf/2009.07529.pdf)| T-IFS 2020|Reinforcement learning|
|[Face spoofing detection based on local ternary label supervision in fully convolutional networks](https://ieeexplore.ieee.org/document/9056824)| T-IFS 2020|Using a map of Ones is the same as a depth map!|
|[Face Anti-Spoofing via Disentangled Representation Learning](https://arxiv.org/pdf/2008.08250.pdf)|ECCV 2020|Disentanglement learning|
|[On Disentangling Spoof Trace for Generic Face Anti-Spoofing](https://arxiv.org/pdf/2007.09273.pdf)|ECCV 2020|Similar idea as the DeSpoofing method|
|[CelebA-Spoof: Large-Scale Face Anti-Spoofing Dataset with Rich Annotations](https://github.com/Davidzhangyuanhan/CelebA-Spoof)|ECCV 2020|Contribute a dataset|
|[Face Anti-Spoofing with Human Material Perception](https://www.researchgate.net/publication/342733508_Face_Anti-Spoofing_with_Human_Material_Perception)|ECCV 2020|2D Attacks|
|[Leveraging Shape, Reflectance and Albedo from Shading for Face Presentation Attack Detection](https://www.researchgate.net/publication/340671825_Leveraging_Shape_Reflectance_and_Albedo_from_Shading_for_Face_Presentation_Attack_Detection)| T-IFS 2020|SfS for albedo, reflectance, and depth map|
|[Deep Spatial Gradient and Temporal Depth Learning for Face Anti-spoofing](https://openaccess.thecvf.com/content_CVPR_2020/papers/Wang_Deep_Spatial_Gradient_and_Temporal_Depth_Learning_for_Face_Anti-Spoofing_CVPR_2020_paper.pdf)|CVPR 2020|RGB, Depth-contrastive loss, [Code](https://github.com/clks-wzz/FAS-SGTD)|
|[Searching Central Difference Convolutional Networks for Face Anti-Spoofing](https://openaccess.thecvf.com/content_CVPR_2020/papers/Yu_Searching_Central_Difference_Convolutional_Networks_for_Face_Anti-Spoofing_CVPR_2020_paper.pdf)|CVPR 2020|RGB, NAS, CDCN, [Code](https://github.com/ZitongYu/CDCN)|
|[Regularized Fine-grained Meta Face Anti-spoofing](https://arxiv.org/abs/1911.10771)|AAAI 2020|RGB, 2D Attack, Meta Learning, [Code](https://github.com/rshaojimmy/AAAI2020-RFMetaFAS); Meta learning|
|[Unsupervised Adversarial Domain Adaptation for Cross-Domain Face Presentation Attack Detection](https://www.researchgate.net/publication/342185474_Unsupervised_Adversarial_Domain_Adaptation_for_Cross-Domain_Face_Presentation_Attack_Detection)|T-IFS 2020|Domain adaptation|
|[Face Anti-Spoofing with Deep Neural Network Distillation](https://www.researchgate.net/publication/342115009_Face_Anti-Spoofing_with_Deep_Neural_Network_Distillation)|IEEE Journal of Selected Topics in Signal Processing 2020|Domain knowledge distillation|
|[Single-Side Domain Generalization for Face Anti-Spoofing](https://openaccess.thecvf.com/content_CVPR_2020/papers/Jia_Single-Side_Domain_Generalization_for_Face_Anti-Spoofing_CVPR_2020_paper.pdf)|CVPR 2020|RGB, [Code](https://github.com/taylover-pei/SSDG-CVPR2020)|
|[Domain Agnostic Feature Learning for Image and Video Based Face Anti-Spooﬁng](https://arxiv.org/pdf/1912.07124.pdf)|CVPRW 2020|RGB, 2D  Attack|
|[Learning Generalized Spoof Cues for Face Anti-spoofing](https://arxiv.org/abs/2005.03922)|ArXiv 2020| RGB, 2D Attack, [Code](https://github.com/vis-var/lgsc-for-fas);|
|[Learning Meta Model for Zero- and Few-shot Face Anti-spoofing](https://arxiv.org/abs/1904.12490)|AAAI 2020|RGB, 2D Presentation Attack, Meta Learning, [Code](https://github.com/qyxqyx/AIM_FAS); few-shot|
|[Learning to Learn Face-PAD: a lifelong learning approach](https://www.researchgate.net/publication/348324514_Learning_to_Learn_Face-PAD_a_lifelong_learning_approach)|IJCB 2020|Life-long learning|
|[Learning Generalizable and Identity-Discriminative Representations for Face Anti-Spoofing](https://dl.acm.org/doi/abs/10.1145/3402446)|ACM TIST 2020|DA|


## Year 2019-2018
|  Title  | Venue | Note |
|:--------|:--------:|:--------:|
|[Attention-Based Two-Stream Convolutional Networks for Face Spoofing Detection](https://ieeexplore.ieee.org/document/8737949)| T-IFS 2019|RGB, 2D Attack|
|[Biometric Face Presentation Attack Detection with Multi-Channel Convolutional Neural Network](http://publications.idiap.ch/downloads/papers/2019/George_TIFS_2019.pdf)|T-IFS 2019|RGB+IR+Depth, 2D Presentation Attack|
|[Face Anti-Spoofing: Model Matters, So Does Data](http://www.cbsr.ia.ac.cn/users/jwan/papers/CVPR2019-spoofing.pdf)|CVPR 2019|RGB, 2D Attack,data augmentation|
|[A Dataset and Benchmark for Large-scale Multi-modal Face Anti-spoofing](https://yuan-gao.net/pdf/CVPR2019%20-%20antispoofing.pdf)|CVPR 2019|RGB+IR+Depth, 2D Attack|
|[Deep Tree Learning for Zero-shot Face Anti-Spoofing](http://cvlab.cse.msu.edu/pdfs/Liu_Stehouwer_Jourabloo_Liu_CVPR2019.pdf)|CVPR 2019|RGB, 2D Attack|
|[Deep Anomaly Detection for Generalized Face Anti Spoofing](http://openaccess.thecvf.com/content_CVPRW_2019/papers/CFS/Perez-Cabo_Deep_Anomaly_Detection_for_Generalized_Face_Anti-Spoofing_CVPRW_2019_paper.pdf)|CVPRW 2019|RGB, 2D Attack|
|[Joint Discriminative Learning of Deep Dynamic Textures for 3D Mask Face Anti-Spoofing](https://ieeexplore.ieee.org.remotexs.ntu.edu.sg/document/8453011)|T-IFS 2019|VIS, 3D Attack|
|[Multi-adversarial Discriminative Deep Domain Generalization for Face Presentation Attack Detection](http://openaccess.thecvf.com/content_CVPR_2019/papers/Shao_Multi-Adversarial_Discriminative_Deep_Domain_Generalization_for_Face_Presentation_Attack_Detection_CVPR_2019_paper.pdf)|CVPR 2019|RGB, 2D Attack,|
|[Exploiting temporal and depth information for multi-frame face anti-spoofing](https://arxiv.org/abs/1811.05118)|ArXiv 2018|RGB,  2D Presentation Attack, Multi-frame |
|[Face De-Spoofing: Anti-Spoofing via Noise Modeling](https://arxiv.org/abs/1807.09968)|ECCV 2018|RGB, 2D Attack, pseudo depth, [Code](https://github.com/yaojieliu/ECCV2018-FaceDeSpoofing)|
|[Learning Deep Models for Face Anti-Spoofing: Binary or Auxiliary Supervision](http://cvlab.cse.msu.edu/pdfs/Liu_Jourabloo_Liu_CVPR2018.pdf)|CVPR 2018|RGB, 2D Attack, pseudo depth+rPPG|
|[Learning generalized deep feature representation for face anti-spoofing](https://rose.ntu.edu.sg/Publications/Documents/Face%20Spoofing%20Detection/Learning%20Generalized%20Deep%20Feature%20Representation%20for%20Face%20Anti-Spoofing.pdf)| T-IFS 2018|RGB, 2D Presentation Attack,|
|[Unsupervised domain adaptation for face anti-spoofing](https://ieeexplore.ieee.org/document/8279564)| T-IFS 2018|RGB, 2D Attack, unsupervised domain adaptation|


## Before 2018
|  Title  | Venue | Note|
|:--------|:--------:|:--------:|
|[Face Anti-Spoofing Using Patch and Depth-Based CNNs](http://cvlab.cse.msu.edu/pdfs/FaceAntiSpoofingUsingPatchandDepthBasedCNNs.pdf)|IJCB 2017|RGB, 2D Attack, pseudo depth|
|[Face Spoofing Detection Using Colour Texture Analysis](https://www.researchgate.net/publication/301571761_Face_Spoofing_Detection_Using_Colour_Texture_Analysis)| T-IFS 2016|RGB, 2D Attack, Color LBP|
|[Spoofing Face Recognition With 3D Masks](https://www.researchgate.net/publication/262605045_Spoofing_Face_Recognition_With_3D_Masks)| T-IFS 2014|3D Mask|
|[Face Spoofing Detection Through Visual Codebooks of Spectral Temporal Cubes](https://www.researchgate.net/publication/281054869_Face_Spoofing_Detection_Through_Visual_Codebooks_of_Spectral_Temporal_Cubes)|IEEE TIP 2015|RGB, 2D Attack,|
|[Person-Specific Face Anti-Spoofing With Subject Domain Adaptation](https://ieeexplore.ieee.org/document/7041231)| T-IFS 2015|RGB, 2D Attack, Person-specific|
|[Face Spoof Detection with Image Distortion Analysis](http://vipl.ict.ac.cn/uploadfile/upload/2017020711092984.pdf)| T-IFS 2015|RGB, 2D Attack, IDA|
|[Using Visual Rhythms for Detecting Video-Based Facial Spoof Attacks](https://www.researchgate.net/publication/275102589_Using_Visual_Rhythms_for_Detecting_Video-Based_Facial_Spoof_Attacks)|T-IFS 2015|VIS, 2D Replay|
|[Face spoofing detection from single images using texture and local shape analysis](https://ieeexplore.ieee.org/document/6117510)|IJCB 2011|RGB, 2D Presentation Attack, LBP|




# System / Mobile Applications
|  Title  | Venue | Note |
|:--------|:--------:|:--------:|
|[Beyond the Pixel World: A Novel Acoustic-Based Face Anti-Spoofing System for Smartphones](https://doi.org/10.1109/TIFS.2022.3202115)|T-IFS 2022|Active acoustic sensing (echo) on smartphones; non-visual modality|
|[Efficient Face Spoofing Detection With Flash](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=9419913)|T-BIOM|Flash|
|[RFace: Anti-Spoofing Facial Authentication Using COTS RFID](https://www4.comp.polyu.edu.hk/~csyqzheng/papers/RFace-INFOCOM21.pdf)|INFOCOM 2021|RFID; privacy preserved|
|[FaceRevelio: A Face Liveness Detection System for Smartphones with a Single Front Camera](https://habiba-farrukh.github.io/files/FaceRevelio.pdf)|MobiCom 2020|RGB+Flashing|
|[EchoPrint: Two-factor Authentication using Acoustics and Vision on Smartphones](https://www.researchgate.net/publication/328325417_EchoPrint_Two-factor_Authentication_using_Acoustics_and_Vision_on_Smartphones)|MobiCom 2018|Acoustic+Vision|
|[Face Flashing: a Secure Liveness Detection Protocol based on Light Reflections](https://arxiv.org/pdf/1801.01949.pdf)|NDSS 2018|RGB+Flashing|
|[Light Field-Based Face Presentation Attack Detection: Reviewing, Benchmarking and One Step Further](https://ieeexplore.ieee.org/document/8271987)| T-IFS 2018|Light Filed-Based|
|[rtCaptcha: A Real-Time CAPTCHA Based Liveness Detection System](https://pdfs.semanticscholar.org/1fb3/99bf4122b5b25ae7784ca73f9b1be6a91cde.pdf)|NDSS 2018|RGB, Captcha|
|[Face Liveness Detection Using a Flash Against 2D Spoofing Attack](http://www.hebmlc.org/UploadFiles/20171014235219706.pdf)| T-IFS 2017|RGB+Flashing, 2D Attack|
|[Your face your heart: Secure mobile face authentication with photoplethysmograms](https://web.asu.edu/sites/default/files/cnsg/files/c38.pdf)|INFORCOM 2017|RGB, rPPG|
|[Seeing your face is not enough: An inertial sensor-based liveness detection for face authentication](https://ink.library.smu.edu.sg/cgi/viewcontent.cgi?article=3884&context=sis_research)|ACM CCS 2015|RGB+Accelerometer|
|[Sensor-assisted facial recognition: an enhanced biometric authentication system for smartphones](https://dl.acm.org/doi/10.1145/2594368.2594373)|Mobisys 2014|RGB+ Sensors|


# Attack
|  Title  | Venue | Note |
|:--------|:--------:|:--------:|
|[IlluAttack: Generating Adversarial Examples via Illumination Transformation for Face Anti-Spoofing](https://doi.org/10.1109/TIFS.2025.3643157)|T-IFS 2026|Physically-realizable illumination-transformation adversarial examples against FAS/liveness|
|[Adversarial Attacks on Both Face Recognition and Face Anti-spoofing Models](https://www.ijcai.org/proceedings/2025/278)|IJCAI 2025|RMA; black-box adversarial attack jointly targeting FR + FAS|
|[Light Can Hack Your Face! Black-box Backdoor Attack on Face Recognition Systems](https://arxiv.org/abs/2009.06996)|ArXiv 2020|Face Recognition Attack|
|[Virtual U: Defeating Face Liveness Detection by Building Virtual Models from Your Public Photos](https://www.usenix.org/system/files/conference/usenixsecurity16/sec16_paper_xu.pdf)|USENIX SS 2018|VR tech for spoofing|


# Notes
+ T-PAMI: [IEEE Transactions on Pattern Analysis and Machine Intelligence](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=34)
+ T-IFS: [IEEE Transactions on Information Forensics and Security](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=10206)
+ T-IP: [IEEE Transactions on Image Processing](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=83)
+ T-DSC: [IEEE Transactions on Cognitive and Developmental Systems](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=7274989)  
+ T-BIOM [IEEE Transactions on Biometrics, Behavior, and Identity Science](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=8423754)
+ CVPR: [Conference on Computer Vision and Pattern Recognition](https://ieeexplore.ieee.org/xpl/conhome/1000147/all-proceedings)
+ ICCV: [International Conference on Computer Vision](https://ieeexplore.ieee.org/xpl/conhome/1000149/all-proceedings)
+ ECCV: [European Conference on Computer Vision (Springer)](https://link.springer.com/conference/eccv)
+ USENIX SS: Proceedings of USENIX Security Symposium 
+ NDSS: The Network and Distributed System Security Symposium
+ Infocom: IEEE International Conference on Computer Communications
+ MobiCom: International Conference On Mobile Computing And Networking
+ CCS: ACM Computer and Communications Security Conference
+ MobiSys: International Conference on Mobile Systems, Applications, and Services
+ IJCB: International Joint Conference on Biometrics 
+ AAAI: [AAAI Conference on Artificial Intelligence](https://aaai.org/conference/aaai/)
+ IJCAI: [International Joint Conference on Artificial Intelligence](https://www.ijcai.org/)
+ NeurIPS: [Conference on Neural Information Processing Systems](https://neurips.cc/)
+ ICLR: [International Conference on Learning Representations](https://iclr.cc/)
+ ACM MM: [ACM International Conference on Multimedia](https://dl.acm.org/conference/mm)
+ ArXiv: Papers that only appear in ArXiv are regarded not published, but they are collected here for reference only.


---
If you feel useful about this repo, we would be happy you are also interested in our works and use our papers your work's reference.

  @article{cai2020drlfas,
      title={DRL-FAS: A Novel Framework Based on Deep Reinforcement Learning for Face Anti-Spoofing},   
      author={Cai, Rizhao and Li, Haoliang and Wang, Shiqi and Chen, Changsheng and Kot, Alex C},   
      journal={IEEE Transactions on Information Forensics and Security},   
      volume={16},  
      pages={937--951},  
      year={2020},   
      publisher={IEEE},
      doi={10.1109/TIFS.2020.3026553}
  
  @ARTICLE{cai2022MP,
  author={Cai, Rizhao and Li, Zhi and Wan, Renjie and Li, Haoliang and Hu, Yongjian and Kot, Alex C.},
  journal={IEEE Transactions on Information Forensics and Security}, 
  title={Learning Meta Pattern for Face Anti-Spoofing}, 
  year={2022},
  volume={},
  number={},
  pages={1-1},
  doi={10.1109/TIFS.2022.3158551}}
  }


@article{li2022one,
  title={One-Class Knowledge Distillation for Face Presentation Attack Detection},
  author={Li, Zhi and Cai, Rizhao and Li, Haoliang and Lam, Kwok-Yan and Hu, Yongjian and Kot, Alex C},
  journal={IEEE Transactions on Information Forensics and Security},
  year={2022},
  publisher={IEEE}
}


