# Projet de Régression Linéaire

Ce projet a pour but de démontrer l'application de la régression linéaire à l'analyse de données. Nous examinerons les concepts de la régression linéaire, de l'analyse du dataset, de la standardisation des données et de la performance du modèle.

## Table des matières

1. [La régression linéaire](#la-regression-lineaire)
   1.1 [Le modèle](#le-modele)
   1.2 [Les erreurs du modèle](#les-erreurs-du-modele)
   1.3 [Gradient](#gradient)
   1.4 [Évaluation du modèle](#evaluation-du-modele)
2. [Analyse du Dataset](#analyse-du-dataset)
   2.1 [Affichage de la forme du DataFrame](#affichage-de-la-forme-du-dataframe)
   2.2 [Statistiques descriptives](#statistiques-descriptives)
   2.3 [Vérification des valeurs manquantes](#verification-des-valeurs-manquantes)
   2.4 [Les colonnes existantes](#les-colonnes-existantes)
   2.5 [Analyse de la corrélation entre les variables](#analyse-de-la-correlation-entre-les-variables)
   2.6 [Traitement du shape](#traitement-du-shape)

---

## La régression linéaire

La régression linéaire est une technique d'apprentissage automatique qui modélise une relation linéaire entre les variables d'entrée et une variable de sortie continue.

## Le modele
On implémente un modèle selon l'équation matricielle <mark>$\displaystyle F=X.θ$</mark> et puis on teste le modèle initiale défini par la valeur initiale de $\displaystyle θ$ qu'on a initialisé d'une manière aléatoire.
## Les erreurs du modele
On mesure les erreurs du modele sur le Dataset X, y en implémenterl'erreur quadratique moyenne.

$$
\displaystyle
J(θ) = \frac{1}{2m} \sum_{i=1}^{m} (h_{θ}(x^{(i)}) - y^{(i)})^{2}  \\
h_{θ}(x) = θ^{T}x = θ_{0} + θ_{1}x_{1}
$$

## Gradient 
On implémente la formule du gradient pour la MSE     

$$
\frac{\partial J(θ)}{\partial θ} = \frac{1}{m} X^{T}.(X.θ - y)
$$

et par la suite on utilise cette fonction dans la descente de gradient:    

$$
\displaystyle
θ = θ - \alpha \frac{\partial J(θ)}{\partial θ} 
$$

![graphe.png](https://miro.medium.com/v2/resize:fit:640/format:webp/1*lYpF8xJ3TiDoq461I0AcOQ.jpeg)

## Evaluation du modèle
Evaluation du modèle - Coefficient de détermination      
**RSE : RELATIVE Squared Error (L'erreur carrée relative)** :

$$
RSE = \frac{\sum_{i=1}^{m} (f(x_{i}) - y_{i})^{2}}{\sum_{i=1}^{m} \left(y - \frac{1}{m}\sum_{j=1}^{m} y_{j}\right)^{2}}
$$

le complement à 1 de la $\displaystyle RSE$ et le coefficient de mdetermination noté $\displaystyle R^{2}$
Tel que : $\displaystyle R^{2} = 1 - RSE$. Le modèle idéale donne  $\displaystyle R^{2} = 1$

![gradien_gif_url](https://muthu.co/wp-content/uploads/2018/09/1_xc5CSmK9d8oeKYxKxenEGg.gif)

