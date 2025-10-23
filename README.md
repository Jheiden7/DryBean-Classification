# DryBean-Classification

## [🔗 View the full notebook on Google Colab](https://colab.research.google.com/github/Jheiden7/DryBean-Classification/blob/main/DryBean%20Classification.ipynb)

<a href="https://archive.ics.uci.edu/dataset/602/dry+bean+dataset">Dataset Link</a>

**Description:**

Images of 13,611 grains from 7 different registered dry bean varieties were captured using a high-resolution camera. From these images, a total of 16 features were extracted — 12 related to dimensions and 4 to shape characteristics.

**Task Type:**

Classification

**Task Description:**

The objective is to identify the type of bean (among the 7 possible classes) based on various geometric and dimensional attributes.

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

**Dry Bean Classes**

<img src="https://miro.medium.com/v2/resize:fit:1400/1*Pasxnagn5s8t5fqPkKYLiQ.png" alt="Dry Beans" />

