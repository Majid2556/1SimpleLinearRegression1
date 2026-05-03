# 1SimpleLinearRegression1

import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import statsmodels.api as sm
import seaborn as sns
sns.set()
data = pd.read_excel('regression-data.xlsx')
data.head()
data.describe()
x = data['meter']
y = data['price']
x.head()
plt.scatter(x,y)
plt.xlabel('meter', fontsize = 20)
plt.ylabel('price', fontsize = 20)
plt.show()

X = sm.add_constant(x)
model = sm.OLS(y,X).fit()
model.summary()
X.head()
plt.scatter(x,y)
yhat = 19.9650 + 5.0786*x
fig = plt.plot(x,yhat, lw=3, c='red')
plt.xlabel('meter', fontsize = 20)
plt.ylabel('price', fontsize = 20)
plt.show()


#👌👌👌👌👌👌👌👌✔✔✔
plt.scatter(x,y)
yhat = 19.965 + 5.078*x
fig = plt.plot(x,yhat, lw=3, c='red')
plt.xlabel('meter', fontsize = 20)
plt.ylabel('price', fontsize = 20)
plt.show()
plt.scatter(x,y)
yhat = -5.684341886080802e-14+ 5.313729187183142*x
fig = plt.plot(x,yhat, lw=3, c='red')
plt.xlabel('meter', fontsize = 20)
plt.ylabel('price', fontsize = 20)
plt.show()
x1 = np.mean(x)
x1
y1 = np.mean(y)
y1
x1*y1
x2 = np.var(x)
x2
x
x3 = sum(x)
x3
x5=(x3-x1)**2
y2 = sum(y)
y2
y3=(y2-y1)
y3
x4=x3-x1
x4
xy1 = (x4*y3)/x5
xy1
y1
y1-(xy1*x1)
z=5.313729187183142*x1
y1-z
