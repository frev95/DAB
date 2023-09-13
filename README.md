# Algorithme DAB

Conception sous forme de pseudo-code

---

```
Le client insère sa carte dans le distributeur
Lancement du processus de vérification
    SI la carte n'est pas conforme
        ALORS le distributeur rejette la carte
        Le programme s'arrête
    SINON SI la carte est bloquée
        ALORS le distributeur avale la carte
        Le programme s'arrête
    SINON
        La carte est valide
        Demande du code de la carte
Le distributeur affiche le message "taper votre code"
Le client tape son code
    SI le code n'est pas correct
        ALORS le distributeur affiche "code erroné"
        ET le compteur de tentatives est incrémenté de 1
        SI le compteur de tentatives est égal à 3
            ALORS le distributeur avale la carte
            Le programme s'arrête
        Demande du code de la carte
    SINON
        Le code est correct
        Demande du montant à retirer

