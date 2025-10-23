# Linking Keystrokes to Writing Processes and Language Quality

This project investigates how keystroke dynamics provide insights into writing quality. It explores automated essay scoring using behavioral features extracted from keystroke logs. The codebase includes all notebooks, scripts, and datasets used in the study.

The full codebase and project files are publicly available on Kaggle here:  
> [https://www.kaggle.com/code/chenglynyi/final-year-project-lyn-yi](https://www.kaggle.com/code/chenglynyi/final-year-project-lyn-yi)

---

## How to Access the Project

You have two ways to explore this project:

### Option 1: View Pre-Executed Notebook on Kaggle

If you just want to read through the project and see the results:

[Open the full notebook on Kaggle](https://www.kaggle.com/code/chenglynyi/keystroke-machine-pipeline)  

No setup required — everything has already been run.

---

### Option 2: Run It Yourself Locally

If you’d like to run the notebook on your own machine:
1. **Clone this GitHub repository:**
   ```bash
   git clone https://github.com/lynyi07/Keystroke-Machine-Learning-Pipeline.git
   cd Keystroke-Machine-Learning-Pipeline

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

5. Open `keystroke_ml_pipeline.ipynb ` and set the following variable:
   ```python
   KAGGLE = False
6. Execute all cells to reproduce the pipeline.

The full written report and appendix for this project are included below:

### Project Documentation

These documents provide detailed background, methodology, and evaluation results supporting the findings of this project.
- [Project Report (Final Write-Up)](project_report.pdf)  
- [Appendix (Supplementary Materials)](project_appendix.pdf)

### Usage Notes

This repository was developed as part of my final year individual project for the BSc Computer Science with a Year in Industry at King’s College London.
It’s intended for academic and non-commercial use only. Please don’t use any part of this work for commercial purposes without permission.

© 2025 Cheng Lyn Yi
