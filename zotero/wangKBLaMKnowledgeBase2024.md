---
Title: "KBLaM: Knowledge Base augmented Language Model"
Year: 2024 (October)
Authors: Xi Wang, Taketomo Isazawa, Liana Mikaelyan, James Hensman
Tags: 

aliases: 
- "KBLaM: Knowledge Base augmented Language Model"
- "KBLaM"
---
> [!ABSTRACT]
>In this paper, we propose Knowledge Base augmented Language Model (KBLAM), a new method for augmenting Large Language Models (LLMs) with external knowledge. KBLAM works with a knowledge base (KB) constructed from a corpus of documents, transforming each piece of knowledge in the KB into continuous key-value vector pairs via pre-trained sentence encoders with linear adapters and integrating them into pre-trained LLMs via a specialized rectangular attention mechanism. Unlike Retrieval-Augmented Generation, KBLAM eliminates external retrieval modules, and unlike in-context learning, its computational overhead scales linearly with KB size rather than quadratically. Our approach enables integrating a large KB of more than 10K triples into an 8B pre-trained LLM of only 8K context window on one single A100 80GB GPU and allows for dynamic updates without model fine-tuning or retraining. Experiments demonstrate KBLAM’s effectiveness in various tasks, including question-answering and open-ended reasoning, while providing interpretable insights into its use of the augmented knowledge. Code and datasets are available at https://github.com/microsoft/KBLaM/
---
> [!tip] LINK
> [Full Text PDF](zotero://select/library/items/5N4UXN7A)

> [!note]
>First, KBLAM maps each triple into a fixed-length key-value vector pair, referred to as a knowledge token, which has sizes identical to the KV cache of a single token and can be seamlessly incorporated into each attention layer of the LLM. In particular, KBLAM encodes from name and property into a key vector, which serves as an identifier, mimicking the key embedding of a token; value into a value vector, which provides the actual content, similar to the value embedding of a token.  Then, KBLAM uses the structure between triples to augment knowledge tokens into the LLM’s attention in a scalable and dynamic way using a simple rectangular attention structure: Triples with different name and property can be considered to represent independent pieces of information, therefore knowledge token from each triple can be encoded and injected into pre-trained LLM independently. This allows the KBLAM’s complexity (memory and time) to grow linearly with respect to the number of triples, unlike in-context learning’s quadratically growing overhead, giving KBLAM much better scalability. Additionally, the independence allows us to update/remove/add a triple by only modifying its corresponding single knowledge token without any further changes, which is not achievable in, e.g. standard KV cache mechanism. Perhaps more importantly, the attention matrix under this design is highly interpretable. As we show in Fig. 4, the model’s use of the knowledge tokens can be directly inspected through the attention score.  Lastly, we show that the linear adapters can be learned using instruction tuning on purely synthetic data (Sec. 5) while being able to generalizes to real data. Different from supervised fine-tuning, which aims to memorize knowledge into model weights, the learning process of KBLAM aims at finding a projection between the pre-trained sentence encoder space and the LLM’s embedding space, which motiviates us the train KBLAM with fully synthetic data since the exact knowledge in the training samples is not important_ [Page 2](zotero://open-pdf/library/items/5N4UXN7A?page=2&annotation=2UM3TJEQ)_
---
> [!note]
>structured attention masks_ [Page 3](zotero://open-pdf/library/items/5N4UXN7A?page=3&annotation=IMCZEVZ4)_
---
> [!note]
>Rectangular Attention: Injecting knowledge token into prompt tokens_ [Page 5](zotero://open-pdf/library/items/5N4UXN7A?page=5&annotation=59JJLEXR)_
---
> [!note]
>The idea is that tokens in the prompt part can attend to, in addition to all previous tokens in the prompt, all knowledge tokens. On the other hand, knowledge tokens cannot attend to each other, i.e. they do not have self-attention nor query embeddings_ [Page 6](zotero://open-pdf/library/items/5N4UXN7A?page=6&annotation=W8B324JM)_
---
> [!note]
>KBLAM’s attention matrix is interpretable. Consider a toy KB of 10 triples, the heatmap shows the attention weights under different questions. We select the 15th attention layer and visualize the post-softmax attention score averaged over all attention heads. The x-axis only shows the keys corresponding the KB part and the y-axis is aligned by the end of each question’s query._ [Page 7](zotero://open-pdf/library/items/5N4UXN7A?page=7&annotation=ZERXAKU4)_
---
> [!note]
>KBLAM attention is an accurate retriever_ [Page 8](zotero://open-pdf/library/items/5N4UXN7A?page=8&annotation=L8IQR36F)_
---
> [!note]
>KBLAM can reason about knowledge_ [Page 9](zotero://open-pdf/library/items/5N4UXN7A?page=9&annotation=FQVH4YN4)_
---
_Further reading [Page 11](zotero://open-pdf/library/items/5N4UXN7A?page=11&annotation=CECYKFRY)_
---
> [!note]
>Improving language models by retrieving from trillions of tokens_ [Page 11](zotero://open-pdf/library/items/5N4UXN7A?page=11&annotation=A8TFM4MP)_
---
> [!note]
>Leveraging passage retrieval with generative models for open domain question answering_ [Page 11](zotero://open-pdf/library/items/5N4UXN7A?page=11&annotation=ANCETR5X)_
---
> [!note]
>Generalization through memorization: Nearest neighbor language models_ [Page 11](zotero://open-pdf/library/items/5N4UXN7A?page=11&annotation=5UA5NT6F)_
---
