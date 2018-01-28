
The below code gives various steps applied on a data set and use of NMF


```python
# Import NMF
from sklearn.decomposition import NMF 
 
import pandas as pd
 
# Create an NMF instance: model
model = NMF(n_components=6)
 
# Fit the model to articles
model.fit(sample_data)
 
# Transform the articles: nmf_features
nmf_features = model.transform(sample_data)
 
# Print the NMF features
print(nmf_features)
 
# Create a DataFrame: components_df
components_df = pd.DataFrame(model.components_,columns=words)
 
# Print the shape of the DataFrame
print(components_df.shape)
 
# Select row 3: component
component = components_df.iloc[3]
 
# Print result of nlargest
print(component.nlargest())
```


```python
# Import NMF
from sklearn.decomposition import NMF
 
# Create an NMF model: model
model = NMF(n_components=7)
 
# Apply fit_transform to samples: features
features = model.fit_transform(samples)
 
# Call show_as_image on each component
for component in model.components_:
    show_as_image(component)

# Select the 0th row of features: digit_features
digit_features = features[0,:]

# Print digit_features
```

NMF can be used to build recommender system. For examples, we can compare two articles using recommender system as shown in the code below


```python
# Perform the necessary imports
import pandas as pd
from sklearn.preprocessing import normalize
 
# Import NMF
from sklearn.decomposition import NMF 
 
# Create an NMF instance: model
model = NMF(n_components=6)
 
# Fit the model to articles
model.fit(articles)
 
# Transform the articles: nmf_features
nmf_features = model.transform(articles)
 
# Normalize the NMF features: norm_features
norm_features = normalize(nmf_features)
 
# Create a DataFrame: df
df = pd.DataFrame(norm_features, index=titles)
 
# Select the row corresponding to 'abcde': article
article = df.loc['abcde']
 
# Compute the dot products: similarities
similarities = df.dot(article)
 
# Display those with the largest cosine similarity
print(similarities.nlargest())
```
