# Linking Keystrokes to Writing Processes and Language Quality

# Overview

This project investigates whether how someone writes can be used to predict how well they write. Instead of relying solely on the finished essay, the study examines the writing process itself through keystroke dynamics. These real time behavioural traces provide insight into planning, fluency, revision patterns and cognitive effort that are not captured in the final written product.

The study uses the publicly available [Linking Writing Processes to Writing Quality](https://www.kaggle.com/competitions/linking-writing-processes-to-writing-quality) dataset, which contains 2,471 timed student writing sessions. From the keystroke logs, a large and diverse set of 1,226 behavioural features was engineered to represent the temporal and structural evolution of writing as it unfolds. These features were combined with a comprehensive machine learning workflow that includes data filtering, model optimisation and interpretability analysis.

The results demonstrate that writing behaviour can contribute meaningfully to automated essay scoring by revealing aspects of writing quality that are not available from text alone. 

# Methodology Summary
<p align="center">
  <img src="assets\pipeline-diagram.png" alt="ML Pipeline Diagram" width="600"><br>
</p>

More detail can be found in the full written report and appendix for this project: 
- [Project Report (Final Write-Up)](project_report.pdf)  
- [Appendix (Supplementary Materials)](project_appendix.pdf)
 
They provide detailed background, methodology, and evaluation results supporting the findings of this project.

# How to Access the Project

You have two ways to explore this project:

## Option 1: View Pre-Executed Notebook on Kaggle

If you just want to read through the project and see the results:

[Open the full notebook on Kaggle](https://www.kaggle.com/code/chenglynyi/keystroke-machine-pipeline)  

No setup required — everything has already been run.

## Option 2: Run It Yourself Locally

If you’d like to run the notebook on your own machine:
1. **Clone this GitHub repository:**
   ```bash
   git clone https://github.com/lynyi07/Keystroke-Machine-Learning-Pipeline.git
   cd Keystroke-Machine-Learning-Pipeline
   ```

2. Download the required datasets:
   - **Preprocessed Dataset (lynyi-data)**:  
     [https://www.kaggle.com/datasets/chenglynyi/lynyi-data](https://www.kaggle.com/datasets/chenglynyi/lynyi-data)

   - **Competition Dataset**:  
     [https://www.kaggle.com/competitions/linking-writing-processes-to-writing-quality](https://www.kaggle.com/competitions/linking-writing-processes-to-writing-quality)

3. Place the files to match the following structure:
    ```
    ├── keystroke_ml_pipeline.ipynb         # Main Jupyter Notebook
    ├── project_report.pdf                      # Project write up 
    ├── project_appendix.pdf                    # Additional Information for write up 
    ├── requirements.txt    
    ├── README.md                               
    ├── input/
    │   └── linking-writing-processes-to-writing-quality/
    │       ├── test_logs.csv                   # Raw test keystroke logs
    │       ├── train_logs.csv                  # Raw train keystroke logs
    │       └── train_scores.csv                # Training essay scores
    │   └── my-data/
    │       ├── ext_df.pickle                       # External essay data
    │       ├── features_summary.csv                # Engineered features descriptions 
    │       ├── preprocessors.pickle                # Preprocessor object
    │       ├── preprocessors_event.pickle          # Event-specific preprocessor 
    │       ├── test_df_preprocessed.pickle         # Preprocessed test feature data
    │       ├── test_log_df_preprocessed.pickle     # Preprocessed test log data
    │       ├── train_df_preprocessed.pickle        # Preprocessed training feature data
    │       └── train_log_df_preprocessed.pickle    # Preprocessed training log data

4. Set up your environment and install dependencies:
    ```bash
    # Step 1: Create a virtual environment
    python -m venv venv

    # Step 2: Activate the virtual environment
    # macOS/Linux
    source venv/bin/activate
    # Windows
    venv\Scripts\activate

    # Step 3: Install dependencies
    pip install -r requirements.txt
    ```

5. Open `keystroke_ml_pipeline.ipynb ` and set the following variable:
   ```python
   KAGGLE = False
   ```
6. Execute all cells to reproduce the pipeline.


# Usage Notes

This repository was developed as part of my final year individual project for the BSc Computer Science with a Year in Industry at King’s College London.
It is intended for academic and non-commercial use only. Please do not use any part of this work for commercial purposes without permission.

