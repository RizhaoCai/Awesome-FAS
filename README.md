# Awesome Face Authentication Security

A curated list of **Face Authentication Security** resources — defending face recognition / authentication systems against attacks. Inspired by [Awesome-deep-vision](https://github.com/kjw0612/awesome-deep-vision), [Awesome-adversarial-machine-learning](https://github.com/yenchenlin/awesome-adversarial-machine-learning), [Awesome-deep-learning-papers](https://github.com/terryum/awesome-deep-learning-papers), [Awesome-NAS](https://github.com/D-X-Y/Awesome-NAS) and [Awesome-Pruning](https://github.com/he-y/Awesome-Pruning).

Please feel free to open a pull request or issue to add papers.

## Attack taxonomy

Attacks against a face authentication system fall into two complementary categories by **where they enter the system**:

| | Type 1 — Presentation Attack | Type 2 — Digital / Injection Attack |
|:--|:--|:--|
| **Definition** | An artefact *presented to the capture sensor* (ISO/IEC 30107) | Forged media *injected into the pipeline*, bypassing the sensor |
| **Examples** | Print, replay, 3D mask | Deepfake (face-swap, reenactment, attribute edit, face synthesis) |
| **Collection** | 📄 **[Face Anti-Spoofing / PAD](./Face-Anti-Spoofing.md)** | 🎭 **[Deepfake / Face Forgery Detection](./Deepfake-Detection.md)** |

> Note: "Presentation Attack" and its detection (PAD) are standardized in **ISO/IEC 30107**. The complementary "injection attack" / Type-1-vs-Type-2 framing is industry-driven (FIDO and biometric vendors) and still being standardized; here it is used as an organizing label.

## Collections

- 📄 **[Face Anti-Spoofing / Presentation Attack Detection](./Face-Anti-Spoofing.md)** (Type 1) — databases, learning-based methods (Before 2018 → 2026), mobile/system liveness, and attacks.
- 🎭 **[Deepfake / Face Forgery Detection](./Deepfake-Detection.md)** (Type 2) — deepfake datasets, CCF-A detection methods (2022 → 2026), and surveys.
- 📊 **[Benchmarks](./Benchmarks/README.md)** — cross-method performance under intra- and cross-dataset protocols ([CASIA ↔ REPLAY-ATTACK](./Benchmarks/CASIA%2BREPLAY-ATTACK.md)).

# Unified (Type 1 + Type 2) Attack Detection

Methods that detect **both** physical presentation and digital/deepfake attacks within a single framework — the bridge between the two collections.

|  Title  | Venue | Note |
|:--------|:--------:|:--------:|
|[FSFM: A Generalizable Face Security Foundation Model via Self-Supervised Facial Representation Learning](https://openaccess.thecvf.com/content/CVPR2025/papers/Wang_FSFM_A_Generalizable_Face_Security_Foundation_Model_via_Self-Supervised_Facial_CVPR_2025_paper.pdf)|CVPR 2025|FSFM; self-supervised ViT foundation model serving both anti-spoofing and forgery detection, [Code](https://github.com/wolo-wolo/FSFM-CVPR25)|
|[Mixture-of-Attack-Experts with Class Regularization for Unified Physical-Digital Face Attack Detection](https://arxiv.org/abs/2504.00458)|AAAI 2025|MoAE-CR; unified physical + digital attack detection; mixture-of-experts + class regularization|
|[Unified Physical-Digital Face Attack Detection](https://arxiv.org/abs/2401.17699)|IJCAI 2024|UniAttackDetection; CLIP prompt learning; introduces the UniAttackData dataset|
|[Benchmarking Joint Face Spoofing and Forgery Detection with Visual and Physiological Cues](https://arxiv.org/abs/2208.05401)|ArXiv 2022|Joint FAS + deepfake benchmark using visual and rPPG physiological cues|
|[Unified Detection of Digital and Physical Face Attacks](http://cvlab.cse.msu.edu/pdfs/deb_liu_jain_arxiv2021_unified.pdf)|ArXiv 2021|Early unified treatment of digital (deepfake/adversarial) and physical (spoof) attacks|

# Notes

Shared venue glossary used across all collections.

+ T-PAMI: [IEEE Transactions on Pattern Analysis and Machine Intelligence](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=34)
+ T-IFS: [IEEE Transactions on Information Forensics and Security](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=10206)
+ T-IP: [IEEE Transactions on Image Processing](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=83)
+ T-DSC: [IEEE Transactions on Cognitive and Developmental Systems](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=7274989)
+ T-BIOM: [IEEE Transactions on Biometrics, Behavior, and Identity Science](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=8423754)
+ CVPR: [Conference on Computer Vision and Pattern Recognition](https://ieeexplore.ieee.org/xpl/conhome/1000147/all-proceedings)
+ ICCV: [International Conference on Computer Vision](https://ieeexplore.ieee.org/xpl/conhome/1000149/all-proceedings)
+ ECCV: [European Conference on Computer Vision (Springer)](https://link.springer.com/conference/eccv)
+ AAAI: [AAAI Conference on Artificial Intelligence](https://aaai.org/conference/aaai/)
+ IJCAI: [International Joint Conference on Artificial Intelligence](https://www.ijcai.org/)
+ NeurIPS: [Conference on Neural Information Processing Systems](https://neurips.cc/)
+ ICLR: [International Conference on Learning Representations](https://iclr.cc/)
+ ACM MM: [ACM International Conference on Multimedia](https://dl.acm.org/conference/mm)
+ ACM CSUR: ACM Computing Surveys
+ CVIU: Computer Vision and Image Understanding · Information Fusion: Elsevier journal
+ USENIX SS: USENIX Security Symposium · NDSS: Network and Distributed System Security Symposium
+ Infocom: IEEE International Conference on Computer Communications
+ MobiCom: International Conference on Mobile Computing and Networking
+ CCS: ACM Conference on Computer and Communications Security
+ MobiSys: International Conference on Mobile Systems, Applications, and Services
+ IJCB: International Joint Conference on Biometrics
+ ISO/IEC 30107: International standard on biometric presentation attack detection
+ ArXiv: Papers that only appear in ArXiv are regarded not published, but they are collected here for reference only.

---
If you find this repo useful, we would be happy if you are also interested in our works and cite them in your work.

```bibtex
@article{cai2020drlfas,
  title={DRL-FAS: A Novel Framework Based on Deep Reinforcement Learning for Face Anti-Spoofing},
  author={Cai, Rizhao and Li, Haoliang and Wang, Shiqi and Chen, Changsheng and Kot, Alex C},
  journal={IEEE Transactions on Information Forensics and Security},
  volume={16}, pages={937--951}, year={2020}, publisher={IEEE},
  doi={10.1109/TIFS.2020.3026553}
}

@article{cai2022MP,
  title={Learning Meta Pattern for Face Anti-Spoofing},
  author={Cai, Rizhao and Li, Zhi and Wan, Renjie and Li, Haoliang and Hu, Yongjian and Kot, Alex C},
  journal={IEEE Transactions on Information Forensics and Security},
  year={2022}, publisher={IEEE},
  doi={10.1109/TIFS.2022.3158551}
}

@article{li2022one,
  title={One-Class Knowledge Distillation for Face Presentation Attack Detection},
  author={Li, Zhi and Cai, Rizhao and Li, Haoliang and Lam, Kwok-Yan and Hu, Yongjian and Kot, Alex C},
  journal={IEEE Transactions on Information Forensics and Security},
  year={2022}, publisher={IEEE}
}
```
