# PhD Thesis: Machine Learning Based Cyber Attacks Targeting on Controlled Information

Everything about code sources, datasets and data sources mentioned in the thesis.

_ _ _

## [Table of contents](README.md)
* Structure of Thesis & Completed Work 
* Literature Review
  * Stealing controlled user activities information
  * Stealing controlled ML model related information
  * Stealing controlled authentication inforamtion
* The Audio Auditor: User-Level Membership Inference with Black-Box Access
* The Audio Auditor: Label-Only User-Level Membership Inference in Internet of Things Voice Services
* The Audio Auditor: No-Label User-Level Membership Inference in Internet of Things Voice Services
* FAAG: Fast Adversarial Audio Generation through Interactive Attack Optimisation
  
_ _ _

### Structure of Thesis & Completed Work
<p>Abstract:</p>
<p>Due to the fast development of machine learning (ML) techniques, cyber attacks utilize ML algorithms to achieve a high success rate and cause a lot of damage. Specifically, the attack against ML models, along with the increasing number of ML-based services, has become one of the most emerging cyber security threats in recent years. We review the ML-based stealing attack in terms of targeted controlled information, including controlled user activities, controlled ML model-related information, and controlled authentication information. An overall attack methodology is extracted and summarized from the recently published research. When the ML model is the target, the attacker can steal model information or mislead the model’s behaviours. The model information stealing attacks can steal the model’s structure information or model’s training set information. Targeting at Automated Speech Recognition (ASR) system, the membership inference method is studied to whether the model’s training set can be inferred at user-level, especially under the black-box access. Under the label-only black-box access, we analyse user’s statistical information to improve the user-level membership inference results. When even the label is not provided, google search results are collected instead, while fuzzy string matching techniques would be utilized to improve membership inference performance. Other than inferring training set information, understanding the model’s structure information can launch an effective adversarial ML attack. The Fast Adversarial Audio Generation (FAAG) method is proposed to generate targeted adversarial examples quickly. By injecting the noise over the beginning part of the audio, the FAAG method can speed up around 60\% compared with the baseline method during the adversarial example generation process. In accordance with these attack methodologies, the limitations and future directions of ML-based cyber attacks are presented. The current countermeasures are also summarized and discussed for adequate protections because of their urgent needs.</p>


