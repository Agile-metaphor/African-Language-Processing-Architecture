# African-Language-Processing-Architecture
Attempt at an AI language processing system that could to provide robust solutions for African language translation and speech processing. Specifically, my goals include creating a network that can perform: Speech-to-Speech, Speech-to-Text, Text-to-Speech and Text-to-Text Translation with Automatic Speech Recognition with a better accuracy than existing solutions.
Initial focus on creating a small scale working prototype using Bibeli-Mimo of the yoruba language, before attempting a larger scale protoype based on the ÌròyìnSpeech dataset.

First stage - 
training small scale text to speech based on Bibeli Mimo

(low quality, not enough data as well?)
Previous x3 stage -
Expanding to include more datasests standardising diacritics of multiple written datasets (modify yoruba-adr?)

Previous x2 stage -
Preparing a demo using vibevoice 1.5B Lora yoruba-adr cleaned and naijavoices https://huggingface.co/datasets/naijavoices/naijavoices-dataset dataset possibly with https://huggingface.co/datasets/facebook/omnilingual-asr-corpus omniASR dataset 

Findings - nope -  vibevoice finetuning is poor for multilingual purpsoes, cross entropy loss too high

Previous stage
try with maya1, voxcpm1.5, echoo-tts maybe? other models

Findings - better start from scratch or almost scratch

Current plan intent for training:- Normalize data → make ADR? → simple ish LLM(text) → ASR(+ADR) → find more speech → improve LLM(text) → TTS → S2ST
Get lots and lots of data, (Attempt to request IroyinSpeech access again after providing current results?).
Clean results
