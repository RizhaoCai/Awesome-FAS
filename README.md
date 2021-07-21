# Awesome-FAS (Face Authentication Security)

A curated list of Face Authentication Security (including face anti-spoofing/face presentation attack/face liveness detection, face attack models, etc.) and related resources. This is inspired by [Awesome-deep-vision](https://github.com/kjw0612/awesome-deep-vision), [Awesome-adversarial-machine-learning](https://github.com/yenchenlin/awesome-adversarial-machine-learning), [Awesome-deep-learning-papers](https://github.com/terryum/awesome-deep-learning-papers), [Awesome-NAS](https://github.com/D-X-Y/Awesome-NAS) and [Awesome-Pruing](https://github.com/he-y/Awesome-Pruning)


Please feel free to pull requests or open an issue to add papers.

# Contents
- [Awesome-FAS (Face Authentication Security)](#awesome-fas-face-authentication-security)
  - [Contents](#contents)
  - [Databases](#databases)
  - [Learning-based Methods](#learning-based-methods)
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
## Year 2021
|  Title  | Venue | Note |
|:--------|:--------:|:--------:|
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
+ ArXiv: Papers that only appear in ArXiv are regarded not published, but they are collected here for reference only.







