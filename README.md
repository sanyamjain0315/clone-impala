# Clone Impala

- This is a neural network that replicates the lyrical flow of the artist 'Tame'Impala'.
- It requires a seed text to base its lyrics off of and the number of words to be generated.

## Model used

- LSTM model was utilised
- The model calculates the next most probable words and and selects the word using np.random.choice (a word with 60% probability of being the next word is also 60% likely to be picked as the next word)

## Running the app

- After cloning the repository, install the requirements using  
  `pip install -r requirements.txt`
- Then in the terminal, type the following command  
  `streamlit run app.py`  
  or  
  `python -m streamlit run app.py`

## Preview

What the web app looks like
![image](https://github.com/sanyamjain0315/clone-impala/assets/111227515/893b8b4b-57e4-4b4c-b215-1e21ebb1a3b2)


## Potential

- This model could also be trained another artists' lyrical corpus
