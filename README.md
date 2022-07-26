# <p align=center>`Histopathology Datasets for Machine Learning`</p>

This is a list of histopathology datasets made public on classification, segmentation, regression and registration tasks.

If you find any mistakes, you know of other datasets that are not listed here or anything else, please write an issue.

I hope this list will help some of you.

# Overview
- [Ressources](#ressources)
- [Classification](#classification)
- [Segmentation](#segmentation)
- [Regression](#regression)
- [Registration](#registration)
- [Organs](#organs)

# Ressources

Please find in the table below some link and information about histopathology dataset that are publicly available.

Dataset name | Organs | Staining | Link | Size | Data | Supervised | Task | WSI/Patch | Other (Magnification, Scanner) | year
--- | --- | --- | --- |--- |--- |--- |--- |--- |--- |---
ACDC-LungHP | Lung | H&E | [link data](https://acdc-lunghp.grand-challenge.org/), [link paper](https://ieeexplore.ieee.org/document/9265237) | Train: 150, Test: 50 | images + xml | yes | seg + classi | wsi | | 2019
ACROBAT 2022 | Breast | IHC + H&E | [link data](https://acrobat.grand-challenge.org/), [link paper](https://openreview.net/pdf?id=5TTocO2VI3r) | Train: 750 train; Valid: 100; Test: 300 | images (1 H&E match to 1-4 IHC) + landmarks | | registration | wsi | 40x - Hamamatsu | 2022
ANHIR | different | different | [link data](https://anhir.grand-challenge.org/), [link paper](https://ieeexplore.ieee.org/document/9058666) | 50+ sets| image + landmarks |  | registration | patch (15k x 15k to 50k x 50k) | 40x, 20x, 10x, different scanner | 2019
ARCH | | | [link data](https://warwick.ac.uk/fac/cross_fac/tia/data/arch), [link paper](https://openaccess.thecvf.com/content/CVPR2021/html/Gamper_Multiple_Instance_Captioning_Learning_Representations_From_Histopathology_Textbooks_and_Articles_CVPR_2021_paper.html) | | | | | | | 2020
BACH - ICIA2018 | Breast | H&E | [link data](https://iciar2018-challenge.grand-challenge.org/Dataset/), [link paper](https://www.sciencedirect.com/science/article/abs/pii/S1361841518307941) | 400 | images (4 classes: normal 100, benign: 100, in situ carcinoma: 100, invasive carcinoma: 100) + 20 unlabeled + 10 labeled WSI (10 patients) | yes and no | classi + seg| Patch (classi, 2048x1536) + WSI (seg) | Leica SCN400 | 2018
BCNB | Breast | | [link data](https://bcnb.grand-challenge.org/), [link paper](https://www.frontiersin.org/articles/10.3389/fonc.2021.759007/full) | 1058 (train 0.6, valid 0.2, test 0.2) | images + roi annotated + patient record | | | wsi | | 2021
BCSS | Breast | H&E | [link data](https://bcsegmentation.grand-challenge.org/), [link paper](https://academic.oup.com/bioinformatics/article/35/18/3461/5307750) | 151 wsi, 20.000 patch| patch + segmentation mask | yes | semantic seg | patch | (TCGA) | 2019
BreakHis	| Breast |	H&E	| [link data](https://web.inf.ufpr.br/vri/databases/breast-cancer-histopathological-database-breakhis/), [link paper](https://www.inf.ufpr.br/lesoliveira/download/TBME-00608-2015-R2-preprint.pdf) |	7.909 (2480 benign, 5429 malignant)	| images + binary label + tumor type (8) (different magnifications: 40x, 100x, 200x, 400x) |	yes |	classi |	Patch (700x460) | 40x, 100x, 200x, 400x | 2016
CAMELYON16 | Lymph node | H&E | [link data](https://camelyon16.grand-challenge.org/), [link paper](https://jamanetwork.com/journals/jama/article-abstract/2665774) | Train: 270 (160 Normal, 110 with metastases); Test: 130 | images + binary masks | yes | classi + seg | WSI | slide level analysis | 2016
CAMELYON17 | Lymph node | H&E | [link data](https://camelyon17.grand-challenge.org/), [link paper](https://ieeexplore.ieee.org/document/8447230) | Train: 500 (100 patients, 5 slides each); Test: 500 | images + binary masks | yes | classi + seg | WSI | patient level analysis | 2017
Cellseg |  |  | [link data](https://neurips22-cellseg.grand-challenge.org/) | | | | instance segmentation | | | 2022
CoNIC 2022 | Colon | H&E | [link data](https://conic-challenge.grand-challenge.org/), [link github](https://github.com/TissueImageAnalytics/CoNIC), [link paper](https://arxiv.org/pdf/2111.14485.pdf) | 4981 patch with 431.913 nuclei of 6 types | image + instance seg mask + classi mask | yes | seg + classi + reg | patch (256x256) | 20x | 2022
CoNSeP - HoVer-Net | Colorectal adenocarcinoma | H&E | [link data](https://warwick.ac.uk/fac/cross_fac/tia/data/hovernet/), [link paper](https://www.sciencedirect.com/science/article/abs/pii/S1361841519301045?via%3Dihub) | Train: 27 images, Test: 14 images, 24.319 nuclei | images + nuclei (location + class) | yes | instance seg + classi (7: other, inflammatory, healthy epithelial, dysplastic/malignant epithelial, figroblast, muscle, endothelial) | patch (1000x1000) |  | 2019
CPM-15 |  | H&E | [link data](https://drive.google.com/drive/folders/11ko-GcDsPpA9GBHuCtl_jNzWQl6qY_-I) | 15 | images + nuclei seg + label | yes | seg + classi | patch |  | 
CPM-17 |  | H&E | [link data](https://drive.google.com/drive/folders/1sJ4nmkif6j4s2FOGj8j6i_Ye7z9w0TfA) | Train: 32, test: 32 | images + nuclei seg + label | yes | seg + classi | patch (500x500) |  | 
CRC-TP | CRC | H&E | [link data](https://warwick.ac.uk/fac/cross_fac/tia/data/crc-tp), [link paper](https://www.sciencedirect.com/science/article/abs/pii/S136184152030061X?via%3Dihub) | 280k patches (from 20 wsi) | images + tissue phenotypes | yes | classification | patch |  | 2020
DigestPath2019 - signet ring cell | Gastric, Intestine | H&E | [link data](https://digestpath2019.grand-challenge.org/), [link paper](https://arxiv.org/pdf/1907.03954.pdf) | Train: 460, Test: 226 | images + cell bounding boxes | partly yes (Train: 77, test: 27) | cell detection | patch (avg 2kx2k) | 40x | 2019
DigestPath2019 - colonoscopy tissue segment | Colon | H&E | [link data](https://digestpath2019.grand-challenge.org/), [link paper](https://arxiv.org/pdf/1907.03954.pdf) | Train: 660, Test: 212 | images + lesion annotation | seg + classi (benign vs malignant) | partly yes (train: 250, test: 90) | patch (avg 5kx5k) | 20x | 2019
GlaS | Colorectal Cancer | H&E | [link data](https://warwick.ac.uk/fac/cross_fac/tia/data/glascontest/), [link paper](https://arxiv.org/pdf/1603.00275v2.pdf) | 165 | Train: 85 (37 benign, 48 malignant); Test: 80 (37 benign, 43 malignant) | yes | classi + seg | Patch (diff sizes - few hundred px) | 20x - Zeiss MIRAX MIDI | 2015
Gelasca et al. | Breast | H&E | [link data](https://bioimage.ucsb.edu/research/bio-segmentation), [link paper]() | 50 | images (malignant/benignant, 1.895 nuclei) + masks | yes | classi + seg | Patch (896x768; 768x512) | |
HEROHE - ECDP2020 | Breast | H&E | [link data](https://ecdp2020.grand-challenge.org/Home/), [link paper](https://arxiv.org/ftp/arxiv/papers/2111/2111.04738.pdf) | Train: 359 (positive: 144, negatives: 215), Test: 150 (positive: 60, negative: 90) | images + binary label | yes | classi | wsi | 20x - 3D Histech Pannoramic 1000 | 2020
Janowczyk et al. | Breast |  H&E | [link data](http://www.andrewjanowczyk.com/use-case-1-nuclei-segmentation/), [link github](https://github.com/choosehappy/public/tree/master/DL%20tutorial%20Code) | 143 | images (12.000 nuclei) + masks| yes | semantic seg | Patch (2000x2000) | 40x | 2015
Kumar | different (8) | H&E | [link data](https://drive.google.com/drive/folders/1bI3RyshWej9c4YoRW-_q7lh7FOFDFUrJ), [link paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7872382) | Train: 16 (13.372 nuclei), test same organ (4.130 nuclei): 8, test diff organ (4.121 nuclei): 6 | images + nuclei seg + label | yes | seg + classi | patch | 40x (TCGA) | 2017
Lizard | Colon | H&E | [link data](https://warwick.ac.uk/fac/cross_fac/tia/data/lizard/), [link paper](https://arxiv.org/pdf/2108.11195.pdf) | 495.179 nuclei | images + instance seg mask | yes | seg | patch | 20x (DigestPath + CRAG + GlaS + PanNuke + CoNSeP + TCGA) | 2021
LYON19 | Multiple (Breast, Colon, Protate) | IHC | [link data](https://lyon19.grand-challenge.org/), [link paper](https://www.sciencedirect.com/science/article/abs/pii/S1361841519300829) | 441 ROIs |  |  |  | patch | | 2019
MIDOG 2021 | Breast | H&E | [link data](https://imig.science/midog2021/the-dataset/), [link paper](https://arxiv.org/pdf/2204.03742.pdf) | 200 wsi: 50 wsi / scanners - 4 scanners | images + roi | | detection of mitotic figues | wsi | | 2021
MIDOG 2022 | different (6 for train 10 for test) | H&E | [link data](https://midog2022.grand-challenge.org/), [link paper]() | Train: 405 cases, 9501 mitotic annotation | images + seg | yes | seg | Patch | | 2022
MoNuSAC 2020 | different (Lung, Prostate, Kidney, Breast) | H&E | [link data](https://monusac-2020.grand-challenge.org/), [link paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9446924) | 31.000 nuclei | images + mask | yes | instance seg + classi | patch | 40x | 2020
MoNuSeg | different (7) | H&E | [link data](https://monuseg.grand-challenge.org/Data/), [link github](https://github.com/ruchikaverma-iitg/MoNuSeg), [link paper](https://ieeexplore.ieee.org/document/8880654) | Train: 30, Test: 14 | images (Train: 22.000 nuclei, Test: 7000) + masks| yes | instance seg | Patch (1000x1000) | 40x (from TCGA) | 2018
Naylor et al. | Breast | H&E | [link data](https://zenodo.org/record/2579118#.Yt5FWt_RaUk), [link paper](https://ieeexplore.ieee.org/document/8438559) | 50 | images (4.022 nuclei, 11 patients) + masks | yes | seg | Patch (512x512) | 40x | 2018
NuCLS | Breast | H&E | [link data](https://nucls.grand-challenge.org/), [link paper](https://arxiv.org/ftp/arxiv/papers/2102/2102.09099.pdf) | 220.000 nuclei from 3.944 roi from 125 patients | roi + bounding bx + classification | yes | nuclear detection + classi + seg | patch | (TCGA) | 2021
PAIP2019 | Liver | H&E | [link data](https://paip2019.grand-challenge.org/), [link paper](https://www.sciencedirect.com/science/article/pii/S1361841520302188) | Train: 50, Valid: 10, Test: 40 | images + binary mask | yes | cancer seg | wsi | 20x - Aperio AT2 | 2019
PAIP2020 | Colon | H&E | [link data](https://paip2020.grand-challenge.org/), [link github](https://github.com/wisepaip/paip2020) | Train: 47, Valid: 31, Test: 40 | images + binary mask | yes | cancer seg | wsi | 40x - Aperio AT2 | 2020
PAIP2021 | Multiple (Colon, Prostate, Pancreas) | H&E | [link data](https://paip2021.grand-challenge.org/Rules/), [link paper](https://arxiv.org/ftp/arxiv/papers/2110/2110.12283.pdf) | Train: 150, Valid: 30, Test: 60 | wsi + xml gt | yes/no | semantic seg | wsi | 20x - Aperio AT2 | 2021
The PANDA challenge | Prostate | H&E | [link data](https://www.kaggle.com/c/prostate-cancer-grade-assessment/data), [link paper](https://www.nature.com/articles/s41591-021-01620-2) | Train: 10.616, Valid: 393, Internal test: 545, External test: 1071 | images + label | yes | classi | wsi | slide level analysis | 2020
PanNuke | multiple (19) | H&E | [link data](https://warwick.ac.uk/fac/cross_fac/tia/data/pannuke), [link github](https://jgamper.github.io/PanNukeDataset/), [link paper](https://arxiv.org/pdf/2003.10778.pdf), [link paper](https://link.springer.com/chapter/10.1007/978-3-030-23937-4_2) | 189.744 nuclei (from >20k wsi) | images + nuclei (position + classi: neoplastic, connective, non-neoplastic epithelial, dead, inflammatory) | yes | instance seg + classi | patch | 40x | 2019
PatchCamelyon	| Lymph node |	H&E |	[link data](https://patchcamelyon.grand-challenge.org/), [link github](https://github.com/basveeling/pcam) [link paper](https://arxiv.org/pdf/1806.03962.pdf)	| 327.680 |	images + binary label	| yes |	classi |	Patch (96x96) | 10x | 2018
SegPC-2021 | Blood |  | [link data](https://segpc-2021.grand-challenge.org/), [link github](https://github.com/dsciitism/SegPC-2021), [link report](https://ieee-dataport.org/open-access/segpc-2021-segmentation-multiple-myeloma-plasma-cells-microscopic-images) | | | | | | | 2021
SPIE-AAPM_NCI BreastPathQ | Breast | H&E | [link data](https://breastpathq.grand-challenge.org/), [link paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8107263/) | 2579 patch from 96 wsi (64 patients) | images + score | yes | regression | patches | 20x | 2019
TCGA | Multiple | H&E | [link data](https://portal.gdc.cancer.gov/) | > 11k |  |  |  | WSI | 
TIGER | Breast | H&E | [link data](https://tiger.grand-challenge.org/) | | | | | | | 2022
TNBC | Breast | H&E | [link data](https://peterjacknaylor.github.io/data/), [link data](https://drive.google.com/drive/folders/1taB8boGyycjV4X1a2vCIAV9fwMxFSS41), [link paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=8438559) | 50 images, 4022 cells (11 patients) | images + nuclei seg + label | yes | seg + classi | patch (512x512) | 40x - Philips Ultra Fast Scanner | 2019
TUPAC16 | Breast | H&E | [link data](https://tupac.grand-challenge.org/), [link paper](https://arxiv.org/ftp/arxiv/papers/1807/1807.08284.pdf) | 500 | images + label | yes (wsi level) | classi | WSI | 40x (from TCGA) | 2019
TUPAC16 - aux| Breast - mitoses| H&E | [link data](https://tupac.grand-challenge.org/) | 73 | images + locations | yes | seg | patch | 40x (from TCGA) Leica SCN400 | 2019
WSSS4LUAD | Lung | H&E | [link data](https://wsss4luad.grand-challenge.org/), [link paper](https://arxiv.org/pdf/2204.06455.pdf) | 87 (Train: 53, valid: 12, Test: 12) | Train: 10.091 patches, Valid: 40 patches, Test: 80 patches; image level for train, pixel level for test/valid | yes | tissue semantic seg | wsi | (67 GDPH, 20 TCGA) | 2021

# Classification

# Regression

# Registration

# Organs
## Breast

## Colon

##

# Author
Marie Duc - PhD Student

email: marie.duc@med.uni-tuebingen.de
