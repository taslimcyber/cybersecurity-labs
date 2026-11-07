# Mininet : détection (Snort) et blocage (iptables)

**Thème** : réseau, sécurité défensive

**Objectif** : voir comment un IDS et un pare-feu travaillent ensemble face à un téléchargement malveillant.

**Environnement** : topologie virtualisée avec Mininet (postes utilisateurs, serveurs en DMZ, routeurs, poste attaquant, faux serveur hébergeant un malware).

## Déroulé

**Détection** : téléchargement d'un fichier malveillant simulé depuis un poste client. Snort, sur le routeur, matche la charge utile avec une signature et génère une alerte dans les logs.

**Investigation** : capture du trafic avec tcpdump (.pcap) pour garder une preuve exploitable, avec IP et ports source/destination.

**Réponse** : règle iptables sur la chaîne FORWARD du routeur pour bloquer tout trafic vers le serveur malveillant. Nouvelle tentative de connexion : timeout.

## Résultat

La chaîne détection (IDS), preuve (capture réseau) et réaction (pare-feu) fonctionne de bout en bout, comme dans un SOC.

**Outils** : Mininet, Snort, tcpdump, iptables
