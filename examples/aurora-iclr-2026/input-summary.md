# Input Summary

Aurora is presented as a multimodal time series foundation model supporting multimodal inputs and zero-shot inference across domains. The paper describes a cross-domain multimodal time series corpus and an architecture that uses time series, text, and endogenous image modalities.

High-level method structure extracted from the supplied PDF:

- Time series are normalized and tokenized through patching and embedding.
- Endogenous images are rendered from time series using FFT-derived periodic structure, reshaping, resizing, image patching, and embedding.
- Text descriptions are tokenized using a BERT-style vocabulary.
- Image and text tokens are encoded using pretrained VisionEncoder/ViT and TextEncoder/BERT.
- Token distillation compresses image and text representations through cross-attention-based distillers.
- Modality-Guided Multi-head Self-Attention constructs multimodal correlations and injects them into temporal attention.
- A cross-attention modality fuser combines time, image, and text representations into fused multimodal representations.
- The decoder uses a ConditionDecoder with causal and cross-transformer components to generate future conditions.
- A Prototype Bank and PrototypeRetriever produce period/trend prototypes from text and image representations.
- Prototype-Guided Flow Matching starts from prototype-based initial tokens rather than pure Gaussian noise to generate probabilistic forecasts.

Central message: Aurora uses text and endogenous image information as domain knowledge to guide temporal representation learning and prototype-guided generative forecasting.
