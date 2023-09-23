# clone-impala

- This is a neural network that replicates the lyrical flow of the artist 'Tame'Impala'.
- It requires a seed text to base its lyrics off of and the number of words to be generated.

## Model used

- LSTM model was utilised
- The model calculates the next most probable words and and selects the word using np.random.choice (a word with 60% probability of being the next word is also 60% likely to be picked as the next word)

## Potential

- This model could also be trained another artists' lyrical corpus
