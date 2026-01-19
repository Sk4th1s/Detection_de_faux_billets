# Detection_de_faux_billets

Dans ce projet le but était de choisir le meilleur algorithme pour de la prédiction de faux billet à partir de leurs dimensions.

# Vérification des données
<h2>Absence de données</h2>
Dans le fichier on voit que certaine ligne ont une colonne vide, j'ai donc regardé si il était possible de prédire la dimension manquante en fonction des autres dimensions.
<img width="1127" height="310" alt="graphe-justif-predi" src="https://github.com/user-attachments/assets/ff08ab5f-1212-4815-9403-7372ce62b8ff" /><br><br>
<img width="1070" height="694" alt="justif-predi" src="https://github.com/user-attachments/assets/dc2ed2c6-0b4a-4375-9d4c-ebd9cde591ae" />

# Lien entre dimension
Corrélation dimension
<img width="700" height="360" alt="corrélation dimension" src="https://github.com/user-attachments/assets/de528b0d-19d1-4aa2-af30-9b313ea60c2d" /><br><br>
<img width="900" height="900" alt="corrélation entre colonne" src="https://github.com/user-attachments/assets/a1f428f2-d00b-4080-92ed-da454646f52f" /><br><br>

J'ai regardé si l'on pouvait déjà remarqué des différences entre les billets (vrai/faux) pour chaque dimension donnée
<img width="700" height="360" alt="diag-auth" src="https://github.com/user-attachments/assets/aa988361-3ce1-48af-af20-e7ca18422ab3" /><br><br>
<img width="700" height="360" alt="height left-auth" src="https://github.com/user-attachments/assets/2cc2f472-66e5-46f1-b4cb-901f2d8bd9a2" /><br><br>
<img width="700" height="360" alt="height right-auth" src="https://github.com/user-attachments/assets/168069fe-9dbe-4f88-8470-5d47e4eb26bd" /><br><br>
<img width="700" height="360" alt="length-auth" src="https://github.com/user-attachments/assets/eb5eb8ac-989e-4657-81a7-2c0873c89634" /><br><br>
<img width="700" height="360" alt="margin low-auth" src="https://github.com/user-attachments/assets/e7a09f2d-377d-4ccb-9a96-b5e3f5b0a923" /><br><br>
<img width="700" height="360" alt="margin up-auth" src="https://github.com/user-attachments/assets/287b12c5-846d-4cd3-89b2-2f16726e34e7" /><br><br>

# Entrainement des différents algo

<h2>3 algorithmes</h2>
Nous avons 3 algorithme différents à tester :
<ul>
  <li>Logistic regression</li>
  <li>KMeans</li>
  <li>SVG</li>
</ul>
Pour Kmeans, il faut définir le nombre de cluster, pour ça j'ai utilisé la méthode du coude.
<img width="700" height="360" alt="methode du coude" src="https://github.com/user-attachments/assets/af1347f2-25d8-4c02-b940-661f5f2cf66d" />

<h2>Comparaison des différents algorithme avec des matrice de confusion</h2>
Pour notre application, le plus important est de retrouver un maximum de faux billets.<br><br>
<img width="700" height="360" alt="Matrice de confusion LR" src="https://github.com/user-attachments/assets/ae2c680c-763e-4517-9be6-96c4caa472cd" /><br><br>
<img width="700" height="360" alt="Matrice confusion Kmeans" src="https://github.com/user-attachments/assets/b8426af6-0094-4b42-bfb3-8dc8361012ad" /><br><br>
<img width="700" height="360" alt="Matrice confusion SVG" src="https://github.com/user-attachments/assets/84ef87be-f37f-4eaa-9354-f42fdf04cc93" /><br><br>

Grâce aux matrice de confusions, on voit rapidement que le meilleur algorithme à utiliser est celui de Regréssion logistique (Logistic Regression), 
qui a retrouvé le plus de faux billets (98/100).
