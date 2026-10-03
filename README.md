# Accélération des modèles de classification : CNN1 (ResNet-style) vs CNN2 (VGG-style)

Projet de comparaison des méthodes d'optimisation et d'accélération de l'apprentissage
pour la classification binaire, avec **deux modèles** :

| Modèle | Description |
|--------|-------------|
| **CNN1** | Architecture inspirée de ResNet-50 (blocs résiduels, BatchNorm, ReLU) |
| **CNN2** | Architecture inspirée de VGG-19 (blocs empilés, Tanh, Dropout) |

Les deux modèles sont évalués sur **4 datasets** de classification binaire réduits en 2D (PCA),
avec une perte **Hinge** et un sous-gradient implémentés manuellement.

## Contenu du notebook

1. Chargement et visualisation des données 
2. Covering number adaptatif
3. Architectures CNN1 / CNN2
4. Perte Hinge et sous-gradient 
5. Line search : Armijo, Goldstein, Wolfe, pas fixe
6. Choix de la direction de descente
7. Accélérateurs  : SGD, Momentum, Nesterov, AdaGrad, RMSProp, Adam
8. Validation et régularisation L1 / L2
9. Online learning : OSD et sous-gradient stochastique 
10. Algorithmes du premier ordre : Perceptron, Passive-Aggressive, OSD 
11. Prediction with Expert Advice (Hedge)
12. Perceptron kernelisé (RBF, polynomial, linéaire)
13. Normes duales et régularisation en ligne
14. Tableau récapitulatif CNN1 vs CNN2

## Structure du dépôt

```
projet-acc/
├── notebooks/
│   └── projet_acc.ipynb
├── requirements.txt
├── .gitignore
└── README.md
```

## Installation et exécution

```bash
git clone https://github.com/<ton-username>/projet-acc.git
cd projet-acc
python -m venv .venv
source .venv/bin/activate        # Windows : .venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook notebooks/projet_acc.ipynb
```

Ou directement sur Google Colab / Kaggle : importer le notebook depuis GitHub.

> Le notebook télécharge un dataset depuis une URL GitHub : une connexion Internet est nécessaire.

## Auteure

Rkia Ouhsain, ENSIAS, Université Mohammed V de Rabat
