# Actress_DL_Classification
Dans ce projet, nous devons réaliser une classification d'images concernant de 3 groupes d'actrices dont deux d'entre eux sont connues pour être des sosies (Natalie Portman et Kiera Nightley). Pour y arriver, nous avons utilisé les CNNs et procédé à certaines opérations en utilisant la framework Pytorch. 

Pour effectuer ce travail, nous disposons d'un dossier d'images conprenant deux sous dossiers:
- `train` qui comprend 429 images 
- `val` qui comprend 168 images
Chacun de ces sous dossiers comprennent eux-mêmes trois sous dossiers dans lesquels sont classés les images en trois classes (`Natalie`, `Kiera`, `Autres`) de format 530x400 pixels.

Ce travail comprend deux grandes parties :
1. La construction d'un réseau avec une configuration experimentale.
2. L'utlisation du le Transfer Learning pour améliorer la classification.

Pour la première partie, nous avons developpé des modèles simples et aussi des modèles assez compliqués qui demandent beaucoup de ressources pour s'entrainer. Nous avons aussi transformé et standardisé les images pour les deux procédures.

Parmi nos modèles définis, celui qui a été le plus performant a été spécifié comme suit :  `config0 = [64,"M", 256, "M", 512, "M"]`. Ce modèle nous a permis d'avoir une accuracy de `55.7%` sur l'ensemble d'entrainement et de `40.5%` sur l'ensemble de validation. Ce qui parait assez pauvre comme résultat mais ce sont les meilleurs résultats qu'on a pu trouver avec toutes ces configurations dont nous avons definies.

En ce qui a trait au tranfer learning, on a pu essayer beaucoup de modèles comme `efficientNet(b0 à b7), ResNet18, ResNet152 et Inception3`. Le résultats dont nous avons trouvé indiquent que le modèle ResNet18 a été le plus adapté pour résoudre ce problème avec `60.7%` d'accuracy sur les données de validation.