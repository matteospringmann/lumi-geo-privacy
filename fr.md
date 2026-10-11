# Politique de confidentialité — Lumi GEO

*English version: [read in English](./).*

*Dernière mise à jour : 11 octobre 2026*

Lumi GEO est une extension pour le navigateur Chrome qui analyse la page web ouverte : ce que les robots IA en voient, données structurées, accès des robots IA, bases SEO, fichier llms.txt.

## Données collectées

**Aucune.** Lumi GEO ne collecte, ne transmet, ne vend et ne partage aucune donnée personnelle ni aucune donnée de navigation.

## Fonctionnement

- L'analyse a lieu **uniquement quand vous cliquez** sur l'icône de l'extension, et seulement sur l'onglet concerné.
- Elle se déroule **entièrement dans votre navigateur**. Aucun serveur appartenant à l'éditeur n'est contacté, et l'extension n'utilise aucune API externe.
- Pour vérifier les fichiers `/robots.txt`, `/llms.txt` et `/llms-full.txt`, et pour obtenir le HTML brut de la page (« vue robot »), l'extension les demande **au site que vous consultez**, exactement comme le ferait votre navigateur (le HTML brut est demandé sans cookies, comme le ferait un robot). Aucune autre adresse n'est contactée.
- Le détail des résultats n'est pas enregistré et disparaît à la fermeture du panneau. Seule la note finale est gardée (voir ci-dessous).

## Stockage local

L'extension mémorise dans votre navigateur (`chrome.storage.local`), et nulle part ailleurs :

- vos préférences d'interface (animations activées ou non, présentation de Lumi déjà vue) ;
- l'**historique des notes de chaque page analysée** (adresse de la page sans ses paramètres, date, note globale et notes des 4 piliers), pour afficher son évolution. Au maximum 30 analyses par page et 300 pages ; les plus anciennes sont oubliées en premier.

Ces informations ne quittent jamais votre appareil. Vous pouvez les effacer à tout moment (Réglages › « Effacer l'historique des notes »), et tout disparaît si vous désinstallez l'extension.

## Lumi IA (IA intégrée à Chrome)

Quand vous cliquez sur « Demander à Lumi », le texte de la page analysée est lu par **l'IA intégrée à Chrome (Gemini Nano)**, qui fonctionne **sur votre ordinateur**. Aucun texte n'est envoyé à un serveur, ni à l'éditeur de Lumi GEO, ni à un service d'IA en ligne. La première fois, Chrome télécharge son modèle d'IA (une seule fois, depuis Google) : c'est Chrome qui gère ce téléchargement, pas Lumi GEO. Les réponses de l'IA ne sont pas enregistrées.

## Rapport PDF

Le rapport est fabriqué dans votre navigateur. Ses données passent par la mémoire de session de Chrome (`chrome.storage.session`), vidée à la fermeture du navigateur, puis s'affichent dans un onglet de l'extension. Le PDF est créé par la fonction d'impression de Chrome : aucun service en ligne n'est utilisé.

## Mesure d'audience et publicité

Aucune. L'extension ne contient ni outil de statistiques, ni traceur, ni publicité.

## Permissions demandées


| Permission  | Usage                                                                                                                    |
| ----------- | ------------------------------------------------------------------------------------------------------------------------ |
| `activeTab` | Lire la page ouverte, uniquement après votre clic sur l'icône                                                            |
| `scripting` | Exécuter le script d'analyse dans cette page, après ce clic                                                              |
| `sidePanel` | Afficher les résultats dans le panneau latéral                                                                           |
| `storage`   | Mémoriser vos préférences d'interface et l'historique des notes, uniquement sur votre appareil ; préparer le rapport PDF |


## Contact

Pour toute question : matteo.spring67@gmail.com