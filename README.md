# hiericaly-pro

from scipy.cluster.hierarchy import dendrogram,linkage
import numpy as n
import pandas as p
import matplotlib.pyplot as plt

data=p.read_csv(r'C:\Users\hmr\Desktop\submission_example.csv')
print(data)
f1= data['ID'].values
f2=data ['medv'].values
plt.rcParams['figure.figsize']=(5,5)
plt.style.use('ggplot')
ar=n.array(list(zip(f1,f2)))
d=linkage(ar,'ward')
dn=dendrogram(d)
b=linkage(ar,'single')
plt.figure(figsize=(5,5))
dn=dendrogram(b)
plt.show()
