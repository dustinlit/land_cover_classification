# Land Cover Classification Using CNN, Random Forest, adn Ensemble Methods

This python project uses satellite imagery from the SAT-4 dataset to classify land cover into four categories — **barren**, **trees**, **grassland**, and **other** — using machine learning. It combines a **Convolutional Neural Network (CNN)** for spatial feature extraction with a **Random Forest** classifier to enhance performance. NDVI is also calculated and used as an additional feature channel to improve vegetation differentiation.

---

## Project Structure

- `Land_Classification.ipynb` — Jupyter notebook containing the full analysis, model training, and evaluation  
- `combined_data.csv` — Results from hyperparameter tuning  
- `es_final.png` — Final loss/accuracy graph from early stopping  
- `requirements.txt` — List of required Python libraries  

---

## Models Implemented

- `CNN` model for end-to-end image classification  
- `Random Forest` model using flattened image input  
- `Ensemble` model combining CNN feature extraction with Random Forest classification  

---

## Key Features

- **NDVI Channel** added to raw satellite data to enhance vegetation detection  
- **Class imbalance** addressed using Scikit-learn’s `compute_class_weight`  
- **Early stopping** used to prevent overfitting  
- **Experiment tracking** across batch size, epochs, and optimizers  
- **Visual demonstration** of predictions (with red/green borders)  
- **Performance comparison** by class (accuracy, precision, recall, F1-score)

---

## Sample Results

| Class     | Best Model   | Accuracy |
|-----------|--------------|----------|
| Barren    | CNN          | 0.98     |
| Trees     | Ensemble     | 0.98     |
| Grassland | Ensemble     | 0.95     |
| Other     | Ensemble     | 0.99     |

---

## Demonstration

The notebook includes a demonstration loop that displays 100 random predictions, with a red border if incorrect and green if correct, along with the image's average NDVI.

---

## Conclusion

The **ensemble model** performed best overall, particularly in differentiating challenging classes like grasslands. Performance tracked closely with NDVI values, indicating strong alignment with physical vegetation patterns.

---

## Requirements

- Python 3.8+
- numpy
- pandas
- matplotlib
- seaborn
- scikit-learn
- tensorflow
- IPython

## Dataset

This project uses a **downsized version (1,000 images)** of the [SAT-4 dataset](https://csc.lsu.edu/~saikat/deepsat/) due to GitHub storage limitations. The full dataset includes **500,000+ labeled images**.

---

## Contact

**Dustin Littlefield**  
[LinkedIn Profile](https://www.linkedin.com/in/dustin-littlefield-629803323)  
<br>
**Email:** dustinlit@gmail.com

---

## License

This project is for **educational and demonstration purposes**. Please credit the author if reused.
