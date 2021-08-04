# COMPETITION LINK
https://www.kaggle.com/c/cassava-leaf-disease-classification

## MY ATTEMPT
- Divided the data since there was an imbalance between Class-3 and the other 4 classes.
- The first model is binary classification between class-3 and others.
- The second model classifies the others into the rest of the four classes.
- The final accuracy of this stacked pipeline is `86.82%`.
- Notebook in `CassavaHW.ipynb` and some results analysis in `CassavaResultsAnalysis.ipynb`.

This is personally very disaapointing since pure fine-tuning on all the five classes is easily able to breach 87%! :frowning_face:

## INTERESTING LINKS
- Ravi Mashru: [Colab Link](https://colab.research.google.com/drive/1T1wM77DFRLARu6YPvWxo6LnjFMv2WNHN?usp=sharing) Reported some interesting comparisions over `fine-tuning` and `fit_one_cycle`
- Kevin Bird: [Github Gist](https://gist.github.com/kevinbird15/d7b252f76e33b6c53bb6259aa37127a9) Has added Clahe and Equalize, nice improvements!
- Abhishek Yadav: Reported a good improvement in performance based on FastAI versions! Intriguing!

## NOTES
- It is quite evident that image augmentations has a good impact on the results. From results seen in Kevin's experiment and the kaggle kernels from the competition, lot of emphasis has been laid on this.
- A good optimizer and a different architecture also seems to have a say.
- Can also play around with class weights and a supporting loss _(focal loss perhaps?)_.
- Ensemble FTW! Quite literally!:smile:
