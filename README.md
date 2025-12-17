<!-- =========================================================
README - Age Of Empire Like (Unreal Engine)
Auteur: Lucas Dos Santos
========================================================= -->

<div align="center">

# 🏰 Age Of Empire Like (RTS Prototype)

**Un prototype RTS style Age of Empires : sélection d’unités, caméra RTS complète, récolte, construction drag & drop, HUD ressources.**

<br/>

<!-- Language switch (clickable) -->
<a href="#english">🇬🇧 English</a> • <a href="#français">🇫🇷 Français</a>

<br/><br/>

<!-- Badges (optionnel) -->
<!--
![Unreal Engine](https://img.shields.io/badge/Unreal%20Engine-5.6%2B-black)
![Platform](https://img.shields.io/badge/Platform-Windows-blue)
-->

</div>

---

<div align="center">

## 🖼️ Screenshots / Images

</div>

> Ajoute tes images dans un dossier `docs/images/` puis remplace les liens ci-dessous.

<p align="center">
  <img src="docs/images/screenshot_01.png" width="32%" />
  <img src="docs/images/screenshot_02.png" width="32%" />
  <img src="docs/images/screenshot_03.png" width="32%" />
</p>

---

# English

## 🎮 About
This project is an **RTS prototype** inspired by *Age of Empires*:
- Unit selection (single click or drag rectangle)
- Full RTS camera controls (drag, edge scrolling, zoom, rotation)
- Resource harvesting (wood, stone, food, gold)
- Storage buildings
- Drag & drop building placement with ghost preview + validation
- HUD showing current resources and max capacity

## ⚙️ Features
✅ Unit selection system (click or selection box)  
✅ RTS camera movement (drag + edge scrolling + zoom + rotation)  
✅ Resource harvesting (wood, stone, food, gold)  
✅ Resource storage buildings  
✅ Drag & drop building construction  
✅ Ghost placement + validation + rotation  
✅ HUD with resources + max visible  

## 🕹️ Controls
**Camera**
- Move camera: **ZQSD** or **screen edge**
- Rotate camera: **Hold Right Mouse Button** + move mouse
- Zoom: **Mouse Wheel**

**Units**
- Select (single): **Left Click**
- Select (box): **Hold Left Click** + drag
- Add to selection: **Shift**
- Remove from selection: **Ctrl**
- Move unit(s): **Right Click**
- Harvest resource: **Select a Worker** + **Right Click** on a resource

**Building**
- Open build menu: **B**
- Drag a building: **Drag & Drop** from the build menu
- Place building: **Left Click** on terrain
- Rotate building: **Rotate button (blue)**
- Cancel placement: **Cancel button (red)**
- Confirm placement: **Confirm button (green)**
- Blocked if not enough resources

## 🏗️ Building System
- Press **B** to open the construction menu
- Drag a building onto the map
- A transparent **ghost** appears
- If placement is valid (on navmesh, no collision) → **green**
- Otherwise → **red**
- Left click to lock the ghost and open the validation UI
- Rotate / Cancel / Confirm from the UI  
- Construction is blocked if you don’t have enough resources

### 🏠 Available Buildings
🪵 Wood Storage  
🪨 Stone Storage  
🍗 Food Storage  
🪙 Gold Storage  

## 🌲 Harvesting & Resources
**Worker Units**
- Select a worker → Right click a resource node
- The unit harvests automatically until the node is empty or inventory/stock is full

**Resources**
- Wood
- Stone
- Gold
- Food

## 📊 HUD / UI
- Dynamic HUD at the top of the screen
- Updates automatically via the resource manager component

## 🧱 Code Architecture (Key Classes)
| System | Main Classes / Elements |
|---|---|
| Units | `ARTSUnitBase`, `AWorkerUnit` |
| Resource Node | `AResourceNode` |
| Harvest Logic | `WorkerUnitStartHarvesting()` |
| Resource Management | `UResourceManagerComponent` |
| Storage Building | `AResourceStorageBuilding` |
| Building Placement | `AGhostBuildingActor`, `ABuildingBase` |
| Placement UI | `UPlacementConfirmationWidget` |
| Build Menu UI | `UConstructionPanelWidget` |
| Main RTS Controller | `ARTSPlayerController` |
| Player State & Resources | `ARTSPlayerState` |

## 🗺️ Roadmap
⏳ Building upgrades  
⏳ Barracks + combat unit spawning  
⏳ Optimized multi-worker pathfinding  
⏳ Enemy AI (simple)  

## 🔧 Requirements
- **Unreal Engine 5.6+**
- Enhanced Input System
- UMG (UI)
- NavigationSystem (placement validation)

## 📦 Download / Build
> Put your downloadable build in **GitHub Releases** (recommended).
- **Latest build:** (add your release link here)
  
## 🚀 Installation & Run

### Requirements
- Windows 10 / 11 (64-bit)
- GPU compatible with DirectX 12
- Unreal Engine runtime included in the build

### How to Run
1. Download the latest build from the **Releases** section
2. Extract the `.zip` file anywhere on your computer
3. Run `AgeOfEmpire.exe`
4. Enjoy the game 🎮

⚠️ Do not move or delete any files inside the build folder.
The executable must stay in its original directory structure.

## 🐞 Known Issues & Troubleshooting

- **Black screen at launch**
  - Make sure all files were extracted correctly
  - Verify your GPU drivers are up to date

- **Low FPS on large maps**
  - Reduce screen resolution
  - Disable background applications

- **Building placement not working**
  - Make sure placement is on valid NavMesh
  - Check available resources

- **Game does not start**
  - Try running the executable as Administrator
  - Make sure Windows Defender did not block the executable

---

# Français

## 🎮 Présentation
Ce projet est un **prototype RTS** inspiré de *Age of Empires* :
- Sélection d’unités (clic simple ou rectangle)
- Caméra RTS complète (drag, bords d’écran, zoom, rotation)
- Récolte de ressources (bois, pierre, nourriture, or)
- Bâtiments de stockage
- Construction par glisser-déposer avec ghost + validation
- HUD ressources (quantité + maximum)

## ⚙️ Fonctionnalités
✅ Système de sélection d’unités (clic ou rectangle)  
✅ Déplacement libre de la caméra (drag + edge scrolling + zoom + rotation)  
✅ Récolte de ressources (bois, pierre, nourriture, or)  
✅ Bâtiments de stockage  
✅ Système de construction par glisser-déposer  
✅ Placement fantôme (ghost) + validation, rotation  
✅ HUD avec ressources + maximum visible  

## 🕹️ Contrôles
**Caméra**
- Déplacer caméra : **ZQSD** ou **bord d'écran**
- Tourner caméra : **Maintenir clic droit** + souris
- Zoom : **Molette souris**

**Unités**
- Sélection clic simple : **Clic gauche**
- Sélection rectangle : **Maintenir clic gauche** + glisser
- Ajouter sélection : **Maj**
- Enlever sélection : **Ctrl**
- Déplacement unité(s) : **Clic droit**
- Récolte ressource : **Sélectionner un Worker** + **clic droit** sur ressource

**Construction**
- Ouvrir menu construction : **B**
- Glisser un bâtiment : **Drag & Drop** depuis le menu
- Placer un bâtiment : **Clic gauche** sur le terrain
- Tourner un bâtiment : **Bouton Rotate (bleu)**
- Annuler construction : **Bouton Cancel (rouge)**
- Confirmer construction : **Bouton Confirme (vert)**
- Bloqué si pas assez de ressource

## 🏗️ Construction & Bâtiments
- Ouvrir le menu avec **B**
- Glisser un bâtiment vers la carte
- Un **ghost** transparent s’affiche
- Si l’emplacement est valide (sur le navmesh, pas de collision) → **vert**
- Sinon → **rouge**
- Clic gauche → bloquer le ghost + ouvrir menu de validation
- Rotation / Annulation / Confirmation via l’UI
- Impossible si pas assez de ressources

### 🏠 Bâtiments disponibles
🪵 Entrepôt de bois  
🪨 Entrepôt de pierre  
🍗 Réserve de nourriture  
🪙 Dépôt d’or  

## 🌲 Récolte & Ressources
**Unités Worker**
- Sélectionner → clic droit sur une ressource
- L’unité récolte automatiquement jusqu’à épuisement ou stock plein

**Ressources gérées**
- Bois
- Pierre
- Or
- Nourriture

## 📊 HUD & Interface
- Affichage dynamique en haut de l’écran
- Le HUD se met à jour automatiquement via le `ResourceManagerComponent`

## 🧱 Architecture du code (classes clés)
| Système | Éléments principaux |
|---|---|
| Unités | `ARTSUnitBase`, `AWorkerUnit` |
| Ressource | `AResourceNode` |
| Récolte | `WorkerUnitStartHarvesting()` |
| Gestion ressources | `UResourceManagerComponent` |
| Stockage | `AResourceStorageBuilding` |
| Placement bâtiment | `AGhostBuildingActor`, `ABuildingBase` |
| UI placement | `UPlacementConfirmationWidget` |
| UI menu build | `UConstructionPanelWidget` |
| PlayerController RTS | `ARTSPlayerController` |
| PlayerState & ressources | `ARTSPlayerState` |

## ✅ À venir (Roadmap)
⏳ Gestion des upgrades de bâtiments  
⏳ Caserne + création d’unités de combat  
⏳ Pathfinding optimisé pour plusieurs Workers  
⏳ IA ennemie (simple)  

## 🔧 Dépendances
- **Unreal Engine 5.6+**
- Enhanced Input System
- UMG pour l'interface
- NavigationSystem pour la validation de placement

## 📦 Télécharger / Build
> Le mieux : mettre la build dans **GitHub Releases**.
- **Dernière build :** (ajoute ton lien de release ici)

## 🚀 Installation & Lancement

### Prérequis
- Windows 10 / 11 (64 bits)
- Carte graphique compatible DirectX 12
- Runtime Unreal Engine inclus dans la build

### Lancer le jeu
1. Télécharger la dernière build depuis les **Releases**
2. Extraire le fichier `.zip` où vous le souhaitez
3. Lancer `AgeOfEmpire.exe`
4. Profiter du jeu 🎮

⚠️ Ne pas déplacer ou supprimer les fichiers de la build.
L’exécutable doit rester dans sa structure d’origine.

## 🐞 Problèmes connus & Dépannage

- **Écran noir au lancement**
  - Vérifier que tous les fichiers sont bien extraits
  - Mettre à jour les pilotes graphiques

- **Baisse de FPS sur les grandes cartes**
  - Réduire la résolution
  - Fermer les applications en arrière-plan

- **Placement de bâtiment impossible**
  - Vérifier que le placement est sur le NavMesh
  - Vérifier les ressources disponibles

- **Le jeu ne se lance pas**
  - Essayer de lancer en tant qu’administrateur
  - Vérifier que Windows Defender n’a pas bloqué l’exécutable

---

## 📄 License
> Ajoute ton fichier `LICENSE` à la racine du repo (et éventuellement un `NOTICE` pour les assets tiers).
