# <p align=center>`Histopathology Datasets for Machine Learning`</p>

This is a list of histopathology datasets made public for classification, segmentation, regression and/or registration tasks.

I am happy if you want to help me update and/or improve this document. I think it helps to have an overview of all the datasets available in the field.

I hope this list will help some of you.

# Overview
- [Resources](#resources)
- [References](#references)
- [Datasets Search](#search)

# Resources

Please find in the table below some link and information about histopathology dataset that are publicly available.

Dataset name | Organs | Staining | Link | Size | Data | Task | WSI/Patch | Other (Magnification, Scanner) | year
--- | --- | --- | --- |--- |--- |--- |--- |--- |---
ACDC-LungHP [1a], [1b] | Lung | H&E | [data](https://acdc-lunghp.grand-challenge.org/), [paper](https://ieeexplore.ieee.org/document/9265237) | Train: 150, Test: 50 | images + xml | seg + classi | wsi | | 2019
ACROBAT 2022 [66] | Breast | Multiple (IHC, H&E) | [data](https://acrobat.grand-challenge.org/), [paper](https://openreview.net/pdf?id=5TTocO2VI3r) | Train: 750 train; Valid: 100; Test: 300 | images (1 H&E match to 1-4 IHC) + landmarks | registration | wsi | 40x - Hamamatsu | 2022
Adipocyte [94] | skin | H&E | [data](https://github.com/ieee8023/countception), [paper](https://arxiv.org/abs/1703.08710) | 150 patches | images+mask |  cell detection | patch (600x600) | 40x | 2017
ADP [2] | multiple | multiple (most H&E) | [data](https://www.dsp.utoronto.ca/projects/ADP/), [github](https://github.com/mahdihosseini/ADP), [paper](https://openaccess.thecvf.com/content_CVPR_2019/papers/Hosseini_Atlas_of_Digital_Pathology_A_Generalized_Hierarchical_Histological_Tissue_Type-Annotated_CVPR_2019_paper.pdf) | Train: 14.134, Valid: 1767, Test: 1767 (100 wsi) | images + 57 hierarchical HTTs (histological tissue type) | multi-label (3) classification (hierarchy) | patch (1088x1088) | 40x - Huron TissueScope LE1.2 WSI | 2019
 AGGC                                             | prostate                                                     | H&E                                     | [data](https://aggc22.grand-challenge.org/AGGC22/), [paper](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4172090) | Subset 1: train 105, test 45; Subset2: train 37 ,test 16; Subset3: train 144, test 67 | images + binary masks                                        | seg + gleason grading                                        | wsi                                   | 20x - Subset1 and Subset2: Akoya Biosciences Scanner, Subset3: each specimen is scanned by multiple scanners | 2022 
AML-Cytomorphology_LMU [67] | Blood | Wright's stain | [data](https://wiki.cancerimagingarchive.net/pages/viewpage.action?pageId=61080958#61080958bcab02c187174a288dbcbf95d26179e8), [paper](https://www.nature.com/articles/s42256-019-0101-9) | 18.365 images from 200 patients || classi | patch (cells) | 100x - M8 digital microscope/scanner | 2019
ANHIR [3] | multiple (Lung, Kidney, Colon, Gastric, Breast)| multiple | [data](https://anhir.grand-challenge.org/), [paper](https://ieeexplore.ieee.org/document/9058666) | 50+ sets| image + landmarks  | registration | patch (15k x 15k to 50k x 50k) | 40x, 20x, 10x, different scanner | 2019
ARCH [4] | multiple | multiple | [data](https://warwick.ac.uk/fac/cross_fac/tia/data/arch), [paper](https://openaccess.thecvf.com/content/CVPR2021/html/Gamper_Multiple_Instance_Captioning_Learning_Representations_From_Histopathology_Textbooks_and_Articles_CVPR_2021_paper.html) | 4270 | images + caption | learn representation from text + image | patch | multiple | 2020
BACH - ICIA2018 [5] | Breast | H&E | [data](https://iciar2018-challenge.grand-challenge.org/Dataset/), [paper](https://www.sciencedirect.com/science/article/abs/pii/S1361841518307941) | 400 | images (4 classes: normal 100, benign: 100, in situ carcinoma: 100, invasive carcinoma: 100) + 20 unlabeled + 10 labeled WSI (10 patients) | classi + seg| Patch (classi, 2048x1536) + WSI (seg) | Leica SCN400 | 2018
BCNB [6] | Breast | H&E | [data](https://bcnb.grand-challenge.org/), [paper](https://www.frontiersin.org/articles/10.3389/fonc.2021.759007/full) | 1058 (train 0.6, valid 0.2, test 0.2) | images + roi annotated + patient record | binary or multiple classi | wsi |  | 2021
BCSS [7] | Breast | H&E | [data](https://bcsegmentation.grand-challenge.org/), [paper](https://academic.oup.com/bioinformatics/article/35/18/3461/5307750) | 151 wsi, 20.000 patch| patch + segmentation mask | semantic seg | patch | (TCGA) | 2019
Bone-Marrow-Cytomorphology [68] | Marrow | May-Grünwald-Giemsa/Pappenheim | [data](https://wiki.cancerimagingarchive.net/pages/viewpage.action?pageId=101941770#101941770bcab02c187174a288dbcbf95d26179e8), [paper](https://ashpublications.org/blood/article/138/20/1917/477932/Highly-accurate-differentiation-of-bone-marrow) | 171.375 cells from 945 patients | images + label | classi (21) | patch (250x250 - single cell) | 40x | 2021 
BRACS [62] | Breast | H&E | [data](https://www.bracs.icar.cnr.it/details/), [paper](https://arxiv.org/pdf/2111.04740.pdf) | 547 wsi, 4539 ROIs, 189 Patients | images + label (6 subtypes tumor + normal) | classi (7) | wsi + patch | 40x - Aperio AT2 | 2021
BreakHis [8] | Breast |	H&E	| [data](https://web.inf.ufpr.br/vri/databases/breast-cancer-histopathological-database-breakhis/), [paper](https://www.inf.ufpr.br/lesoliveira/download/TBME-00608-2015-R2-preprint.pdf) |	7.909 (2480 benign, 5429 malignant)	| images + binary label + tumor type (8) (multiple magnifications: 40x, 100x, 200x, 400x) |	classi |	Patch (700x460) | 40x, 100x, 200x, 400x | 2016
BreCaHAD [9] | Breast | H&E | [data](https://figshare.com/articles/dataset/BreCaHAD_A_Dataset_for_Breast_Cancer_Histopathological_Annotation_and_Diagnosis/7379186) [paper](https://bmcresnotes.biomedcentral.com/articles/10.1186/s13104-019-4121-7) | 162 | images + centroid with label | classi (6: mitosis, apoptosis, tumor nuclei, non-tumor nuclei, tubule, non-tubule) | patch (1360x1024) | 40x - Zeiss | 2019
CAMEL [63] | Colon | | [data](https://github.com/ThoroughImages/CAMEL), [paper](https://arxiv.org/abs/1908.10555) | 177 wsi (156 with adenoma) | image + label (binary)| classi | patch (1280x1280) | | 2019
CAMELYON16 [10] | Lymph node | H&E | [data](https://camelyon16.grand-challenge.org/), [paper](https://jamanetwork.com/journals/jama/article-abstract/2665774) | Train: 270 (160 Normal, 110 with metastases); Test: 130 | images + binary masks | classi + seg | WSI | slide level analysis | 2016
CAMELYON17 [11] | Lymph node | H&E | [data](https://camelyon17.grand-challenge.org/), [paper](https://ieeexplore.ieee.org/document/8447230) | Train: 500 (100 patients, 5 slides each); Test: 500 | images + binary masks | classi + seg | WSI | patient level analysis | 2017
CAMELYON [12] | Breast (Lymph node) | H&E | [paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6007545/) | 1399 wsi | | | wsi | | 2017
CATCH [88] | Skin (Canine) | H&E | [data](https://www.cancerimagingarchive.net/collection/catch/), [paper](https://www.nature.com/articles/s41597-022-01692-w) | 350 wsi, 12.424 polygon annotations (13 classes) | images + contours (JSON) | seg + classi | wsi | 40x Aperio ScanScope CS2 (Leica) | 2022
Cellseg [13] | multiple | multiple | [data](https://neurips22-cellseg.grand-challenge.org/), [paper](https://proceedings.mlr.press/v212/lee23b.html), [github](https://github.com/JunMa11/NeurIPS-CellSeg) | | images + limited labeled patches | instance (cell) segmentation | wsi |  | 2022
Chaoyang [57] | Colon | H&E | [data](https://bupt-ai-cz.github.io/HSA-NRL/), [github](https://github.com/bupt-ai-cz/HSA-NRL), [paper](https://ieeexplore.ieee.org/abstract/document/9600806) | Train: 111 normal, 842 serrated, 1404 adenocarcinoma, 664 adenoma, Test: 705 normal, 321 serrated, 840 adenocarcinoma, 273 adenoma samples | images + label | classi | patch (512×512) |  | 2021
CoCaHis [61] | Colon | H&E | [data](https://cocahis.irb.hr/), [paper](https://www.sciencedirect.com/science/article/abs/pii/S1746809420305085) | 82 (19 patients) | images + mask from different annotator | seg | patch | | 2021
CoNIC 2022 [14] | Colon | H&E | [data](https://conic-challenge.grand-challenge.org/), [github](https://github.com/TissueImageAnalytics/CoNIC), [paper](https://arxiv.org/pdf/2111.14485.pdf) | 4981 patch with 431.913 nuclei of 6 types | image + instance seg mask + classi mask | seg + classi + reg | patch (256x256) | 20x | 2022
CoNSeP - HoVer-Net [15] | Colorectal adenocarcinoma | H&E | [data](https://warwick.ac.uk/fac/cross_fac/tia/data/hovernet/), [paper](https://www.sciencedirect.com/science/article/abs/pii/S1361841519301045?via%3Dihub) | Train: 27 images, Test: 14 images, 24.319 nuclei | images + nuclei (location + class) | instance seg + classi (7: other, inflammatory, healthy epithelial, dysplastic/malignant epithelial, figroblast, muscle, endothelial) | patch (1000x1000) | 40x (UHCW) | 2019
CPM-15 [16] | brain | H&E | [data](https://drive.google.com/drive/folders/11ko-GcDsPpA9GBHuCtl_jNzWQl6qY_-I) | 15 (2905 nuclei) | images + nuclei seg + label | seg + classi | patch (400x400, 600x1000) | 20x, 40x (TCGA) | 
CPM-17 [17] | brain | H&E | [data](https://drive.google.com/drive/folders/1sJ4nmkif6j4s2FOGj8j6i_Ye7z9w0TfA), [paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6454006/) | Train: 32, test: 32 (7570 nuclei) | images + nuclei seg + label | seg + classi | patch (500x500 to 600x600) | 20x, 40x (TCGA) | 2019
CPTAC-AML | Marrow, Blood || [data](https://wiki.cancerimagingarchive.net/display/Public/CPTAC-AML#47677483bcab02c187174a288dbcbf95d26179e8) | 120 images from 88 patients |||| 40x | 2020
CPTAC-BRCA | Breast || [data](https://wiki.cancerimagingarchive.net/display/Public/CPTAC-BRCA#70227748bcab02c187174a288dbcbf95d26179e8) | 642 images from 134 patients |||| 40x | 2021 
CPTAC-COAD | Colon || [data](https://wiki.cancerimagingarchive.net/display/Public/CPTAC-COAD#70227852bcab02c187174a288dbcbf95d26179e8) | 373 images from 106 patients |||| 40x | 2021
CPTAC-OV | Ovary || [data](https://wiki.cancerimagingarchive.net/display/Public/CPTAC-OV#70227856bcab02c187174a288dbcbf95d26179e8) | 222 images from 102 patients |||| 40x | 2021
CRAG - MILD-Net [18] | Colon | H&E | [data](https://warwick.ac.uk/fac/cross_fac/tia/data/mildnet/), [paper](https://www.sciencedirect.com/science/article/abs/pii/S1361841518306030?via%3Dihub) | Train: 173, Valid: 40 | image + segmentation | instance seg | patch (around 1500x1500) | 20x | 2019
CRCHisto [19] | Colon | H&E | [data](https://warwick.ac.uk/fac/cross_fac/tia/data/crchistolabelednucleihe/), [paper](https://ieeexplore.ieee.org/document/7399414) | 100 images, 29.756 nuclei (10 wsi, 9 patients) | images + point nuclei class label | seg + classi (epithelial, inflammatory, fibroblast, miscellaneous) | patch (500x500) | 20x - Omnyx VL120 (UHCW) | 2016
CRC-TP [20] | CRC | H&E | [data](https://warwick.ac.uk/fac/cross_fac/tia/data/crc-tp), [paper](https://www.sciencedirect.com/science/article/abs/pii/S136184152030061X?via%3Dihub) | 280k patches (from 20 wsi) | images + tissue phenotypes | classi | patch |  | 2020
CryoNuSeg [21] | multiple (10: adrenal gland, larynx, lymph nodes, mediastinum, pancreas, pleura, skin, testes, thymus, and thyroid gland) | H&E | [data](https://www.kaggle.com/datasets/ipateam/segmentation-of-nuclei-in-cryosectioned-he-images), [github](https://github.com/masih4/CryoNuSeg), [paper](https://www.sciencedirect.com/science/article/pii/S0010482521001438) | 8000 nuclei from 30 patches (from 30 wsi) | images + segmentation masks + binary labels | nuclei segmentation | patch (512x512) | 40x (from TCGA) | 2021
DHMC-Kidney [85] | Renal Cell Carcinoma | H&E | [data](https://bmirds.github.io/KidneyCancer/), [paper](https://www.nature.com/articles/s41598-021-86540-4) | 563 wsi | images + label | classi | wsi | 20x - Aperio AT2 | 2021 
DHMC-Lung [86] | Lung Adenocarcinoma | H&E | [data](https://bmirds.github.io/LungCancer/), [paper](https://www.nature.com/articles/s41598-019-40041-7) | 143 wsi | images + label | classi | wsi | 20x or 40x - Aperio AT2 | 2019 
DiagSeg [58] | Prostate | H&E | [data](https://github.com/michalkoziarski/DiagSet), [paper](https://arxiv.org/abs/2105.04014) | >2.6M patches (from 430 scans) 430 fully annotated scans, 4675 scans with binary diagnosis, and 46 scans with diagnosis given independently by a group of 9 histopathologists |  | classi (256×256) | patch | 5x, 10x, 20x, 40x - Hamamatsu C12000-22 | 2021
DigestPath2019 - signet ring cell [22] | multiple (Gastric, Intestine) | H&E | [data](https://digestpath2019.grand-challenge.org/), [paper](https://arxiv.org/pdf/1907.03954.pdf) | Train: 460, Test: 226 | images + cell bounding boxes | cell detection | patch (avg 2kx2k) | 40x | 2019
DigestPath2019 - colonoscopy tissue segment [23] | Colon | H&E | [data](https://digestpath2019.grand-challenge.org/), [paper](https://arxiv.org/pdf/1907.03954.pdf) | Train: 660, Test: 212 | images + lesion annotation | seg + classi (benign vs malignant) | patch (avg 5kx5k) | 20x | 2019
DLBCL-morphology [69] | Lymph Node | Multiple (H&E, IHC) | [data](https://wiki.cancerimagingarchive.net/pages/viewpage.action?pageId=119702520#119702520bcab02c187174a288dbcbf95d26179e8), [paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8137959/) | 52.194 patches - 246 images from 209 patients  | images + ROIs | | wsi - patch (240x240) | 40x - Aperio AT2 | 2022
ENDO-AID [] | Endometrial Carcinoma | H&E | [data](https://zenodo.org/record/7372187#.Y-C6I4TMKUk), [info](endo-aid.grand-challenge.org/) | Test: 91 wsi | images + 15 pathologists assessments | grading score | wsi | 0.5um/px - 3DHistech P1000 | 2022
Gelasca et al. [26] | Breast | H&E | [data](https://bioimage.ucsb.edu/research/bio-segmentation) | 50 | images (malignant/benignant, 1.895 nuclei) + masks | classi + seg | Patch (896x768; 768x512) | |
GlaS [24] | Colorectal (Gland) | H&E | [data](https://warwick.ac.uk/fac/cross_fac/tia/data/glascontest/), [paper](https://arxiv.org/pdf/1603.00275v2.pdf) | 165 | Train: 85 (37 benign, 48 malignant); Test: 80 (37 benign, 43 malignant) | classi + seg | Patch (diff sizes - few hundred px) | 20x - Zeiss MIRAX MIDI | 2015
Gleason_CNN [25] | Prostate | H&E | [data](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/OCYCMP), [github](https://github.com/eiriniar/gleason_CNN), [paper](https://www.nature.com/articles/s41598-018-30535-1) | 5 tissue microarrays (200-300 spots) | images + patch and pixel annotation | classi | patch (3100x3100) | 40x - NanoZoomer-XR Digital slide scanner, Hamamatsu | 2018
GTEx Portal [77] | Multiple | H&E | [data](https://gtexportal.org/home/histologyPage), [paper](https://www.nature.com/articles/ng.2653?report=reader) | 948 patients (multiple slides per patients) | images + genes + metadata |  | | | 
HER2 Contest [60] | Breast | Multiple (H&E, IHC) | [data](https://warwick.ac.uk/fac/cross_fac/tia/data/her2contest), [paper](https://onlinelibrary.wiley.com/doi/full/10.1111/his.13333) | 172 wsi from 86 patients | image + label (scoring) | classi (4 classes: 0, 1+, 2+, 3+) | wsi | 4x-40x - Hamamatsu NanoZoomer C9600 | 2016
HEROHE - ECDP2020 [27a], [27b] | Breast | H&E | [data](https://ecdp2020.grand-challenge.org/Home/), [paper](https://arxiv.org/ftp/arxiv/papers/2111/2111.04738.pdf) | Train: 359 (positive: 144, negatives: 215), Test: 150 (positive: 60, negative: 90) | images + binary label | classi | wsi | 20x - 3D Histech Pannoramic 1000 | 2020
HER2 tumor ROIs [70] | Breast | H&E | [data](https://wiki.cancerimagingarchive.net/pages/viewpage.action?pageId=119702524), [paper](https://www.nature.com/articles/s41379-021-00911-w) | 273 | images + ROIs + label | classi (binary) | patch (512x512) | 20x - Aperio ScanScope | 2022 
HunCRC [71] | Colon | H&E | [data](https://wiki.cancerimagingarchive.net/pages/viewpage.action?pageId=91357370), [github](https://github.com/qbeer/qupath-binarymask-extension), [github](https://github.com/patbaa/crc_data_paper), [paper](https://www.nature.com/articles/s41597-022-01450-y) | 101,389 patches - 200 wsi (from 200 patients) | images + label | classi (10) | wsi - patch (512x512) | 40x - 3DHistech Pannoramic 1000 | 2022
IMP-CRS 2024 [81a],[81b],[81c] | Colorectal | H&E | [data](https://rdm.inesctec.pt/dataset/nis-2023-008), [paper](https://www.nature.com/articles/s41698-024-00539-4) | Train 4433 wsi, Test: 900 wsi | images + label | classi (3) | wsi | 40x - Leica GT450 | 2024
Janowczyk et al. [28] | Breast |  H&E | [data](http://www.andrewjanowczyk.com/use-case-1-nuclei-segmentation/), [github](https://github.com/choosehappy/public/tree/master/DL%20tutorial%20Code) | 143 | images (12.000 nuclei) + masks | semantic seg | Patch (2000x2000) | 40x | 2015
Kather et al. [29] | Colon | H&E | [data](https://zenodo.org/record/1214456#.Yt_SxN_RZhE), [github](https://github.com/jnkather/deep-stroma-histology/tree/v0.2), [paper](https://journals.plos.org/plosmedicine/article?id=10.1371/journal.pmed.1002730) | Train: 100k (86 wsi), Valid: 7180 (25 wsi) | image + label (9 tissue type) | classi | patch (224x224) |  | 2018
Kather et al. [30] | Colon | H&E | [data](https://zenodo.org/record/2530835#.Yt_ZdN_RZhE), [data](https://zenodo.org/record/2530789#.Yt_Zc9_RZhE), [data](https://zenodo.org/record/2532612#.Yt_Zdd_RZhE), [github](https://github.com/jnkather/MSIfromHE), [paper](https://www.nature.com/articles/s41591-019-0462-y#data-availability) |   |  | seg (tumor detection) + classi (MSI detection) |   |  | 2019
KIMIA Path24C [65] | multiple | multiple (IHC, H&E, Masson's trichrome) | [data](https://kimialab.uwaterloo.ca/kimia/index.php/pathology-images-kimia-path24/), [paper](https://arxiv.org/pdf/2102.07611.pdf) | Train: 22.591, Valid: 1.325 from 24 wsi |  |  | patch (1000x1000) | 20x - TissueScope LE 1.0. | 2021
Komura et al. [64] | multiple (32) | H&E | [data](https://zenodo.org/record/5889558#.YuJHdd_RaUk), [paper](https://www.sciencedirect.com/science/article/pii/S2211124722001486?via%3Dihub) | 271.700  | images + cancer type | classi | patch (256x256) | 6 magnification (from TCGA) | 2021
Kumar [31] | multiple (8) | H&E | [data](https://drive.google.com/drive/folders/1bI3RyshWej9c4YoRW-_q7lh7FOFDFUrJ), [paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7872382) | Train: 16 (13.372 nuclei), test same organ (4.130 nuclei): 8, test diff organ (4.121 nuclei): 6 | images + nuclei seg + label | seg + classi | patch (1000x1000) | 40x (TCGA) | 2017
LC25000 [54] | multiple (lung, colon) | H&E | [data](https://github.com/tampapath/lung_colon_image_set), [paper](https://arxiv.org/ftp/arxiv/papers/1912/1912.12142.pdf) | 25.000 (5 classes) | images + label | patch (768x768) | classi | 60x | 2019
Lizard [32] | Colon | H&E | [data](https://warwick.ac.uk/fac/cross_fac/tia/data/lizard/), [paper](https://arxiv.org/pdf/2108.11195.pdf) | 495.179 nuclei | images + instance seg mask | seg | patch | 20x (DigestPath + CRAG + GlaS + PanNuke + CoNSeP + TCGA) | 2021
LYON19 [33] | Multiple (Breast, Colon, Protate) | IHC | [data](https://lyon19.grand-challenge.org/), [paper](https://www.sciencedirect.com/science/article/abs/pii/S1361841519300829) | Test: 441 ROIs - 171.166 cells | images + corrdinates of cell | cell detection | patch | Pannoramic 250Flash II scanner | 2019
MBM [94] | brone | H&E | [data](https://github.com/ieee8023/countception), [paper](https://arxiv.org/abs/1703.08710) | 44 patches | images+mask |  cell detection | patch (600x600) | 40x | 2017
MHIST [79] | colorectal polyps | H&E | [data](https://bmirds.github.io/MHIST/), [paper](https://arxiv.org/pdf/2101.12355.pdf) | 3,152 patches (train: 2,175; test: 977) | images + annotations + annotator agreement | classi (2) | patch (224x224) | 40x - Aperio AT2 | 2021
MIDOG 2021 [34] | Breast | H&E | [data](https://imig.science/midog2021/the-dataset/), [paper](https://arxiv.org/pdf/2204.03742.pdf) | 200 wsi: 50 wsi / scanners - 4 scanners | images + roi | detection of mitotic figues | wsi | | 2021
MIDOG 2022 [35] | multiple (6 for train 10 for test) | H&E | [data](https://midog2022.grand-challenge.org/) | Train: 405 cases, 9501 mitotic annotation | images + seg | seg | Patch | | 2022
MIDOG++ [93] | multiple | H&E | [data](https://doi.org/10.6084/m9.figshare.c.6615571.v1), [paper](https://www.nature.com/articles/s41597-023-02327-4) | 503 ROIs + 12k mitotic figures | images + object centers | detection of mitotic figures | ROIs | | 2023 
MITOS_WSI_CCMCT [89] | Skin (Canine) | H&E | [data](https://doi.org/10.6084/m9.figshare.c.4552445.v1), [paper](https://www.nature.com/articles/s41597-019-0290-4) | 32 wsi | images + mitotic figures (45k)/ hard negatives (28k) | detection of mitotic figues | wsi | 40x Aperio ScanScope CS2 (Leica) | 2019
MITOS_WSI_CMC [90] | Breast (Canine) | H&E | [data](https://doi.org/10.6084/m9.figshare.c.4951281.v1), [paper](https://www.nature.com/articles/s41597-020-00756-z#citeas) | 21 wsi | images + mitotic figures (14k)/ hard negatives (35k) | detection of mitotic figues | wsi | 40x Aperio ScanScope CS2 (Leica) | 2020
MoNuSAC 2020 [36] | multiple (Lung, Prostate, Kidney, Breast) | H&E | [data](https://monusac-2020.grand-challenge.org/), [paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9446924) | 31.411 nuclei from 209 images | images + mask | instance seg + classi | patch (81x113 to 1422x2162) | 40x (TCGA) | 2020
MoNuSeg [37a], [37b] | multiple (7) | H&E | [data](https://monuseg.grand-challenge.org/Data/), [github](https://github.com/ruchikaverma-iitg/MoNuSeg), [paper](https://ieeexplore.ieee.org/document/8880654) | Train: 30, Test: 14 | images (Train: 22.000 nuclei, Test: 7000) + masks| instance seg | Patch (1000x1000) | 40x (from TCGA) | 2018
Multi-Scanner SCC [92] | Skin (Canine) | H&E | [data](https://zenodo.org/records/7418555), [paper](https://link.springer.com/chapter/10.1007/978-3-658-41657-7_46) | 44 samples á 5 scanners (220 wsi) | images + contours (JSON) | registration + segmentation | wsi | 5 scanners | 2023 
NADT-Prostate [72] | Prostate | Multiple (H&E, IHC) | [data](https://wiki.cancerimagingarchive.net/pages/viewpage.action?pageId=91357374), [paper](https://www.sciencedirect.com/science/article/pii/S0302283821002074?via%3Dihub) | 1401 images from 37 patients |||| 20x | 2021
Naylor et al. [38] | Breast | H&E | [data](https://zenodo.org/record/2579118#.Yt5FWt_RaUk), [paper](https://ieeexplore.ieee.org/document/8438559) | 50 | images (4.022 nuclei, 11 patients) + masks | seg | Patch (512x512) | 40x | 2018
NuClick [59] | Lymphocyte | IHC | [data](https://warwick.ac.uk/fac/cross_fac/tia/data/nuclick/), [paper](https://arxiv.org/pdf/2005.14511.pdf) | Train: 671, Valid: 200 | images + mask | seg | patch (256x256) |  | 2020
NuCLS [39] | Breast | H&E | [data](https://nucls.grand-challenge.org/), [paper](https://arxiv.org/ftp/arxiv/papers/2102/2102.09099.pdf) | 220.000 nuclei from 3.944 roi from 125 patients | roi + bounding bx + classification |  nuclear detection + classi + seg | patch | (TCGA) | 2021
OCELOT [78] | Multiple (Bladder, Endometrium, Head-and-neck, Kidney, Prostate, Stomach) | H&E | [data](https://ocelot2023.grand-challenge.org/ocelot2023/), [paper](https://openaccess.thecvf.com/content/CVPR2023/html/Ryu_OCELOT_Overlapped_Cell_on_Tissue_Dataset_for_Histopathology_CVPR_2023_paper.html), [website](https://lunit-io.github.io/research/publications/ocelot/) | 304 Whole Slide Images (WSIs) (tr:val:te 6:2:2) | images + cell annotation + tissue annotation | cell and tissue detection (multitask learning) | patch (1024x1024) | (TCGA) | 2023
Osteosarcoma-Tumor-Assessment | Bone | H&E | [data](https://wiki.cancerimagingarchive.net/pages/viewpage.action?pageId=52756935#52756935bcab02c187174a288dbcbf95d26179e8) | 1144 images from 4 || classi (3: non-tumor, viable tumor, necrosis) | patch (1024x1024) | 10x | 2019
Ovarian Bevacizumab Response [73a], [73b] | Ovary | H&E | [data](https://wiki.cancerimagingarchive.net/pages/viewpage.action?pageId=83593077#83593077f7288fc2370a43c3a1278185270ffc60), [paper](https://www.nature.com/articles/s41597-022-01127-6), [paper](https://www.sciencedirect.com/science/article/abs/pii/S0895611122000660) | 288 (78 patients) | images + clinical information | classi (treatment effectiveness) | wsi (avg 54342x41048) | 20x - Leica AT2 | 2021 
PAIP2019 [40] | Liver | H&E | [data](https://paip2019.grand-challenge.org/), [paper](https://www.sciencedirect.com/science/article/pii/S1361841520302188) | Train: 50, Valid: 10, Test: 40 | images + binary mask | cancer seg | wsi | 20x - Aperio AT2 | 2019
PAIP2020 [41] | Colon | H&E | [data](paip2020.grand-challenge.org/), [github](https://github.com/wisepaip/paip2020) | Train: 47, Valid: 31, Test: 40 | images + binary mask | cancer seg | wsi | 40x - Aperio AT2 | 2020
PAIP2021 [42] | Multiple (Colon, Prostate, Pancreas) | H&E | [data](https://paip2021.grand-challenge.org/Rules/), [paper](https://arxiv.org/ftp/arxiv/papers/2110/2110.12283.pdf) | Train: 150, Valid: 30, Test: 60 | wsi + xml gt | semantic seg | wsi | 20x - Aperio AT2 | 2021
PAIP2023 | multiple organ | H&E | [data](https://2023paip.grand-challenge.org/download/) | | | | | | 2023 
The PANDA challenge [43]  | Prostate | H&E | [data](https://www.kaggle.com/c/prostate-cancer-grade-assessment/data), [paper](https://www.nature.com/articles/s41591-021-01620-2) | Train: 10.616, Valid: 393, Internal test: 545, External test: 1071 | images + label | classi | wsi | slide level analysis | 2020
Pan-tumor T-lymphocyte dataset [91] | Multiple | IHC (CD3) | [data](https://doi.org/10.5281/zenodo.7500843), [paper](https://doi.org/10.1016/j.jpi.2023.100301) | 92 ROIs | images + cell annotations | detection + classification | wsi | 40x NanoZoomer 2.0-HT (Hamamatsu) | 2023
SegPath [87] | multiple | H&E | [data](https://dakomura.github.io/SegPath/), [paper](https://www.cell.com/patterns/fulltext/S2666-3899(23)00019-3) | 158,687 patches | images + label + mask | semantic seg | patch | 20x - Zeiss MIRAX MIDI | 2023 
PanNuke [44a], [44b] | multiple (19) | H&E | [data](https://warwick.ac.uk/fac/cross_fac/tia/data/pannuke), [github](https://jgamper.github.io/PanNukeDataset/), [paper](https://arxiv.org/pdf/2003.10778.pdf), [paper](https://link.springer.com/chapter/10.1007/978-3-030-23937-4_2) | 189.744 nuclei (from >20k wsi) | images + nuclei (position + classi: neoplastic, connective, non-neoplastic epithelial, dead, inflammatory) | instance seg + classi | patch | 40x | 2019
PatchCamelyon [45a], [45b] | Lymph node |	H&E |	[data](https://patchcamelyon.grand-challenge.org/), [github](https://github.com/basveeling/pcam) [paper](https://arxiv.org/pdf/1806.03962.pdf)	| 327.680 |	images + binary label	| classi |	Patch (96x96) | 10x | 2018
PATHVQA [80] | Multiple | Multiple | [data](https://drive.google.com/drive/folders/1G2C2_FUCyYQKCkSeCRRiTTsLDvOAjFj5), [paper](https://arxiv.org/pdf/2003.10286.pdf), [github](https://github.com/UCSD-AI4H/PathVQA) | 32,799 open-ended questions from 4,998 images | image + question + answer | VQA | patch/image | | 2020
Post-NAT-BRCA [74] | Breast | H&E | [data](https://wiki.cancerimagingarchive.net/pages/viewpage.action?pageId=52758117#52758117bcab02c187174a288dbcbf95d26179e8), [paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6124665/) | 96 images from 54 patients | images + clinical info + annotation tumor cellularity and cell labels |  | wsi | 20x - Aperio | 2021
Prostate Fused-MRI-Pathology [83] | Prostate | H&E | [data](https://www.cancerimagingarchive.net/collection/prostate-fused-mri-pathology/) | 114 images from 16 patients | images + tumor Annotations + mpMRI | | wsi | 20x - Aperio | 2016 
SegPC-2021 [46a], [46b], [46c], [46d] | Blood | Jenner-Giemsa | [data](https://segpc-2021.grand-challenge.org/), [github](https://github.com/dsciitism/SegPC-2021), [report](https://ieee-dataport.org/open-access/segpc-2021-segmentation-multiple-myeloma-plasma-cells-microscopic-images) | 775 images, Train: 298, Valid: 200, Test: 277 | images + nucleus and cytoplasma | plasma cell segmentation |  | | 2021
SICAPv2 [55] | Prostate | H&E | [data](https://data.mendeley.com/datasets/9xxm58dvs3/1), [paper](https://arxiv.org/pdf/2105.10490.pdf) | 155 (from 95 patients) | images + global Gleason scores and patch-level Gleason grades | classi | wsi | 40x - Ventana iScan Coreo | 2020
SLN-Breast [75] | Breast | H&E | [data](https://wiki.cancerimagingarchive.net/pages/viewpage.action?pageId=52763339), [paper](https://www.nature.com/articles/s41591-019-0508-1) | 130 wsi from 78 patients | images + binary label | classi (binary - cancer/no cancer) | wsi | 20x -  Leica Aperio AT2 | 2021
SPIE-AAPM_NCI BreastPathQ [47] | Breast | H&E | [data](https://breastpathq.grand-challenge.org/), [paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8107263/) | 2579 patch from 96 wsi (64 patients) | images + score | regression | patches | 20x | 2019
TCGA [48] | Multiple | H&E | [data](https://portal.gdc.cancer.gov/), [data](https://portal.imaging.datacommons.cancer.gov/explore/) | > 11k |  |  | WSI ||
TCGA-TIL-WSI [76] | Multiple (13) | H&E | [data](https://wiki.cancerimagingarchive.net/pages/viewpage.action?pageId=33948919#33948919036220c66a5a436f90e4a0b54367bfae), [github](https://github.com/SBU-BMI/u24_lymphocyte), [paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5943714/) | 5200 |||| (from TCGA) | 2019
TIGER [49] | Breast | H&E | [data](https://tiger.grand-challenge.org/), [paper](https://arxiv.org/abs/2206.11943), [github](https://github.com/DIAGNijmegen/pathology-tiger-baseline), [github](https://github.com/DIAGNijmegen/pathology-tiger-algorithm-example) | WSIROIS: 195 wsi, WSIBULK: 93, WSITILS: 82 | images + rois + label (7) | detection + segmentation + TILs scoring | wsi | (from TCGA, RUMC, JB) | 2022
TissueNet | Uterine cervix | H&E | [data](https://www.drivendata.org/competitions/67/competition-cervical-biopsy/page/254/), [github](https://github.com/drivendataorg/tissuenet-cervical-biopsies) | 1,016 WSIs; 5,926 patches (1200x1200 px) | images + annotation + metadata + labels | classi (4) | wsi + patches | MIRAX, Aperio, Hamamatsu | 2020
TNBC [50] | Breast | H&E | [data](https://peterjacknaylor.github.io/data/), [data](https://drive.google.com/drive/folders/1taB8boGyycjV4X1a2vCIAV9fwMxFSS41), [paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=8438559) | 50 images, 4022 cells (11 patients) | images + nuclei seg + label | seg + classi | patch (512x512) | 40x - Philips Ultra Fast Scanner (Curie Inst.) | 2019
Tolkach Y. et al. [84] | oesophageal adenocarcinomas | H&E | [data](https://zenodo.org/records/7548828), [paper](https://www.thelancet.com/journals/landig/article/PIIS2589-7500(23)00027-4/fulltext) | UKK1: 34,704 patches from 22 wsi (20 patients); WNS: 121,642 patches from 62 wsi (15 patients); CHA: 32,796 patches from 214 wsi (69 patients); TCGA:178,187 patches from 22 wsi (22 patients) | images + label | classi (11) | patch(256x256) | 40x - Nanozoomer S360 | 2023 
TUPAC16 [51] | Breast | H&E | [data](https://tupac.grand-challenge.org/), [paper](https://arxiv.org/ftp/arxiv/papers/1807/1807.08284.pdf) | 500 | images + label | classi (wsi level) | WSI | 40x (from TCGA) | 2019
TUPAC16 - aux [52] | Breast - mitoses| H&E | [data](https://tupac.grand-challenge.org/) | 73 | images + locations | seg | patch | 40x (from TCGA) Leica SCN400 | 2019
UniToPatho [56] | Colon | H&E | [data](https://github.com/EIDOSlab/UNITOPATHO), [paper](https://ieeexplore.ieee.org/document/9506198) | 9.536 from 292 wsi | images + label (6 classes) | classi | patch | 20x - Hamamatsu Nanozoomer S210 | 2021
UPENN-GBM [82] | glioblastoma | H&E | [data](https://www.cancerimagingarchive.net/collection/upenn-gbm/),[paper](https://www.nature.com/articles/s41597-022-01560-7) | 71 wsi from 34 patients | images + clinical data + mpMRI |  | WSI | 40x | 2022 
VisioMel | Melanoma | H&E | [data](https://www.drivendata.org/competitions/148/visiomel-melanoma/page/717/), [code](https://drivendata.co/blog/visiomel-melanoma-benchmark) | train: 1342 wsi, test: 600, valid: 1200, 16 WSIs annotated | images + annotation + clinical metadata + label | classi (2) |  |  |2023
WSSS4LUAD [53] | Lung | H&E | [data](https://wsss4luad.grand-challenge.org/), [paper](https://arxiv.org/pdf/2204.06455.pdf) | 87 (Train: 53, valid: 12, Test: 12) | Train: 10.091 patches, Valid: 40 patches, Test: 80 patches; image level for train, pixel level for test/valid | tissue semantic seg | wsi | (67 GDPH, 20 TCGA) | 2021

# References
[1a] Li, Zhang, et al. "Computer-aided diagnosis of lung carcinoma using deep learning-a pilot study." arXiv preprint arXiv:1803.05471 (2018).

[1b] Li, Zhang, et al. "Deep learning methods for lung cancer segmentation in whole-slide histopathology images—the acdc@ lunghp challenge 2019." IEEE Journal of Biomedical and Health Informatics 25.2 (2020): 429-440.

[2] Hosseini, Mahdi S., et al. "Atlas of digital pathology: A generalized hierarchical histological tissue type-annotated database for deep learning." Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition. 2019.

[3] Borovec, Jiří, et al. "ANHIR: automatic non-rigid histological image registration challenge." IEEE transactions on medical imaging 39.10 (2020): 3042-3052.

[4] Gamper, Jevgenij, and Nasir Rajpoot. "Multiple instance captioning: Learning representations from histopathology textbooks and articles." Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition. 2021.

[5] Aresta, Guilherme, et al. "Bach: Grand challenge on breast cancer histology images." Medical image analysis 56 (2019): 122-139.

[6] Xu, Feng, et al. "Predicting axillary lymph node metastasis in early breast cancer using deep learning on primary tumor biopsy slides." Frontiers in oncology 11 (2021): 759007.

[7] Amgad, Mohamed, et al. "Structured crowdsourcing enables convolutional segmentation of histology images." Bioinformatics 35.18 (2019): 3461-3467.

[8] Spanhol, Fabio A., et al. "A dataset for breast cancer histopathological image classification." Ieee transactions on biomedical engineering 63.7 (2015): 1455-1462.

[9] Aksac, Alper, et al. "BreCaHAD: a dataset for breast cancer histopathological annotation and diagnosis." BMC research notes 12.1 (2019): 1-3.

[10] Bejnordi, Babak Ehteshami, et al. "Diagnostic assessment of deep learning algorithms for detection of lymph node metastases in women with breast cancer." Jama 318.22 (2017): 2199-2210.

[11] Bandi, Peter, et al. "From detection of individual metastases to classification of lymph node status at the patient level: the camelyon17 challenge." IEEE transactions on medical imaging 38.2 (2018): 550-560.

[12] Litjens, Geert, et al. "1399 H&E-stained sentinel lymph node sections of breast cancer patients: the CAMELYON dataset." GigaScience 7.6 (2018): giy065.

[13] Kwanyoung Lee, Hyungjo Byun, Hyunjung Shim Proceedings of The Cell Segmentation Challenge in Multi-modality High-Resolution Microscopy Images, PMLR 212:1-11, 2023. 

[14] Graham, Simon, et al. "Conic: Colon nuclei identification and counting challenge 2022." arXiv preprint arXiv:2111.14485 (2021).

[15] Graham, Simon, et al. "Hover-net: Simultaneous segmentation and classification of nuclei in multi-tissue histology images." Medical Image Analysis 58 (2019): 101563.

[16] Vu, Quoc Dang, et al. "Methods for segmentation and classification of digital microscopy tissue images." Frontiers in bioengineering and biotechnology (2019): 53.

[17] Vu, Quoc Dang, et al. "Methods for segmentation and classification of digital microscopy tissue images." Frontiers in bioengineering and biotechnology (2019): 53.

[18] Graham, Simon, et al. "MILD-Net: Minimal information loss dilated network for gland instance segmentation in colon histology images." Medical image analysis 52 (2019): 199-211.

[19] Sirinukunwattana, Korsuk, et al. "Locality sensitive deep learning for detection and classification of nuclei in routine colon cancer histology images." IEEE transactions on medical imaging 35.5 (2016): 1196-1206.

[20] Javed, Sajid, et al. "Cellular community detection for tissue phenotyping in colorectal cancer histology images." Medical image analysis 63 (2020): 101696.

[21] Mahbod, Amirreza, et al. "CryoNuSeg: A dataset for nuclei instance segmentation of cryosectioned H&E-stained histological images." Computers in biology and medicine 132 (2021): 104349.

[22] Li, Jiahui, et al. "Signet ring cell detection with a semi-supervised learning framework." International conference on information processing in medical imaging. Springer, Cham, 2019.

[23] Li, Jiahui, et al. "Signet ring cell detection with a semi-supervised learning framework." International conference on information processing in medical imaging. Springer, Cham, 2019.

[24] Sirinukunwattana, Korsuk, et al. "Gland segmentation in colon histology images: The glas challenge contest." Medical image analysis 35 (2017): 489-502.

[25] Arvaniti, Eirini, et al. "Automated Gleason grading of prostate cancer tissue microarrays via deep learning." Scientific reports 8.1 (2018): 1-11.

[26]

[27a] Conde-Sousa, Eduardo, et al. "HEROHE Challenge: assessing HER2 status in breast cancer without immunohistochemistry or in situ hybridization." arXiv preprint arXiv:2111.04738 (2021).

[27b] La Barbera, David, et al. "Detection of her2 from haematoxylin-eosin slides through a cascade of deep learning classifiers via multi-instance learning." Journal of Imaging 6.9 (2020): 82.

[28]

[29] Kather, Jakob Nikolas, Halama, Niels, & Marx, Alexander. (2018). 100,000 histological images of human colorectal cancer and healthy tissue (v0.1) [Data set]. Zenodo. https://doi.org/10.5281/zenodo.1214456

[30] Kather, Jakob Nikolas, et al. "Deep learning can predict microsatellite instability directly from histology in gastrointestinal cancer." Nature medicine 25.7 (2019): 1054-1056.

[31] Kumar, Neeraj, et al. "A dataset and a technique for generalized nuclear segmentation for computational pathology." IEEE transactions on medical imaging 36.7 (2017): 1550-1560.

[32] Graham, Simon, et al. "Lizard: a large-scale dataset for colonic nuclear instance segmentation and classification." Proceedings of the IEEE/CVF International Conference on Computer Vision. 2021.

[33] Swiderska-Chadaj, Zaneta, et al. "Learning to detect lymphocytes in immunohistochemistry with deep learning." Medical image analysis 58 (2019): 101547.

[34] Aubreville, Marc, et al. "Mitosis domain generalization in histopathology images--The MIDOG challenge." arXiv preprint arXiv:2204.03742 (2022).

[35] Aubreville, Marc, et al. "Mitosis domain generalization challenge (2021)." 25th International Conference on Medical Image Computing and Computer Assisted Intervention (MICCAI 2022). 2022.

[36] Verma, Ruchika, et al. "MoNuSAC2020: A multi-organ nuclei segmentation and classification challenge." IEEE Transactions on Medical Imaging 40.12 (2021): 3413-3423.

[37a] Kumar, Neeraj, et al. "A multi-organ nucleus segmentation challenge." IEEE transactions on medical imaging 39.5 (2019): 1380-1391.

[37b] Kumar, Neeraj, et al. "A dataset and a technique for generalized nuclear segmentation for computational pathology." IEEE transactions on medical imaging 36.7 (2017): 1550-1560.

[38] Naylor, Peter, et al. "Segmentation of nuclei in histopathology images by deep regression of the distance map." IEEE transactions on medical imaging 38.2 (2018): 448-459.

[39] Amgad, Mohamed, et al. "Nucls: A scalable crowdsourcing, deep learning approach and dataset for nucleus classification, localization and segmentation." arXiv preprint arXiv:2102.09099 (2021).

[40] Kim, Yoo Jung, et al. "PAIP 2019: Liver cancer segmentation challenge." Medical Image Analysis 67 (2021): 101854.

[41] 

[42] Nateghi, Ramin, and Fattaneh Pourakpour. "Perineural Invasion Detection in Multiple Organ Cancer Based on Deep Convolutional Neural Network." arXiv preprint arXiv:2110.12283 (2021).

[43] Bulten, Wouter, et al. "Artificial intelligence for diagnosis and Gleason grading of prostate cancer: the PANDA challenge." Nature medicine 28.1 (2022): 154-163.

[44a] Gamper, Jevgenij, et al. "Pannuke: an open pan-cancer histology dataset for nuclei instance segmentation and classification." European congress on digital pathology. Springer, Cham, 2019.

[44b] Gamper, Jevgenij, et al. "Pannuke dataset extension, insights and baselines." arXiv preprint arXiv:2003.10778 (2020).

[45a] Veeling, Bastiaan S., et al. "Rotation equivariant CNNs for digital pathology." International Conference on Medical image computing and computer-assisted intervention. Springer, Cham, 2018.

[45b] Bejnordi, Babak Ehteshami, et al. "Diagnostic assessment of deep learning algorithms for detection of lymph node metastases in women with breast cancer." Jama 318.22 (2017): 2199-2210.

[46a] Gupta, Anubha, et al. "Segpc-2021: Segmentation of multiple myeloma plasma cells in microscopic images." IEEE Dataport 1.1 (2021): 1.

[46b] Gupta, Anubha, et al. "GCTI-SN: Geometry-inspired chemical and tissue invariant stain normalization of microscopic medical images." Medical Image Analysis 65 (2020): 101788.

[46c] Gehlot, Shiv, Anubha Gupta, and Ritu Gupta. "Ednfc-net: Convolutional neural network with nested feature concatenation for nuclei-instance segmentation." ICASSP 2020-2020 IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP). IEEE, 2020.

[46d] Gupta, Anubha, et al. "PCSeg: Color model driven probabilistic multiphase level set based tool for plasma cell segmentation in multiple myeloma." PloS one 13.12 (2018): e0207908.

[47] Petrick, Nicholas A., et al. "SPIE-AAPM-NCI BreastPathQ Challenge: an image analysis challenge for quantitative tumor cellularity assessment in breast cancer histology images following neoadjuvant treatment." Journal of Medical Imaging 8.3 (2021): 034501.

[48] R. L. Grossman, A. P. Heath, V. Ferretti, H. E. Varmus, D. R. Lowy, W. A. Kibbe, and L. M. Staudt. Toward a shared vision for cancer genomic data. New England Journal of Medicine, 375(12):1109–1112, 2016.

[49] Shephard, Adam, et al. "TIAger: Tumor-Infiltrating Lymphocyte Scoring in Breast Cancer for the TiGER Challenge." arXiv preprint arXiv:2206.11943 (2022).

[50] P. Naylor, M. Laé, F. Reyal and T. Walter, "Segmentation of Nuclei in Histopathology Images by Deep Regression of the Distance Map," in IEEE Transactions on Medical Imaging, vol. 38, no. 2, pp. 448-459, Feb. 2019, doi: 10.1109/TMI.2018.2865709

[51] Veta, Mitko, et al. "Predicting breast tumor proliferation from whole-slide images: the TUPAC16 challenge." Medical image analysis 54 (2019): 111-121.

[52] Veta, Mitko, et al. "Predicting breast tumor proliferation from whole-slide images: the TUPAC16 challenge." Medical image analysis 54 (2019): 111-121.

[53] Han, Chu, et al. "WSSS4LUAD: Grand Challenge on Weakly-supervised Tissue Semantic Segmentation for Lung Adenocarcinoma." arXiv preprint arXiv:2204.06455 (2022).

[54] Borkowski, Andrew A., et al. "Lung and colon cancer histopathological image dataset (lc25000)." arXiv preprint arXiv:1912.12142 (2019).

[55] Silva-Rodríguez, Julio, et al. "Going deeper through the Gleason scoring scale: An automatic end-to-end system for histology prostate grading and cribriform pattern detection." Computer Methods and Programs in Biomedicine 195 (2020): 105637.

[56] Barbano, Carlo Alberto, et al. "UniToPatho, a labeled histopathological dataset for colorectal polyps classification and adenoma dysplasia grading." 2021 IEEE International Conference on Image Processing (ICIP). IEEE, 2021.

[57] Zhu, Chuang, et al. "Hard Sample Aware Noise Robust Learning for Histopathology Image Classification." IEEE Transactions on Medical Imaging 41.4 (2021): 881-894.

[58] Koziarski, Michał, et al. "DiagSet: a dataset for prostate cancer histopathological image classification." arXiv preprint arXiv:2105.04014 (2021).

[59] Koohbanani, Navid Alemi, et al. "NuClick: a deep learning framework for interactive segmentation of microscopic images." Medical Image Analysis 65 (2020): 101771.

[60] Qaiser, Talha, et al. "Her 2 challenge contest: a detailed assessment of automated her 2 scoring algorithms in whole slide images of breast cancer tissues." Histopathology 72.2 (2018): 227-238.

[61] Sitnik, Dario, et al. "A dataset and a methodology for intraoperative computer-aided diagnosis of a metastatic colon cancer in a liver." Biomedical Signal Processing and Control 66 (2021): 102402.

[62] Brancati, Nadia, et al. "Bracs: A dataset for breast carcinoma subtyping in h&e histology images." arXiv preprint arXiv:2111.04740 (2021).

[63] Xu, Gang, et al. "Camel: A weakly supervised learning framework for histopathology image segmentation." Proceedings of the IEEE/CVF International Conference on Computer Vision. 2019.

[64] Komura, Daisuke, et al. "Universal encoding of pan-cancer histology by deep texture representations." Cell Reports 38.9 (2022): 110424.

[65] Shafiei, Sobhan, et al. "Colored Kimia Path24 Dataset: Configurations and Benchmarks with Deep Embeddings." arXiv preprint arXiv:2102.07611 (2021).

[66] Weitz, Philippe, et al. "ACROBAT-Automatic Registration of Breast Cancer Tissue."

[67] Matek, Christian, et al. "Human-level recognition of blast cells in acute myeloid leukaemia with convolutional neural networks." Nature Machine Intelligence 1.11 (2019): 538-544.

[68] Matek, Christian, et al. "Highly accurate differentiation of bone marrow cell morphologies using deep neural networks on a large image data set." Blood, The Journal of the American Society of Hematology 138.20 (2021): 1917-1927.

[69] Vrabac, Damir, et al. "DLBCL-Morph: Morphological features computed using deep learning for an annotated digital DLBCL image set." Scientific Data 8.1 (2021): 1-8.

[70] Farahmand, Saman, et al. "Deep learning trained on hematoxylin and eosin tumor region of Interest predicts HER2 status and trastuzumab treatment response in HER2+ breast cancer." Modern Pathology 35.1 (2022): 44-51.

[71] Pataki, Bálint Ármin, et al. "HunCRC: annotated pathological slides to enhance deep learning applications in colorectal cancer screening." Scientific Data 9.1 (2022): 1-7.

[72] Wilkinson, Scott, et al. "Nascent prostate cancer heterogeneity drives evolution and resistance to intense hormonal therapy." European urology 80.6 (2021): 746-757.

[73a] Wang, Ching-Wei, et al. "Histopathological whole slide image dataset for classification of treatment effectiveness to ovarian cancer." Scientific Data 9.1 (2022): 1-5.

[73b] Wang, Ching-Wei, et al. "Weakly supervised deep learning for prediction of treatment effectiveness on ovarian cancer from histopathology images." Computerized Medical Imaging and Graphics 99 (2022): 102093.

[74] Peikari, Mohammad, et al. "Automatic cellularity assessment from post‐treated breast surgical specimens." Cytometry Part A 91.11 (2017): 1078-1087.

[75] Campanella, Gabriele, et al. "Clinical-grade computational pathology using weakly supervised deep learning on whole slide images." Nature medicine 25.8 (2019): 1301-1309.

[76] Saltz, Joel, et al. "Spatial organization and molecular correlation of tumor-infiltrating lymphocytes using deep learning on pathology images." Cell reports 23.1 (2018): 181-193.

[77] Lonsdale, John, et al. "The genotype-tissue expression (GTEx) project." Nature genetics 45.6 (2013): 580-585.

[78] Ryu, Jeongun, et al. "OCELOT: Overlapped Cell on Tissue Dataset for Histopathology." Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition. 2023.

[79] Jerry Wei, Arief Suriawinata, Bing Ren, Xiaoying Liu, Mikhail Lisovsky, Louis Vaickus, Charles Brown, Michael Baker, Naofumi Tomita, Lorenzo Torresani, Jason Wei, Saeed Hassanpour, “A Petri Dish for Histopathology Image Analysis”, International Conference on Artificial Intelligence in Medicine (AIME), 12721:11-24, 2021. 

[80] Do, Tuong, et al. "Multiple meta-model quantifying for medical visual question answering." Medical Image Computing and Computer Assisted Intervention–MICCAI 2021: 24th International Conference, Strasbourg, France, September 27–October 1, 2021, Proceedings, Part V 24. Springer International Publishing, 2021.

[81a] Oliveira, S.P., Neto, P.C., Fraga, J., Montezuma, D., Monteiro, A., Monteiro, J., Ribeiro, L., Gonçalves, S., Pinto, I.M. and Cardoso, J.S., 2021. CAD systems for colorectal cancer from WSI are still not ready for clinical acceptance. Scientific Reports, 11(1), pp.1-15. https://doi.org/10.1038/s41598-021-93746-z

[81b] Neto, P.C., Oliveira, S.P., Montezuma, D., Fraga, J., Monteiro, A., Ribeiro, L., Gonçalves, S., Pinto, I.M. and Cardoso, J.S., 2022. iMIL4PATH: A semi-supervised interpretable approach for colorectal whole-slide images. Cancers, 14(10). https://doi.org/10.3390/cancers14102489

[81c] Neto, P.C., Montezuma, D., Oliveira, S.P., Oliveira, D., Fraga, J., Monteiro, A., Monteiro, J., Ribeiro, L., Gonçalves, S., Reinhard, S., Zlobec ,I. , Pinto, I.M. and Cardoso, J.S., 2024. An interpretable machine learning system for colorectal cancer diagnosis from pathology slides. npj Precision Oncology. https://doi.org/10.1038/s41698-024-00539-4

[82] Bakas, Spyridon, et al. "The University of Pennsylvania glioblastoma (UPenn-GBM) cohort: advanced MRI, clinical, genomics, & radiomics." *Scientific data* 9.1 (2022): 453.

[83] Madabhushi, A., & Feldman, M. (2016). **Fused Radiology-Pathology Prostate Dataset (Prostate Fused-MRI-Pathology)** . The Cancer Imaging Archive. doi; [10.7937/k9/TCIA.2016.tlpmr1am](http://doi.org/10.7937/k9/TCIA.2016.tlpmr1am)

[84] Tolkach, Yuri, et al. "Artificial intelligence for tumour tissue detection and histological regression grading in oesophageal adenocarcinomas: a retrospective algorithm development and validation study." *The Lancet Digital Health* 5.5 (2023): e265-e275.

[85] Mengdan Zhu, Bing Ren, Ryland Richards, Matthew Suriawinata, Naofumi Tomita, Saeed Hassanpour, "Development and Evaluation of a Deep Neural Network for Histologic Classification of Renal Cell Carcinoma on Biopsy and Surgical Resection Slides", Scientific Reports;11:7080 (2021).

[86] Jason Wei, Laura Tafe, Yevgeniy Linnik, Louis Vaickus, Naofumi Tomita, Saeed Hassanpour, "Pathologist-level Classification of Histologic Patterns on Resected Lung Adenocarcinoma Slides with Deep Neural Networks", Scientific Reports;9:3358 (2019).

[87] Daisuke Komura, Takumi Onoyama, Koki Shinbo, Hiroto Odaka, Minako Hayakawa, Mieko Ochi, Ranny Rahaningrum Herdiantoputri, Haruya Endo, Hiroto Katoh, Tohru Ikeda, Tetsuo Ushiku, Shumpei Ishikawa,
Restaining-based annotation for cancer histology segmentation to overcome annotation-related limitations among pathologists, Patterns, Volume 4, Issue 2, 2023, 100688, https://doi.org/10.1016/j.patter.2023.100688.

[88] Wilm, Frauke, Fragoso, Marco, Marzahl, Christian, Qiu, Jingna, Puget, Chloé, Diehl, Laura, Bertram, Christof A., Klopfleisch, Robert, Maier, Andreas, Breininger, Katharina and Aubreville, Marc. "Pan-tumor CAnine cuTaneous Cancer Histology (CATCH) dataset". Sci Data 9, 588 (2022). https://doi.org/10.1038/s41597-022-01692-w

[89] Bertram, Christof A., Aubreville, Marc, Marzahl, Christian, Maier, Andreas and Klopfleisch, Robert. "A large-scale dataset for mitotic figure assessment on whole slide images of canine cutaneous mast cell tumor". Sci Data 6, 274 (2019). https://doi.org/10.1038/s41597-019-0290-4

[90] Aubreville, Marc, Bertram, Christof A., Donovan, Taryn A., Marzahl, Christian, Maier, Andreas and Klopfleisch, Robert. "A completely annotated whole slide image dataset of canine breast cancer to aid human breast cancer research". Sci Data 7, 417 (2020). https://doi.org/10.1038/s41597-020-00756-z  

[91] Wilm, Frauke et al. "Pan-tumor T-lymphocyte detection using deep neural networks: Recommendations for transfer learning in immunohistochemistry". Journal of Pathology Informatics. Vol. 14, 100301 (2023).

[92] Wilm, Frauke, Fragoso, Marco, Bertram, Christof A., Stathonikos, Nikolas, Öttl, Mathias, Qiu, Jingna, Klopfleisch, Robert, Maier, Andreas, Breininger, Katharina and Aubreville, Marc. Proceedings of the German Workshop on Medical Image Processing (BVM), pp 206–211 (2023). 

[93] Aubreville Marc, Wilm, Frauke et al. "A comprehensive multi-domain dataset for mitotic figure detection". Sci Data 10, 484 (2023). https://doi.org/10.1038/s41597-023-02327-4 

[94] Paul Cohen, Joseph, et al. "Count-ception: Counting by fully convolutional redundant counting." Proceedings of the IEEE International conference on computer vision workshops. 2017. https://doi.org/10.1109/ICCVW.2017.9

# Search
- [Google Dataset Research](https://datasetsearch.research.google.com/search?src=0&query=histology&docid=L2cvMTFqbl8zcWY5ag%3D%3D)
- [Kaggle](https://www.kaggle.com/search?q=histology)
- [Zenodo](https://zenodo.org/search?page=1&size=20&q=dataset%20histology)
- [Grand Challenge](https://grand-challenge.org/)
- [Warwick](https://warwick.ac.uk/fac/cross_fac/tia/data/)
- [Cancer Imaging Archive](https://www.cancerimagingarchive.net/histopathology-imaging-on-tcia/)
- [GDC Data Portal](https://portal.gdc.cancer.gov/repository?facetTab=files&filters=%7B%22op%22%3A%22and%22%2C%22content%22%3A%5B%7B%22op%22%3A%22in%22%2C%22content%22%3A%7B%22field%22%3A%22files.data_category%22%2C%22value%22%3A%5B%22biospecimen%22%5D%7D%7D%2C%7B%22op%22%3A%22in%22%2C%22content%22%3A%7B%22field%22%3A%22files.data_type%22%2C%22value%22%3A%5B%22Slide%20Image%22%5D%7D%7D%5D%7D)
- [Kimia Lab](https://kimialab.uwaterloo.ca/kimia/index.php/data-and-code-2/)
- [Data Mendeley](https://data.mendeley.com/research-data/?type=DATASET&search=histology)
- [Harvard Dataverse](https://dataverse.harvard.edu/dataverse/harvard?q=histology)
- [Driven Data](https://www.drivendata.org/competitions/search/?category=health)
- [Deep Microscopy](https://deepmicroscopy.org/current-projects/)

# Author
Marie (Duc) Stettler
