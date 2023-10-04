# Clone Impala

## Overview

'Clone Impala' is a lyrics generating model, trained on the artist Tame Impala's complete collection of lyrics. With just a seed text to get started with generating the lyrics, and the number of further words to be generated, the model can generate new lyrics while replicating the style of the artist.

If you just want to download the model, click [here](https://github.com/sanyamjain0315/clone-impala/blob/main/models/double_LSTM_mk2.h5)

## Tech Stack

- **Model training:** [Tensorflow](https://www.tensorflow.org/)
- **Frontend:** [Streamlit](https://streamlit.io/)
- **Data gathering:** [Genius api](https://genius.com/developers)

## Model description

- We utilized a double LSTM model with dropout layers added in for regularization
- The final layer of the model is a dense layer of the same size as the vocabulary size.
- Finaly layer outputs the probability of each word for being the next word for a provided input next.
- We can either select the word with the highest probability as the next word **or** we can use `numpy.random.choice` where a word with higher probability has a higher chance of being selected as the next word

## Challenges faced and future prospects

The model is not in a perfect state. The lines produced by the model may sometimes make grammatical or contextual sense, but the lyrics generated as a whole does not have a clear scemantic meaning.  

This is still better than the initial model that produced gibbrish. It can be further improved by tuning of the hyperparameters, more reguarization and/or training for more epochs (a bit difficult considering present hardware).  

Another future prospect could be to utilize **Generative Adverserial Networks** (GANs) to generate the lyrics.

## Running the app

- After cloning the repository, install the requirements using  
  `pip install -r requirements.txt`
- To run the streamlit app, type the following command  
  `streamlit run app.py`  
  or  
  `python -m streamlit run app.py`

## Preview

What the streamlit app looks like
![image](https://github.com/sanyamjain0315/clone-impala/assets/111227515/893b8b4b-57e4-4b4c-b215-1e21ebb1a3b2)
