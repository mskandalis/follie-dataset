# FOLLIE dataset for NL-to-FOL and NLI tasks

FOLLIE (First-Order Logic for Language Inference and Entailment) is the first dataset for French with natural language sentences and their corresponding first-order logic (FOL) formulas.

The sentences in the dataset were drawn from all the existing French Natural Language Inference (NLI) datasets, namely DACCORD, FraCaS-FR, GQNLI-FR, RTE3-FR (dev and test), SICK-FR, and XNLI (dev and test). These datasets are structured as sentence pairs (premise(s) and hypothesis) annotated with a gold label (entailment, neutral, or contradiction).
The resulting FOLLIE dataset preserves all these elements, in addition to providing logical representations of the sentences. It can therefore be used either for natural language–to–FOL translation tasks or for NLI/RTE tasks using neurosymbolic approaches (i.e., solving NLI by reasoning over FOL formulas).

The logical formulas follow the format used in the NLTK package, thus they are fully compatible with the NLTK Logic Parser.

# Acknowledgements

This work was supported by the Defence Innovation Agency (AID) of the Directorate General of Armament (DGA) of the French Ministry of Armed Forces, and by the ICO, _Institut Cybersécurité Occitanie_, funded by Région Occitanie, France.
