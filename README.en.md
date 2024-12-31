# Pretherapeutic Tumor Board text model for Prostate Cancer Patients using Random Forest Classification

The aim of this project was to explore the capabilities of classical machine learning algorithms for urological tumor board prediction in the era of Deep Learning. The main goal was to train and validate a machine learning algorithm for automatic generation of tumor board recommendations using data from our institutional tumor board documentation system. Men diagnosed with prostate cancer are routinely referred to our pretherapeutic tumor board first as part of our certified comprehensive cancer center workflow. This guarantees multidisciplinary expertise and individually-tailored diagnostic and therapeutic recommendations for every patient.

The data was preprocessed using regular expression scripts as well as manually by our staff. Potential clinical predictors were extracted from the tumor board patient histories and stored as continuous or categorical variables in a dedicated database. The outcome variables were extracted the same way and stored as boolean variables. Since different recommendations are possible simultaneously, the final outcome variable was defined as a multi-label outcome.

We trained and tested three different multivariable machine learning algorithms best suited for multi-label classification tasks, Decision Tree, Random Forest and K-Nearest Neighbour. Input variables were age, PSA, DRE, ISUP category, number of positice biopsy cylinders, number of total biopsy cylinders and preexisting conditions (hypertension, diabetes mellitus, coronary artery disease, obesity, prior surgeries). Outcome variables were recommendations for PSMA-PET imaging, conventional imaging (CT and bone scintigraphy), active surveillance and local therapy (radical prostatectomy and radiation therapy).

All models were trained and validated by a train-test split of 80:20. Overall accuracy, precision, recall and f1-scores for each single outcome were evaluated in the test set. 95% confidence intervalls were calculated using bootstrap sampling with n=1000. The best model was finally saved in pickle format and used for a simple frontend web application for demonstration purposes.

The code for the web application can be accessed via this [repository](https://github.com/ukd-uro/pretb_rf_app) on this hub. The application itself is served via [Streamlit Community Cloud](https://pretb-rf.streamlit.app).

> [!Note]
> Feel free to contact us for questions or ideas on this or potential new projects.
