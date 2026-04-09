# Harmonic Analysis for Edge-Based Smart Grids
## Feature Engineering and Network-Efficient Power Estimation

> **Authors:** Silva et al. (2026)  
> **Institution:** University of Brasília (UnB), Brazil  
> **Repository:** [Harmonic-Analysis-for-Edge-Based-Smart-Grids](https://github.com/leonardolsms/Harmonic-Analysis-for-Edge-Based-Smart-Grids.git)

---

### ⚡ CONTEXT / PROBLEM
High-frequency electrical measurements enable detailed harmonic analysis for advanced applications like **Non-Intrusive Load Monitoring (NILM)**. However, current research trends favor increasingly complex deep learning models. These models impose:
*   **High Computational Cost:** Limiting deployment on low-power hardware.
*   **Network Overhead:** Requiring massive data transmission to the cloud.
*   **Latency Issues:** Hindering real-time response in smart grid environments.

### 🎯 OBJECTIVE
This research investigates the role of **feature engineering** in harmonic-based power estimation. The goal is to shift from *model-centric complexity* to *feature-centric design*, enabling lightweight, network-efficient, and edge-ready intelligence.

### 🛠️ METHODOLOGY
*   **Data Acquisition:** High-frequency NILM dataset (8 kHz sampling) using the ATM90E36A energy metering IC.
*   **Feature Space:** Extraction of current harmonics from the 1st to the 32nd order (h1–h32).
*   **Experimental Protocol:** Leakage-aware design with session-based train/test splits to prevent data contamination.
*   **Benchmarking:** Comparative analysis between lightweight linear models and sophisticated deep learning architectures (e.g., Seq2Point).

### 📈 KEY FINDINGS
> **The Dominance of the Fundamental Harmonic (h1)**
> 
>![Alt text](Results/Table01.png)
> 
> **Result:** h1 alone explains nearly all variance in active power (**R² ≈ 0.9999**).


The study reveals that adding higher-order harmonics (h2–h32) does not significantly improve predictive performance. The underlying mapping is inherently low-complexity and can be captured by minimal resource algorithms.
>
>>![Alt text](Results/Tablet04.png)
>
The table 03 indicate that all evaluated models achieve similar predictive performance, with R² values close to 1.0 and low error metrics. However, significant differences emerge in terms of computational efficiency. Linear models, particularly those using only the fundamental harmonic (h1), exhibit substantially lower inference latency and memory consumption compared to ensemble-based methods such as Random Forest and XGBoost. Despite their simplicity, these models maintain comparable accuracy, suggesting that the prediction task has low intrinsic complexity.

These findings highlight that increased model complexity does not necessarily translate into better performance in this context. Instead, lightweight models provide a more efficient and scalable solution, especially for edge-based deployments where computational resources are limited.

From a networking perspective, reduced inference latency enables faster decision-making and decreases end-to-end delay, while lower memory requirements facilitate deployment across large-scale distributed systems.
>
>>![Alt text](Results/Table03.png)
>
### 🚀 TECHNICAL CONTRIBUTIONS
- **Feature-Centric Analysis:** Tailored harmonic representations for smart grid power estimation.
- **Leakage-Aware Protocol:** A robust experimental framework ensuring reliable evaluation without data leakage.
- **Empirical Proof of Dominance:** Demonstrating that h1 is the primary driver of electrical behavior prediction.
- **Edge-Ready Insights:** Analysis of network implications for scalable smart grid deployments.

### 🌐 PRACTICAL / NETWORK IMPACT
*   **Edge Computing Benefits:** Local inference at the smart meter level reduces the need for raw data offloading.
*   **Bandwidth Reduction:** Drastic decrease in data transmission requirements by focusing only on the h1 component.
*   **Latency Improvements:** Near-instantaneous local processing supports real-time demand response and anomaly detection.
*   **Scalability & Privacy:** Distributed computation mitigates cloud bottlenecks and keeps sensitive high-resolution data local.

### 📝 CONCLUSION
Harmonic-aware machine learning is not just a modeling choice—it is a **network design strategy**. By leveraging feature dominance (h1), we can replace expensive models with lightweight approaches, enabling scalable, low-latency, and privacy-aware intelligent services in modern smart grid infrastructures.

---

### 🏷️ KEYWORDS
`Harmonic Analysis` • `Edge Computing` • `Smart Grids` • `Feature Engineering` • `Network Efficiency` • `NILM`

---
## Dataset

The dataset used in this study is publicly available and was obtained from the
high-frequency NILM repository maintained by [Dinar et al. 2025] The dataset can be
accessed at https://github.com/fariddinar/nilm-dataset (accessed on 20 December 2025).


## 📂 Repository Structure

```text
notebook/    -> Jupyter notebook with all experiments
data/scripts -> Instructions to obtain the dataset
figures/     -> Final figures used in the paper
paper/       -> LaTeX source of the camera-ready paper
results/     -> Tables with numerical results
bibliographic_references  -> Bibliographic_references used.

---
*Summary based on the article: "Harmonic Analysis for Edge Based Smart Grids: Feature Engineering and Network-Efficient Power Estimation"*
