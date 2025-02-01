# Biased Dataset Clustering: Greedy Preprocessing & k-Means Integration on Large Scale Data

## 📌 Project Overview  
This project addresses challenges in applying **k-means clustering** to biased datasets by implementing a **parallelized greedy clustering algorithm** for preprocessing. The algorithm reduces dataset size by selecting representatives based on a tunable distance threshold (τ), enabling efficient clustering. A comparative analysis with **random subsampling** evaluates computational efficiency and clustering quality.

**Dataset**: 118,821 data points with inherent biases (e.g., age, wealth).  
**Goal**: Mitigate bias effects by preprocessing data into representative clusters (1%, 10%, 25% sizes) and compare methods.

---

## 🚀 Key Features  
1. **Parallelized Greedy Clustering**:  
   - Reduces dataset to target cluster ratios (1%, 10%, 25%) via adaptive τ tuning.  
   - Optimized for cache behavior and minimal memory usage.  
2. **k-Means Integration**:  
   - Clusters representatives from preprocessing step.  
   - Post-processing assigns original data points to clusters.  
3. **Random Subsampling Baseline**:  
   - Generates comparison dataset by randomly sampling equivalent proportions.  
4. **Performance Analysis**:  
   - Metrics: Runtime, memory usage, Silhouette Score, intra/inter-cluster distances.  

---

## 🔍 Findings  
1. **Greedy Clustering**:  
   - Achieved target cluster sizes (1%, 10%, 25%) with τ=100.  
   - **Runtime**: 43.19s | **Memory**: 1.03MB.  
   - **Clustering Quality**: Silhouette Score (-0.0029), Intra-cluster distance (15,289.29).  
2. **Random Subsampling**:  
   - **Runtime**: 37.14s | **Memory**: Negligible.  
   - **Clustering Quality**: Silhouette Score (0.1127), Intra-cluster distance (12,397.45).  
3. **Conclusion**:  
   - Subsampling outperformed in speed and clustering quality for this dataset.  
   - Greedy clustering offers structured preprocessing for bias mitigation but requires tuning.  

---

## 🛠 System Requirements 
### Dependencies  
- Python 3.8+  
- Libraries: `numpy`, `pandas`, `scikit-learn`, `multiprocessing`

---

## 📄 License  
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

