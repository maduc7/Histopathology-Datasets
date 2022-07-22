# Histopathology Datasets
Ressources of histopathology datasets

Dataset name | Organs | Staining | Link | Size | Data | Supervised | Task | WSI/Patch | Other 
--- | --- | --- | --- |--- |--- |--- |--- |--- |--- 
TCGA | Multiple | H&E | https://portal.gdc.cancer.gov/ | > 11k |  |  |  | WSI | 
CAMELYON16 | Lymph node | H&E | https://camelyon16.grand-challenge.org/ | Train: 270 (160 Normal, 110 with metastases); Test: 130 | images + binary masks | yes | classi + seg | WSI | slide level analysis
CAMELYON17 | Lymph node | H&E | https://camelyon17.grand-challenge.org/ | Train: 500 (100 patients, 5 slides each); Test: 500 | images + binary masks | yes | classi + seg | WSI | patient level analysis
PatchCamelyon	| Lymph node |	H&E |	https://patchcamelyon.grand-challenge.org/	| 327.680 |	images + binary label	| yes |	classi |	Patch (96x96)
BreakHis	| Breast |	H&E	| https://web.inf.ufpr.br/vri/databases/breast-cancer-histopathological-database-breakhis/ |	7.909 (2480 benign, 5429 malignant)	| images + binary label + tumor type (8) (different magnifications: 40x, 100x, 200x, 400x) |	yes |	classi |	Patch (700x460)
GlaS
BACH
MoNuSeg
TUPAC16
