# Analysis of The Supernatural and Humanity as a Representation of Tribulation Over Time

A topic modeling analysis exploring how supernatural themes in literature reflect changing values across three centuries of storytelling.

## Overview

This project uses BERTopic to analyze and compare supernatural narratives from three distinct eras:
- **Grimm Fairy Tales** (1857) - 104-206 stories from Carnegie Mellon's digital folklore collection
- **H.P. Lovecraft Stories** (1917-1937) - 104 stories from the original Lovecraft corpus
- **Modern Fan Fiction** (2001+) - 104 contemporary stories inspired by Lovecraft from the Lovecraft eZine

## Research Question

## Methodology

### Data Processing
- Stories organized into labeled corpora with metadata (genre, publication year, era)
- Preprocessing with custom stop words and CountVectorizer
- Era labels: Fairytale (1857), Lovecraft (1917-1937), Post-Lovecraft (1938-1970), Modern (1971-2000), Contemporary (2001+)

### Model Configuration
- **Embedding Model**: Sentence Transformer (all-mpnet-base-v2)
- **Representation Model**: KeyBERTInspired with MMR (diversity=0.3)
- **Clustering**: HDBSCAN (min_cluster_size=8, min_samples=3)
- **Dimensionality Reduction**: UMAP (n_neighbors=15, n_components=5, metric='cosine')

### Experiments
We created 36 different BERTopic models testing:
- 9 corpus combinations (single, paired, and triple corpus combinations)
- 4 parameter configurations (full custom settings, HDBSCAN only, UMAP only, stop words only)

## Key Findings

Our analysis revealed fundamental differences in narrative focus across eras:

- **Grimm Fairy Tales**: 

- **Lovecraft Stories**: 

- **Modern Fan Fiction**:
  
### Model Performance
- Coherence scores ranged from 0.35-0.49 across models
- Configuration with all custom parameters (stop words + HDBSCAN + UMAP) consistently produced the best results
- Lower outlier rates correlated with better practical clustering quality

## Evaluation Metrics

- **OCTIS Coherence Score**: Topic quality measurement
- **Diversity Score**: Thematic variety within corpus
- **Uniqueness Score**: Topic separation and distinctiveness
- **Outlier Analysis**: Model confidence and edge case handling

## Requirements

- Python 3.8+
- BERTopic
- OCTIS
- sentence-transformers
- UMAP
- HDBSCAN
- scikit-learn

## Conclusion
