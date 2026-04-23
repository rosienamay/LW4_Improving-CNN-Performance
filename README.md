# 📝 LW4_Improving CNN Performance Using Regularization, Fine-Tuning, and Advanced Evaluation

🖇️**Collab Link Here:** https://colab.research.google.com/drive/144qb6dy_Vp9RJuLIYUa-bQQY3PyzAGvx#scrollTo=0e49067d
--

❓GUIDE QUESTIONS (Student Explanation & Reflection)📝
--
A. Model Evaluation Analysis
--
1. What were the weakest-performing classes based on the confusion matrix? <br>
💬Answer: Based on the confusion matrix, the weakest performing classes are the ones with fewer correct predictions. Vanda Baby Angel has only 274 correct which results it to become the lowest value and shows heavy confusion with vanda classes.<br>
2. How did Precision, Recall, and F1-score vary across classes? <br>
💬Answer: The metrics mostly mirror what you see in the confusion matrix. Classess that are clearly recognized like Cymbrium have high precision and recall, so their F1-scores are strong. But classes like Vanda Baby Angel or Oncostelopsis struggle more, because the model mixes them up with similar looking orchids, which leads to lower recall and sometimes lowwer precision too, which brings their F1-scores down. <br>
3. What does a low recall indicate in your model? <br>
💬Answer: A low recall basically means the model is missing some actual examples of that class. In other words, even when the class is present, the model may labels ot as something else. Usually because it looks too similar to the other classess or the model hasn't learned its features well enough. <br>
4. How does AUC score reflect model performance compared to accuracy? <br>
💬Answer: Accuracy will tell you how often the model is right, while AUC shows how well it separates the classess overall. So even if accuracy looks good, a lower AUC means the model still struggles to clearly determine classes. <br>

B. Model Improvement
--
5. How did data augmentation affect validation accuracy?
6. Why is Batch Normalization important in CNNs?
7. What role did Dropout play in improving your model?
8. How did Early Stopping prevent overfitting?

C. Performance Comparison
--
9. What improvements were observed after modifying the model?
10. Which enhancement contributed the most to performance improvement? Why?
11. Did the gap between training and validation accuracy decrease? Explain.

D. Explainability (Grad-CAM Integration)
--
12. How did Grad-CAM help in understanding model predictions?
13. Did the improved model focus on more relevant regions? Provide evidence.
14. Why is explainability important in real-world AI applications?
