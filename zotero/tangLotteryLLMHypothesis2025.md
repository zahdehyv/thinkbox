---
Title: "The Lottery LLM Hypothesis, Rethinking What Abilities Should LLM Compression Preserve?"
Year: 2025 (February)
Authors: Zhenheng Tang, Xiang Liu, Qian Wang, Peijie Dong, Bingsheng He, Xiaowen Chu, Bo Li
Tags: 

- Computer_Science_-_Machine_Learning

- Computer_Science_-_Computation_and_Language

- Computer_Science_-_Artificial_Intelligence

- Computer_Science_-_Formal_Languages_and_Automata_Theory

aliases: 
- "The Lottery LLM Hypothesis, Rethinking What Abilities Should LLM Compression Preserve?"
- ""
---
> [!ABSTRACT]
>Motivated by reducing the computational and storage costs of LLMs, model compression and KV cache compression have attracted much attention from researchers. However, current methods predominantly emphasize maintaining the performance of compressed LLMs, as measured by perplexity or simple accuracy on tasks of common sense knowledge QA and basic arithmetic reasoning. In this blog, we present a brief review of recent advancements in LLMs related to retrievalaugmented generation, multi-step reasoning, external tools, and computational expressivity, all of which substantially enhance LLM performance. Then, we propose a lottery LLM hypothesis suggesting that for a given LLM and task, there exists a smaller lottery LLM capable of producing the same performance as the original LLM with the assistance of multi-step reasoning and external tools. Based on the review of current progress in LLMs, we discuss and summarize the essential capabilities that the lottery LLM and KV cache compression must possess, which are currently overlooked in existing methods.
---
> [!tip] LINK
> [PDF](zotero://select/library/items/YEVENGL5)

> [!note]
>These basic transformers fall short of Turing completeness, as they are incapable of solving problems that are complete for classes larger than T C0, such as simulating automata, which is N C1-complete._ [Page 4](zotero://open-pdf/library/items/YEVENGL5?page=4&annotation=RIH9UBVQ)_
---
> [!note]
>Recent research indicates that autoregressive decoding, which facilitates the processing of arbitrarily long input strings, can simulate a universal Turing machine_ [Page 4](zotero://open-pdf/library/items/YEVENGL5?page=4&annotation=2JWQYIQ3)_
---
> [!note]
>Stack-Attention_ [Page 4](zotero://open-pdf/library/items/YEVENGL5?page=4&annotation=9A7J38ES)_
---
> [!note]
>With the integration of external memory and simple regular expression parsers, transformers can simulate the execution of a universal Turing machine, specifically U15,2_ [Page 4](zotero://open-pdf/library/items/YEVENGL5?page=4&annotation=GK5LIJ6K)_
---
> [!note]
>Planning and Scheduling_ [Page 5](zotero://open-pdf/library/items/YEVENGL5?page=5&annotation=NZZHYSWS)_
---
> [!note]
>The essence of multi-step reasoning lies in decomposing the original problem into multiple sub-problems and addressing them sequentially. This process involves planning and scheduling. To facilitate autonomous planning and scheduling, recent studies propose employing LLMs as meta-agents to orchestrate planning and scheduling, wherein the original problem is decomposed, and the meta-agent delegates sub-problems to other LLMs based on the schedule_ [Page 5](zotero://open-pdf/library/items/YEVENGL5?page=5&annotation=SQNZ65V9)_
---
> [!note]
>With the aid of external symbolic reasoning, LLMs can also engage in planning and scheduling to resolve problems_ [Page 5](zotero://open-pdf/library/items/YEVENGL5?page=5&annotation=FDGYY8CQ)_
---
> [!important] Image
> ![[zotero/tangLotteryLLMHypothesis2025/image-5-x305-y160.png]]
> _algorithm A for solving with the smaller LLM [Page 5](zotero://open-pdf/library/items/YEVENGL5?page=5&annotation=YN4XCKE2)_
---
