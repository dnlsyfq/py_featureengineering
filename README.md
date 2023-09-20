
# Dimensionality Reduction

## t-SNE visualization of high dimensional data
to visualize high dimensional data using feature extraction
* remove non numerical data
* fitting t-SNE
  ```
  from sklearn.manifold import TSNE
  m = TSNE(learning_rate=50) // high learning rate cause algorithm to be more adventurious , low learning rate cause to be conservative , learning rate 10 to 1000
  tnse_features = m.fit_transform(df_numeric)
  tsne_features[1:4,:]
  df['x'] = tsne_features[:,0]
  df['y'] = tsne_features[:,1]

  sns.scatterplot(x='x',y='y',data=df)

  sns.scatterplot(x='x',y='y',hue='BMI_class',data=df)
  ```
