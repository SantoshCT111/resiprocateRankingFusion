# Reciprocate Ranking Fusion for RAG

## Overview
This repository implements Reciprocate Ranking Fusion (RRF) for Retrieval-Augmented Generation (RAG) systems. RRF is an effective method to combine multiple retrieval sources or strategies to improve the quality and relevance of retrieved context for language models.

## Features
- Implementation of Reciprocate Ranking Fusion algorithm
- Support for multiple document retrieval methods
- Easy integration with existing RAG pipelines
- Configurable ranking parameters

## Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/resiprocateRankingFusion.git
cd resiprocateRankingFusion

# Install dependencies
pip install -r requirements.txt
```

## Usage

```python
from rag_rrf import ReciprocateRankingFusion

# Initialize with retrieval sources
rrf = ReciprocateRankingFusion(
    retrievers=[retriever1, retriever2, retriever3],
    k=60  # RRF constant parameter
)

# Get fused results
results = rrf.retrieve("Your query here")
```

## How It Works
Reciprocate Ranking Fusion combines rankings from multiple retrieval sources by giving each document a score based on its position in each ranking. The formula is:

RRF score = Σ 1/(k + r)

Where:
- r is the rank of the document in a given list
- k is a constant (default: 60)

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

## License
This project is licensed under the MIT License - see the LICENSE file for details.