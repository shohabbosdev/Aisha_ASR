---

language:
- uz
license: apache-2.0
base_model: openai/whisper-medium
tags:
- generated_from_trainer
datasets:
- mozilla-foundation/common_voice_17_0
metrics:
- wer
model-index:
- name: Whisper Medium UZB
  results:
  - task:
      name: Automatic Speech Recognition
      type: automatic-speech-recognition
    dataset:
      name: Common Voice 17.0
      type: mozilla-foundation/common_voice_17_0
      config: uz
      split: None
      args: 'config: uz, split: test'
    metrics:
    - name: Wer
      type: wer
      value: 31.77905998468049
      
---

<!-- This model card has been generated automatically according to the information the Trainer had access to. You
should probably proofread and complete it, then remove this comment. -->

# Whisper Medium UZB - AISHA

This model is a fine-tuned version of [openai/whisper-medium](https://huggingface.co/openai/whisper-medium) on the Common Voice 17.0 dataset.
It achieves the following results on the evaluation set:
- Loss: 0.2859
- Wer: 31.7790

## Model description

More information needed

## Intended uses & limitations

More information needed

Founder: Rifat Mamayusupov

## Training and evaluation data

More information needed

## Training procedure

### Training hyperparameters

The following hyperparameters were used during training:
- learning_rate: 1e-05
- train_batch_size: 16
- eval_batch_size: 8
- seed: 42
- gradient_accumulation_steps: 2
- total_train_batch_size: 32
- optimizer: Adam with betas=(0.9,0.999) and epsilon=1e-08
- lr_scheduler_type: linear
- lr_scheduler_warmup_steps: 500
- training_steps: 4000
- mixed_precision_training: Native AMP

### Training results

| Training Loss | Epoch  | Step | Validation Loss | Wer     |
|:-------------:|:------:|:----:|:---------------:|:-------:|
| 0.5187        | 0.5392 | 1000 | 0.4935          | 44.1403 |
| 0.3423        | 1.0785 | 2000 | 0.4008          | 37.6948 |
| 0.3018        | 1.6177 | 3000 | 0.3739          | 36.3575 |
| 0.2401        | 2.1569 | 4000 | 0.2821          | 31.7791 |


### Framework versions

- Transformers 4.41.2
- Pytorch 2.3.1+cu121
- Datasets 2.20.0
- Tokenizers 0.19.1