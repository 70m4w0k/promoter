# PROMOTER

Projet : realisation d'une dao simplifiée d'investissement immobilier

-Un token erc20 "PROMOTER" est crée

-Les utilisateurs souhaitant participer à la dao achetent ce token et sont ajoutés sur une whitelist

-Les fonds sont stockés sur un contrat 'fund'

-Un owner 'dirigeant' est nommé tous les 6 mois

-il y a un contrat Voting avec plusieurs "phases"

-les phases sont gerées par l'owner (sauf phase 3)

-Phase 1 : les membres de la whitelist proposent un bien à acheter ou à vendre, avec un montant associé

-Phase 2 : les membres choisissent une proposition

-Phase 3 : Au bout d'1 semaine, le vote est automatiquement clos, les fonds sont débloqué pour l'owner (qui dans la vraie vie irait acheter ou vendre le bien)

-Les votes ne se font pas avec un simple compteur qui s'incremente mais avec le 'poid de vote' du membre de la dao:

    exemple : l'utilisateur 'A' possede 2 $PROMOTER, l'utilisateur 'B' possede 1000 $PROMOTER
            A vote pour proposition1, proposition1.voteCount = 2.
            B vote pour proposition2, proposition2.voteCount = 1000.

-L'owner peut deposer une somme dans une fonction du contrat qui repartirait cette somme entre les utilisateurs (toujours selon leurs poids)

-Les utilisateurs peuvent exceptionnellement débouter l'owner mais il faut que + de 80% du poid de vote total en fasse la demande

-le premier owner est initialisé grace à un script

-à faire sur truffle et déployer sur ropsten


