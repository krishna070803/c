//data classification
install.packages("party") → Select 0-Cloud  
library("party")
input.dat <- readingSkills[c(1:105),] 
png(file="decision_tree.png") 
 output.tree <- ctree(nativeSpeaker ~ age + shoeSize + score,data=input.dat) 
 plot(output.tree) 
 dev.off() 
plot(output.tree)

//clustring
newirir <- iris
print(newiris)
newiris$Species <- NULL 
(kc <- kmeans (newiris, 3))
 plot(newiris[c("Sepal.Length","Sepal.Width")],col = kc$cluster)

//linear regression
 x <- c(100,110,130,143,156,170) 
>> y <- c(50,55,60,72,66,89) 
>> r <- lm(y ~ x) 
>> print(r) 
 print(summary(r)) 
a <- data.frame(x=130) 
>> res <- predict(r,a) 
>> print(res) 
plot(y,x,col="red",main = 
"HEIGHT_AND_WEIGHT",abline(lm(x~y)),cex=1.3,pch=16,xlab="Weight",ylab="Height) 

//7 o read data from a CSV file, perform simple data analysis, 
//and generate basic insights kmeans
import numpy as np 
import matplotlib.pyplot as plt 
import pandas as pd 
from sklearn.cluster import KMeans 
 
dataset = pd.read_csv("Mall_Customers.csv") 
x = dataset.iloc[:, [3, 4]].values 
kmeans = KMeans(n_clusters=5, init='k-means++', max_iter=300, n_init=10, 
random_state=0) 
y_kmeans = kmeans.fit_predict(x) 
colors = ['red', 'blue', 'green', 'cyan', 'magenta'] 
for i in range(5): 
    plt.scatter(x[y_kmeans == i, 0], x[y_kmeans == i, 1], s=100, c=colors[i], label=f'Cluster 
{i+1}') 
plt.scatter(kmeans.cluster_centers_[:, 0], kmeans.cluster_centers_[:, 1], s=300, c='yellow', 
label='Centroids') 
plt.title("Clusters and Centroids") 
plt.xlabel("Annual Income (k$)") 
plt.ylabel("Spending Score (1-100)") 
plt.legend() plt.show()

//knn
from sklearn.datasets import load_iris 
from sklearn.model_selection import train_test_split 
from sklearn.neighbors import KNeighborsClassifier 
from sklearn.metrics import accuracy_score 
 
X, y = load_iris(return_X_y=True) 
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3, random_state=42) 
 
knn = KNeighborsClassifier(n_neighbors=3) 
knn.fit(X_train, y_train) 
y_pred = knn.predict(X_test) 
print(f'Accuracy: {accuracy_score(y_test, y_pred):.2f}') 

//colab
import pandas as pd 
import seaborn as sns 
import matplotlib.pyplot as plt 
 
# Load the data from the CSV file (with correct path) 
 
df = pd.read_csv('/content/Book1.csv') 
 
df.columns = df.columns.str.strip() 
 
# Plot 
 
sns.lineplot(data=df, x='Date', y='Sales', marker='o') 
plt.title('Sales Over Time') 
plt.xticks(rotation=45) 
plt.show() 
