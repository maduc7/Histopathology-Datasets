# Histopathology Datasets
Ressources of histopathology datasets

Dataset name | Organs | Staining | Link | Size | Data | Supervised | Task | WSI/Patch | Other (Magnification, Scanner) | year
--- | --- | --- | --- |--- |--- |--- |--- |--- |--- 
TCGA | Multiple | H&E | https://portal.gdc.cancer.gov/ | > 11k |  |  |  | WSI | 
CAMELYON16 | Lymph node | H&E | https://camelyon16.grand-challenge.org/ | Train: 270 (160 Normal, 110 with metastases); Test: 130 | images + binary masks | yes | classi + seg | WSI | slide level analysis | 2016
CAMELYON17 | Lymph node | H&E | https://camelyon17.grand-challenge.org/ | Train: 500 (100 patients, 5 slides each); Test: 500 | images + binary masks | yes | classi + seg | WSI | patient level analysis | 2017
PatchCamelyon	| Lymph node |	H&E |	https://patchcamelyon.grand-challenge.org/	| 327.680 |	images + binary label	| yes |	classi |	Patch (96x96) | 2018
BreakHis	| Breast |	H&E	| https://web.inf.ufpr.br/vri/databases/breast-cancer-histopathological-database-breakhis/ |	7.909 (2480 benign, 5429 malignant)	| images + binary label + tumor type (8) (different magnifications: 40x, 100x, 200x, 400x) |	yes |	classi |	Patch (700x460) | 40x, 100x, 200x, 400x | 2016
GlaS | Colorectal Cancer | H&E | https://warwick.ac.uk/fac/cross_fac/tia/data/glascontest/ | 165 | Train: 85 (37 benign, 48 malignant); Test: 80 (37 benign, 43 malignant) | yes | classi + seg | Patch (diff sizes - few hundred px) | 20x - Zeiss MIRAX MIDI | 2015
BACH + ICIA2018 | Breast | H&E | https://iciar2018-challenge.grand-challenge.org/Dataset/ | 400 | images (4 classes: normal 100, benign: 100, in situ carcinoma: 100, invasive carcinoma: 100) + 20 unlabeled + 10 labeled WSI (10 patients) | yes and no | classi + seg| Patch (classi, 2048x1536) + WSI (seg) | Leica SCN400 | 2018
TUPAC16 | Breast | H&E | https://tupac.grand-challenge.org/ | 500 | images + label | yes (wsi level) | classi | WSI | (from TCGA) | 2019
TUPAC16 - aux| Breast - mitoses| H&E | https://tupac.grand-challenge.org/ | 73 | images + locations | yes | seg | patch | 40x (from TCGA) Leica SCN400 | 2019
ANHIR | different | different | https://anhir.grand-challenge.org/ | 50+ sets| image + landmarks |  | registration | patch (15k x 15k to 50k x 50k) | 40x, 20x, 10x, different scanner | 2019
SPIE-AAPM_NCI BreastPathQ | Breast | H&E | https://breastpathq.grand-challenge.org/ | 2579 patch from 96 wsi (64 patients) | images + score | yes | regression | patches | 20x | 2019
ACDC-LungHP | Lung | H&E | https://acdc-lunghp.grand-challenge.org/ | Train: 150, Test: 50 | images + xml | yes | seg + classi | wsi | | 2019
LYON19 | Multiple (Breast, Colon, Protate) | IHC | https://lyon19.grand-challenge.org/ | 441 ROIs |  |  |  | patch | | 2019
DigestPath2019 - signet ring cell | Gastric, Intestine | H&E | https://digestpath2019.grand-challenge.org/ | Train: 460, Test: 226 | images + cell bounding boxes | partly yes (Train: 77, test: 27) | cell detection | patch (avg 2kx2k) | 40x | 2019
DigestPath2019 - colonoscopy tissue segment | Colon | H&E | https://digestpath2019.grand-challenge.org/ | Train: 660, Test: 212 | images + lesion annotation | seg + classi (benign vs malignant) | partly yes (train: 250, test: 90) | patch (avg 5kx5k) | 20x | 2019
HEROHE - ECDP2020 | Breast | H&E | https://ecdp2020.grand-challenge.org/Home/, https://arxiv.org/ftp/arxiv/papers/2111/2111.04738.pdf | Train: 359 (positive: 144, negatives: 215), Test: 150 (positive: 60, negative: 90) | images + binary label | yes | classi | wsi | 20x - 3D Histech Pannoramic 1000 | 2020
MoNuSAC 2020 | different (Lung, Prostate, Kidney, Breast) | H&E | https://monusac-2020.grand-challenge.org/, https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9446924 | 31.000 nuclei | images + mask | yes | seg + classi | patch | 40x | 2020
PanNuke | multiple (19) | H&E | https://warwick.ac.uk/fac/cross_fac/tia/data/pannuke, https://jgamper.github.io/PanNukeDataset/ | 189.744 nuclei (from >20k wsi) | images + nuclei (position + classi: neoplastic, connective, non-neoplastic epithelial, dead, inflammatory) | yes | seg + classi | patch | 40x | 2019
CoNSeP | | | | | | | | | |
CRCHisto | | | | | | | | | |
CPM-17 | | | | | | | | | |
ARCH | | | https://openaccess.thecvf.com/content/CVPR2021/papers/Gamper_Multiple_Instance_Captioning_Learning_Representations_From_Histopathology_Textbooks_and_Articles_CVPR_2021_paper.pdf, https://warwick.ac.uk/fac/cross_fac/tia/data/arch | | | | | | | 2020
HoVer-Net | | | https://warwick.ac.uk/fac/cross_fac/tia/data/hovernet/ | | | | nuclei seg | | | 2019
PAIP2020 | Colon | H&E | https://paip2020.grand-challenge.org/ | Train: 47, Valid: 31, Test: 40 | images + binary mask | yes | cancer seg | wsi | 40x - Aperio AT2 | 2020
PAIP2019 | Liver | H&E | https://paip2019.grand-challenge.org/ | Train: 50, Valid: 10, Test: 40 | images + binary mask | yes | cancer seg | wsi | 20x - Aperio AT2 | 2019
The PANDA challenge | Prostate | H&E | https://www.kaggle.com/c/prostate-cancer-grade-assessment/data | Train: 10.616, Valid: 393, Internal test: 545, External test: 1071 | images + label | yes | classi | wsi | slide level analysis | 2020
SegPC-2021 | Blood |  | https://segpc-2021.grand-challenge.org/ | | | | | | | 2021
PAIP2021 | Multiple (Colon, Prostate, Pancreas) | H&E | https://paip2021.grand-challenge.org/Rules/ | Train: 150, Valid: 30, Test: 60 | wsi + xml gt | yes/no | semantic seg | wsi | 20x - Aperio AT2 | 2021
NuCLS | Breast | H&E | https://nucls.grand-challenge.org/ | 220.000 nuclei from 3.944 roi from 125 patients | roi + bounding bx + classification | yes | nuclear detection + classi + seg | patch | (TCGA) | 2021
BCSS | Breast | H&E | https://bcsegmentation.grand-challenge.org/ | 151 wsi, 20.000 patch| patch + segmentation mask | yes | semantic seg | patch | (TCGA) | 2019
WSSS4LUAD | Lung | H&E | https://wsss4luad.grand-challenge.org/ | 87 (Train: 53, valid: 12, Test: 12) | Train: 10.091 patches, Valid: 40 patches, Test: 80 patches; image level for train, pixel level for test/valid | yes | tissue semantic seg | wsi | (67 GDPH, 20 TCGA) | 2021
Lizard | Colon | H&E | https://warwick.ac.uk/fac/cross_fac/tia/data/lizard/ | 495.179 nuclei | images + instance seg mask | yes | seg | patch | 20x (DigestPath + CRAG + GlaS + PanNuke + CoNSeP + TCGA) | 2021
CoNIC 2022 | Colon | H&E | https://conic-challenge.grand-challenge.org/ | 4981 patch with 431.913 nuclei of 6 types | image + instance seg mask + classi mask | yes | seg + classi + reg | patch (256x256) | 20x | 2022
BCNB | Breast | | https://bcnb.grand-challenge.org/ | 1058 (train 0.6, valid 0.2, test 0.2) | images + roi annotated + patient record | | | wsi | | 2021
ACROBAT 2022 | Breast | IHC + H&E | https://acrobat.grand-challenge.org/ | Train: 750 train; Valid: 100; Test: 300 | images (1 H&E match to 1-4 IHC) + landmarks | | wsi registration | | registration | wsi | | 2022
Cell Segmentation in Multimodality High resolution Microscopy Images |  |  | https://neurips22-cellseg.grand-challenge.org/ | | | | instance segmentation | | | 2022
TIGER | Breast | H&E | https://tiger.grand-challenge.org/ | | | | | | | 2022
MIDOG 2021 | Breast | H&E | https://imig.science/midog2021/ | 50 wsi / scanners - 4 scanners | | | | | | 2021
MIDOG 2022 | different (6 for train 10 for test) | H&E | https://midog2022.grand-challenge.org/ | Train: 405 cases, 9501 mitotic annotation | images + seg | yes | seg | Patch | | 2022
MoNuSeg | different (7) | H&E | https://monuseg.grand-challenge.org/Data/ | Train: 30, Test: 14 | images (Train: 22.000 nuclei, Test: 7000) + masks| yes | seg | Patch (1000x1000) | 40x (from TCGA) | 2018
Janowczyk et al. | Breast |  H&E | http://www.andrewjanowczyk.com/use-case-1-nuclei-segmentation/ | 143 | images (12.000 nuclei) + masks| yes | seg | Patch (2000x2000) | 40x | 2015
Wienert et al. | different (5) | H&E | https://www.nature.com/articles/srep00503 | 36 | images (7.931 nuclei) + masks | yes | seg | Patch (600x600) | 20x | 2012
Naylor et al. | Breast | H&E | https://zenodo.org/record/2579118#.Yt5FWt_RaUk | 50 | images (4.022 nuclei, 11 patients) + masks | yes | seg | Patch (512x512) | 40x | 2018
Gelasca et al. | Breast | H&E | https://bioimage.ucsb.edu/research/bio-segmentation | 50 | images (malignant/benignant, 1.895 nuclei) + masks | yes | classi + seg | Patch (896x768; 768x512) | |
