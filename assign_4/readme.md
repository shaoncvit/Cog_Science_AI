# Brain Encoding and Decoding Analysis Report
# Shaon Bhattacharyya 2023701018

## Executive Summary

This report presents a comprehensive analysis of brain encoding and decoding experiments using various language models (SBERT1, SBERT2, T5, and CLIP) across different cognitive domains (language, vision, dmn, and task) for two subjects (subj1 and subj2).

## 1. Encoding Analysis

### 1.1 Model Performance Comparison

#### Table 1: Overall Encoding Performance (Pearson Correlation)
| Model   | Subject | Language | Vision | DMN    | Task   |
|---------|---------|----------|---------|---------|---------|
| SBERT1  | subj1   | 0.7744   | 0.8186  | 0.5981  | 0.6064  |
| SBERT2  | subj1   | 0.6946   | 0.7539  | 0.4865  | 0.4983  |
| T5      | subj1   | 0.7646   | 0.8071  | 0.5742  | 0.5927  |
| CLIP    | subj1   | 0.6577   | 0.7228  | 0.4531  | 0.4643  |
| SBERT1  | subj2   | 0.6339   | 0.7904  | 0.5242  | 0.4619  |
| SBERT2  | subj2   | 0.5210   | 0.7137  | 0.3966  | 0.3459  |
| T5      | subj2   | 0.6210   | 0.7789  | 0.5066  | 0.4443  |
| CLIP    | subj2   | 0.4852   | 0.6824  | 0.3661  | 0.3133  |

### 1.2 Key Findings - Encoding

1. **Best Performing Model**: SBERT1 consistently outperforms other models across domains
   - Highest correlation in vision domain (0.8186 for subj1)
   - Strong performance in language domain (0.7744 for subj1)

2. **Domain Performance**:
   - Vision domain shows strongest correlations across all models
   - DMN and Task domains show relatively lower correlations
   - Language domain shows second-best performance

3. **Subject Variation**:
   - Subject 1 shows consistently higher correlations than Subject 2
   - Pattern of domain performance is consistent across subjects

### 1.3 Masking Analysis

#### Table 2: Performance Impact of POS Masking (Pearson Correlation Drop)
| Subject | POS  | Language | Vision | DMN    | Task   |
|---------|------|----------|---------|---------|---------|
| subj1   | NOUN | 0.0038   | 0.0054  | 0.0058  | -0.0036 |
| subj1   | VERB | -0.0029  | -0.0035 | -0.0069 | -0.0086 |
| subj1   | ADJ  | -0.0028  | -0.0017 | -0.0069 | -0.0083 |
| subj2   | NOUN | 0.0092   | 0.0063  | 0.0180  | 0.0086  |
| subj2   | VERB | -0.0057  | -0.0034 | -0.0046 | -0.0128 |
| subj2   | ADJ  | -0.0027  | -0.0018 | -0.0011 | N/A     |

## 2. Decoding Analysis

### 2.1 Model Performance Comparison

#### Table 3: Decoding Performance Metrics
| Model   | Subject | Domain    | Pearson | 2V2    | Rank  | Top-5  |
|---------|---------|-----------|----------|---------|--------|---------|
| SBERT1  | subj1   | Language  | 0.3266   | 0.9958  | 1.60   | 81.34%  |
| SBERT1  | subj1   | Vision    | 0.3396   | 0.9969  | 1.00   | 84.21%  |
| CLIP    | subj1   | Language  | 0.8355   | 0.9951  | 6.70   | 47.19%  |
| T5      | subj1   | Vision    | 0.4512   | 0.9954  | 1.80   | 80.38%  |

### 2.2 Key Findings - Decoding

1. **Reconstruction Quality**:
   - CLIP shows highest Pearson correlation (0.83-0.86)
   - Better semantic preservation but lower exact matching
   - SBERT1 and T5 show better Top-5 accuracy despite lower Pearson

2. **Model Characteristics**:
   - SBERT models: Better at exact sentence reconstruction
   - CLIP: Better at semantic similarity but higher rank
   - T5: Balanced performance across metrics

3. **Domain-specific Performance**:
   - Vision domain generally shows better performance
   - Language domain shows more variability across models

## 3. Conclusions and Recommendations

### 3.1 Key Takeaways

1. **Model Selection**:
   - SBERT1 is optimal for encoding tasks
   - CLIP is preferred for semantic preservation in decoding
   - T5 offers good balance for general applications

2. **Domain Considerations**:
   - Vision domain shows most robust performance
   - DMN and Task domains need improvement
   - Language domain shows consistent but moderate performance

### 3.2 Recommendations

1. **Model Development**:
   - Focus on improving DMN and Task domain performance
   - Investigate CLIP's semantic understanding capabilities
   - Consider ensemble approaches combining SBERT1 and CLIP

2. **Application Guidelines**:
   - Use SBERT1 for encoding-critical applications
   - Employ CLIP for semantic analysis tasks
   - Consider subject-specific model tuning

### 3.3 Future Directions

1. **Research Priorities**:
   - Investigate subject-specific variations
   - Develop improved DMN/Task domain architectures
   - Explore multi-model fusion approaches

2. **Technical Improvements**:
   - Enhanced POS-aware encoding
   - Better cross-domain generalization
   - Reduced subject-specific performance variance

---
*Note: This report is based on experimental results from brain encoding and decoding tasks using various language models and two subjects.* 