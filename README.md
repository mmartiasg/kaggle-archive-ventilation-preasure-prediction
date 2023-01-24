# kaggle-archive-ventilation-preasure-prediction

This is the work I did for a pass competition in 2021

The objective is to simulate a ventilator connected to a sedated patien's lung. it seems simple but spoiler alert it's not that easy. There is only 3 seconds per breath you have to work with. I've tried several thecniques with relative susscess but a lot to lear from that.

I've tested several models architectures and feature engineering:
  - 1DConv model: the thing is 1DConv just destroy the secuential data it did not work well
  - GRU: This was the best of all
  - Dense layer: This was my baseline
  - A combination between 1DConv and GRU
  - A combination between 1Dconv and LSTM
