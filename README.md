# African-Language-Processing-Architecture
Attempt at an AI language processing system that could to provide robust solutions for African language translation and speech processing. Specifically, my goals include creating a network that can perform: Speech-to-Speech, Speech-to-Text, Text-to-Speech and Text-to-Text Translation with Automatic Speech Recognition with a better accuracy than existing solutions.
Initial focus on creating a small scale working prototype using Bibeli-Mimo of the yoruba language, before attempting a larger scale protoype based on the ÌròyìnSpeech dataset.

---

## Stage 1 – Small-Scale TTS (Current)

- Train a basic text-to-speech model using Bibeli Mímọ́
- Output quality is low

**Likely reasons:**
- Not enough data
- Data quality issues
- Diacritics inconsistencies

---

## Stage 2 – Demo Attempts with Existing Models

Tried preparing a demo using:

- VibeVoice 1.5B (LoRA)
- `yoruba-adr` (cleaned)
- NaijaVoices  
  https://huggingface.co/datasets/naijavoices/naijavoices-dataset
- Possibly OmniASR  
  https://huggingface.co/datasets/facebook/omnilingual-asr-corpus

**Findings:**
- VibeVoice fine-tuning is poor for multilingual use
- Cross-entropy loss too high
- Generalisation is bad

---

## Stage 3 – Dataset Expansion & Diacritics Work

- Expanded to multiple written Yoruba datasets
- Tried standardising diacritics across datasets
- Looked into modifying `yoruba-adr`

Still messy. Diacritics + orthography are a major blocker.

---

## Stage 4 – Model Exploration

Looked into (or tested):

- `maya1`
- `voxcpm1.5`
- `echoo-tts`
- Other similar models

**Conclusion:**  
Better to start from scratch (or almost scratch) than to fight pretrained multilingual models.

---

## Stage 5 – Current Training Intent / Plan

**Rough pipeline:**

Normalize data  
→ create / improve ADR  
→ simple-ish text LLM  
→ ASR (+ ADR)  
→ collect more speech  
→ improve text model  
→ TTS  
→ Speech-to-Speech

**Main requirement:** a lot more data.

**Plans:**
- Clean results properly
- Produce some decent samples
- Re-request ÌròyìnSpeech access later, using current progress as proof

---

## Status

- Acceptable progress so far
- More ample outputs possible soon-ish
