# Neural-Network-NGO-Success

## Background

Neural Networks are great for revealing hidden patterns, especially in complex data sets that don't have a disitnct relationship.
Synthetic data on NGO campaigns was used to predict which campaigns would be most successful and efficitently allocate funds.
The goal was to predict with over a 75% accuracy of wether a campgain would be successful or fail.

### Setup

Data was preprocessed by dropping categories that did not provide insight such as the name and organization id
The data was then scaled to reduce distorions of categories with larger magnitudes. 
Outliers were removed to further remove distorions.
The target variable was declared to be IS_SUCCESSFUL, which was whether past campaigns were successful.
The model was run once and then optimized to imporve accuracy.

##Results

- First Attempt
nn.add(tf.keras.layers.Dense(units=80, activation="relu", input_dim=features))
nn.add(tf.keras.layers.Dense(units=45, activation="relu"))
nn.add(tf.keras.layers.Dense(units=1, activation="sigmoid"))
 0.72.6% accuracy

- Second Attempt
- The name of an organization was added as an input feature
- 1 extra relu layer was added

0.75% accuracy

Adding an extra layer and including the name of the organizer of a campaign improved the model. 
It is likely that campaigns that had successful campaign in the past are more likely to succeed in the future.
In addition, another layer allows the Neural Network more chances to find deeper patterns.
