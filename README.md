# Bibliotheque
  Le programme :
     -crée des auteurs
     -crée des œuvres associées
     -stocke des exemplaires dans une bibliothèque
     -liste les exemplaires
     -filtre ceux en anglais
     -affiche les auteurs à succès
     -compte les exemplaires d’une œuvre

## Classes à implémenter
Les classes suivantes doivent être définies :
  -Auteur
  -Oeuvre
  -Exemplaire
  -Bibliotheque

### Classe Auteur
    Un auteur est défini par :son nom (string),un indicateur indiquant s’il a reçu un prix

     Méthodes :
       1.Constructeur (nom + indicateur, false par défaut)
       2.getNom()
       3.getPrix()

➡️ Un Auteur ne doit pas être copiable

### Classe Oeuvre
    Une œuvre est définie par :
     -son titre (string)
     -une référence constante vers son auteur
     -sa langue (string)

     Méthodes :
        1.constructeur (titre, auteur, langue)
        2.getTitre()
        3.getAuteur() (retourne une référence constante)
        4.getLangue()
        5.affiche() → format : <titre>, <auteur>, en <langue>
        6.destructeur affichant : "L’oeuvre <titre>, <auteur>, en <langue> n’est plus disponible."
➡️ Une Oeuvre ne doit pas être copiable

### Classe Exemplaire
    Un exemplaire est défini par une référence à une œuvre.

    Méthodes :
      1.constructeur → affiche :
      2.Nouvel exemplaire de : <titre>, <auteur>, en <langue>
      3.constructeur de copie → affiche :Copie d’un exemplaire de : <titre>, <auteur>, en <langue>
      4.destructeur → affiche : Un exemplaire de "<titre>, <auteur>, en <langue>" a été jeté !
      5.getOeuvre()
      6.affiche() →Exemplaire de : <titre>, <auteur>, en <langue>
      
### Classe Bibliotheque
     Une bibliothèque est définie par :
       -un nom
       -un ensemble de pointeurs vers des exemplaires (vector)
       
     Méthodes :
        -constructeur → affiche :La bibliothèque <nom> est ouverte !
        -getNom()
        -stocker() qui ajoute un ou plusieurs exemplaires d’une œuvre ,allocation dynamique obligatoire,ajout en fin de vector
        -lister_exemplaires() qui affiche tous les exemplaires ou ceux d’une langue donnée
        -compter_exemplaires()
        -afficher_auteurs(bool) qui affiche les auteurs et options pour filtrer les auteurs primé        
        -destructeur → affiche :"La bibliothèque <nom> ferme ses portes,et détruit ses exemplaires ":puis libère la mémoire

      Ces méthodes constituent l’interface des classes. 


