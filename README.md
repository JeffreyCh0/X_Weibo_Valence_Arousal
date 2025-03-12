# X_Weibo_Valence_Arousal
This is the github repository for the paper [Language-based Valence and Arousal Expressions between the United States and China: a Cross-Cultural Examination](https://arxiv.org/pdf/2401.05254) [1] from the findings of NAACL 2025.

## Data
The data are stored in a [Google Drive](https://drive.google.com/drive/folders/1snwfk8QG6W2MaCnnb_MItlljInfCaJw5?usp=sharing) folder. The data are separated into three parts: VA_score, n-gram, and LDA. Due to the sensitivity of the data, we do not release the content of original posts. Please contact us for special requests. 

### VA_score
The post level valence and arousal score data are stored in the `VA_score` folder. The scores are labeled with NRC_VAD [2] lexica. The data are stored in the following format:
```
VA_score/
│
└───tw_NRC.csv # for Twitter/X posts
└───wb_NRC.csv # for Sina Weibo posts
```

### n-gram
The data used for generating N-gram barplots are stored in the `n-gram` folder. They are stored in the following format:
```
n-gram/
│
└───twitter/
│   │
│   └───tw_1gram_a_neg_org.txt
│   └───tw_1gram_a_pos_org.txt
│   └───tw_1gram_v_neg_org.txt
│   └───tw_1gram_v_pos_org.txt
│
└───weibo/
    │
    └───wb_a_neg_org.txt
    └───wb_a_pos_org.txt
    └───wb_v_neg_org.txt
    └───wb_v_pos_org.txt
    └───wb_a_neg.txt
    └───wb_a_pos.txt
    └───wb_v_neg.txt
    └───wb_v_pos.txt
```

  In each subfolder, top correlated N-gram is ordered and separated by positive/neagtive, and valence/arousal.  
  For Weibo, we present both original Chinese 1-2-grams (`_org`), and also translated versions.  
  For Twitter, since all 2-grams are not significant, we only share 1-gram data.  

### LDA
The data used for generating LDA plots are stored in the `LDA` folder. They are stored in the following format:
```
LDA\
│
└───twitter_topic_message_topic_tagcloud.csv
└───twitter_topic_message.csv
└───weibo_topic_message_topic_tagcloud.csv
└───weibo_topic_message.csv
```

  Each `_topic_message.csv` file contains LDA [3] topics and correlation statistics with valence and arousal scores, where LDA is calculated on the post level.   
  Each `_tagcloud.csv` shows the corresponding top words within each topic.  

# Contact
If you have any questions, please contact Jeffrey (Young-Min) Cho: jch0 at seas dot upenn dot edu

# References
[1] Cho, Young-Min, et al. "Language-based Valence and Arousal Expressions between the United States and China: a Cross-Cultural Examination." To appear in Findings of NAACL 2025.
[2] Mohammad, Saif M. “Obtaining Reliable Human Ratings of Valence, Arousal, and Dominance for 20,000 English Words.” Proceedings of the 56th Annual Meeting of the Association for Computational Linguistics (ACL), Melbourne, Australia, July 2018.  
[3] Blei, David M., Andrew Y. Ng, and Michael I. Jordan. "Latent dirichlet allocation." Journal of machine Learning research 3.Jan (2003): 993-1022.  