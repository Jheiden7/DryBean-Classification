# Dry Bean Classification

## [🔗 View the full notebook on Google Colab](https://colab.research.google.com/github/Jheiden7/DryBean-Classification/blob/main/DryBean%20Classification.ipynb)

## Information:

**Repository:** UCI Machine Learning.

[Dataset Link](https://archive.ics.uci.edu/dataset/602/dry+bean+dataset")

**Description:** Images of 13,611 grains from 7 different registered dry bean varieties were captured using a high-resolution camera. From these images, a total of 16 features were extracted — 12 related to dimensions and 4 to shape characteristics.

**Task to perform:** Classification

**Task Description:** The objective is to identify the type of bean (among the 7 possible classes) based on various geometric and dimensional attributes.

**Number of observations:** 13,611

**Attribute information:**

| Attribute               | Type        | Description                                                                                        |
| ----------------------- | ----------- | -------------------------------------------------------------------------------------------------- |
| **Area (A)**            | Numeric     | The area of the bean region, representing the number of pixels within its boundary.                |
| **Perimeter (P)**       | Numeric     | The circumference of the bean, defined as the total length of its contour.                         |
| **MajorAxisLength (L)** | Numeric     | The distance between the endpoints of the longest line that can be drawn across the bean.          |
| **MinorAxisLength (l)** | Numeric     | The longest line that can be drawn perpendicular to the major axis of the bean.                    |
| **AspectRatio (K)**     | Numeric     | The ratio between the major and minor axis lengths.                                                |
| **Eccentricity (Ec)**   | Numeric     | Eccentricity of the ellipse having the same second-moment characteristics as the bean region.      |
| **ConvexArea (C)**      | Numeric     | The number of pixels in the smallest convex polygon that encloses the bean surface.                |
| **EquivDiameter (Ed)**  | Numeric     | Diameter of a circle with the same area as the bean.                                               |
| **Extent (Ex)**         | Numeric     | Ratio between the area of the bean and the area of its bounding box.                               |
| **Solidity (S)**        | Numeric     | Also known as convexity. Ratio between the pixels in the convex hull and those in the bean region. |
| **Roundness (R)**       | Numeric     | Calculated using the formula $\frac{4πA}{P^2}$.                                                    |
| **Compactness (CO)**    | Numeric     | Measures how round the object is, defined as Ed/L.                                                 |
| **ShapeFactor1 (SF1)**  | Numeric     | —                                                                                                  |
| **ShapeFactor2 (SF2)**  | Numeric     | —                                                                                                  |
| **ShapeFactor3 (SF3)**  | Numeric     | —                                                                                                  |
| **ShapeFactor4 (SF4)**  | Numeric     | —                                                                                                  |
| **Class**               | Categorical | Seker, Barbunya, Bombay, Cali, Dermason, Horoz, and Sira                                           |

## Dry Bean Classes

<img src="https://miro.medium.com/v2/resize:fit:1400/1*Pasxnagn5s8t5fqPkKYLiQ.png" alt="Dry Beans" />

## Business Understanding:

In the agricultural and food industries, the classification of products like dry beans is a critical step for quality control, pricing, and trade. Traditionally, this process relies on manual inspection, which can be subjective, time-consuming, and prone to human error. Automating this classification using measurable physical properties ensures consistency, improves efficiency, and adds significant value to the supply chain. By developing a model that can accurately classify bean types based on their features, we can create a reliable and objective system for quality assurance.

With this in mind, the following analyses are proposed to understand the dataset and the relationships between the bean features and their classes:

 - **Feature Distribution by Bean Class:** Different types of beans are distinguished by unique physical characteristics. To build an effective classification model, we must first understand which features are most discriminative. By visualizing the distribution (e.g., using box plots or histograms) of key morphological features like `Area`, `Perimeter`, `Roundness`, and `Compactness` for each bean class, we can identify the primary physical traits that separate one type from another. This analysis is fundamental to understanding the basis for our classification.

- **Correlation Between Morphological Features:** The physical features of a bean are often interrelated. For example, a larger `Area` is likely to be correlated with a larger `Perimeter`. Understanding these relationships is crucial for feature selection and for avoiding multicollinearity in certain models. A correlation heatmap will be generated to visualize the strength and direction of the relationships between all pairs of features. This will help us understand the beans' underlying geometric properties and select a concise set of features for the model.

- **Class Balance Investigation:** In any classification problem, it is important to know the distribution of the target classes. If the dataset contains significantly more samples of one bean type than another, a model trained on this data may become biased towards the majority class, performing poorly on less common bean types. A bar chart showing the number of samples for each bean class will be created to assess whether the dataset is balanced. This is a critical step to ensure the final model is fair and reliable for all categories.

- **Visualizing Class Separability:** While looking at individual feature distributions is useful, it's also important to see how features interact. By creating scatter plots of the most discriminative pairs of features (e.g., `Compactness` vs. `Roundness`), with points colored by their bean class, we can visually assess the separability of the classes. This provides an intuitive understanding of the classification task's difficulty and helps in diagnosing where the model might struggle to distinguish between certain bean types.

