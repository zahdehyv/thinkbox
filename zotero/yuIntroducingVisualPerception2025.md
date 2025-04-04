---
Title: "Introducing Visual Perception Token into Multimodal Large Language Model"
Year: 2025 (February)
Authors: Runpeng Yu, Xinyin Ma, Xinchao Wang
Tags: 

- ComputerScience/ComputerVisionandPatternRecognition

- ComputerScience/MachineLearning

aliases: 
- "Introducing Visual Perception Token into Multimodal Large Language Model"
- ""
---
> [!ABSTRACT]
>To utilize visual information, Multimodal Large Language Model (MLLM) relies on the perception process of its vision encoder. The completeness and accuracy of visual perception significantly influence the precision of spatial reasoning, fine-grained understanding, and other tasks. However, MLLM still lacks the autonomous capability to control its own visual perception processes, for example, selectively reviewing specific regions of an image or focusing on information related to specific object categories. In this work, we propose the concept of Visual Perception Token, aiming to empower MLLM with a mechanism to control its visual perception processes. We design two types of Visual Perception Tokens, termed the Region Selection Token and the Vision Re-Encoding Token. MLLMs autonomously generate these tokens, just as they generate text, and use them to trigger additional visual perception actions. The Region Selection Token explicitly identifies specific regions in an image that require further perception, while the Vision Re-Encoding Token uses its hidden states as control signals to guide additional visual perception processes. Extensive experiments demonstrate the advantages of these tokens in handling spatial reasoning, improving fine-grained understanding, and other tasks. On average, the introduction of Visual Perception Tokens improves the performance of a 2B model by 23.6\%, increasing its score from 0.572 to 0.708, and even outperforms a 7B parameter model by 13.4\% (from 0.624). Please check out our repo https://github.com/yu-rp/VisualPerceptionToken
---
> [!tip] LINK
> [Preprint PDF](zotero://select/library/items/IRJ98WRN)

