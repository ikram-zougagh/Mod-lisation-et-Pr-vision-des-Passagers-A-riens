# Modélisation et Prévision des Passagers Aériens 

## Introduction
Les données temporelles sont omniprésentes dans de nombreux domaines, notamment la finance, la météorologie et la santé. Comprendre les modèles sous-jacents et anticiper les tendances futures dans ces séries temporelles est crucial pour la prise de décisions informées. Ce projet vise à explorer plusieurs techniques de modélisation et de prévision des séries temporelles à partir du jeu de données sur le nombre de passagers aériens.

## Objectifs du Projet
L'objectif principal de ce projet est d'investiguer l'utilisation des modèles de prévision des séries temporelles. Plus spécifiquement, nous cherchons à :

- Évaluer l'efficacité des Réseaux Neuronaux Artificiels (ANN), qui sont capables d'apprendre des motifs complexes et de s'adapter dynamiquement aux données temporelles.
- Examiner l'efficacité des LSTMs pour traiter des séquences temporelles étendues, capturant des dépendances à long terme.
- Comparer les performances des modèles ARIMA, ANN et LSTM pour déterminer celui qui est le plus adapté à notre jeu de données.

## Analyse Exploratoire
Avant de procéder à la modélisation, une analyse exploratoire des données a été réalisée. Cela a impliqué un examen statistique initial et des visualisations pour comprendre les tendances, les saisons et les variations présentes dans le jeu de données. Ces étapes sont essentielles pour préparer les données à la modélisation.

## Modélisation avec ARIMA
### Présentation d'ARIMA
Le modèle ARIMA (AutoRegressive Integrated Moving Average) est utilisé pour modéliser les séries temporelles en capturant les tendances et les motifs saisonniers. L'approche ARIMA se compose de trois éléments : le terme autoregressif (AR), le terme d'intégration (I) et le terme de moyenne mobile (MA).

### Méthodologie
1. **Baseline Model :** Un modèle de persistance a été utilisé comme référence.
2. **Identification des composants :** Identification des valeurs de \( p \), \( d \) et \( q \) à l'aide de l'ACF et PACF.
3. **Estimation du modèle :** Utilisation de la méthode de Grid Search pour déterminer les ordres optimaux.
4. **Validation et Prédictions :** Affichage des prévisions par rapport aux données réelles.

### Résultats
Après l'exécution, le meilleur modèle identifié était ARIMA(12, 1, 3) avec un RMSE de 16.496. Les graphiques illustratifs montrent comment les prévisions d'ARIMA se comparent aux données réelles.

## Modélisation avec ANN
### Présentation des ANN
Les Réseaux Neuronaux Artificiels (ANN) sont des outils puissants pour capturer des relations non linéaires dans les données. Ils apprennent à partir des données et sont capables de généraliser à de nouvelles informations.

### Méthodologie
1. **Baseline Model :** Un modèle ANN de base a été développé pour évaluer les performances.
2. **Estimation du modèle :** Utilisation de la méthode de Grid Search pour déterminer les paramètres optimaux, comme le nombre de couches cachées et de neurones.
3. **Validation et Prédictions :** Les prévisions ont été évaluées par rapport aux données réelles.

### Résultats
Le meilleur modèle ANN a été déterminé avec 4 couches cachées et 50 neurones, atteignant un RMSE de 22.79. Les graphiques illustrent les prédictions du modèle par rapport aux données réelles.

## Modélisation avec LSTM
### Présentation des LSTM
Les réseaux de neurones à mémoire à long terme (LSTM) sont une variante des ANN spécialement conçue pour gérer des séquences de données. Ils sont capables de capturer les dépendances à long terme grâce à leur architecture unique.

### Méthodologie
1. **Baseline Model :** Élaboration d'un modèle LSTM de base pour évaluer les performances.
2. **Estimation du modèle :** Utilisation de la méthode de Grid Search pour explorer différentes configurations.
3. **Validation et Prédictions :** Les prévisions LSTM ont été validées par rapport aux données réelles.

### Résultats
Le modèle LSTM a atteint un RMSE de 26.82, avec les meilleurs paramètres étant 150 neurones. Les résultats sont visualisés pour comparer les prévisions LSTM avec les données réelles.

## Comparaison des Modèles
La comparaison des performances des modèles a révélé que :

- **ARIMA :** Meilleur modèle avec un RMSE de 16.496, indiquant une capacité solide à prédire les séries temporelles.
- **ANN :** Bien qu'il ait un RMSE plus élevé de 22.79, il reste significativement meilleur que le modèle de persistance.
- **LSTM :** A montré une amélioration par rapport à la persistance, mais avec un RMSE de 26.82, il a eu des performances globales moins impressionnantes que ARIMA.

## Conclusion
Ce projet a exploré différentes méthodes de prévision des séries temporelles, mettant en lumière les forces et les faiblesses de chacune. ARIMA s'est avéré être le modèle le plus performant pour notre jeu de données, en fournissant des prévisions précises adaptées à la tendance linéaire prédominante. Les résultats soulignent l'importance de choisir une méthode de modélisation qui correspond aux caractéristiques spécifiques des données. Ce projet ouvre la voie à des applications futures prometteuses dans des domaines où la compréhension des tendances temporelles est essentielle.

---

Merci de votre attention !
