# FOLLIE dataset for NL-to-FOL and NLI tasks

FOLLIE (First-Order Logic for Language Inference and Entailment) is the first dataset for French with natural language sentences and their corresponding first-order logic (FOL) formulas.

The sentences in the dataset were drawn from all the existing French Natural Language Inference (NLI) datasets, namely DACCORD, FraCaS-FR, GQNLI-FR, RTE3-FR (dev and test), SICK-FR, and XNLI (dev and test). These datasets are structured as sentence pairs (premise(s) and hypothesis) annotated with a gold label (entailment, neutral, or contradiction).
The resulting FOLLIE dataset preserves all these elements for the converted sentences, in addition to providing logical representations of the sentences. It can therefore be used either for natural language–to–FOL translation tasks or for NLI/RTE tasks using neurosymbolic AI approaches (i.e., solving NLI by reasoning over FOL formulas).

The logical formulas follow the format used in the NLTK package, thus they are fully compatible with the NLTK Logic Parser.

FOLLIE dataset is also available on [huggingface.co](https://huggingface.co/datasets/maximoss/follie).

# Use

The dataset can be used for the task of translating French sentences into their corresponding logical representation in first-order logic, or for the task of natural language inference (NLI) with (neuro)symbolic AI methods. The NL-to-FOL task is a sequence-to-sequence task, whereas the NLI task is a sentence-pair classification task.

If used for NLI, you should only keep the rows where the FOL formulas for both all the premise(s) and the hypothesi(e)s are available, and filter out the rows where one of the two is not available in the dataset.

# Cite

TBA soon, but for the moment you can cite this paper:

**BibTex**
````BibTeX
@inproceedings{skandalis-etal-2025-neurosymbolic,
    title = "Neurosymbolic {AI} for Natural Language Inference in {F}rench : combining {LLM}s and theorem provers for semantic parsing and natural language reasoning",
    author = "Skandalis, Maximos  and
      Abzianidze, Lasha  and
      Moot, Richard  and
      Retor{\'e}, Christian  and
      Robillard, Simon",
    editor = "Evang, Kilian  and
      Kallmeyer, Laura  and
      Pogodalla, Sylvain",
    booktitle = "Proceedings of the 16th International Conference on Computational Semantics",
    month = sep,
    year = "2025",
    address = {D{\"u}sseldorf, Germany},
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2025.iwcs-main.21/",
    pages = "242--253",
    ISBN = "979-8-89176-316-6",
    abstract = "In this article, we describe the first comprehensive neurosymbolic pipeline for the task of Natural Language Inference (NLI) for French, with the synergy of Large Language Models (CamemBERT) and automated theorem provers (GrailLight, LangPro). LLMs prepare the input for GrailLight by tagging each token with Part-of-Speech and grammatical information based on the Type-Logical Grammar formalism. GrailLight then produces the lambda-terms given as input to the LangPro theorem prover, a tableau-based theorem prover for natural logic originally developped for English. Currently, the proposed system works on the French version of SICK dataset. The results obtained are comparable to the ones on the English and Dutch versions of SICK with the same LangPro theorem prover, and are better than the results of recent transformers on this specific dataset.Finally, we have identified ways to further improve the results obtained, such as giving access to the theorem prover to lexical knowledge via a knowledge base for French."
}
````
**ACL**

Maximos Skandalis, Lasha Abzianidze, Richard Moot, Christian Retoré, and Simon Robillard. 2025. [Neurosymbolic AI for Natural Language Inference in French : combining LLMs and theorem provers for semantic parsing and natural language reasoning](https://aclanthology.org/2025.iwcs-main.21/). In *Proceedings of the 16th International Conference on Computational Semantics*, pages 242–253, Düsseldorf, Germany. Association for Computational Linguistics.

# Acknowledgements

This work was supported by the Defence Innovation Agency (AID) of the Directorate General of Armament (DGA) of the French Ministry of Armed Forces, and by the ICO, _Institut Cybersécurité Occitanie_, funded by Région Occitanie, France.
