# Awesome-FAS (Face Anti-Spoofing)

A curated list of Face Anti-Spoofing and related resources. This is inspired by [awesome-deep-vision](https://github.com/kjw0612/awesome-deep-vision), [awesome-adversarial-machine-learning](https://github.com/yenchenlin/awesome-adversarial-machine-learning), [awesome-deep-learning-papers](https://github.com/terryum/awesome-deep-learning-papers), [Awesome-NAS](https://github.com/D-X-Y/Awesome-NAS) and [Awesome-Pruing](https://github.com/he-y/Awesome-Pruning)


Please feel free to pull requests or open an issue to add papers.

## Databases
|  Name  | Publisher | Release year | Attack | 
|:--------|:--------:|:--------:|:--------:|
|[CASIA SURF](https://www.researchgate.net/publication/329388462_CASIA-SURF_A_Dataset_and_Benchmark_for_Large-scale_Multi-modal_Face_Anti-spoofing)|CASIA CBSR|2019|Replay (2D, IR data)|
|[OULU-NPU](https://sites.google.com/site/oulunpudatabase/)| OULU University, Finland | 2018|Replay, Print(2D)|
|[SiW (Spoofing in the Wild)](http://cvlab.cse.msu.edu/spoof-in-the-wild-siw-face-anti-spoofing-database.html)| Michigan State University| 2018 |2D: Replay, Print|
|[HKBU-MARs](http://rds.comp.hkbu.edu.hk/mars/)|HKBU|2018|3D MASK|
|[IDIAP 3D Mask Attack Dataset](https://www.idiap.ch/dataset/3dmad)|Idiap Research Institute|2013|3D Mask|
|[IDIAP Replay Attack](https://www.idiap.ch/dataset/replayattack)|Idiap Research Institute|2012|Replay, Print(2D)|
|[CASIA FASD](http://www.cbsr.ia.ac.cn/english/FASDB_Agreement/Agreement.pdf)| CASIA CBSR |2012|Replay, Print(2D)|

## Contents
- [Common CNN-Based Methods](#Common-CNN-Based-Methods)
- [Traditional Methods](#Traditional-Methods)
- [Domain Generalization](#Domain-Generalization)
- [Zero/few-shot Learning or Anomaly Detection](#Zero/few-shot-Learning-or-Anomaly-Detection)


### Abbreviations for remarks

|  Data type |  `RGB` |  `IR`   |`SL`|`PC`|
|:------------|:--------------:|:----------------------:|:----------:|:----------:|
| Explanation | RGB data| Infrared data | Structure light data | Point Cloud data|

### Common CNN-Based Method
|  Title  | Venue | Remarks |
|:--------|:--------:|:--------:|
|[Biometric Face Presentation Attack Detection with Multi-Channel Convolutional Neural Network](http://publications.idiap.ch/downloads/papers/2019/George_TIFS_2019.pdf)|IEEE TIFS 2019|RGB|
|[Attention-Based Two-Stream Convolutional Networks for Face Spoofing Detection](https://ieeexplore.ieee.org/document/8737949)|IEEE TIFS 2019|RGB|
|[Face Anti-Spoofing: Model Matters, So Does Data](http://www.cbsr.ia.ac.cn/users/jwan/papers/CVPR2019-spoofing.pdf)|CVPR 2019|RGB|
|[A Dataset and Benchmark for Large-scale Multi-modal Face Anti-spoofing](https://yuan-gao.net/pdf/CVPR2019%20-%20antispoofing.pdf)|CVPR 2019|RGB+IR+Depth|
|[Face De-Spoofing: Anti-Spoofing via Noise Modeling](https://arxiv.org/abs/1807.09968)|ECCV 2018|RGB,[Code](https://github.com/yaojieliu/ECCV2018-FaceDeSpoofing)|
|[Learning Deep Models for Face Anti-Spoofing: Binary or Auxiliary Supervision](http://cvlab.cse.msu.edu/pdfs/Liu_Jourabloo_Liu_CVPR2018.pdf)|CVPR 2018|RGB, pseudo Depth+rPPG|
|[Face Anti-Spoofing Using Patch and Depth-Based CNNs](http://cvlab.cse.msu.edu/pdfs/FaceAntiSpoofingUsingPatchandDepthBasedCNNs.pdf)|IJCB 2017|RGB, pseudo Depth|

### Traditional Methods
|  Title  | Venue | Remarks |
|:--------|:--------:|:--------:|
|[Face Spoofing Detection Using Colour Texture Analysis](https://www.researchgate.net/publication/301571761_Face_Spoofing_Detection_Using_Colour_Texture_Analysis)|IEEE TIFS 2016|RGB, Color LBP|
|[Face Spoofing Detection Through Visual Codebooks of Spectral Temporal Cubes](https://www.researchgate.net/publication/281054869_Face_Spoofing_Detection_Through_Visual_Codebooks_of_Spectral_Temporal_Cubes)|IEEE TIP 2015|RGB|
|[Face Spoof Detection with Image Distortion Analysis](http://vipl.ict.ac.cn/uploadfile/upload/2017020711092984.pdf)|IEEE TIFS 2015|RGB|
|[Face spoofing detection from single images using texture and local shape analysis](https://ieeexplore.ieee.org/document/6117510)|IJCB 2011|RGB, LBP|


### Domain Generalization
|  Title  | Venue | Remarks |
|:--------|:--------:|:--------:|
|[Multi-adversarial Discriminative Deep Domain Generalization for Face Presentation Attack Detection](http://openaccess.thecvf.com/content_CVPR_2019/papers/Shao_Multi-Adversarial_Discriminative_Deep_Domain_Generalization_for_Face_Presentation_Attack_Detection_CVPR_2019_paper.pdf)|CVPR 2019|RGB|
|[Learning generalized deep feature representation for face anti-spoofing](https://rose.ntu.edu.sg/Publications/Documents/Face%20Spoofing%20Detection/Learning%20Generalized%20Deep%20Feature%20Representation%20for%20Face%20Anti-Spoofing.pdf)|IEEE TIFS 2018|RGB|
|[Unsupervised domain adaptation for face anti-spoofing](https://ieeexplore.ieee.org/document/8279564)|IEEE TIFS 2018|RGB|
|[Person-Specific Face Antispoofing With Subject Domain Adaptation](https://ieeexplore.ieee.org/document/7041231)|IEEE TIFS 2015|RGB, Person-specific|


### Zero/few-shot Learning or Anomaly Detection
|  Title  | Venue | Remarks |
|:--------|:--------:|:--------:|
|[Deep Tree Learning for Zero-shot Face Anti-Spoofing](http://cvlab.cse.msu.edu/pdfs/Liu_Stehouwer_Jourabloo_Liu_CVPR2019.pdf)|CVPR 2019|RGB|
|[Deep Anomaly Detection for Generalized Face Anti Spoofing](http://openaccess.thecvf.com/content_CVPRW_2019/papers/CFS/Perez-Cabo_Deep_Anomaly_Detection_for_Generalized_Face_Anti-Spoofing_CVPRW_2019_paper.pdf)|CVPRW 2019|RGB|


### System / Mobile Applications
|  Title  | Venue | Remarks |
|:--------|:--------:|:--------:|
|[Face Flashing: a Secure Liveness Detection Protocol based on Light Reflections](https://arxiv.org/pdf/1801.01949.pdf)|NDSS 2018|RGB+Flashing|
|[Light Field-Based Face Presentation Attack Detection: Reviewing, Benchmarking and One Step Further](https://ieeexplore.ieee.org/document/8271987)|IEEE TIFS 2018|Light Filed-Based|
|[rtCaptcha: A Real-Time CAPTCHA Based Liveness Detection System](https://pdfs.semanticscholar.org/1fb3/99bf4122b5b25ae7784ca73f9b1be6a91cde.pdf)|NDSS 2018|RGB+Captcha|
|[Face Liveness Detection Using a Flash Against 2D Spoofing Attack](http://www.hebmlc.org/UploadFiles/20171014235219706.pdf)|IEEE TIFS 2017|RGB+Flashing|
|[Your face your heart: Secure mobile face authentication with photoplethysmograms](https://web.asu.edu/sites/default/files/cnsg/files/c38.pdf)|INFORCOM 2017|RGB+rPPG|
|[Sensor-assisted facial recognition: an enhanced biometric authentication system for smartphones](http://qurinet.ucdavis.edu/pubs/conf/shaxun-mobisys.pdf)|Mobisys 2014|RGB+Sensor|

### Attack
|  Title  | Venue | Remarks |
|:--------|:--------:|:--------:|
|[Virtual U: Defeating Face Liveness Detection by Building Virtual Models from Your Public Photos](https://www.usenix.org/system/files/conference/usenixsecurity16/sec16_paper_xu.pdf)|USENIX SS 2018|VR tech for spoofing|












