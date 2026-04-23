# 📝 LW4_Improving CNN Performance Using Regularization, Fine-Tuning, and Advanced Evaluation

🖇️**Collab Link Here:** https://colab.research.google.com/drive/144qb6dy_Vp9RJuLIYUa-bQQY3PyzAGvx#scrollTo=0e49067d
--

❓GUIDE QUESTIONS (Student Explanation & Reflection)📝
--
A. Model Evaluation Analysis
--
**1. What were the weakest-performing classes based on the confusion matrix?** <br>
💬Answer: Based on the confusion matrix, the weakest performing classes are the ones with fewer correct predictions. Vanda Baby Angel has only 274 correct which results it to become the lowest value and shows heavy confusion with vanda classes.<br>
**2. How did Precision, Recall, and F1-score vary across classes? **<br>
💬Answer: The metrics mostly mirror what you see in the confusion matrix. Classess that are clearly recognized like Cymbrium have high precision and recall, so their F1-scores are strong. But classes like Vanda Baby Angel or Oncostelopsis struggle more, because the model mixes them up with similar looking orchids, which leads to lower recall and sometimes lowwer precision too, which brings their F1-scores down. <br>
**3. What does a low recall indicate in your model?** <br>
💬Answer: A low recall basically means the model is missing some actual examples of that class. In other words, even when the class is present, the model may labels ot as something else. Usually because it looks too similar to the other classess or the model hasn't learned its features well enough. <br>
**4. How does AUC score reflect model performance compared to accuracy? **<br>
💬Answer: Accuracy will tell you how often the model is right, while AUC shows how well it separates the classess overall. So even if accuracy looks good, a lower AUC means the model still struggles to clearly determine classes. <br>

B. Model Improvement
--
**5. How did data augmentation affect validation accuracy? **<br>
💬Answer: Data augmentation usually improves validation accuracy by making the model better at handling variations. It helps prevent overfitting, so instead of just memorizing training images, the model generalizes better, and it will lead to stable and higher performance. <br>
**6. Why is Batch Normalization important in CNNs? **<br>
💬Answer: Batch Normalization is used in CNNs because it makes training a lot more stable and faster. Basically, it keeps the values inside the network from getting too large or too small as data flows through so the model doesn't have to keep adjusting to big changes while learning. <br>
**7. What role did Dropout play in improving your model?** <br>
💬Answer: Dropout helped improve the model by reducing overfitting. During training, it randomly "turns off" so the network can't rely too much on specific features or paths. This forces it to learn more generally instead of memorizing the training data, which usually leads to better performance on the unseen data.  <br>
**8. How did Early Stopping prevent overfitting?** <br>
💬Answer: It helps prevent overfitting by monitoring the model's performance on a validation set during training and stopping the process when that performance stops improving. So instead of letting the model keep training and start memorizing noise in the training data, it basically saves the version of the model that performed best on unseen data.  <br>

C. Performance Comparison
--
**9. What improvements were observed after modifying the model?** <br>
💬Answer: After modifying the model, the main improvement was better generalization, meaning it performed more consistently on unseen data. The traininng became more stable, overfitting was reduced, and the validation accuracy improved or became closer to the training accuracy. Overall, the model didn't just memorize the training set, it actually learned more useful patterns. <br>
**10. Which enhancement contributed the most to performance improvement? Why?** <br>
💬Answer: More likely from Early Stopping combined with Dropout. Because the Early Stopping prevents the model from overtraining and locking into noise, while Dropout forces it to learn more general features instead of relying on specific neurons. Between the two, Early Stopping hoften has the most noticeable impact because it directly stops overfitting at the right point, so you keep the best version of the model instead of a later worse one. <br>
**11. Did the gap between training and validation accuracy decrease? Explain.** <br>
💬Answer: Yes, the gap usually decreased after the improvements. Before adding things like Dropout, Batch Normalization, or Early Stopping, the model tends to perform much better on training data than on validation data, which is a sign of overfitting. After these changes, the model learns more general patterns and doesn't just memorize the training set, so the validaition accuracy gets closer to the training accuracy, making the gap smaller and the model more balanced. <br>

D. Explainability (Grad-CAM Integration)
--
**12. How did Grad-CAM help in understanding model predictions?** <br>
💬Answer: It helped by showing which parts of the image the CNN focused on when making a prediction. It creates a heatmap over the input image, highlighting the regions that contributed most to the model's decision. This makes it easier to understand whether the model is actually looking at meaningful features or getting distracted by irrelevant background noise, so you can better trust its predictions. <br>
**13. Did the improved model focus on more relevant regions? Provide evidence.** <br>
💬Answer: Yes, in most cases the improved model focused on more relevant regions. From the Grad-CAM visualizations, the heatmaps became more concentrated on the actual object of interes rather than scattered accross the background. Compared to the earlier model, which sometimes highlighted irrelevant areas, the improved version showed clearer and more focused activation on meaningful features, which aligns with its better validation performance.<br>
**14. Why is explainability important in real-world AI applications?** <br>
💬Answer: It is important because in real-world use, people need to trust and understand how an AI system makes decisions. It also helps developers detect biases or mistakes in the model, especially in sensitive areas like for example in health related scenarios where wrong predictions can have serious consequences. When you can explain what the model is focusing on, it's easier to improve it and make sure it's behaving correctly.  <br>
