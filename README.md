# Descriptive

import pandas as pd
my_dict={'Name of Country':["Bhutan","Singapore","Bangladesh","Sri Lanka",
                            "India"], 'Infant mortality rate':[21,2,24,7,29]}
df=pd.DataFrame(my_dict)
df

#Scatterplot
x =[1,2,3,4,5,6,7,8,9,10]
y =[-2,4,6,72,2,23,253,25,1,2]
plt.scatter(x,y)
plt.title('X vs Y')
plt.xlabel('x')
plt.ylabel('y')
plt.show()

#Linespace
x =np.linspace(0,10,10000)
y=np.cos(x)
plt.plot(x,y)
plt.show()

#histogram
ds = np.array([22,87,23,23,21,21,1,2,31,3,213,1,31,312])
fig,ax =plt.subplots(figsize=(8,5))
ax.hist(ds,bins=[0,25,50,75,100])
plt.show()

#HEatmaps
my_map = np.random.randn(6, 6)

plt.imshow(my_map)
plt.colorbar()
plt.show()

#piechart
# Creating dataset
cars = ['Kia', 'Van', 'EV', 'TESLA', 'Alto', 'Swift']

data = [23, 17, 35, 2, 30, 23]

# Creating plot
fig = plt.figure(figsize =(9, 6))
plt.pie(data, labels = cars,autopct='%1.1f%%', explode=(0,0,0,0.2,0,0))
plt.show()


#mean
df['Math_Score'].mean()

## Geometric Mean of the column in dataframe
from scipy import stats
print(stats.gmean([4,11,123,132,1]))
# Row wise geometric mean of the dataframe
from scipy import stats
stats.gmean(df.iloc[:,1:3],axis=1)
# Geometric mean of the specific column
stats.gmean(df.loc[:,"Stats_Score"])

@Q1 and Q3
Q1 = h['Spending_USD'].quantile(0.25)
Q3 = h['Spending_USD'].quantile(0.75)
IQR = Q3 - Q1
print("Inter quartile range for the Spending_USD columns: ", IQR)
#Identifying the outlier
lowelimit = Q1-1.5*IQR
upperlimit = Q3+1.5*IQR
print("The outlieres are: ", upperlimit, ", ", lowelimit)

#Binom
from scipy.stats import binom
# p = 1/4 = 0.25 probability of getting correct answer
p = binom.pmf(n = 6, k = 4, p = 0.25)
print("The probability that student gets exactly 4 questions right: ", p , 'or ', 3.3, "%")
#Binom distributions
print( "The mean of the distribution: ", binom.mean(n = 6, p = 0.25))
print()
print("The variance of the distribution: ", binom.var(n = 6, p = 0.25))
print()
print("The standard deviation of the distribution: ", binom.std(n = 6, p = 0.25))


