# Event-log enrichment from procurement notices: an expert-validated LLM framework in the legal domain

**Ivan Spada, Roberto Nai, Davide Audrito, Vittoria Sofia Margherita Trifiletti and Emilio Sulis**

---
## Abstract

Legal and administrative sources often describe procedural steps that are not recorded in structured data, making them difficult to include in process mining analyses. In this work, we present an approach that uses Large Language Models (LLMs) to extract events and dates from unstructured legal texts. The methodology is applied to a dataset of Italian procurement notices published since 2022 on the official EU platform, Tenders Electronic Daily (TED), demonstrating how LLMs can extract valuable information, such as administrative decisions adopted prior to tender publication. These extracted elements are incorporated into existing event logs, thereby enhancing the quality of process analysis. A sample of the extracted data has been manually reviewed by legal experts to assess the relevance and correctness of the automated detection. The results suggest that this approach can help identify procedural steps hidden in free text, thereby supporting more complete and accurate representations of legal workflows.

---

## Repository structure

- `article/` — final article (short)

- `res/` — resources and outputs
	- `event_extraction/` — input and processed CSVs, LLM outputs
	- `evaluation/` — annotation guidelines, samples and annotation spreadsheets
	- `preliminary_evaluation/` — gold standard and per-model prompt outputs (CSV/JSON)
	- `prompts/` — prompt templates (zero-shot, few-shot, CoT, system prompt)

- `src/` — code and notebooks
	- `step1_data_preparation.ipynb` — data cleaning and CSV generation
	- `step2_llm_event_detection.ipynb` — prompt execution and result collection
	- `vars.py` — paths and configuration constants used by notebooks

---

## Quick start

1. Open the notebooks with Jupyter Lab or Notebook.
2. Run `step1_data_preparation.ipynb` to prepare data.
3. Run `step2_llm_event_detection.ipynb` to generate or process LLM outputs (API keys required if calling external models).

---

## Notes

- Files in `res/` are experimental outputs and may be overwritten by the notebooks.
- Use the annotation spreadsheets in `res/evaluation/` only after backing them up.

---
## Connected Projects
Please see also the TED project here: [https://github.com/roberto-nai/TED-OD-EVENTLOG](https://github.com/roberto-nai/TED-OD-EVENTLOG).  

---

## Citation

If you use these scripts, please cite:

```bibtex
@inproceedings{DBLP:conf/jurix/SpadaNATS25,
	author       = {Ivan Spada and
									Roberto Nai and
									Davide Audrito and
									Vittoria Margherita Sofia Trifiletti and
									Emilio Sulis},
	editor       = {R{\'{e}}ka Markovich and
									Luigi Di Caro and
									Amon Rapp and
									Claudio Schifanella},
	title        = {An Expert-Validated {LLM} Framework for Transforming Legal Procurement
									Texts into Actionable Data},
	booktitle    = {Legal Knowledge and Information Systems - {JURIX} 2025: The Thirty-eighth
									Annual Conference, Turin, Italy, 9-11 December 2025},
	series       = {Frontiers in Artificial Intelligence and Applications},
	pages        = {356--363},
	publisher    = {{IOS} Press},
	year         = {2025},
	url          = {https://doi.org/10.3233/FAIA251610},
	doi          = {10.3233/FAIA251610},
}
```

---



---

For questions or issues, please contact the project author [ivan.spada@unito.it](ivan.spada@unito.it).
