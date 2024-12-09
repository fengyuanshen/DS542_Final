# DS542 Final Project: Harnessing Transformers for Fraud Detection

**Author**: Fengyuan Shen

This repository contains the final project for the DS542 Deep Learning Course. The work focuses on utilizing a Transformer-based model to improve credit card fraud detection, addressing challenges such as severe class imbalance and complex transaction patterns. By leveraging techniques like SMOTE and Focal Loss, the project aims to enhance the minority-class recall (fraud detection) while maintaining robust performance on the majority class.

## Repository Contents

- **Final Report**:  
  - **DS542_Final_Project_Report.pdf**: A comprehensive document detailing the dataset, preprocessing steps, models, methodologies, experimental results, and conclusions.
  
- **Presentations & Video**:  
  - **DS542_Final_Project_Presentation.pdf** and **DS542_Final_Project_Presentation.pptx**: Slides outlining the project's objectives, approach, and findings.  
  - **DS542_Final_Project_Presentation.mp4**: A recorded presentation summarizing the project.

- **Code & Data**:  
  - **Final_Project.ipynb**: Jupyter Notebook implementing the data preprocessing, model training (including SMOTE, Focal Loss, and Transformer-based architecture), and evaluation procedures.  
  - **creditcard.zip**: The credit card fraud detection dataset used for the experiments.  
  - **results.pkl**: Serialized results from the experiments (e.g., model predictions and metrics).

- **Supporting Files**:  
  - **DS542_Final_Project_Latex**: Source LaTeX files for the final report. 
  - **Project Proposal**: The initial project proposal, outlining the motivation and intended approach. 
  - **images/**: Directory containing figures, confusion matrices, and visualizations used in the report and presentations. 
  - **Github_repo_link.txt**: A text file linking to this repository. 

## Key Techniques & Insights

- **Transformer Architecture**:  
  Unlike RNN-based methods, the Transformer captures both short- and long-range dependencies via self-attention, allowing efficient parallelization and potentially better handling of complex feature interactions.

- **SMOTE**:  
  Applied to the training set to mitigate the extreme class imbalance. By oversampling minority instances, the model gains a more balanced view of both classes, improving fraud recall.

- **Focal Loss**:  
  Experimented with various values of the \(\gamma\) parameter to place greater emphasis on hard-to-classify fraud cases. Identifying an optimal \(\gamma\) allowed the Transformer to surpass even a well-tuned Logistic Regression baseline in terms of minority-class recall.

- **Baseline Comparisons**:  
  Models such as Logistic Regression, Random Forest, MLP, and LSTM served as benchmarks. Although Logistic Regression performed surprisingly well after SMOTE, targeted tuning of the Transformer with Focal Loss enabled it to exceed the baseline’s minority-class detection capabilities.

## Results & Future Work

- **Results**:  
  The best-performing Transformer configuration achieved higher fraud recall than Logistic Regression while maintaining a competitive ROC AUC score. However, some trade-offs remain, as improving fraud detection slightly reduced non-fraud recall.

- **Future Directions**:  
  We did not employ a separate validation set in this project, opting instead to maximize minority-class usage. To enhance generalization and prevent overfitting, future work could explore time-series cross-validation or similar techniques. Additionally, integrating more interpretability methods and experimenting with advanced architectures or external data sources may further improve performance and provide actionable insights for fraud prevention.

## License

This project is licensed under the [MIT License](LICENSE).

## Contact

For questions or further information, please contact **[shenfy@bu.edu](mailto:shenfy@bu.edu)**.