# Medical Text Classification using BioBERT

## 🎯 프로젝트 개요
의료 텍스트 분류를 위한 다양한 NLP 모델 비교 연구

## 🔧 분류 모델들
1. **패턴 매칭 분류기** - 규칙 기반 접근법
2. **렉시콘 베이스 분류기** - 사전 기반 분류
3. **BioBERT 분류기** - 의료 특화 BERT 모델
4. **앙상블 분류기** - 패턴매칭 + BioBERT 결합

## 📊 주요 성과
- **최종 분류 정확도 98% 이상(2025년5월20일현재)** 달성
- 다양한 접근법 비교 분석 완료
- 의료 텍스트 분류 방법론 확립

## 🛡️ 데이터 보호
- 모든 데이터는 익명화 처리됨
- 의료기관 정보 비공개
- 연구 목적으로만 활용

# Medical Text Classification using BioBERT

<div align="center">

![BioBERT](https://img.shields.io/badge/BioBERT-Medical%20NLP-blue?style=for-the-badge)
![Accuracy](https://img.shields.io/badge/Accuracy-97%25%2B-green?style=for-the-badge)
![Python](https://img.shields.io/badge/Python-3.8%2B-yellow?style=for-the-badge)

</div>

## 🎯 Project Overview

This project presents a comprehensive comparative study of various Natural Language Processing (NLP) models for medical text classification, achieving **97%+ accuracy** in clinical text analysis.

The research explores multiple approaches to medical text classification, from traditional rule-based methods to state-of-the-art transformer models, providing insights into the effectiveness of different methodologies in healthcare NLP applications.

## 🔧 Classification Models

### 1. **Pattern Matching Classifier**
- **Approach**: Rule-based classification system
- **Method**: Regular expressions and predefined patterns
- **Use Case**: Baseline model for structured medical terminology

### 2. **Lexicon-Based Classifier**
- **Approach**: Dictionary-based classification
- **Method**: Medical terminology dictionaries and keyword matching
- **Use Case**: Domain-specific vocabulary recognition

### 3. **BioBERT Classifier**
- **Approach**: Medical domain-specific BERT model
- **Method**: Pre-trained BioBERT fine-tuned for classification tasks
- **Use Case**: State-of-the-art contextual understanding

### 4. **Ensemble Classifier**
- **Approach**: Hybrid model combining Pattern Matching + BioBERT
- **Method**: Weighted ensemble of rule-based and deep learning models
- **Use Case**: Optimized performance through model combination

## 📊 Key Achievements

- ✅ **Final Classification Accuracy: 98.3%** (15 errors out of 886 cases)
- ✅ **Initial Pattern Matching Baseline: ~70%** accuracy
- ✅ Progressive improvement through iterative model development
- ✅ **Final Distribution Analysis:**
  - PCL (Pancreatic Cystic Lesion): 436 cases (49.2%)
  - Non-PCL: 373 cases (42.1%) 
  - Uncertain: 77 cases (8.7%)
- ✅ **Zone Classification:**
  - Standard zone: 809 cases (91.3%)
  - Uncertain zone: 77 cases (8.7%)
## 🏗️ Repository Structure

```
Medical-Text-Classification-BioBERT/
├── README.md
├── notebooks/
│   ├── 01_Pattern_Matching_Classifier.ipynb
│   ├── 02_Lexicon_Based_Classifier.ipynb
│   ├── 03_BioBERT_Classifier.ipynb
│   └── 04_Ensemble_Classifier.ipynb
├── src/
│   ├── pattern_matcher.py
│   ├── lexicon_classifier.py
│   ├── biobert_model.py
│   └── ensemble_model.py
├── reports/
│   ├── analysis_report.md
│   └── methodology_comparison.pdf
└── docs/
    └── technical_specifications.md
```

## 🔬 Methodology

### Data Processing Pipeline
1. **Text Preprocessing**: Cleaning and normalization of medical texts
2. **Feature Extraction**: Domain-specific feature engineering
3. **Model Training**: Individual model development and training
4. **Ensemble Integration**: Combination of complementary approaches
5. **Performance Evaluation**: Comprehensive metrics analysis

### Model Comparison Framework
- **Accuracy**: Overall classification performance
- **Precision/Recall**: Class-specific performance metrics
- **F1-Score**: Balanced performance measurement
- **Computational Efficiency**: Processing time and resource usage
  
## 🔬 Development Journey

## 📈 Performance Metrics

| Model | Accuracy | Precision | Recall | F1-Score | Notes |
|-------|----------|-----------|--------|----------|-------|
| Pattern Matching (Initial) | ~70% | - | - | - | Baseline approach |
| **BioBERT Classifier** | **79.4%** | **79.5%** | **79.4%** | **79.4%** | Single model performance |
| **Final Ensemble Model** | **98.3%** | - | - | - | **Production system (15/886 errors)** |

## 🛠 Technical Requirements

```python
# Core Dependencies
torch>=1.9.0
transformers>=4.15.0
scikit-learn>=1.0.0
pandas>=1.3.0
numpy>=1.21.0
matplotlib>=3.5.0
seaborn>=0.11.0

# BioBERT Model
biobert-pytorch>=1.0.0
```

## 🚀 Quick Start

```bash
# Clone repository
git clone https://github.com/yourusername/Medical-Text-Classification-BioBERT.git
cd Medical-Text-Classification-BioBERT

# Install dependencies
pip install -r requirements.txt

# Run ensemble classifier
python src/ensemble_model.py
```

## 📋 Usage Example

```python
from src.ensemble_model import MedicalTextEnsemble

# Initialize ensemble classifier
classifier = MedicalTextEnsemble()

# Load pre-trained models
classifier.load_models()

# Classify medical text
text = "Patient presents with..."
result = classifier.predict(text)
confidence = classifier.get_confidence(text)

print(f"Classification: {result}")
print(f"Confidence: {confidence:.2f}")
```

## 🎯 Applications

### Clinical Use Cases
- **Radiology Report Classification**: Automated categorization of imaging findings
- **Pathology Report Analysis**: Systematic classification of diagnostic reports
- **Clinical Note Processing**: Structured analysis of physician notes
- **Medical Literature Mining**: Automated research paper categorization

### Research Applications
- **Comparative NLP Studies**: Benchmarking different classification approaches
- **Medical AI Development**: Foundation for advanced healthcare AI systems
- **Clinical Decision Support**: Integration with electronic health records

## 🛡️ Data Protection & Ethics

### Privacy Safeguards
- ✅ **Complete Data Anonymization**: All patient identifiers removed
- ✅ **Institutional Privacy**: Medical institution information protected
- ✅ **Research Purpose Only**: Data used exclusively for academic research
- ✅ **HIPAA Compliance**: Adherence to healthcare privacy regulations

### Ethical Considerations
- **Transparent Methodology**: Open-source approach for reproducibility
- **Bias Mitigation**: Comprehensive evaluation across diverse medical texts
- **Clinical Validation**: Results validated by medical domain experts

## 📊 Technical Innovations

### Novel Contributions
1. **Hybrid Ensemble Architecture**: Combination of rule-based and transformer models
2. **Medical Domain Adaptation**: Specialized fine-tuning for healthcare NLP
3. **Performance Optimization**: Balanced accuracy and computational efficiency
4. **Comparative Analysis Framework**: Systematic evaluation methodology

## 🔮 Future Directions

### Short-term Goals
- [ ] Multi-language support for international medical texts
- [ ] Real-time processing optimization
- [ ] Integration with clinical workflow systems

### Long-term Vision
- [ ] Expansion to multi-modal medical data (text + images)
- [ ] Development of specialized medical NLP toolkit
- [ ] Collaborative platform for medical AI research

## 📞 Contact & Collaboration

For research collaboration, technical questions, or clinical applications:

**Principal Investigator**: Boyoung Kang 
**Email**: bykang2015@gmail.com
**Institution**: SKKU
**Research Focus**: Medical NLP, Healthcare AI, Clinical Text Mining

## 📄 Citation

```bibtex
@misc{medical_text_classification_2025,
  title={Medical Text Classification using BioBERT: A Comparative Study},
  author={[Your Name]},
  year={2025},
  note={Available at: https://github.com/yourusername/Medical-Text-Classification-BioBERT}
}
```

## 🏷️ Keywords

`medical NLP` `BioBERT` `text classification` `healthcare AI` `clinical text mining` `ensemble learning` `medical informatics` `natural language processing` `healthcare technology`

---

<div align="center">

**🌟 If this project helps your research, please consider giving it a star! 🌟**

</div>
