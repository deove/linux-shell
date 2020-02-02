# linux-shell
–connect  3 parametres, machine existe, user existe
                vérifier le password
                touch mesreminder et inspecter s’il y a un nouveau message
                touch com_information
                touch recieve_mes
                touch information 
                importer “$user $machine $time” a fichier information
                arrive sur le prompt: nom_utilisateur@nom_machine
-admin    créer directory admin dans réseau
               céer directory root dans admin
               fixer le password comme « admin »
               vérifier le password
               touch information
               importer “$user $machine $time” a fichier information
               arrive sur le prompt: rvsh >
who        Imprimer le contenu d’information d’utilisateur dans cette machine
rusers      Parcour le sous-répertoire de reseau et parcour le sous-répertoire de machine
               Imprimer le contenu d’information d’utilisateur dans cette machine
rhost       Parcour le sous-répertoire de reseau et imprimer le nom de machine
connect [machine]      
              Parcour le sous-répertoire de reseau pour trouver cette machine. Apres c'est trouvé, on connect le compte dans cette machine.(le compte est le nom d’utilisateur present)
su [user][machine]
              cd machine
              cd user 
              vérifier le password de cet user et connecter cet user.(Si cet user est root, ce n’est pas possible)
passwd [user]
             Entrer le password current. Si c’est correct, entrer le nouveau password et changer le contenu du fichier password.(user ne peut pas changer le password des autres)
finger [user][machine]
            cd machine
            cd user
            imprimer le fichier com_information de cet user(si le user est root, ce n’est pas possible)
write [user][machine][message]
            cd machine
            cd user
            importer le message au fichier recieve_mes et envoyer un signal « message » au fichier mesreminder.
            Chaque fois vous connectez, il vas inspecter le fichier mesreminder. S’il n’est pas vide, il vas vous informer « vous avez recu un nouveau message ».(Vous ne pouvez pas envoyer un message a root)
read     Imprimer le contenu du fichier recieve_mes d’utilisateur current.
            Apres vous lisez, il vas supprimer le fichier mesreminder.
host [machine]
            Vous devez choisir enlever ou ajouter
            Enlever   il vas vérifier s’il y a cette machine et le supprimer.
            Ajouter   il vas ajouter cette machine dans reseau
users [user]
           Vous devez choisir enlever ou ajouter
           Ajouter   Pour donner les droits d’acces a une ou plusieurs machines, j’ai utilisé while true(exit pour quitter).
                         Entrer ajouter cet user au quelle machine.
                         Creer tous les fichier comme connecter.
                         Importer un password au fichier password.
           Enlever   Parcour les sous-répertoires du reseau
                         Parcour les sous-répertoires de machine
                         Trouver cet user et le supprimer.
afinger [user]
           Parcour les sous-répertoires du reseau
           Parcour les sous-répertoires de machine
           Trouver cet user.
           Donner deux questions « Quelle est votre profession? » et « Quelle est votre sexe? »
           Importer les repondres et le contenu du fichier information au fichier com_information.
           Parce que le meme user peut exister dans plusiers machines, j’ai faite un counter pour distinger.






         