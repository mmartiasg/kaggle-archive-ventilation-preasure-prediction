# kaggle-archive-ventilation-preasure-prediction

This is the work I did for a pass competition in 2021

The objective is to simulate a ventilator connected to a sedated patient's lung. it seems simple but spoiler alert it's not that easy. There are only 3 seconds per breath you have to work with. I've tried several techniques with relative success but a lot to learn from.

I've tested several models architectures and feature engineering:
  - 1DConv model: This was the best model so far it shouldn't be that good and that is because the 1DConv destroys the information in the sequence. Maybe it got better when I code the time as a sin and cosine signal thus the sequence order is encoded in it.
  - GRU: This was the best of all
  - Dense layer: This was my baseline
  - A combination between 1DConv and GRU
  - A combination between 1Dconv and LSTM

Notes:
 - the C and R have an exponential decay behaviour thus the value I have is the starting value.
 - Along 3 seconds the value will decay (1/R_C_train)*np.exp(-(time_step_train-3))
 - The time is modelled as a signal in terms of sin and cosine
 - The decision to choose a model with 1DConv is because they are faster and the results at the end were good. Even though it is not the best architecture... I was working in a mbp 2017 by that time.

