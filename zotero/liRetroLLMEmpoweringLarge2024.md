---
Title: "RetroLLM: Empowering Large Language Models to Retrieve Fine-grained Evidence within Generation"
Year: 2024 (December)
Authors: Xiaoxi Li, Jiajie Jin, Yujia Zhou, Yongkang Wu, Zhonghua Li, Qi Ye, Zhicheng Dou
Tags: 

- Computer_Science_-_Computation_and_Language

- Computer_Science_-_Artificial_Intelligence

- Computer_Science_-_Information_Retrieval

aliases: 
- "RetroLLM: Empowering Large Language Models to Retrieve Fine-grained Evidence within Generation"
- "RetroLLM"
---
> [!ABSTRACT]
>Large language models (LLMs) exhibit remarkable generative capabilities but often suffer from hallucinations. Retrieval-augmented generation (RAG) offers an effective solution by incorporating external knowledge, but existing methods still face several limitations: additional deployment costs of separate retrievers, redundant input tokens from retrieved text chunks, and the lack of joint optimization of retrieval and generation. To address these issues, we propose RetroLLM, a unified framework that integrates retrieval and generation into a single, cohesive process, enabling LLMs to directly generate fine-grained evidence from the corpus with constrained decoding. Moreover, to mitigate false pruning in the process of constrained evidence generation, we introduce (1) hierarchical FM-Index constraints, which generate corpus-constrained clues to identify a subset of relevant documents before evidence generation, reducing irrelevant decoding space; and (2) a forward-looking constrained decoding strategy, which considers the relevance of future sequences to improve evidence accuracy. Extensive experiments on five open-domain QA datasets demonstrate RetroLLM’s superior performance across both in-domain and out-ofdomain tasks. The code is available at https: //github.com/sunnynexus/RetroLLM.
---
> [!tip] LINK
> [PDF](zotero://select/library/items/BMXAXK4T)

> [!note]
>FM-Index_ [Page 2](zotero://open-pdf/library/items/BMXAXK4T?page=2&annotation=KXQ42VVC)_
---
> [!important] Image
> ![[zotero/liRetroLLMEmpoweringLarge2024/image-4-x59-y539.png]]
> _intuitive workflow [Page 4](zotero://open-pdf/library/items/BMXAXK4T?page=4&annotation=HEZ4783R)_
---
> [!note]
>References_ [Page 9](zotero://open-pdf/library/items/BMXAXK4T?page=9&annotation=J4ZM8HMZ)_
---
> [!note]
>The FM-Index_ [Page 15](zotero://open-pdf/library/items/BMXAXK4T?page=15&annotation=MKMNSUHI)_
---
> [!note]
>BurrowsWheeler Transform (BWT)_xdxdxd [Page 15](zotero://open-pdf/library/items/BMXAXK4T?page=15&annotation=79MN27T4)_
---
> [!note]
>The FM-Index is based on the Burrows-Wheeler Transform (BWT)_ [Page 15](zotero://open-pdf/library/items/BMXAXK4T?page=15&annotation=PY7UZJDC)_
---
> [!note]
>The BWT of a string S is computed by sorting all cyclic rotations of S lexicographically and then taking the last column of the sorted rotations. This transformation rearranges the characters of the string in a way that enhances its compressibility, which is key to the FM-Index’s space efficiency._ [Page 15](zotero://open-pdf/library/items/BMXAXK4T?page=15&annotation=KLB4D7TZ)_
---
> [!note]
>The FM-Index stores only two columns from the BWT matrix: the first (F) and last (L) columns. These columns capture the relative order of the characters in all cyclic rotations of S. More precisely: - The first column (F) contains the sorted characters of the text S. - The last column (L) contains the last character of each of the cyclic rotations of S._ [Page 15](zotero://open-pdf/library/items/BMXAXK4T?page=15&annotation=XWHUB2GP)_
---
> [!note]
>Additionally, to enable efficient searching, the FM-Index uses additional data structures, such as the Wavelet Tree, to store the L column efficiently. This allows for fast rank and select operations, which are essential for searching._ [Page 15](zotero://open-pdf/library/items/BMXAXK4T?page=15&annotation=JFQFS69W)_
---
> [!note]
>Backward Search_ [Page 15](zotero://open-pdf/library/items/BMXAXK4T?page=15&annotation=H2H6EKUN)_
---
> [!note]
>Count_ [Page 15](zotero://open-pdf/library/items/BMXAXK4T?page=15&annotation=Q7DCPR5P)_
---
> [!note]
>Locate_ [Page 15](zotero://open-pdf/library/items/BMXAXK4T?page=15&annotation=F7VGN2M3)_
---
> [!note]
>Extract_ [Page 16](zotero://open-pdf/library/items/BMXAXK4T?page=16&annotation=PD2SBNYM)_
---
> [!note]
>E5_ [Page 19](zotero://open-pdf/library/items/BMXAXK4T?page=19&annotation=YHRG3BDH)_
---
