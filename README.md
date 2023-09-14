# Algorithme DAB 1
*1 distributeur automatique de billets*

##
####Conception sous forme de pseudo-code

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
Le distributeur affiche le message "choisissez le montant du retrait"
Le client choisit son montant
Lancement du processus de vérification du solde client
    SI montant > solde client OU le montant dépasse le plafond autorisé
        Le retrait est refusé
        Le distributeur en affiche la raison
        Le distributeur relance la demande du montant à retirer
    SINON
        Le retrait est autorisé
        Lancement du processus de vérification du solde DAB
            SI montant > solde DAB
                    Le retrait est refusé
                    Le distributeur en affiche la raison
                    Le distributeur relance la demande du montant à retirer
            SINON
                Le retrait est autorisé
                Le distributeur délivre les billets
Le client récupère sa carte bancaire
Le client récupère les billets
Fin du programme