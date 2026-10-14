# Politique de confidentialité — Lumi GEO

*English version: [read in English](./).*

*Dernière mise à jour : 14 octobre 2026*

Lumi GEO est une extension pour le navigateur Chrome qui analyse la page web ouverte : ce que les robots IA en voient, données structurées, accès des robots IA, bases SEO, fichier llms.txt.

## Données collectées

**Aucune pour l'analyse.** Lumi GEO ne collecte, ne transmet, ne vend et ne partage aucune donnée de navigation : les pages que vous analysez et leurs résultats ne quittent jamais votre appareil.

Seule exception : l'**abonnement Pro**, facultatif (voir plus bas). Il est géré par Lemon Squeezy, qui reçoit les informations nécessaires au paiement.

## Fonctionnement

- L'analyse a lieu **uniquement quand vous cliquez** sur l'icône de l'extension, et seulement sur l'onglet concerné.
- Elle se déroule **entièrement dans votre navigateur**. Aucun serveur appartenant à l'éditeur n'est contacté, et l'analyse n'utilise aucune API externe.
- Pour vérifier les fichiers `/robots.txt`, `/llms.txt` et `/llms-full.txt`, et pour obtenir le HTML brut de la page (« vue robot »), l'extension les demande **au site que vous consultez**, exactement comme le ferait votre navigateur (le HTML brut est demandé sans cookies, comme le ferait un robot). Avec « Analyser le site » (Pro), quand vous cliquez dessus, le sitemap et jusqu'à 20 pages **du même site** sont demandés de la même façon, l'une après l'autre. Aucune autre adresse n'est contactée.
- Le détail des résultats n'est pas enregistré et disparaît à la fermeture du panneau. Seule la note finale est gardée (voir ci-dessous).

## Stockage local

L'extension mémorise dans votre navigateur (`chrome.storage.local`), et nulle part ailleurs :

- vos préférences d'interface (animations activées ou non, présentation de Lumi déjà vue) ;
- si vous êtes abonné : votre **clé de licence** et l'identifiant de son activation dans ce navigateur, ainsi que votre **dernier plan connu** (gratuit ou Pro, état de la clé, adresse e-mail de l'achat), pour qu'un abonné garde Pro quelques jours sans connexion ;
- l'**historique des notes de chaque page analysée** (adresse de la page sans ses paramètres, date, note globale et notes des 4 piliers), pour afficher son évolution. Au maximum 30 analyses par page et 300 pages ; les plus anciennes sont oubliées en premier ;
- pour le plan gratuit, le **compteur quotidien d'analyses** (5 pages différentes par jour) : la date du jour et un code court calculé à partir de chaque page analysée dans la journée. Ce code ne contient pas l'adresse de la page et ne permet pas de la retrouver. Ce compteur repart de zéro chaque jour.

Ces informations ne quittent jamais votre appareil. Vous pouvez effacer l'historique des notes à tout moment (Réglages › « Effacer l'historique des notes ») ; le compteur quotidien se remplace de lui-même chaque jour ; tout disparaît si vous désinstallez l'extension.

## Lumi IA (IA intégrée à Chrome)

Quand vous cliquez sur « Demander à Lumi », le texte de la page analysée est lu par **l'IA intégrée à Chrome (Gemini Nano)**, qui fonctionne **sur votre ordinateur**. Aucun texte n'est envoyé à un serveur, ni à l'éditeur de Lumi GEO, ni à un service d'IA en ligne. La première fois, Chrome télécharge son modèle d'IA (une seule fois, depuis Google) : c'est Chrome qui gère ce téléchargement, pas Lumi GEO. Les réponses de l'IA ne sont pas enregistrées.

## Rapport PDF

Le rapport est fabriqué dans votre navigateur. Ses données passent par la mémoire de session de Chrome (`chrome.storage.session`), vidée à la fermeture du navigateur, puis s'affichent dans un onglet de l'extension. Le PDF est créé par la fonction d'impression de Chrome : aucun service en ligne n'est utilisé.

## Abonnement Pro (facultatif)

Lumi GEO Pro est un abonnement payant. Les paiements sont gérés par **Lemon Squeezy** (lemonsqueezy.com), vendeur officiel (« merchant of record ») : la page de paiement est la sienne, et Lumi GEO ne voit jamais votre numéro de carte.

- Après le paiement, Lemon Squeezy vous envoie une **clé de licence** par e-mail. Vous la collez dans Lumi GEO (Plans).
- Rien n'est envoyé à Lemon Squeezy tant que vous n'avez pas saisi de clé.
- Avec une clé, l'extension envoie à l'API de licences de Lemon Squeezy (api.lemonsqueezy.com) **uniquement la clé, l'identifiant de son activation et le libellé « Lumi GEO (Chrome) »** : quand vous l'activez, à chaque ouverture du panneau (pour vérifier que l'abonnement est toujours actif), et quand vous la retirez du navigateur.
- Lemon Squeezy reçoit ce que vous saisissez sur sa page de paiement (adresse e-mail, moyen de paiement, adresse de facturation) et le traite selon sa propre politique de confidentialité : [Lemon Squeezy](https://www.lemonsqueezy.com/privacy).
- Aucune donnée de navigation ni aucun résultat d'analyse ne lui est jamais envoyé.

## Mesure d'audience et publicité

Aucune. L'extension ne contient ni outil de statistiques, ni traceur, ni publicité.

## Permissions demandées


| Permission  | Usage                                                                                                                    |
| ----------- | ------------------------------------------------------------------------------------------------------------------------ |
| `activeTab` | Lire la page ouverte, uniquement après votre clic sur l'icône                                                            |
| `scripting` | Exécuter le script d'analyse dans cette page, après ce clic                                                              |
| `sidePanel` | Afficher les résultats dans le panneau latéral                                                                           |
| `storage`   | Mémoriser vos préférences d'interface, l'historique des notes, votre plan et le compteur quotidien des analyses gratuites ; préparer le rapport PDF |


## Contact

Pour toute question : matteo.spring67@gmail.com