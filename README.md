# Histopathology Datasets
Ressources of histopathology datasets

Dataset name | Organs | Staining | Link | Size | Data | Supervised | Task | WSI/Patch | Other
--- | --- | --- | --- |--- |--- |--- |--- |--- |--- 
TCGA | Multiple | H&E | https://portal.gdc.cancer.gov/ | > 11k |  |  |  | WSI | 
CAMELYON16 | Lymph node | H&E | https://camelyon16.grand-challenge.org/ | Train: 270 (160 Normal, 110 with metastases); Test: 130 | images + binary masks | yes | classi + seg | WSI | slide level analysis
CAMELYON17 | Lymph node | H&E | https://camelyon17.grand-challenge.org/ | Train: 500 (100 patients, 5 slides each); Test: 500 | images + binary masks | yes | classi + seg | WSI | patient level analysis | 
PatchCamelyon	| Lymph node |	H&E |	https://patchcamelyon.grand-challenge.org/	| 327.680 |	images + binary label	| yes |	classi |	Patch (96x96)
BreakHis	| Breast |	H&E	| https://web.inf.ufpr.br/vri/databases/breast-cancer-histopathological-database-breakhis/ |	7.909 (2480 benign, 5429 malignant)	| images + binary label + tumor type (8) (different magnifications: 40x, 100x, 200x, 400x) |	yes |	classi |	Patch (700x460)
GlaS | Colorectal Cancer | H&E | https://warwick.ac.uk/fac/cross_fac/tia/data/glascontest/ | 165 | Train: 85 (37 benign, 48 malignant); Test: 80 (37 benign, 43 malignant) | yes | classi + seg | Patch (diff sizes - few hundred px) | 20x
BACH | Breast | H&E | https://iciar2018-challenge.grand-challenge.org/Dataset/ | 400 | images (4 classes: normal 100, benign: 100, in situ carcinoma: 100, invasive carcinoma: 100) + 20 unlabeled + 10 labeled WSI (10 patients) | yes and no | classi + seg| Patch (classi, 2048x1536) + WSI (seg) |
TUPAC16 | Breast | H&E | https://tupac.grand-challenge.org/ | 500 | images + label | yes (wsi level) | classi | WSI | (from TCGA)
TUPAC16 - aux| Breast - mitoses| H&E | https://tupac.grand-challenge.org/ | 73 | images + locations | yes | seg | patch | 40x (from TCGA)
ICIAR 2018 | 
ANHIR | 
BreastPathQ |
ACDC-LungHP | 
LYON19 | 
RAIP 2019 | 
DigestPath2019 | 
HEROHE | 
MoNuSAC 2020 | 
RAIP2020 |
The PANDA challenge | 
SegPC-2021 | 
PAIP2021 | 
NuCLS | 
Breast Cancer Segmentation | 
WSSS4LUAD  
MIDOG Challenge 2021 | 
Lizard | Colon | H&E | https://warwick.ac.uk/fac/cross_fac/tia/data/lizard/ | 495.179 nuclei | images + instance seg mask | yes | seg | patch | 20x (DigestPath + CRAG + GlaS + PanNuke + CoNSeP + TCGA)
CoNIC 2022 | Colon | H&E | https://conic-challenge.grand-challenge.org/ | 4981 patch with 431.913 nuclei of 6 types | image + instance seg mask + classi mask | yes | seg + classi + reg | patch (256x256) | 20x
BCNB | Breast | | https://bcnb.grand-challenge.org/ | 1058 (train 0.6, valid 0.2, test 0.2) | images + roi annotated + patient record | | | wsi | 
ACROBAT 2022 | Breast | IHC + H&E | https://acrobat.grand-challenge.org/ | Train: 750 train; Valid: 100; Test: 300 | images (1 H&E match to 1-4 IHC) + landmarks | | wsi registration | | registration | wsi | 
Cell Segmentation in Multimodality High resolution Microscopy Images |  |  | https://neurips22-cellseg.grand-challenge.org/ | | | | instance segmentation | | 
TIGER | Breast | H&E | https://tiger.grand-challenge.org/ | 
MIDOG 2022 | different (6 for train 10 for test) | H&E | https://midog2022.grand-challenge.org/ | Train: 405 cases, 9501 mitotic annotation | images + seg | yes | seg | Patch | 
MoNuSeg | different (7) | H&E | https://monuseg.grand-challenge.org/Data/ | Train: 30, Test: 14 | images (Train: 22.000 nuclei, Test: 7000) + masks| yes | seg | Patch (1000x1000) | 40x (from TCGA)
Janowczyk et al. | Breast |  H&E | http://www.andrewjanowczyk.com/use-case-1-nuclei-segmentation/ | 143 | images (12.000 nuclei) + masks| yes | seg | Patch (2000x2000) | 40x
Wienert et al. | different (5) | H&E | https://www.nature.com/articles/srep00503 | 36 | images (7.931 nuclei) + masks | yes | seg | Patch (600x600) | 20x
Naylor et al. | Breast | H&E | https://zenodo.org/record/2579118#.Yt5FWt_RaUk | 50 | images (4.022 nuclei, 11 patients) + masks | yes | seg | Patch (512x512) | 40x
Gelasca et al. | Breast | H&E | https://bioimage.ucsb.edu/research/bio-segmentation | 50 | images (malignant/benignant, 1.895 nuclei) + masks | yes | classi + seg | Patch (896x768; 768x512) |
