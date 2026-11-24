# Épure

*Créé et développé par **Lenny Alidor**. © 2026 Lenny Alidor — tous droits réservés ([licence](LICENCE.txt)).*

**Épure donne à Windows 11 une interface plus simple, plus pratique et plus utile au quotidien** : un Dock, une barre des menus en haut de l'écran, une île, la grille **Applications** et **Fichiers**, un explorateur de fichiers propre à Épure.

- Aucun droit administrateur, ni pour l'installer ni pour l'utiliser.
- Rien d'autre à installer.
- Windows reste intact : on le retrouve tel quel en arrêtant ou en désinstallant Épure.

> Épure est en **phase de test**. Les versions sont publiées dans [Releases](../../releases), avec la description de leurs changements.

---

## Sommaire

1. [Ce que fait Épure](#1-ce-que-fait-épure)
2. [Installer](#2-installer)
3. [Les raccourcis clavier](#3-les-raccourcis-clavier)
4. [Les mises à jour](#4-les-mises-à-jour)
5. [Revenir à une version précédente](#5-revenir-à-une-version-précédente)
6. [Signaler un problème](#6-signaler-un-problème)
7. [Désinstaller](#7-désinstaller)
8. [Licence](#8-licence)

---

## 1. Ce que fait Épure

### Le bureau
- **Dock** en bas de l'écran : loupe au survol, applis épinglées et ouvertes, applis en arrière-plan, Téléchargements et Corbeille, masquage automatique.
- **Barre des menus** en haut, une par écran :
  - menus de l'appli au premier plan ;
  - **son** avec le choix de la sortie audio en un clic ;
  - **batterie** avec le temps restant ;
  - Wi-Fi, Centre de contrôle, date et calendrier.
- **Île** en haut, au centre :
  - musique et vidéos en cours (clic sur la pochette pour revenir à l'appli qui joue) ;
  - téléchargements, minuteur, bloc-notes, volume et luminosité ;
  - annonces (Wi-Fi, Bluetooth, batterie, mode Avion…).
- **Applications** : toutes les applis en grille, recherche, dossiers par glisser-déposer.
- **Centre de contrôle** : Wi-Fi, Bluetooth, Ne pas déranger, mode sombre, mode Avion, mode d'alimentation, éclairage nocturne, volume, luminosité…
- **Vue d'ensemble** (Windows + Tab) :
  - toutes les fenêtres, avec leur nom toujours lisible ;
  - les fenêtres ancrées ensemble restent groupées ;
  - bureaux virtuels.
- **Sélecteur d'applis** (Alt + Tab) : les applis ouvertes dans plusieurs fenêtres montrent la liste de leurs fenêtres.

### Fichiers, l'explorateur d'Épure
- Remplace l'Explorateur de Windows partout : dossiers, Corbeille, Windows + E, Windows + R.
- Vues icônes, liste et colonnes, aperçu rapide avec Espace, mode clair ou sombre.
- Barre latérale : Accueil, Récents, Applications, Nettoyage, Corbeille, épinglés, cloud, collections, disques, Linux (WSL).
- **Images** : convertir (PNG, JPG, BMP, TIFF, GIF ; WebP et HEIC en lecture) et **retirer le fond**.
- **Nettoyage** : installeurs déjà utilisés, doublons, très gros fichiers, vieux téléchargements, fichiers temporaires. Tout part à la Corbeille.
- **« Choisir dans Fichiers »** sous les fenêtres Enregistrer et Ouvrir des autres applis.

### Outils
- **Exécuter** (Windows + R), **presse-papiers** avec historique (Windows + V).
- **Projeter** (Windows + P), **recopie de l'écran** sans fil (Windows + K).
- **Assistant** (Windows + Espace), **audio partagé** sur plusieurs sorties.

---

## 2. Installer

Tu as reçu deux fichiers : **`Installer-Epure.cmd`** et **`Installer-Epure.ps1`**.

1. Mets-les dans le **même dossier**.
2. Double-clique sur **`Installer-Epure.cmd`**, tape **`1`**, puis Entrée.
3. Réponds **O** si tu veux qu'Épure démarre avec Windows.
4. Épure se lance : le Dock, la barre des menus et l'île apparaissent.

> Si Windows affiche **« Windows a protégé votre ordinateur »**, clique sur **Informations complémentaires**, puis sur **Exécuter quand même**. L'appli n'est simplement pas signée.

Tu peux ensuite supprimer les deux fichiers : l'installateur reste sur ton PC, sous le nom **« Épure - outils »** dans le menu Démarrer.

---

## 3. Les raccourcis clavier

| Raccourci | Ce que ça fait |
|---|---|
| `Windows` (seul) | Menu Épure |
| `Windows + E` | Ouvrir **Fichiers** |
| `Windows + R` | Fenêtre **Exécuter** d'Épure |
| `Windows + Tab` | Vue d'ensemble |
| `Windows + A` | Centre de contrôle |
| `Windows + Espace` | Assistant |
| `Windows + V` | Presse-papiers (historique, recherche, épingles) |
| `Windows + P` | Projeter |
| `Windows + K` | Recopie de l'écran sans fil |
| `Alt + Tab` | Sélecteur d'applis : `↑ ↓` choisissent la fenêtre, `Q` quitte l'appli, `H` la masque |
| `Ctrl + Alt + Échap` | Forcer une appli à quitter |

---

## 4. Les mises à jour

Quand une nouvelle version sort, une petite fenêtre apparaît en haut à droite : **« Épure X est disponible »**, avec un résumé de ce qui change.
- **Installer** : Épure télécharge la version, se remplace et redémarre tout seul.
- **Plus tard** : elle ne te sera plus proposée avant la version suivante.

Le détail de chaque version est dans [Releases](../../releases), et dans le fichier `Nouveautes.md` du dossier d'Épure.

---

## 5. Revenir à une version précédente

Ouvre **« Épure - outils »** dans le menu Démarrer :

| Choix | Ce qu'il fait |
|---|---|
| **1** | Installer la dernière version |
| **2** | **Revenir à la version précédente** (instantané, sans Internet) |
| **3** | **Installer la dernière version stable** (la plus sûre) |
| **4** | Choisir une version dans la liste |
| **5** | Désinstaller Épure |

Après un retour en arrière, la version qui posait problème ne te sera plus proposée. La suivante le sera normalement.

---

## 6. Signaler un problème

Envoie à Lenny Alidor une phrase sur ce qui s'est passé, et si possible la fin du journal. Dans PowerShell :

```powershell
Get-Content "$env:APPDATA\Epure\dock-natif.log" -Tail 60 | Set-Clipboard
```

Colle ensuite le presse-papiers dans ton message.

**Épure a disparu (plus de Dock ni de barre des menus) ?** Relance-le depuis le raccourci **Épure** du menu Démarrer ou du Bureau.

---

## 7. Désinstaller

**« Épure - outils »**, choix **`5`**. La barre des tâches de Windows revient. Tu peux aussi effacer tes réglages et le journal.

---

## 8. Licence

Épure est le travail de **Lenny Alidor**. Tu peux l'utiliser gratuitement pour le tester, mais pas le redistribuer, le modifier ni le décompiler. Voir [`LICENCE.txt`](LICENCE.txt).

Windows est une marque de Microsoft. Épure n'est ni affilié à Microsoft, ni approuvé par Microsoft.
