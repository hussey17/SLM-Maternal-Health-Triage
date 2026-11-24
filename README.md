# Infrastructure Agnostic Maternal Health Triage

**Deploying Fine Tuned and Quantized Small Language Models in Low Resource Settings**

Hassaan Tayyab, Imran Haider and Muhammad Ibrahim Anwar (equal contribution)
Lahore University of Management Sciences (LUMS), course project

Full write-up: [`CS5606_G7_Writeup.pdf`](CS5606_G7_Writeup.pdf)

## Summary

We test whether small language models (SLMs) running offline can replace a cloud LLM for generating maternal health records from health-worker dictations in code-switched Roman Urdu.

- **Data:** 150 synthetic clinical dictations, grounded in published maternal-health vocabularies and WHO antenatal care guidelines, with realistic speech-recognition errors and explicit and implicit red flags.
- **Models:** Gemma 2 2B, Llama 3.2 3B and Qwen 2.5 3B, compared with Gemini 2.5 Flash.
- **RQ1:** Off-the-shelf SLMs vs the cloud LLM.
- **RQ2:** LoRA fine-tuning on 120 cases.
- **RQ3:** 4-bit NF4 quantization for budget mobile hardware.
- **Evaluation:** an LLM-as-judge scores each record on a 90-point, eight-dimension clinical rubric, validated against two clinicians.

Fine-tuned SLMs matched or exceeded the cloud baseline, and 4-bit Qwen 3B matched it (62.14 vs 62.34 out of 90) within 2 GB of memory.

## Repository contents

| Path | Contents |
|---|---|
| `CS5606_G7_Writeup.pdf` | Final write-up |
| `Group 7 Proposal.*`, `G7_Methodology.*`, `Paper Structure.docx` | Proposal, methodology and paper outline |
| `Deliverables Phase 2/` | Interview protocol, user-needs report and literature review |
| `Interview Deliverable Dump/` | Synthetic transcription pilots, generation script and prompt template |
| `CS5606 200 Transcriptions - Claude Sonnet 4.6.docx` | Synthetic dictation corpus |
| `System_Prompt.txt` | Prompt used to generate the synthetic dictations |
| `Findings/` | Per-RQ results (CSV) and evaluation figures |
| `Quantization/` | Generated records from the 4-bit models, one JSON per case |
| `Presentation Template.ppt` | Presentation slides |

All dictations are synthetic. No real patient data is included.

Papers by other authors that we consulted are not redistributed here. They are cited in the write-up's reference list.
