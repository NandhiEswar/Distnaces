# Distance and Similarity Metrics

This project provides an overview of various **distance** and **similarity metrics** used in data analysis, machine learning, and other computational tasks. These metrics are commonly applied in areas such as text analysis, clustering, and spatial computations.

---

## Metrics Covered

### 1. **Euclidean Distance**
- Measures the straight-line distance between two points in n-dimensional space.
- **Formula**:  
  \[
  d(p, q) = \sqrt{\sum_{i=1}^{n} (q_i - p_i)^2}
  \]

---

### 2. **Cosine Similarity**
- Measures the cosine of the angle between two non-zero vectors.
- **Formula**:  
  \[
  \text{Cosine Similarity} = \frac{\vec{A} \cdot \vec{B}}{||\vec{A}|| \, ||\vec{B}||}
  \]

---

### 3. **Jaccard Similarity**
- Measures the similarity between two sets as the ratio of the intersection over the union.
- **Formula**:  
  \[
  J(A, B) = \frac{|A \cap B|}{|A \cup B|}
  \]

---

### 4. **Haversine Distance**
- Used to calculate the distance between two points on a sphere (e.g., Earth).
- **Formula**:  
  \[
  a = \sin^2\left(\frac{\Delta\phi}{2}\right) + \cos(\phi_1) \cos(\phi_2) \sin^2\left(\frac{\Delta\lambda}{2}\right)
  \]
  \[
  d = 2r \cdot \arcsin(\sqrt{a})
  \]

---

### 5. **Hamming Distance**
- Counts the number of differing elements between two binary sequences.
- **Formula**:  
  \[
  H(A, B) = \text{Count}(A_i \neq B_i)
  \]

---

### 6. **Manhattan Distance**
- Measures the distance between two points along the axes at right angles.
- **Formula**:  
  \[
  d(p, q) = \sum_{i=1}^{n} |q_i - p_i|
  \]

---

### 7. **Minkowski Distance**
- A generalized metric that includes both Euclidean and Manhattan distances as special cases.
- **Formula**:  
  \[
  d(p, q) = \left(\sum_{i=1}^{n} |q_i - p_i|^p\right)^{1/p}
  \]

---

### 8. **Chebyshev Distance**
- Measures the maximum absolute difference between two points.
- **Formula**:  
  \[
  d(p, q) = \max(|q_i - p_i|)
  \]

---

### 9. **Sørensen-Dice Coefficient**
- Measures similarity between two sets.
- **Formula**:  
  \[
  D(A, B) = \frac{2 |A \cap B|}{|A| + |B|}
  \]

---

## How to Use

You can use Python libraries like `scipy`, `numpy`, or custom implementations to compute these distances. For example:
```python
from scipy.spatial.distance import euclidean, cosine, cityblock

# Euclidean Distance
point1 = [1, 2]
point2 = [3, 4]
distance = euclidean(point1, point2)
print("Euclidean Distance:", distance)

# Cosine Similarity
similarity = 1 - cosine(point1, point2)
print("Cosine Similarity:", similarity)
