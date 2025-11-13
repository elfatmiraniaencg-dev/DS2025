# --- Imports nécessaires ---
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
from sklearn.datasets import load_iris

# --- Chargement du dataset ---
iris = load_iris(as_frame=True)
df = iris.frame
df.columns = ['sepal_length', 'sepal_width', 'petal_length', 'petal_width', 'species']

# --- Aperçu des données ---
print("Aperçu du dataset :")
display(df.head())

# --- Statistiques descriptives ---
print("\nStatistiques descriptives :")
display(df.describe())

# --- Comptage des classes ---
print("\nRépartition des espèces :")
print(df['species'].value_counts())

# --- Visualisation 1 : Histogrammes par variable ---
sns.set(style="whitegrid")
df.hist(bins=20, figsize=(10,8))
plt.suptitle("Distribution des variables numériques", fontsize=14)
plt.show()

# --- Visualisation 2 : Pairplot pour observer les relations entre variables ---
sns.pairplot(df, hue="species", diag_kind="kde", corner=True)
plt.suptitle("Relations entre les variables selon les espèces", y=1.02)
plt.show()

# --- Visualisation 3 : Matrice de corrélation ---
plt.figure(figsize=(6,5))
sns.heatmap(df.corr(), annot=True, cmap="coolwarm", fmt=".2f")
plt.title("Matrice de corrélation")
plt.show()

# --- Visualisation 4 : Boxplots pour comparer les espèces ---
fig, axes = plt.subplots(2, 2, figsize=(12, 8))
sns.boxplot(data=df, x="species", y="sepal_length", ax=axes[0,0])
sns.boxplot(data=df, x="species", y="sepal_width", ax=axes[0,1])
sns.boxplot(data=df, x="species", y="petal_length", ax=axes[1,0])
sns.boxplot(data=df, x="species", y="petal_width", ax=axes[1,1])
plt.suptitle("Comparaison des variables selon l'espèce")
plt.show()

