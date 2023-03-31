# Adversarial_Attacks_Detection_NLP

In this work, the aim was to develop adversarial text attacks detectors for NLP application, especially for Transformer model-based ones. To do so, we rely on Out-Of-Distribution (OOD) samples detection methods. 

We applied three methods for out-of-distribution samples detection:
Max-softmax, 
Doctor discriminator,
Mahanobis distance based detector 

As evaluation metrics we have used:
AUROC
AUPR

Steps : 
1 - We build a Sentiment classifier using a pretrained transformer models (You can choose bert or Roberta), and we train it on various NLP benchmark datasets (imdb,ag-news,sst2).

2 - Then we use a text attack generator according to this repository https://github.com/bangawayoo/adversarial-examples-in-text-classification, to generate adversarial samples (we have put some generated attacks file in the attack foler). 

3 - Then we applied out-of-distribution samples detection method, and compute evaluation metrics 

NB: We didn't have a lot ressource to properly train our model To test different scenario we provide at the top of our notebook a config file as global variable

Global Variable
PRE_TRAINED_MODEL_NAME = 'bert-base-cased' #'robbert-base-cased' PATH_to_attack_data="/content/drive/MyDrive/adversarial-examples-in-text-classification/imdb__textattackbert-base-uncased-imdb_bert__pwws.csv" PATH_to_saved_model="/content/drive/MyDrive/cache/best_model_state.bin"
