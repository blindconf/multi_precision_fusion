# Precision-Varying Prediction (PVP)
# [INTERSPEECH 2026] Precision-Varying Prediction (PVP): Robustifying ASR systems against adversarial attacks



This paper [Precision-Varying Prediction (PVP): Robustifying ASR systems against adversarial attacks](https://arxiv.org/abs/2305.17000) is submitted to Interspeech 2026. A demo with a selection of benign, adversarial, and noisy data employed in our experiments is available online: [PVP Demo](Link: ).
>  With the increasing deployment of automated and agentic systems, ensuring the adversarial robustness of Automatic Speech Recognition (ASR) models has become critical. We observe that changing the precision of an ASR model during inference reduces the likelihood of adversarial attacks to succeed. We take advantage of this fact to make the models more robust by simple random sampling of the precision during prediction. Moreover, the insight can be turned into an adversarial example detection strategy by comparing outputs resulting from different precisions and leveraging a simple Gaussian classifier.
     An experimental analysis demonstrates a significant increase in robustness and competitive detection performance for various ASR models and attack types. 
## Prerequisites
Before running the PVP scripts, the following tasks need to be completed:
1. SpeechBrain installation
2. Download datasets
3. Download pre-trained ASR models
4. Generate adversarial examples
   
#### 1. SpeechBrain installation
We analyze a variety of fully integrated PyTorch-based deep learning E2E speech engines using [SpeechBrain](https://github.com/speechbrain/speechbrain). 
Please refer to their website for instructions on how to install it.
We perform evaluations of our detectors using an NVIDIA A40 GPU with 48 GB of memory, along with ASR recipes from SpeechBrain version 0.5.14.

#### 2. Download datasets
We use the following large-scale speech corpus:
* [LibriSpeech (English)](https://www.openslr.org/12)

#### 3. Download pre-trained ASR models
We provide our [pre-trained models](https://ruhr-uni-bochum.sciebo.de/s/lpjW0vxFikG2WqD) that can be used to generate adversarial examples and to test our PVP defense strategy.
In addition, Speechbrain contains pre-trained models that can also be used:

* [CRDNN with CTC/Attention trained on LibriSpeech](https://huggingface.co/speechbrain/asr-crdnn-rnnlm-librispeech)

* [wav2vec 2.0 with CTC trained on LibriSpeech]((https://huggingface.co/speechbrain/asr-wav2vec2-librispeech))

* [Transformer trained on LibriSpeech](https://huggingface.co/speechbrain/asr-transformer-transformerlm-librispeech)

* [Transformer - Whisper](https://huggingface.co/openai/whisper-large-v3)


* [] ()
  
#### 4. Adversarial attacks

1. Generate adversarial examples (e.g., CW or psychoacoustic attacks) by setting the desired precision in the model **hyperparameter configuration files**.
2. Train or run the attack using these precision settings to produce adversarial audio samples.
3. For **cross-precision evaluation**, modify the **inference precision** used by the ASR model when decoding the generated samples.
4. Example `.csv` files for the **LibriSpeech** corpus, including CW adversarial examples and their target transcriptions, are provided in the `results/` folder.
5. These files can also be used as inputs to reproduce or generate the adversarial examples.
The data should be stored using the following folder structure:
```
data_set
└──librispeech
    ├── test-clean
    ├── cw
    ├── ...
└──aishell
    ├── test-clean
    ├── cw
    ├── ...
└──cv-italian
    ├── test-clean
    ├── cw
    ├── ...
└──cv-german
    ├── test-clean
    ├── cw
    ├── ...
```

### Computing Characteristics


1. Run the ASR model on the same input using multiple precision settings.
2. Collect the resulting transcriptions from each precision configuration.
3. Compute pairwise differences between the transcriptions using **Word Error Rate (WER)**.
4. Average these differences to obtain the **precision-diversity score**.
5. Compare the score against the distribution computed from benign samples to identify potential adversarial inputs.


### Building and evaluating Gaussian classifiers

1. Run the ASR model on the same input `x` using multiple precision settings `{p1, ..., pK}`.
2. Collect the resulting transcriptions: `Y(x) = {f_p1(x), ..., f_pK(x)}`.
3. Compute the pairwise transcription differences using Word Error Rate (WER).
4. Average all pairwise WER values to obtain the **precision-diversity score** `D(x)`.
5. Estimate the mean `μ` and variance `σ²` of `D(x)` on benign samples.
6. Flag an input as **adversarial** if its score deviates significantly from this benign distribution.
python distriblock_classifiers.py -h


positional arguments:
  FOLDER_ORIG  Folder path that contains the characteristics of the benign examples.
  FOLDER_ADV   Folder path that contains the characteristics of the adversarial examples.```

options:
  -h, --help   show this help message and exit


