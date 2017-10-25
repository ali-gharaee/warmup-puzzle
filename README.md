# A few puzzles for unsupervised learning / structure discovery

This is a warm-up assignment. It has two purposes: 
it gives you an idea of how it is to work with unlabeled data,
and it gives me
an idea on what I can (realistically) expected from the participants.

For this assignment, you will use four artificially generated data sets,
each stored as a CSV file.

- [Data set 1](data-set1.csv)
- [Data set 2](data-set2.csv)
- [Data set 3](data-set3.csv)
- [Data set 4](data-set4.csv)

Each row in the data files corresponds to a data point,
and each column corresponds to a feature.

Your task is to discover the structure in these data sets.
Each data set contains 2000 data points with an underlying structure.
Particularly,
the data in all data sets come from multiple multi-variate random variables.
In other words,
the underlying structure suggests that each data point belongs to a group
which is not indicated in the data.
You are free to use any method,
including plotting and eyeballing the data.
If you do not use an automated (machine learning) method for your solution, 
however,
describe which method(s) would be useful,
for example, to assign each data point to a sensible group or cluster.

Provide your answer by editing this file,
and briefly explaining your solution for each data set.
Figures and/or other visual material are welcome.
You can provide short code segments inline below,
or check in the code as separate files in your repository.

## Your solutions
import csv
import pandas as pd
from sklearn import cluster, datasets
from numpy import genfromtxt
import matplotlib.pyplot as plt

from mpl_toolkits.mplot3d import Axes3D
import matplotlib.pyplot as plt
from matplotlib import cm
from matplotlib.ticker import LinearLocator, FormatStrFormatter
import numpy as np

import numpy as np
from mpl_toolkits.mplot3d import Axes3D

import matplotlib.pyplot as plt
import csv

x = []
y = []
z = []

csv1 = 'warm-up-data/data-set1.csv'
csv2 = 'warm-up-data/data-set2.csv'
csv3 = 'warm-up-data/data-set3.csv'
csv4 = 'warm-up-data/data-set4.csv'

with open(csv3, 'r') as csvfile:
    plots = csv.reader(csvfile, delimiter=',')
    for row in plots:
        x.append((row[0]))
        y.append((row[1]))
        z.append((row[2]))

plt.plot(x, y, label='Loaded from file!')
plt.xlabel('x')
plt.ylabel('y')
plt.title('Interesting Graph\nCheck it out')
plt.legend()
plt.show()

x_dim = np.array(x)
y_dim = np.array(y)
z_dim = np.array(z)

fig = plt.figure()
ax = fig.gca(projection='3d')
surf = ax.plot_surface(x_dim, y_dim, z_dim, cmap=cm.coolwarm,
                       linewidth=0, antialiased=False)
fig.colorbar(surf, shrink=0.5, aspect=5)
plt.show()



#
# fig = plt.figure()
# ax1 = fig.add_subplot(111, projection='3d')
#
# x_dim = np.array(x)
# y_dim = np.array(y)
# z_dim = np.array(z)
#
# ax1.scatter(x_dim, y_dim, z_dim)
# plt.show()

# csv1 = pd.read_csv("warm-up-data/data-set1.csv")

# clustering data
# iris = datasets.load_iris()
# X_iris = csvReader[0]
# y_iris = csvReader[1]
# k_means = cluster.KMeans(n_clusters=3)
# k_means.fit(X_iris)
# print(k_means.labels_[::10])
# print(y_iris[::10])






### Data set 1
It's a 3 classes data
### Data set 2
It's 2 classes data
### Data set 3
It's 3 surfaces data
### Data set 4



