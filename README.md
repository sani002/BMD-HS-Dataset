# BMD-HS Dataset: Heart Sound Recordings for Automated Cardiovascular Disease Diagnosis

The BMD-HS dataset is a groundbreaking collection of heart sound recordings, meticulously curated to enhance automated cardiovascular disease (CVD) diagnosis. This dataset contains over 800 recordings, classified into six categories, including common valvular diseases: Aortic Stenosis (AS), Aortic Regurgitation (AR), Mitral Regurgitation (MR),  Multi Disease (MD), and Mitral Stenosis (MS), along with healthy (Normal) samples.

## Key Features:
- **Multi-label annotations**: Allows nuanced classification by capturing unique disease states, including both single and multi-valvular diseases.
- **Echocardiographic data**: Includes echocardiographic (ECHO) data to provide additional diagnostic context, making the dataset more comprehensive for cardiovascular disease research.
- **Diverse demographic representation**: Recorded at the National Institute of Cardiovascular Disease, Dhaka, the dataset includes a gender-balanced collection of heart sounds, ensuring its relevance for healthcare in Bangladesh and similar regions.
- **Balanced class representation**: Recordings were collected from 20 healthy subjects and 20 subjects for each valvular disease class, addressing class imbalance issues.
- **Rich metadata**: Annotations include disease presence, severity, and demographic information, enabling in-depth research and potential discovery of new correlations.
- **Multi-disease data**: Includes patients with multiple valvular diseases, offering a complex dataset that reflects real-world scenarios where patients often suffer from more than one cardiovascular condition.

## Dataset Structure

### 1. Train Folder
- **Files**: Contains 872 `.wav` audio files.
- **Details**: Recordings were taken from 59 patients in 8 different positions, with each recording lasting 20 seconds. The recordings were sampled at a frequency of 4 kHz.

### 2. Train.csv
- **Purpose**: Contains training labels and corresponding recording file names for each patient.
- **Columns**:
  - **patient_id**: File names in the train folder.
  - **AS**: Label for Aortic Stenosis (0 = absent, 1 = present).
  - **AR**: Label for Aortic Regurgitation (0 = absent, 1 = present).
  - **MR**: Label for Mitral Regurgitation (0 = absent, 1 = present).
  - **MS**: Label for Mitral Stenosis (0 = absent, 1 = present).
  - **MD**: Label for multi-disease patients (0 = disease, 1 = normal).
  - **N**: Label for normal patients (0 = disease, 1 = normal).
  - **recording_1** to **recording_8**: File names for the 8 recordings corresponding to different positions for each patient.

### 3. Additional_metadata.csv
- **Purpose**: Provides supplemental information about patients, which can be used for enhancing predictions or making inferences.
- **Columns**:
  - **patient_id**: File names in the train folder.
  - **Age**: Age of the patient.
  - **Gender**: Gender of the patient (M = male, F = female).
  - **Smoker**: Smoking status (0 = does not smoke, 1 = smokes).
  - **Lives**: Living area of the patient (U = urban, F = rural).

### Key Points:
- **Preprocessing & Augmentation**: Due to the limited size of the training set, effective preprocessing and augmentation techniques are crucial.
- **Transfer Learning**: Leveraging external publicly available datasets for transfer learning is encouraged.
- **Metadata Utilization**: Finding correlations between the valvular disease classes and the provided metadata (age, gender, smoking status, living area) could improve model performance.

## Weaknesses:
- **Imbalanced Dataset**: Despite efforts to balance class representation, some variations in disease severity and demographics may still introduce imbalances, potentially affecting model training and performance.
  
## Potential Impact

The BMD-HS dataset represents a diverse demographic, making it particularly relevant for research and healthcare development in regions like Bangladesh. The inclusion of multi-label annotations, echocardiographic data, and comprehensive representation of cardiac health states holds significant promise for the advancement of AI-based diagnostic tools for cardiovascular diseases, especially in underserved regions.

---

This version includes the mention of echocardiographic data and multi-disease data as key features and highlights the dataset's potential imbalance as a weakness.

## Citations

If this dataset helped your research, please cite the following papers:

Ali, S. N., Zahin, A., Shuvo, S. B., Nizam, N. B., Nuhash, S. I. S. K., Razin, S. S., Sani, S. M. S., Rahman, F., Nizam, N. B., Azam, F. B., Hossen, R., Ohab, S., Noor, N., & Hasan, T. (2024). [BUET Multi-disease Heart Sound Dataset: A Comprehensive Auscultation Dataset for Developing Computer-Aided Diagnostic Systems.](https://doi.org/10.48550/arXiv.2409.00724) arXiv preprint arXiv:2409.00724.

>@article{Nafisa2024,<br />
  title={BUET Multi-disease Heart Sound Dataset: A Comprehensive Auscultation Dataset for Developing Computer-Aided Diagnostic Systems},<br />
  author={Ali, Shams Nafisa and Zahin, Afia and Shuvo, Samiul Based and Nizam, Nusrat Binta and Nuhash, Shoyad Ibn Sabur Khan and Razin, Sayeed Sajjad and Sani, S.M. Sakeef and Rahman, Farihin and Nizam, Nawshad Binta and Azam, Farhat Binte and Hossen, Rakib and Ohab, Sumaiya and Noor, Nawsabah and Hasan, Taufiq},<br />
  journal={arXiv preprint arXiv:2409.00724},<br />
  year={2024}<br />
}
