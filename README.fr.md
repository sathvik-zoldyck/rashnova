<div align="center">

<img src="assets/rashnova-banner.png" alt="Rashnova, la boîte noire de votre ordinateur portable, par Alcyone Secure" width="100%">

# Rashnova

### Un enregistreur d'activité pour Windows qui révèle toute altération

**Confiez votre PC. Récupérez-le avec un registre scellé de ce qui en a été fait.**

[![Latest release](https://img.shields.io/github/v/release/sathvik-zoldyck/rashnova?style=flat-square&label=release&labelColor=111111&color=F25C05)](https://github.com/sathvik-zoldyck/rashnova/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/sathvik-zoldyck/rashnova/total?style=flat-square&labelColor=111111&color=F25C05)](https://github.com/sathvik-zoldyck/rashnova/releases)
[![Platform](https://img.shields.io/badge/Windows-10%20%7C%2011%20%28x64%29-F25C05?style=flat-square&labelColor=111111)](#requirements)
[![Price](https://img.shields.io/badge/price-free-F25C05?style=flat-square&labelColor=111111)](#download)
[![Licence](https://img.shields.io/badge/licence-proprietary-555555?style=flat-square&labelColor=111111)](LICENSE)

[**Télécharger**](https://github.com/sathvik-zoldyck/rashnova/releases/latest) ·
[**Site web**](https://www.alcyonesecure.com) ·
[**Limites connues**](KNOWN_LIMITS.md) ·
[**Confidentialité**](#privacy) ·
[**Sécurité**](SECURITY.md)

</div>

> **Langues** &nbsp;·&nbsp; [English](README.md) · [हिन्दी](README.hi.md) · [ಕನ್ನಡ](README.kn.md) · [മലയാളം](README.ml.md) · [Español](README.es.md) · **Français** · [Deutsch](README.de.md) · [Português](README.pt.md) · [日本語](README.ja.md) · [Bahasa Indonesia](README.id.md) · [עברית](README.he.md)

---
> [!NOTE]
> Cette page est traduite de l'anglais. L'application Rashnova est en anglais : les noms des boutons et des écrans sont
> donc donnés ici en anglais. En cas de différence avec la [version anglaise](README.md), c'est la version anglaise qui fait foi.


Rashnova enregistre ce qui se passe sur un PC Windows pendant que quelqu'un d'autre l'a entre les mains : chez un
réparateur, au service informatique, ou chez toute personne à qui vous le confiez. Lancez une **Repair session** avant de
le confier. Quand le PC revient, terminez-la : Rashnova vous donne un verdict et un rapport de ce qui a été ouvert, copié,
renommé et supprimé, des programmes lancés et des clés USB branchées.

Chaque entrée est scellée à la précédente : le registre montre donc si quelque chose a été modifié ou supprimé, et il
montre chaque intervalle pendant lequel rien n'a pu être enregistré. Tout reste sur votre ordinateur. Pas de compte, pas
de cloud, pas de télémétrie.


> [!NOTE]
> Ce dépôt est l'endroit où Rashnova est **publié** : installateurs, notes de version, limites connues et politique
> de sécurité. Rashnova est un logiciel propriétaire d'[Alcyone Secure](https://www.alcyonesecure.com) ; son code source
> n'est pas publié ici.


## Sommaire

- [Pourquoi Rashnova](#why)
- [Ce qu'il fait](#what-it-does)
- [Ce qu'il n'enregistre jamais](#never)
- [Comment ça marche](#how)
- [Téléchargement et installation](#download)
- [Configuration requise](#requirements)
- [Confidentialité](#privacy)
- [Limites connues](#limits)
- [Mises à jour](#updates)
- [Aide et sécurité](#support)
- [Licence](#licence)

<a name="why"></a>
## Pourquoi Rashnova

Les avions, les trains et les navires ont une boîte noire. Un ordinateur qui quitte vos mains n'a rien, et la
personne qui le tient a accès à tout ce qu'il contient.

Et cet accès est utilisé. Dans une [étude de 2022 menée par des chercheurs de l'Université de Guelph](https://arxiv.org/abs/2211.05824)
(publiée à l'IEEE Symposium on Security and Privacy 2023), des ordinateurs portables ont été laissés une nuit chez 12
réparateurs, avec la journalisation activée. Les techniciens de six d'entre eux ont accédé aux données personnelles qu'ils
contenaient, et deux ont copié des données hors de l'ordinateur. Les antivirus et les outils de sécurité des postes n'ont
jamais été conçus pour le remarquer : on avait remis les clés à cette personne.

Rashnova n'est pas de la prévention. C'est une preuve, pour que ce qui s'est passé puisse être vérifié plutôt que
débattu.

> *La confiance, c'est bien. La preuve, c'est mieux.*

<a name="what-it-does"></a>
## Ce qu'il fait

<table>
<tr>
<td width="50%" valign="top">

**Repair Mode (mode réparation).** Une session surveillée, démarrée avec votre PIN avant de confier le PC et
terminée avec votre PIN quand vous le récupérez. Elle enregistre les fichiers ouverts, créés, renommés, copiés et
supprimés, les programmes lancés, les commandes PowerShell exécutées, les connexions, et les supports de stockage USB
branchés, y compris chaque fichier écrit dessus. Un redémarrage, un arrêt ou une mise en veille ne termine jamais la
session : le rapport montre chaque interruption et sa durée.

</td>
<td width="50%" valign="top">

<img src="assets/screenshots/session-summary.png" alt="Résumé de session : un verdict, les événements les plus notables et la vérification de la chaîne">

</td>
</tr>
<tr>
<td width="50%" valign="top">

<img src="assets/screenshots/session-explorer.png" alt="Explorateur de session : chaque événement dans le temps, par programme et par dossier">

</td>
<td width="50%" valign="top">

**Un registre que vous pouvez vérifier.** Chaque session se termine par un verdict et un rapport à enregistrer en
PDF, en page web ou en tableur. L'explorateur de session montre chaque événement dans le temps, par programme et par
dossier, et la vérification de la chaîne vous dit si le registre est intact. Ce que vous enregistrez est une copie ;
l'original reste là où Rashnova le conserve.

</td>
</tr>
<tr>
<td width="50%" valign="top">

**Le Readout hebdomadaire.** Votre semaine en un verdict, avec au plus quelques points à regarder. Marquez chacun
"that was me" (c'était moi) ou "that wasn't me" (ce n'était pas moi). Il dit aussi, en termes simples, ce que Rashnova
peut voir et ce qu'il ne peut pas voir.

</td>
<td width="50%" valign="top">

<img src="assets/screenshots/weekly-readout.png" alt="Le Readout hebdomadaire : un verdict pour la semaine, des points à regarder, l'activité par jour">

</td>
</tr>
<tr>
<td width="50%" valign="top">

<img src="assets/screenshots/always-on-choice.png" alt="Le choix entre un enregistrement limité aux sessions et un enregistrement permanent">

</td>
<td width="50%" valign="top">

**Enregistrement permanent (always-on), seulement si vous le choisissez.** Désactivé tant que vous ne l'activez pas.
Il conserve l'irréversible et l'alarmant (suppressions définitives, fichiers d'apparence sensible, tout ce qui entre sur
un support amovible ou en sort), pas votre usage quotidien de vos propres fichiers. Le désactiver se fait en un clic
depuis la zone de notification ou Settings, et ne demande jamais votre PIN.

</td>
</tr>
<tr>
<td width="50%" valign="top">

**Depuis la zone de notification.** Voyez qu'une session enregistre, terminez-la, lancez un contrôle de 30 secondes
de l'activité des fichiers en direct (Monitor Now), ou ouvrez le dernier rapport.

</td>
<td width="50%" valign="top" align="center">

<img src="assets/screenshots/quick-panel.png" alt="Le panneau rapide dans la zone de notification de Windows" width="70%">

</td>
</tr>
</table>

<sub>Les captures montrent Rashnova avec une session d'exemple (une utilisatrice fictive, "Riya").</sub>

<a name="never"></a>
## Ce qu'il n'enregistre jamais

Rashnova enregistre **le fait** qu'une chose s'est produite, pas ce qui était à l'écran. Il n'enregistre pas :

- les frappes au clavier
- le contenu du presse-papiers
- votre écran, en images ou en vidéo
- votre caméra ou votre micro
- le contenu de vos documents, photos, e-mails ou messages
- les pages web que vous visitez, ni leur contenu

Deux choses qu'il enregistre méritent d'être connues. Pendant une Repair session, les commandes PowerShell sont
enregistrées quand elles s'exécutent, ainsi que la ligne de démarrage complète de chaque programme qu'une personne lance :
un navigateur ouvert depuis un lien montre donc ce lien.

Un rapport dit par exemple que `Bank_Statement_Aug2026.pdf` a été ouvert depuis `Documents\Finance` par
Microsoft Edge à 15:01:16. Il ne dit pas ce que contenait le relevé.

<a name="how"></a>
## Comment ça marche

1. **Installez.** Setup installe Rashnova et son enregistreur en arrière-plan.
2. **Choisissez un PIN.** Le PIN est vérifié par l'enregistreur, pas par la fenêtre de l'application.
3. **Avant de le confier :** **Repair Mode > Activate**, puis votre PIN.
4. **Confiez-le.** Tout ce qui figure dans "Ce qu'il fait" est écrit dans un registre scellé.
5. **À son retour :** **Deactivate**, puis votre PIN. Vous obtenez un verdict, un rapport et la vérification de la chaîne.

L'enregistreur fonctionne comme un service Windows : il continue d'enregistrer, que quelqu'un ouvre la fenêtre de
Rashnova ou non, et il redémarre tout seul après un redémarrage.

**Chaque session se termine par l'un de quatre verdicts :**

| Verdict | Signification |
| --- | --- |
| **Quiet** | Le registre est vérifié, il est complet, et rien d'important ne s'est produit. |
| **Notable** | Au moins un événement élevé (high) ou critique (critical) : à lire. |
| **Compromised** | Le registre présente un trou pendant la session (l'ordinateur était éteint, en veille ou en redémarrage, ou la surveillance a été interrompue) ou montre une interférence : il ne peut donc pas répondre de toute la session. |
| **Chain broken** | Le registre ne se vérifie pas. Tout est quand même affiché, marqué comme non vérifié. |

<a name="download"></a>
## Téléchargement et installation

| Fichier | Pour qui |
| --- | --- |
| **`Rashnova-Setup-1.1.0.exe`** | Tout le monde. Installe d'abord le .NET 8 Desktop Runtime de Microsoft si votre PC ne l'a pas, puis Rashnova. |
| `Rashnova-1.1.0.msi` | Les administrateurs qui déploient avec leurs propres outils. Nécessite le .NET 8 Desktop Runtime déjà installé. |
| `SHA256SUMS.txt` | Le SHA-256 de chaque fichier, pour vérifier votre téléchargement. |

1. Téléchargez `Rashnova-Setup-1.1.0.exe` depuis la [dernière version](https://github.com/sathvik-zoldyck/rashnova/releases/latest).
2. **Vérifiez le fichier** (recommandé). Dans PowerShell :
   ```powershell
   Get-FileHash "$env:USERPROFILE\Downloads\Rashnova-Setup-1.1.0.exe"
   ```
   Le hash doit correspondre exactement à celui de `SHA256SUMS.txt` et des notes de version.
3. Lancez-le. Windows SmartScreen affiche **"Windows protected your PC"** avec un éditeur inconnu, car
   l'installateur n'est pas encore signé numériquement (voir les [limites connues](KNOWN_LIMITS.md)). Choisissez
   **More info**, puis **Run anyway**.
4. Acceptez les [conditions de licence](https://www.alcyonesecure.com/terms), installez et ouvrez Rashnova.
5. Choisissez un PIN, puis gardez l'enregistrement limité aux sessions (par défaut) ou activez l'enregistrement
   permanent.


> [!IMPORTANT]
> Un PIN oublié ne peut pas être récupéré, ni par nous ni par personne. Notez-le en lieu sûr.
> Désactiver l'enregistrement permanent ne demande jamais le PIN.


**Vous venez de BlackBox 1.0.1 ?** Rashnova est le nouveau nom de BlackBox. Téléchargez et installez 1.1.0.

<a name="requirements"></a>
## Configuration requise

- Windows 10 ou Windows 11, 64 bits (testé sur Windows 10)
- Microsoft .NET 8 Desktop Runtime (Setup l'installe s'il manque)
- L'accord d'un administrateur pour installer, car l'enregistreur fonctionne comme un service Windows

<a name="privacy"></a>
## Confidentialité

- **Local uniquement.** Le registre est écrit et conservé sur votre ordinateur. Il n'y a ni compte ni cloud dans 1.1.0,
  et Rashnova n'envoie aucune donnée d'utilisation.
- **Deux petites requêtes,** qui ne contiennent rien de votre registre : une vérification quotidienne sur
  alcyonesecure.com d'une nouvelle version et, pendant une Repair session, une vérification de l'heure auprès du serveur de
  temps de Microsoft.
- **Qui peut lire le registre.** Le compte Windows qui a choisi le PIN, et les administrateurs de l'ordinateur. La
  seconde copie est chiffrée, et Rashnova ne l'ouvre qu'après avoir vérifié votre PIN. Les administrateurs de l'ordinateur
  peuvent quand même la lire.
- **Prévenez les personnes qui utilisent votre PC.** L'enregistrement permanent couvre tout l'ordinateur, y compris les
  personnes qui n'ouvrent jamais Rashnova.
- **Un réglage de Windows, dit clairement.** La première fois que l'enregistrement est activé, Rashnova active la
  journalisation des scripts PowerShell de Windows et note la valeur précédente du réglage. Il ne désactive jamais un
  réglage activé par quelqu'un d'autre.

<a name="limits"></a>
## Limites connues

Nous publions ce que Rashnova ne fait pas, pour que vous décidiez en connaissance de cause. L'essentiel :

- **Rien ne peut être enregistré pendant que l'ordinateur est éteint, en veille ou en redémarrage.** La session continue,
  et le rapport montre chaque interruption et sa durée.
- **Les administrateurs peuvent lire le registre.** Aucun programme ne peut cacher ses fichiers à un administrateur Windows.
- **L'installateur n'est pas encore signé numériquement,** donc Windows SmartScreen avertit avant de le lancer.
- **Le blocage du stockage USB n'est pas dans 1.1.0.** Chaque clé USB et chaque fichier copié dessus sont enregistrés ;
  le blocage arrivera dans une mise à jour.

La liste complète, avec la raison de chaque limite et ce qui est prévu (en anglais) : **[KNOWN_LIMITS.md](KNOWN_LIMITS.md)**.

<a name="updates"></a>
## Mises à jour

Une fois par jour, Rashnova vérifie sur alcyonesecure.com s'il existe une nouvelle version et vous prévient. Vous la
téléchargez et l'installez vous-même ; votre registre, votre PIN et vos réglages sont conservés. Chaque version est
publiée ici avec ses notes et son SHA-256. Voir le [journal des modifications](CHANGELOG.md).

<a name="support"></a>
## Aide et sécurité

- **Aide :** consultez [SUPPORT.md](SUPPORT.md) ou écrivez à **support@alcyonesecure.com**.
- **Bugs :** [ouvrez un issue](https://github.com/sathvik-zoldyck/rashnova/issues/new/choose). Ne publiez jamais votre
  registre, des noms de fichiers ou quoi que ce soit de personnel dans un issue.
- **Failles de sécurité :** n'ouvrez pas d'issue public. Suivez [SECURITY.md](SECURITY.md).

<a name="licence"></a>
## Licence

Rashnova est un logiciel propriétaire, gratuit sur les appareils qui vous appartiennent ou que vous êtes autorisé à
surveiller. Voir [LICENSE](LICENSE) et les [conditions](https://www.alcyonesecure.com/terms) (en anglais ; elles font
foi). Les documents et images de ce dépôt sont © Alcyone Secure.

---

<div align="center">

<img src="assets/alcyone-owl.png" alt="Alcyone Secure" width="40">

**Alcyone Secure** · Conçu à Bengaluru, Inde · [alcyonesecure.com](https://www.alcyonesecure.com)

*La sécurité n'est pas seulement la prévention. La sécurité, c'est la responsabilité.*

</div>