|Chapter         | Related Work          | Accepted/Published by|
|:-------------|:------------------|:------|
|Literature Review    |Machine Learning Based Cyber Attacks Targeting on Controlled Information: A Survey    |ACM Computing Survey 2021 (Accepted [arxiv](https://arxiv.org/abs/2102.07969)) |
|The Audio Auditor: User-Level Membership Inference with Black-Box Access    |The Audio Auditor: Participant-Level Membership Inference in Internet of Things Voice Services    |CCS PPML Workshop (Poster) |
|The Audio Auditor: Label-Only User-Level Membership Inference in Internet of Things Voice Services    |The audio auditor: user-level membership inference in Internet of Things voice services    |[PoPETs 2021](https://researchonline.jcu.edu.au/64660/1/64660.pdf) |
|The Audio Auditor: No-Label User-Level Membership Inference in Internet of Things Voice Services    |To submit to...    |None |
|FAAG: Fast Adversarial Audio Generation through Interactive Attack Optimisation    |FAAG: Fast Adversarial Audio Generation through Interactive Attack Optimisation    |IEEE Transactions on Computers 2021 (Accepted) |


_ _ _
### Literature Review
Part of the content comes from our survey paper: [Machine Learning Based Cyber Attacks Targeting on Controlled Information: A Survey](https://github.com/skyInGitHub/Machine-Learning-Based-Cyber-Attacks-Targeting-on-Controlled-Information-A-Survey)

#### [Stealing controlled user activities information](https://github.com/skyInGitHub/Machine-Learning-Based-Cyber-Attacks-Targeting-on-Controlled-Information-A-Survey/blob/master/user_activities.md)
<p> According to utilized kernel data and sensor data, controlled user activities information were stolen with timing analysis and frequency analysis. For the attack using kernel data, we review the attack utilizing the interrupt sources like procfs and OS-level information like memory, network, and file system information. The sensor information can reveal the controlled user activity information indirectly, i.e. acoustic and magnetic data.</p>

#### [Stealing controlled ML model related information](https://github.com/skyInGitHub/Machine-Learning-Based-Cyber-Attacks-Targeting-on-Controlled-Information-A-Survey/blob/master/ml_model_related.md)
<p>Leveraging the query inputs and outputs, model description can be stolen by equation-solving, patch-finding and linear least square methods, while training samples can be stolen by model inversion attack, the GAN attack, and membership inference attack.</p>

#### [Stealing controlled authentication inforamtion](https://github.com/skyInGitHub/Machine-Learning-Based-Cyber-Attacks-Targeting-on-Controlled-Information-A-Survey/blob/master/authentication.md)
<p>The controlled authentication information mainly contains keystroke data, secret keys and password data. As shown in Fig 4, classification models or probabilistic models are trained to steal the controlled authentication information. Leveraging the acceleration, acoustic and video information, we review the attack stealing these keystroke information. We also investigate the attack stealing controlled secret key information via analyzing the state of targeted cache set. Moreover, we study the password guessing attack by analyzing the password patterns with ML techniques.</p>


_ _ _
### The Audio Auditor: User-Level Membership Inference with Black-Box Access
<p>Abstract:</p> [link](auditor_black-box.md)
<p>Voice interfaces and assistants implemented by various services have become increasingly sophisticated, powered by increased availability of data. However, users' audio data needs to be guarded while enforcing data-protection regulations, such as the GDPR law and the COPPA law. To check the unauthorized use of audio data, we propose an audio auditor for users to audit speech recognition models. Specifically, users can check whether their audio recordings were used as a member of the model's training dataset or not. In this chapter, we focus our work on a DNN-HMM-based automatic speech recognition model over the TIMIT audio data. As a proof-of-concept, the success rate of participant-level membership inference can reach up to 90\% with eight audio samples per user, resulting in an audio auditor.</p>


_ _ _
### The Audio Auditor: Label-Only User-Level Membership Inference in Internet of Things Voice Services
<p>Abstract:</p> [link](auditor_label-only.md)
<p>With the rapid development of deep learning techniques, the popularity of voice services implemented on various Internet of Things (IoT) devices is ever increasing. In this chapter, we examine user-level membership inference in the problem space of voice services, by designing an audio auditor to verify whether a specific user had unwillingly contributed audio used to train an automatic speech recognition (ASR) model under strict black-box access. With user representation of the input audio data and their corresponding translated text, our trained auditor is effective in user-level audit. We also observe that the auditor trained on specific data can be generalized well regardless of the ASR model architecture. We validate the auditor on ASR models trained with LSTM, RNNs, and GRU algorithms on two state-of-the-art pipelines, the hybrid ASR system and the end-to-end ASR system. Finally, we conduct a real-world trial of our auditor on iPhone Siri, achieving an overall accuracy exceeding 80\%. We hope the methodology developed in this chapter and findings can inform privacy advocates to overhaul IoT privacy.</p>


_ _ _
### The Audio Auditor: No-Label User-Level Membership Inference in Internet of Things Voice Services
<p>Abstract:</p> [link](auditor_no-label.md)
<p>With the fast development of machine learning techniques, the voice services embeded in various Internet of Things (IoT) devices becomes the most popular function in people's daily life. In this chapter, we examine user-level membership inference targeting an automatic speech recognition (ASR) model within the voice services under no-label black-box access. Specifically, we design a user-level audio auditor to determine whether a specific user had unwillingly contributed audio used to train the ASR model, when the service only reacts on user's query audio without providing the translated text. With user representation of the input audio data and their corresponding system's reaction, our auditor shows an effective auditing in user-level membership inference. Our experiments shows that the auditor behaves better with more training samples and samples with more audios per user. We evaluate the auditor on ASR models trained with different algorithms (LSTM, RNNs, and GRU) on the hybrid ASR system (Pytorch-Kaldi). We hope the methodology developed in this chapter and findings can inform privacy advocates to overhaul IoT privacy.</p>


_ _ _
### FAAG: Fast Adversarial Audio Generation through Interactive Attack Optimisation
<p>Abstract: [link](FAAG.md) </p>
<p>Automatic Speech Recognition services (ASRs) inherit deep neural networks' vulnerabilities like crafted adversarial examples. Existing methods often suffer from low efficiency because the target phases are added to the entire audio sample, resulting in high demand for computational resources. This chapter proposes a novel scheme named FAAG as an iterative optimization-based method to generate targeted adversarial examples quickly. By injecting the noise over the beginning part of the audio, FAAG generates adversarial audio in high quality with a high success rate timely. Specifically, we use audio's logits output to map each character in the transcription to an approximate position of the audio's frame. Thus, an adversarial example can be generated by FAAG in approximately two minutes using CPUs only and around ten seconds with one GPU while maintaining an average success rate over 85\%. Specifically, the FAAG method can speed up around 60\% compared with the baseline method during the adversarial example generation process. Furthermore, we found that appending benign audio to any suspicious examples can effectively defend against the targeted adversarial attack. We hope that this work paves the way for inventing new adversarial attacks against speech recognition with computational constraints.</p>



[back](https://github.com/skyInGitHub/PhD_thesis)
