# Conversational Short-phrase Speaker Diarization Challenge

## Rules

All participants should adhere to the following rules: 

1.	DATA: Only MagicData RAMC (openslr 123), VoxCeleb Data (openslr 49) and CN-Celeb Corpus (openslr 82) are allowed to use. Data augmentation could be used to process the training sets, and two noise datasets, i.e., MUSAN (openslr 17), RIRNoise (openslr 28), are allowed.
2.	The use of Test dataset in any form of non-compliance is strictly prohibited, including but not limited to use the Test dataset to fine-tune or train the model. 
3.	Multi-system fusion is allowed. However, fusing systems with same structure is not encouraged.  
4.	All models should train on the allowed datasets. Specifically, pre-train model using other datasets (including unlabeled data) are not allowed in this challenge. 
5.	The right of final interpretation belongs to the organizer. In case of special circumstances, the organizer will coordinate the interpretation. 

## Dataset

The MagicData-RAMC corpus contains 180 hours of conversational speech data recorded from native speakers of Mandarin Chinese over mobile phones with a sampling rate of 16 kHz. The dialogs in MagicData-RAMC are classified into 15 diversified domains and tagged with topic labels, ranging from science and technology to ordinary life. Accurate transcription and precise speaker voice activity timestamps are manually labeled for each sample. Speakers' detailed information is also provided. As a Mandarin speech dataset designed for dialog scenarios with high quality and rich annotations, MagicData-RAMC enriches the data diversity in the Mandarin speech community and allows extensive research on a series of speech-related tasks, including automatic speech recognition, speaker diarization, topic detection, keyword search, text-to-speech, etc. Please refer to [MagicData RAMC](https://github.com/MagicHub-io/MagicData-RAMC)

## Baseline

We use VBHMM x-vectors (aka VBx) trained by VoxCeleb Data (openslr-49) and CN-Celeb Corpus (openslr-82) as baseline system. X-vectors embeddings are extracted by ResNet, and besides, agglomerative hierarchical clustering with variational Bayes HMM resegmentation are conducted to get final result. Please refer to [MagicData RAMC](https://github.com/MagicHub-io/MagicData-RAMC)


## Scoring tool

We adopt Conversational-DER (CDER) to evaluate the speaker diarization system. In real conversations, there are cases that a shorter duration contains vital information. The evaluation of the speaker diarization system based on the time duration is difficult to reflect the recognition performance of short-term segments. Our basic idea is that for each speaker, regardless of the length of the spoken sentence, all type of mistakes should be equally reflected in the final evaluation metric. Based on this, we intend to evaluate the performance of the speaker diarization system on the sentence level under conversational scenario (utterance level). Please refer to [CDER Metric](https://github.com/MagicHub-io/CDER_Metric)

## Contact

If you have any questions, please contact us. You could open an issue on github or [email us](open@magicdatatech.com]).
