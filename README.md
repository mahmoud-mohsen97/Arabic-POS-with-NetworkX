# Arabic POS Tagging with NetworkX

This project demonstrates Part-of-Speech (POS) tagging for Arabic text and visualizes the results using NetworkX graphs. The goal is to build a pipeline that performs POS tagging on Arabic text and represents the grammatical relationships between words in a network graph. This pipeline leverages both rule-based and deep learning approaches to improve accuracy.

## Approach 1: Rule-Based and Deep Learning POS Tagging

1. Rule-Based Methods (spaCy and Stanza)
  - spaCy-UDPipe: Implements rule-based POS tagging using pre-trained models, but struggles with mixed-language texts.
  - Stanza: Provides improved accuracy for Arabic text, though it faces challenges with English names in mixed texts.
2. Deep Learning Method (Bi-LSTM and Transformers)
  - Bi-LSTM: A sequence-labeling model that captures contextual information for improved POS tagging accuracy.
  - Transformers (CAMeL-BERT): Fine-tuned BERT model for Modern Standard Arabic (MSA), offering superior accuracy, especially in handling mixed-language texts.

## Network Graph Construction
NetworkX is used to build a network graph where:

- Nodes represent words and their corresponding POS tags.
- Edges depict sequential and syntactic relationships between words.

This visualization helps in understanding the structure of Arabic sentences and their grammatical dependencies.

## Dataset
The project uses two datasets:

1. Arabic PUD (Universal Dependencies): Contains 998 sentences and 16 POS tags.
2. Arabic Article (CyShield): A single article in Arabic, containing mixed-language text (Arabic and English names).

## Results
- Rule-Based (spaCy/Stanza): Provides fast tagging but struggles with mixed-language content.
- Bi-LSTM: Achieves 94.24% accuracy, showing robust performance in handling sequential Arabic text.
- Transformer-Based (CAMeL-BERT): Delivers superior accuracy, solving tokenization and classification issues with mixed-language content.

## Tools and Resources
- POS Tagging: spaCy, Stanza, Hugging Face Transformers.
- Visualization: NetworkX, Matplotlib, Arabic-reshaper, and python-bidi for correct display of Arabic text in graphs.
- Modeling: Keras, TensorFlow for Bi-LSTM, and CAMeL-BERT for transformer-based approaches.

## Conclusion
Deep learning-based models, especially transformers like BERT, significantly outperform rule-based methods in POS tagging for Arabic, particularly with mixed-language texts. The use of NetworkX provides an effective visual representation of grammatical structures and word relationships.
