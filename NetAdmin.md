# TP Infra  NetAdmin, "Chef" Bryan

## Feuille de route  
**1. Document de Conception du Réseau (DCR)** :

Commencez par créer un schéma détaillé du réseau, y compris les équipements (routeurs, commutateurs, pare-feux, points d'accès sans fil, etc.), les segmentations de réseau et les liaisons inter-sites.
Assurez-vous d'inclure des informations sur la topologie du réseau, les adresses IP, les plages d'adresses, les VLAN (Virtual LAN) et la stratégie de routage.
Identifiez clairement les zones de confiance (par exemple, la production, le département de management, la succursale) et les zones non de confiance (Internet).
  
  **2. Matrice des Flux :**

Créez une matrice qui détaille les flux de données entre les différents segments du réseau.
Spécifiez l'origine, la destination, les ports utilisés, les protocoles et toutes les règles de sécurité associées à chaque flux.
Cette matrice servira de base pour configurer les pare-feux et autres dispositifs de sécurité.  

**3. Document de Configuration des Équipements :**

Élaborez un guide détaillé de configuration pour chaque équipement réseau, y compris les routeurs, les commutateurs, les pare-feux, etc.
Assurez-vous d'inclure des configurations pas à pas avec des commentaires expliquant les raisons derrière chaque choix de configuration.
Garantissez la cohérence des configurations pour une gestion aisée et une reproductibilité.  

**4. Plan de Sécurité du Réseau :**

Documentez toutes les mesures de sécurité mises en œuvre, y compris les configurations de pare-feu, les solutions IDS/IPS, les stratégies d'authentification, etc.
Mettez en avant la stratégie de sécurité globale de l'entreprise et la manière dont elle est mise en œuvre dans l'infrastructure réseau.
Identifiez les zones de risque potentielles et détaillez les mesures prises pour les atténuer.
Rapport de Monitoring et de Performance :

Détaillez les outils et méthodes utilisés pour surveiller le réseau, ainsi que les performances observées.
Incluez des statistiques de performance, les incidents détectés (s'il y en a eu), et des recommandations pour les améliorations futures.
Montrez comment la surveillance est intégrée dans la gestion quotidienne du réseau pour garantir la disponibilité et la sécurité.  

**5. Document de Test :**

Créez un ensemble de tests conçus pour valider la fonctionnalité et la sécurité du réseau.
Spécifiez les scénarios de test, les méthodologies utilisées, les résultats attendus et les résultats observés.
Assurez-vous que les tests couvrent tous les aspects importants de la sécurité et de la connectivité du réseau.
N'oubliez pas de collaborer étroitement avec l'équipe IT de SecureTech Industries pour garantir que les solutions proposées sont alignées sur les besoins de l'entreprise et les exigences en matière de sécurité. Une communication claire et une documentation précise sont essentielles pour la réussite de ce projet.    
# Technique  
**1. Segmentation par Zones Fonctionnelles :**

Siège Social : Cette zone comprend le département de production, le département de management et l'équipe IT.
Succursale : Cette zone englobe le showroom, les espaces administratifs et la connexion VPN sécurisée au siège social.
Commerciaux Itinérants : Cette zone est destinée aux utilisateurs distants (commerciaux itinérants) avec un accès sécurisé aux ressources de l'entreprise.  
**2. Segmentation par VLAN :**

Utilisez les VLAN pour isoler les différents départements et fonctions au sein du siège social et de la succursale. Par exemple, un VLAN pour la production, un VLAN pour le management, un VLAN pour le showroom, etc.
Mettez en place un VLAN dédié pour les commerciaux itinérants, avec des mécanismes de sécurité tels que l'authentification forte pour garantir un accès sécurisé.  
**3. Pare-feux et Sécurité :**

Installez des pare-feux au niveau du siège social et de la succursale pour filtrer le trafic entrant et sortant. Configurez-les en fonction des règles définies dans la matrice des flux.
Mettez en place des systèmes IDS/IPS pour la détection et la prévention des menaces, en surveillant le trafic réseau en temps réel.
Appliquez des ACL (Listes de Contrôle d'Accès) pour limiter l'accès aux ressources sensibles.  
**4. VPN :**

Utilisez des technologies VPN pour établir une connexion sécurisée entre le siège social et la succursale. Optez pour un VPN robuste et chiffré pour protéger la communication entre les deux sites.  
**5.QoS (Qualité de Service) :**

Configurez la qualité de service pour prioriser le trafic critique, notamment le trafic de voix sur IP (VoIP) et les applications essentielles à l'entreprise.  
**6.Solutions de Monitoring :**

Mettez en œuvre des outils de surveillance pour surveiller l'état et les performances du réseau, y compris la détection des pannes et des anomalies.
Assurez-vous d'avoir des alertes en place pour réagir rapidement aux problèmes potentiels.  
**7.Redondance et Haute Disponibilité :**

Envisagez la redondance au niveau des équipements critiques tels que les pare-feux, les routeurs et les commutateurs pour garantir une haute disponibilité.  
**8.Sécurité des Commerciaux Itinérants :**

Pour les commerciaux itinérants, implémentez une solution VPN sécurisée avec authentification forte, telle que l'authentification à deux facteurs (2FA) pour garantir une connexion sécurisée depuis des emplacements distants.
Cette structure de réseau hiérarchique avec une segmentation appropriée, des pare-feux, des VPN sécurisés, une surveillance proactive et une priorisation de la qualité de service contribuera à répondre aux exigences élevées en matière de sécurité et de connectivité de SecureTech Industries. Assurez-vous également de documenter soigneusement la conception du réseau, comme indiqué dans les livrables attendus.

# Rapport de Monitoring et de Performance

NTOP (Network Top) est un outil de surveillance réseau open source qui offre des fonctionnalités avancées pour l'analyse du trafic réseau. Il permet de collecter des informations sur le trafic réseau en temps réel et de les présenter sous forme de tableaux de bord, de graphiques et de rapports détaillés. NTOP est principalement utilisé pour surveiller et analyser le trafic réseau, la qualité de service (QoS), la sécurité du réseau et les performances du réseau.

Voici quelques-unes des fonctionnalités clés de NTOP :

**1. Analyse du trafic en temps réel :** NTOP permet de visualiser le trafic réseau en temps réel, y compris les débits, les protocoles utilisés, les adresses IP sources et de destination, etc.

**2. Rapports détaillés :** Il génère des rapports détaillés sur l'utilisation de la bande passante, les statistiques de protocole, les flux de données, les adresses IP les plus actives, etc.

**3. Analyse de la qualité de service (QoS) :** NTOP peut surveiller les performances du réseau, y compris la latence, la gigue et la perte de paquets, ce qui est essentiel pour garantir une bonne expérience utilisateur.

**4. Détection d'anomalies :** Il peut identifier les anomalies dans le trafic réseau, ce qui est utile pour la détection d'intrusions et la sécurité du réseau.

**5. Intégration avec d'autres outils :** NTOP peut être intégré avec d'autres outils de surveillance réseau, tels que Wireshark, pour une analyse plus approfondie du trafic.

Quant à SELKS (Suricata Elastic Logstash Kibana Scirius), il s'agit d'une distribution Linux basée sur Debian spécialement conçue pour la surveillance de la sécurité réseau. SELKS intègre plusieurs outils open source, notamment :

**1. Suricata :** Un moteur de détection d'intrusion réseau (IDS/IPS) qui analyse le trafic réseau en temps réel pour détecter les menaces.

**2. Elasticsearch :** Une base de données de recherche et d'analyse distribuée qui stocke les données de journalisation générées par Suricata.

**3. Logstash :** Un outil de collecte, de transformation et d'expédition de journaux qui agrège les données de Suricata et les prépare pour l'indexation dans Elasticsearch.

**4. Kibana :** Une interface de visualisation des données qui permet de créer des tableaux de bord interactifs et de générer des rapports à partir des données de journalisation stockées dans Elasticsearch.

**5. Scirius :** Une interface web qui facilite la gestion et la configuration de Suricata.

En combinant ces outils, SELKS offre une solution complète de surveillance de la sécurité réseau. Il permet de détecter les activités malveillantes, d'analyser les journaux de sécurité et de visualiser les données de manière conviviale à l'aide de Kibana.

Pour surveiller le réseau à l'aide de SELKS et NTOP, voici les étapes générales que vous pouvez suivre :

**1. :** Installez SELKS sur une machine dédiée.

**2. :** Configurez Suricata pour surveiller le trafic réseau et générer des journaux de sécurité.

**3. :** Utilisez NTOP pour surveiller et analyser le trafic réseau en temps réel.

**4. :** Utilisez Kibana pour créer des tableaux de bord personnalisés et des rapports basés sur les données de journalisation de Suricata stockées dans Elasticsearch.

Cela vous permettra d'avoir une surveillance réseau complète avec un accent particulier sur la sécurité grâce à SELKS et une analyse approfondie du trafic avec NTOP.

### Aperçu
