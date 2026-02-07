Pour ce projet, j'ai mis en place un machine virtuelle uniquement grâce à vmware en host-only, 
sans accès à internet et sans services expos&s hors SSH. L'attaquant peut-être local ou distant 
et est au départ un utilisateur non privilégié. J'ai établi une connexion ssh entre ma machine hôte et la vm. 
J'ai mis en place 4 failles : un utilisateur avec un mot de passe faible appelé 'jay', un script avec 
des privilèges supérieurs contenant des informations sensibles lisible grâce à une mauvaise utilisation 
de la variable d'environnement PATH, un script cron mal configuré, et un binaire SUID mal configuré. 
Ce projet est un projet personnel et à but purement pédagogique. Ma configuration est volontairement vunérable. 
J'ai voulu créé des failles systèmes afin de mieux comprendre comment un environnement Linux fonctionne 
et apprendre de façon concrète comment corriger ces erreurs. J'ai voulu experimenter avec l'élévation de privilèges, 
la gestion de permissions, et la surface d'attaque système. 

vuln-linux-lab/
├── README.md
├── challenges/
│   	├── ch1/
│		└── ch1
│		└── ch1.c 
│   		└── private_notes.txt
│		└── enoncé.txt
│   	├── ch2/
│		└── enoncé.txt
│   	├── ch3/
│		└── enoncé.txt
├── setup/
│   ├── cron/
│   │   └── vulnerable_cron.sh
│   └── install_suid.sh
├── suid/
│   ├── vuln.c
│   └── Makefile
├── screenshots/
│   ├── path_exploit.png
│   ├── cron_exploit.png
│   └── suid_root.png
└── docs/
    ├── architecture.md
    ├── attack_chain.md
    └── mitigations.md



