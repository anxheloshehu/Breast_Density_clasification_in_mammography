# Breast Density Assessment from Mammograms Using Statistical Features and a DNN

Breast density is a significant risk factor for breast cancer because it greatly affects the interpretability of mammograms,
as dense tissue can obscure tumors and reduce the sensitivityof screening. Therefore, automated and accurate assessment
of breast density has become a major focus of AI research inrecent years, in addition to cancer detection.

In this study, we propose a method for breast density determination that combines a static preprocessing pipeline with mathematically derived image features. Features such as histogram bimodality (Bm), ratio of dark-over-light pixel  (R\_DoL), and entropy measures (e2, Rel\_e), along with patient age, were extracted from mammograms to provide reliable and interpretable indicators of density classes. ANOVA analysis confirmed significant differences among density groups for the selected features.  

These features were then combined into a deep neural network model to classify mammograms into four classes (A, B, C, D) and two classes (AB vs CD). Using 5-Fold Stratified Cross-Validation with 3 runs each on the Mammomat Inspiration Device from the VinDr-Mammo dataset, the model achieved high performance and stability across folds, with weighted average metrics of accuracy $ACC = 82.77\% \pm 0.38$, AUC $AUC = 89.43\% \pm 0.235$, F1-score $F1 = 79.55.\% \pm 0.19$, and sensitivity $Sens = 82.77\% \pm 0.38$ for the four-class classification. For the two-class classification (AB vs CD), the model reached $ACC = 93.76\% \pm 0.18$, $AUC = 94.73\% \pm 0.205$, $F1 =92.62\% \pm 0.33$, and $Sens = 99.24\% \pm 0.195$.
