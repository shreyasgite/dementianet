
DementiaNet
==============================

**[Colab Walkthrough](https://drive.google.com/drive/folders/1CYDqhwvHMFiKD4tz2z-T16-eQhxPf6qe?usp=sharing)**

DementiaNet is a longitudinal spontaneous speech (audio) dataset for dementia screening. These are audio samples scrapped from youtube for public figures and celebrities:
- who had confirmed dementia diagnoses for Dementia data
- who lived on to beyond 90 years without any noticeable decline in cognitive health for No-dementia data. 

The sample dataset contains a hundred individuals with a confirmed dementia diagnosis. Spontaneous speech samples (audio) range from time after the confirmed diagnosis to ten years before the symptoms appear. And a hundred individuals over the age of eighty with no cognitive decline (NC) and active in their field of work. Spontaneous speech samples for the NC group fall into three buckets, five years, ten years and fifteen years before death or current age.
Early analysis of this dataset shows above 70% accuracy. According to our knowledge, DementiaNet is the largest publicly available longitudinal dataset for dementia prediction/screening.

**Note that this is a preliminary release.** The raw data used for constructing the data sets and the youtube URLs are available upon request.


### Download
* DementiaNet: [Google Sheet with URLs and metadata](https://docs.google.com/spreadsheets/d/1ih3FjEsiKDctS2oFhZKXah-OrzEridgUDHKu2awXSx8/edit?usp=sharing)
* Dementia data: [dementia audio clips](https://drive.google.com/drive/folders/1GKlvbU57g80-ofCOXGwatDD4U15tpJ4S?usp=sharing)
* No-Dementia data: [nodementia audio clips](https://drive.google.com/drive/folders/1jm7w7J8SfuwKHpEALIK6uxR9aQZR1q8I?usp=sharing)
* Code: [Colab starter code](https://drive.google.com/drive/folders/1CYDqhwvHMFiKD4tz2z-T16-eQhxPf6qe?usp=sharing)
* train file: [train_dm.csv](https://drive.google.com/file/d/1bDsEo_LNP1sAtoKfIfwCkdC_PEzs3S0u/view?usp=sharing)
* valid file: [valid_dm.csv](https://drive.google.com/file/d/1-89Y_Jc-uItJskT_cGTiEVqVhw85QXpa/view?usp=sharing)


### Motivation
Alzheimer's sucks!
The development of Alzheimer's starts long before the onslaught of symptoms. By the time the symptoms are diagnosed, it is too late to treat the condition. If we could diagnose Alzheimer's early enough, studies have shown that lifestyle changes and therapies can significantly slow the progression of Alzheimer's disease. Catching cognitive impairment early is essential to helping those with the condition.

However I could not find any open dataset containing longitudinal audio samples of spontaneous speech for Alzheimer's. Hence the DementiaNet. 


### Approach
Dementia Data:
For the positive audio samples, I went for public figures and celebrities with confirmed cases of dementia diagnosis. Upon confirming the diagnosis, we tried finding interviews with said person after the said onslaught of symptoms or confirmation, between zero and five years, between five and ten years and between ten and fifteen years before the symptoms took over. 

No-Dementia Data:
To avoid any data leakage or false negatives, we had to be extra careful here. We started with public figures and celebrities who were confirmed, centurions and stayed with individuals who are still alive and above 85 or passed away after being 90 years old without any signs or diagnosis of dementia. 
We then collected three audio samples per individual, one after they were above age 70, one between age 55 and 70 and one where they were younger than 55 years old. 

We focused on spontaneous interviews for the audio samples and strictly avoided speeches, movie scenes, and anything where the person of interest could rehearse or read the text. 


### Documentation
* WIP


### Next up
* Clean the data - noise and background audio separation. 
* Create a pipeline for ASR and train the system together wtih audio and text.
* Upload the data to Huggingface. 
* Extend the data to 1000 individuals. If you are open to play around with raw data, do get in touch. 


### Acknowledgements
* The training script were taken from [Mehrdad Farahani's](https://github.com/m3hrdadfi) [notebooks](https://github.com/m3hrdadfi/soxan) for speech classification
* Most of my learning for working with audio and huggingface came from [Patrick's](https://twitter.com/PatrickPlaten) excellent [tutorials](https://huggingface.co/blog/fine-tune-xlsr-wav2vec2) on the topic. 


### Contact
If you are curious about the DementiaNet or have any questoins/suggestions, let us know - hey@tuul.ai
