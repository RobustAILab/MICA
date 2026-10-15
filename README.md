# MICA: Deep Incomplete Multi-View Clustering via Multi-Level Imputation and Contrastive Alignment

**Ziyu Wang, Yiming Du, Yao Wang, Rui Ning, and Lusi Li**

📄 **Published in [Neural Networks](https://www.sciencedirect.com/journal/neural-networks), Volume 181, Article 106851 (2025)**

---

## 📖 Overview

**MICA** (**M**ulti-Level **I**mputation and **C**ontrastive **A**lignment) is a deep incomplete multi-view clustering framework designed to learn robust and discriminative representations from multi-view data with missing observations.

MICA integrates **multi-level missing-data imputation** with **instance-level and cluster-level contrastive learning** to effectively recover missing information, enhance cross-view representation alignment, and improve clustering performance.

## 🏗️ Framework

![MICA Framework](https://github.com/user-attachments/assets/261b5dd8-e837-42dc-b125-11bbc0fdb83a)

*Overview of the proposed MICA framework.*

## ✨ Key Features

- **Multi-View Learning:** Supports heterogeneous multi-view datasets and learns complementary information across views.
- **Multi-Level Imputation:** Recovers missing information through imputation mechanisms to improve representation completeness.
- **Contrastive Alignment:** Employs instance-level and cluster-level contrastive learning to enhance cross-view consistency.
- **Unified Clustering:** Integrates information from available views to generate coherent clustering assignments.
- **Comprehensive Evaluation:** Supports multiple benchmark datasets and clustering evaluation metrics.

## ⚙️ Requirements

The implementation requires the following dependencies:

- Python 3.6+
- PyTorch 1.7+
- NumPy
- scikit-learn
- SciPy

Install the required packages using:

```bash
pip install torch numpy scikit-learn scipy
```

## 🚀 Usage

### 1. Dataset Configuration

MICA supports the following benchmark datasets:

| Dataset | Description |
|---|---|
| MSRCv1 | Multi-view image dataset |
| MNIST-USPS | Handwritten digit datasets |
| Scene | Scene image dataset |
| Hand | Handwritten digit dataset |
| Fashion | Fashion image dataset |
| BDGP | Biological multi-view dataset |

Select a dataset using the `--db` argument.

### 2. Key Parameters

| Parameter | Description |
|---|---|
| `--db` | Dataset name |
| `--seed` | Random seed for reproducibility |
| `--mse_epochs` | Number of pre-training epochs |
| `--con_epochs` | Number of contrastive fine-tuning epochs |
| `--learning_rate` | Initial learning rate |
| `--batch_size` | Training batch size |
| `--gpu` | GPU device ID |
| `--load_pre_model` | Load a pre-trained model |
| `--load_full_model` | Load a fully trained model |

### 3. Pre-Trained Models

To load a pre-trained model, enable:

```bash
--load_pre_model True
```

To load a fully trained model, enable:

```bash
--load_full_model True
```

These options should be appended to the appropriate training or evaluation command.

## 🧠 Model Architecture

MICA consists of four key components:

**1. View-Specific Encoders and Decoders**

Learn latent representations from individual views and reconstruct view-specific information.

**2. Missing Data Imputation**

Employs KNN-based imputation mechanisms to estimate missing features and improve representation completeness.

**3. Contrastive Representation Alignment**

Combines instance-level and cluster-level contrastive objectives to enhance discriminative representation learning and cross-view consistency.

**4. Multi-View Fusion and Clustering**

Integrates complementary information across views to produce unified clustering results.

## 📚 Citation

If you find this repository useful in your research, please cite our paper:

**Ziyu Wang, Yiming Du, Yao Wang, Rui Ning, and Lusi Li.**  
"Deep Incomplete Multi-view Clustering via Multi-level Imputation and Contrastive Alignment."  
*Neural Networks*, vol. 181, Article 106851, 2025.

```bibtex
@article{wang2025deep,
  title={Deep Incomplete Multi-view Clustering via Multi-level Imputation and Contrastive Alignment},
  author={Wang, Ziyu and Du, Yiming and Wang, Yao and Ning, Rui and Li, Lusi},
  journal={Neural Networks},
  volume={181},
  pages={106851},
  year={2025},
  publisher={Elsevier}
}
```

## 📬 Contact

For questions about the implementation or research collaboration, please contact the authors or open an issue in this repository.

## 📜 License

Please refer to the repository's `LICENSE` file for licensing information, if provided.
