Cookbook Chef de déploiement d'un noeud mongodb sur le cloud ikoula
==========================================================================

Ce cookbook chef vous permet de déployer très rapidement un noeud mongodb
sur une instance m1.small du cloud ikoula en zone de routage direct. 

Pour pouvoir lancer l'application de ce cookbook vous devez :
-------------------------------------------------------------

- Avoir un compte sur le <a href="https://express.ikoula.com/cloud-public">cloud public ikoula</a>
- Configurer un groupe de sécurité comme indiqué <a href="https://support.ikoula.com/index-1-2-2870-Groupes-s%C3%A9curit%C3%A9-routage-directe.html">içi</a>
- Avoir accès a une machine linux de préférence ubuntu ou debian
- installer votre environnement (ruby, gem, chef, knife-solo, knife-cloudstack, git, berkshelf) comme indiqué
  <a href="https://www.ikoula-blog.com/knife">içi</a>
- cloner ce repository sur votre machine locale
- configurer le fichier knife.rb fourni avec vos clés api et secrete comme indiqué
  <a href="https://www.ikoula-blog.com/knife">içi</a>
- lancer le script **create_mongodb_keypair.sh**
  celui ci va vous créer une paire de clés. La clé publique sera déployée
  par la suite sur vos instances. La clé privée est sauvegardée dans le fichier
  mongodb.key
- lancer enfin le script **create_mongodb_node_basic_networking_zone.sh**

L'instance sera déployée (vous récuperez l'ip et le mot de passe sur la console)
et chef installera automatiquement mongodb.
