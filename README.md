# README.md

## Bot Discord avec Analyse de Sentiment et Détection de Langue

Ce bot Discord intègre des fonctionnalités d'analyse de sentiment et de détection de langue en utilisant Azure Text Analytics. Il surveille des canaux spécifiques pour les messages entrants, analyse leur contenu et envoie des alertes avec les résultats de l'analyse de sentiment à un canal de signalement désigné.

### Prérequis

Avant d'exécuter le bot, assurez-vous de disposer des éléments suivants :

- Python installé sur votre système.
- Un compte de service Azure Text Analytics avec des identifiants valides.
- Le jeton du bot Discord.
- Un fichier YAML contenant les clés API (par exemple, `api-keys.yaml`).

### Installation

1. Clonez ce dépôt sur votre machine locale :

    ```bash
    git clone <repository-url>
    ```

2. Installez les paquets Python requis :

    ```bash
    pip install -r requirements.txt
    ```

3. Configurez les clés API :

   Créez un repetoire "private" puis à ajoutee un fichier `api-keys.yaml`  avec la structure suivante :
   ```yaml
   discord_bot_token: VOTRE_JETON_DE_BOT_DISCORD
   text_analytics_key: VOTRE_CLÉ_ANALYTIQUE_DE_TEXTE_AZURE
   text_analytics_endpoint: VOTRE_POINT_DE_TERMINAISON_ANALYTIQUE_DE_TEXTE_AZURE
   ```

### Utilisation

Pour exécuter le bot, exécutez la commande suivante dans votre terminal :

```bash
python bot.py
```

### Fonctionnalités

Le bot effectue les actions suivantes :

1. **Initialisation du Client Discord** : Initialise le client Discord avec les intentions nécessaires pour accéder aux guildes, aux messages et aux membres.

2. **Initialisation du Client Text Analytics** : Initialise le client Text Analytics avec les identifiants Azure pour l'analyse de sentiment et la détection de langue.

3. **Surveillance des Canaux** : Surveille des canaux spécifiques nommés "test-bot-g1", "test-bot-g2", "test-bot-g3" et "test-bot-g4" pour les messages entrants.

4. **Analyse de Sentiment** : Analyse le sentiment des messages entrants en utilisant Azure Text Analytics et affiche le sentiment (par exemple, positif, négatif, neutre).

5. **Détection de Langue** : Détecte la langue des messages entrants en utilisant Azure Text Analytics et affiche la langue détectée.

6. **Reconnaissance d'Entités** : Reconnaît les entités nommées dans les messages entrants en utilisant Azure Text Analytics et affiche les entités reconnues.

7. **Envoi d'Alertes** : Envoie des alertes avec les résultats de l'analyse de sentiment à un canal de signalement désigné nommé "report-bot-g2".

### Remarques

- Le bot ignore les messages des utilisateurs avec des noms spécifiques (par exemple, "Bully Macguire#2062", "Arsene Deghela#3390", "MessageBot#9405") pour éviter de traiter des messages inutiles.

- Le bot effectue l'analyse de sentiment et la détection de langue uniquement sur les messages provenant de canaux de test spécifiques. Les messages provenant d'autres canaux sont ignorés.

### Contributeurs groupe 2

- [Thelma LUM]
- [Maxime Jores SIGNE FOKOUI]
- [ Franck malève Takuete ]
