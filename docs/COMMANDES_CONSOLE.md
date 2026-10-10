# Référence des commandes et identifiants — Farmer's Dynasty 2

Version étudiée : **0.51.05 (22/09/2026)**. Source : chaînes extraites de `Farm2.exe` et observations de désassemblage précédentes.

> **Attention :** les 351 entrées sont des **candidats**, pas 351 commandes console vérifiées. Elles comprennent des variables, fonctions internes, mots de scripts et noms techniques. Aucune modification de l'EXE n'est nécessaire pour consulter cette documentation. Les descriptions non confirmées sont des hypothèses, et une entrée présente dans le binaire peut être inutilisable depuis la console.

## Convention de validation

- **Confirmé** : fonctionnement/syntaxe établi par analyse ou essai.
- **Identifié** : nom trouvé, effet déduit mais non testé.
- **À déterminer** : nature de l'entrée ou syntaxe inconnue.
- **Prudence** : effet potentiellement destructif.

## Syntaxes utiles connues

```text
AddPallet 1             # palette de bois, essence aléatoire
AddPallet 4             # briques
AddPallet 27            # peinture ; couleur non garantie
AddDryPallet 1          # palette de bois sèche
setcash 100000          # à tester sur une sauvegarde de test
```

`AddPallet` reçoit un ID de matériau ; la seconde valeur numérique sert à l'humidité pour le bois et **pas** à choisir l'essence. Pour l'ID 1, essences internes : 0 Pin, 1 Chêne, 2 Bouleau, 3 Épicéa, 4 Peuplier.

## Catalogue par catégorie

### Économie et inventaire

| Nom | Description | Statut |
|---|---|---|
| `cash` | Modifie l'argent ; paramètre numérique, effet exact à confirmer | Identifié |
| `setcash` | Définit une valeur d'argent ; entier lu par le gestionnaire | Identifié |
| `give` | Ajoute un objet d'après son identifiant interne | Identifié |
| `AddPallet` | Crée une palette à partir d'un ID de matériau ; bois ID 1 avec essence aléatoire | Confirmé |
| `AddDryPallet` | Crée une palette sèche ; bois ID 1 avec essence aléatoire | Confirmé |
| `AddPlanks` | Liée aux planches ; effet non confirmé | Identifié |
| `SetMillPlanks` | Modifie le stock de planches de scierie ; paramètre numérique | Identifié |
| `SawMillPlanks` | Commande apparentée au stock de planches de scierie | Identifié |
| `AddPaint` | Ajout de peinture ; paramètres à confirmer | Identifié |
| `GiveSeedlings` | Fonction liée à « GiveSeedlings » ; effet et paramètres à confirmer | À déterminer |
| `giveseedlings` | Fonction liée à « giveseedlings » ; effet et paramètres à confirmer | À déterminer |
| `AddMachines` | Fonction liée à « AddMachines » ; effet et paramètres à confirmer | À déterminer |
| `AddBale` | Fonction liée à « AddBale » ; effet et paramètres à confirmer | À déterminer |
| `AddKule` | Fonction liée à « AddKule » ; effet et paramètres à confirmer | À déterminer |
| `fill` | Fonction liée à « fill » ; effet et paramètres à confirmer | À déterminer |
| `fillsilo` | Fonction liée à « fillsilo » ; effet et paramètres à confirmer | À déterminer |

### Compétences, progression et quêtes

| Nom | Description | Statut |
|---|---|---|
| `ResetSkills` | Réinitialisation des compétences (effet à tester) | Identifié |
| `SkillsProgress` | Progression des compétences ; paramètres à identifier | Identifié |
| `UnlockPerk` | Débloque un avantage ; ID à identifier | Identifié |
| `LockPerk` | Verrouille un avantage ; ID à identifier | Identifié |
| `StartQuest` | Fonction liée à « StartQuest » ; effet et paramètres à confirmer | À déterminer |
| `CompleteQuest` | Fonction liée à « CompleteQuest » ; effet et paramètres à confirmer | À déterminer |
| `NextQuest` | Fonction liée à « NextQuest » ; effet et paramètres à confirmer | À déterminer |
| `DumpQuestList` | Fonction liée à « DumpQuestList » ; effet et paramètres à confirmer | À déterminer |
| `QuestRaport` | Fonction liée à « QuestRaport » ; effet et paramètres à confirmer | À déterminer |
| `AutoQuests` | Fonction liée à « AutoQuests » ; effet et paramètres à confirmer | À déterminer |
| `SetAchievement` | Fonction liée à « SetAchievement » ; effet et paramètres à confirmer | À déterminer |
| `UnlockAchievement` | Fonction liée à « UnlockAchievement » ; effet et paramètres à confirmer | À déterminer |
| `ClearAllAchievements` | Effacement des succès ; potentiellement destructif | Prudence |
| `UnlockFurniture` | Fonction liée à « UnlockFurniture » ; effet et paramètres à confirmer | À déterminer |
| `UnlockAllTractors` | Fonction liée à « UnlockAllTractors » ; effet et paramètres à confirmer | À déterminer |
| `UnlockSuperfoods` | Fonction liée à « UnlockSuperfoods » ; effet et paramètres à confirmer | À déterminer |
| `LockDLC` | Fonction liée à « LockDLC » ; effet et paramètres à confirmer | À déterminer |
| `UnlockDLC` | Fonction liée à « UnlockDLC » ; effet et paramètres à confirmer | À déterminer |

### Personnage et interactions

| Nom | Description | Statut |
|---|---|---|
| `Warm` | Besoin de chaleur du personnage | Identifié |
| `Food` | Besoin alimentaire du personnage | Identifié |
| `Stamina` | Endurance du personnage | Identifié |
| `Temperature` | Fonction liée à « Temperature » ; effet et paramètres à confirmer | À déterminer |
| `Humidity` | Fonction liée à « Humidity » ; effet et paramètres à confirmer | À déterminer |
| `warmth` | Fonction liée à « warmth » ; effet et paramètres à confirmer | À déterminer |
| `stamina` | Fonction liée à « stamina » ; effet et paramètres à confirmer | À déterminer |
| `temperature` | Fonction liée à « temperature » ; effet et paramètres à confirmer | À déterminer |
| `humidity` | Fonction liée à « humidity » ; effet et paramètres à confirmer | À déterminer |
| `DirtyHands` | Fonction liée à « DirtyHands » ; effet et paramètres à confirmer | À déterminer |
| `CurrentClothingDirty` | Fonction liée à « CurrentClothingDirty » ; effet et paramètres à confirmer | À déterminer |
| `SetClothing` | Fonction liée à « SetClothing » ; effet et paramètres à confirmer | À déterminer |
| `Clothing` | Fonction liée à « Clothing » ; effet et paramètres à confirmer | À déterminer |
| `PlayerModel` | Fonction liée à « PlayerModel » ; effet et paramètres à confirmer | À déterminer |
| `FastRun` | Fonction liée à « FastRun » ; effet et paramètres à confirmer | À déterminer |
| `Teleport` | Téléportation ; destination à préciser | Identifié |
| `teleport` | Téléportation ou variante de commande | Identifié |
| `TalkToNPC` | Fonction liée à « TalkToNPC » ; effet et paramètres à confirmer | À déterminer |
| `CanTalkToNPC` | Fonction liée à « CanTalkToNPC » ; effet et paramètres à confirmer | À déterminer |
| `Kid0Born` | Fonction liée à « Kid0Born » ; effet et paramètres à confirmer | À déterminer |
| `Kid1Born` | Fonction liée à « Kid1Born » ; effet et paramètres à confirmer | À déterminer |
| `Kid0Age` | Fonction liée à « Kid0Age » ; effet et paramètres à confirmer | À déterminer |
| `Kid1Age` | Fonction liée à « Kid1Age » ; effet et paramètres à confirmer | À déterminer |
| `SetGameEra` | Fonction liée à « SetGameEra » ; effet et paramètres à confirmer | À déterminer |
| `SetFinishedDate` | Fonction liée à « SetFinishedDate » ; effet et paramètres à confirmer | À déterminer |
| `BuyDuck` | Fonction liée à « BuyDuck » ; effet et paramètres à confirmer | À déterminer |
| `BuySheep` | Fonction liée à « BuySheep » ; effet et paramètres à confirmer | À déterminer |
| `BuyRooster` | Fonction liée à « BuyRooster » ; effet et paramètres à confirmer | À déterminer |

### Monde, agriculture et bâtiments

| Nom | Description | Statut |
|---|---|---|
| `AddVehicle` | Crée un véhicule | Identifié |
| `DeleteVehicle` | Supprime un véhicule | Identifié |
| `FixVehicle` | Répare un véhicule | Identifié |
| `FixBuilding` | Fonction liée à « FixBuilding » ; effet et paramètres à confirmer | À déterminer |
| `UpdateBuildings` | Mise à jour du sous-système Buildings | À déterminer |
| `CheckRebuilt` | Fonction liée à « CheckRebuilt » ; effet et paramètres à confirmer | À déterminer |
| `CheckRepaired` | Fonction liée à « CheckRepaired » ; effet et paramètres à confirmer | À déterminer |
| `AddPlantedTree` | Fonction liée à « AddPlantedTree » ; effet et paramètres à confirmer | À déterminer |
| `Cultivate` | Fonction liée à « Cultivate » ; effet et paramètres à confirmer | À déterminer |
| `Plow` | Fonction liée à « Plow » ; effet et paramètres à confirmer | À déterminer |
| `Plant` | Fonction liée à « Plant » ; effet et paramètres à confirmer | À déterminer |
| `Field` | Fonction liée à « Field » ; effet et paramètres à confirmer | À déterminer |
| `seed` | Fonction liée à « seed » ; effet et paramètres à confirmer | À déterminer |
| `AnimalFood` | Fonction liée à « AnimalFood » ; effet et paramètres à confirmer | À déterminer |
| `Fuel` | Fonction liée à « Fuel » ; effet et paramètres à confirmer | À déterminer |
| `fuel` | Fonction liée à « fuel » ; effet et paramètres à confirmer | À déterminer |
| `Time` | Fonction liée à « Time » ; effet et paramètres à confirmer | À déterminer |
| `Year` | Fonction liée à « Year » ; effet et paramètres à confirmer | À déterminer |
| `year` | Fonction liée à « year » ; effet et paramètres à confirmer | À déterminer |
| `LockTime` | Bloque le temps | Identifié |
| `AllowSleep` | Fonction liée à « AllowSleep » ; effet et paramètres à confirmer | À déterminer |
| `Weather` | Réglage de la météo | Identifié |
| `Snow` | Fonction liée à « Snow » ; effet et paramètres à confirmer | À déterminer |
| `Spring` | Fonction liée à « Spring » ; effet et paramètres à confirmer | À déterminer |
| `Summer` | Fonction liée à « Summer » ; effet et paramètres à confirmer | À déterminer |
| `Autumn` | Fonction liée à « Autumn » ; effet et paramètres à confirmer | À déterminer |
| `Winter` | Fonction liée à « Winter » ; effet et paramètres à confirmer | À déterminer |

### Affichage et diagnostic

| Nom | Description | Statut |
|---|---|---|
| `DrawHUD` | Affichage / visualisation de HUD | À déterminer |
| `DrawFPS` | Affiche les images par seconde | Identifié |
| `DrawWorld` | Affichage / visualisation de World | À déterminer |
| `DrawMainGame` | Affichage / visualisation de MainGame | À déterminer |
| `DrawSprites` | Affichage / visualisation de Sprites | À déterminer |
| `DrawModels` | Affichage / visualisation de Models | À déterminer |
| `DrawTerrain` | Affichage / visualisation de Terrain | À déterminer |
| `DrawZTerrain` | Affichage / visualisation de ZTerrain | À déterminer |
| `DrawTerrainNormals` | Affichage / visualisation de TerrainNormals | À déterminer |
| `DrawFields` | Affichage / visualisation de Fields | À déterminer |
| `DrawCrops` | Affichage / visualisation de Crops | À déterminer |
| `DrawGrass` | Affichage / visualisation de Grass | À déterminer |
| `DrawLights` | Affichage / visualisation de Lights | À déterminer |
| `DrawShadows` | Affichage / visualisation de Shadows | À déterminer |
| `DrawWater` | Affichage / visualisation de Water | À déterminer |
| `DrawSky` | Affichage / visualisation de Sky | À déterminer |
| `DrawDust` | Affichage / visualisation de Dust | À déterminer |
| `DrawBirds` | Affichage / visualisation de Birds | À déterminer |
| `DrawDetail` | Affichage / visualisation de Detail | À déterminer |
| `DrawPaths` | Affichage / visualisation de Paths | À déterminer |
| `DrawWorkerPaths` | Affichage / visualisation de WorkerPaths | À déterminer |
| `DrawCharacterPaths` | Affichage / visualisation de CharacterPaths | À déterminer |
| `DrawPhysics` | Affichage / visualisation de Physics | À déterminer |
| `DrawWires` | Affichage / visualisation de Wires | À déterminer |
| `DrawSkeletons` | Affichage / visualisation de Skeletons | À déterminer |
| `WireFrame` | Fonction liée à « WireFrame » ; effet et paramètres à confirmer | À déterminer |
| `DrawAlbedo` | Affichage / visualisation de Albedo | À déterminer |
| `DrawNormals` | Affichage / visualisation de Normals | À déterminer |
| `DrawGlossiness` | Affichage / visualisation de Glossiness | À déterminer |
| `DrawSSS` | Affichage / visualisation de SSS | À déterminer |
| `DrawMultitextures` | Affichage / visualisation de Multitextures | À déterminer |
| `DrawProjectors` | Affichage / visualisation de Projectors | À déterminer |
| `DrawCameraCoordinates` | Affichage / visualisation de CameraCoordinates | À déterminer |
| `DrawMinusLights` | Affichage / visualisation de MinusLights | À déterminer |
| `DrawLinearLights` | Affichage / visualisation de LinearLights | À déterminer |
| `DrawCompass` | Affichage / visualisation de Compass | À déterminer |
| `DrawMachineNames` | Affichage / visualisation de MachineNames | À déterminer |
| `ListObjects` | Liste ou inspecte des objets ; format à vérifier | Identifié |
| `DebugMeshes` | Débogage : Meshes | À déterminer |
| `DebugBuildings` | Débogage : Buildings | À déterminer |
| `DebugCharacters` | Débogage : Characters | À déterminer |
| `DebugTraffic` | Débogage : Traffic | À déterminer |
| `DebugLights` | Débogage : Lights | À déterminer |
| `DebugVM` | Débogage : VM | À déterminer |
| `DebugWarzones` | Débogage : Warzones | À déterminer |
| `DebugHeroLights` | Débogage : HeroLights | À déterminer |
| `DebugPerformance` | Débogage : Performance | À déterminer |
| `Profiler` | Fonction liée à « Profiler » ; effet et paramètres à confirmer | À déterminer |
| `DumpPhysics` | Fonction liée à « DumpPhysics » ; effet et paramètres à confirmer | À déterminer |
| `PrintPolygonCount` | Fonction liée à « PrintPolygonCount » ; effet et paramètres à confirmer | À déterminer |

### Moteur, rendu et environnement

| Nom | Description | Statut |
|---|---|---|
| `AOEnable` | Fonction liée à « AOEnable » ; effet et paramètres à confirmer | À déterminer |
| `AOPower` | Fonction liée à « AOPower » ; effet et paramètres à confirmer | À déterminer |
| `HDREnable` | Fonction liée à « HDREnable » ; effet et paramètres à confirmer | À déterminer |
| `EnableAntialiasing` | Fonction liée à « EnableAntialiasing » ; effet et paramètres à confirmer | À déterminer |
| `CinematicFilter` | Fonction liée à « CinematicFilter » ; effet et paramètres à confirmer | À déterminer |
| `Desaturacja` | Fonction liée à « Desaturacja » ; effet et paramètres à confirmer | À déterminer |
| `desaturate` | Fonction liée à « desaturate » ; effet et paramètres à confirmer | À déterminer |
| `FogNear` | Fonction liée à « FogNear » ; effet et paramètres à confirmer | À déterminer |
| `FogDist` | Fonction liée à « FogDist » ; effet et paramètres à confirmer | À déterminer |
| `FogCone` | Fonction liée à « FogCone » ; effet et paramètres à confirmer | À déterminer |
| `VFogMul` | Fonction liée à « VFogMul » ; effet et paramètres à confirmer | À déterminer |
| `VFogPower` | Fonction liée à « VFogPower » ; effet et paramètres à confirmer | À déterminer |
| `VFogHeight` | Fonction liée à « VFogHeight » ; effet et paramètres à confirmer | À déterminer |
| `VFogMax` | Fonction liée à « VFogMax » ; effet et paramètres à confirmer | À déterminer |
| `VFogGroundCurve` | Fonction liée à « VFogGroundCurve » ; effet et paramètres à confirmer | À déterminer |
| `SkyLightMul` | Fonction liée à « SkyLightMul » ; effet et paramètres à confirmer | À déterminer |
| `SkyLightPower` | Fonction liée à « SkyLightPower » ; effet et paramètres à confirmer | À déterminer |
| `SkyLightR` | Fonction liée à « SkyLightR » ; effet et paramètres à confirmer | À déterminer |
| `SkyLightG` | Fonction liée à « SkyLightG » ; effet et paramètres à confirmer | À déterminer |
| `SkyLightB` | Fonction liée à « SkyLightB » ; effet et paramètres à confirmer | À déterminer |
| `SunFlareMul` | Fonction liée à « SunFlareMul » ; effet et paramètres à confirmer | À déterminer |
| `SunFlareWeight` | Fonction liée à « SunFlareWeight » ; effet et paramètres à confirmer | À déterminer |
| `SunFlareDensity` | Fonction liée à « SunFlareDensity » ; effet et paramètres à confirmer | À déterminer |
| `SunFlareDecay` | Fonction liée à « SunFlareDecay » ; effet et paramètres à confirmer | À déterminer |
| `SunFlareNumSamples` | Fonction liée à « SunFlareNumSamples » ; effet et paramètres à confirmer | À déterminer |
| `SunFlareNumSamples` | Fonction liée à « SunFlareNumSamples » ; effet et paramètres à confirmer | À déterminer |
| `RecalculateCamera` | Fonction liée à « RecalculateCamera » ; effet et paramètres à confirmer | À déterminer |
| `RecalculateSkyShadow` | Fonction liée à « RecalculateSkyShadow » ; effet et paramètres à confirmer | À déterminer |
| `UpdatePhysics` | Mise à jour du sous-système Physics | À déterminer |
| `UpdateEngine` | Mise à jour du sous-système Engine | À déterminer |
| `UpdateTraffic` | Mise à jour du sous-système Traffic | À déterminer |
| `UpdateFields` | Mise à jour du sous-système Fields | À déterminer |
| `UpdateGrass` | Mise à jour du sous-système Grass | À déterminer |
| `UpdateMainGame` | Mise à jour du sous-système MainGame | À déterminer |
| `UpdateStepSimulation` | Mise à jour du sous-système StepSimulation | À déterminer |
| `UpdateObjects` | Mise à jour du sous-système Objects | À déterminer |
| `UpdateObjectsLinked` | Mise à jour du sous-système ObjectsLinked | À déterminer |
| `UpdateObjectsLoop` | Mise à jour du sous-système ObjectsLoop | À déterminer |
| `SectorHide` | Fonction liée à « SectorHide » ; effet et paramètres à confirmer | À déterminer |
| `SectorShow` | Fonction liée à « SectorShow » ; effet et paramètres à confirmer | À déterminer |
| `SectorShowAll` | Fonction liée à « SectorShowAll » ; effet et paramètres à confirmer | À déterminer |
| `DeleteDead` | Suppression d'entités mortes ; effet précis non vérifié | Prudence |
| `DeleteNotImportant` | Suppression d'entités jugées non importantes ; potentiellement destructif | Prudence |
| `WipeOut` | Potentiellement destructif ; NE PAS TESTER sans analyse | Prudence |

### Console et rapports

| Nom | Description | Statut |
|---|---|---|
| `exec` | Fonction liée à « exec » ; effet et paramètres à confirmer | À déterminer |
| `print` | Fonction liée à « print » ; effet et paramètres à confirmer | À déterminer |
| `quit` | Fonction liée à « quit » ; effet et paramètres à confirmer | À déterminer |
| `list` | Fonction liée à « list » ; effet et paramètres à confirmer | À déterminer |
| `goto` | Fonction liée à « goto » ; effet et paramètres à confirmer | À déterminer |
| `runworld` | Fonction liée à « runworld » ; effet et paramètres à confirmer | À déterminer |
| `RaportVariables` | Fonction liée à « RaportVariables » ; effet et paramètres à confirmer | À déterminer |
| `RaportUndefinedTextures` | Fonction liée à « RaportUndefinedTextures » ; effet et paramètres à confirmer | À déterminer |
| `RaportDoubleTextures` | Fonction liée à « RaportDoubleTextures » ; effet et paramètres à confirmer | À déterminer |
| `raportsubsets` | Fonction liée à « raportsubsets » ; effet et paramètres à confirmer | À déterminer |
| `extractusedtextures` | Fonction liée à « extractusedtextures » ; effet et paramètres à confirmer | À déterminer |

### Autres chaînes candidates — classification à poursuivre

Ces identifiants ont été trouvés dans le même ensemble de chaînes, mais ne doivent **pas** être présentés comme des commandes utilisables sans preuve supplémentaire.

| Identifiant | Description | Statut |
|---|---|---|
| `Chapter` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `Sprite` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `Debug` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `DebugMeshMgr` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `SetColor` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `UseAnimationCurve` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `ReloadDialogs` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `WaitBetweenFrames` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `Condition` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `AllowWirebrush` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `DrawGlobalAlbedo` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `Chainsaw` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `FALSE` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `TestDig` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `range` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `BigTextures` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `SkinmeshesFromFiles` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `MeshesFromFiles` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `TexturesFromFiles` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `label` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `actor` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `Upgrade` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `GrassLoDDistanceCoef` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `WorkerU` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `LightOnFeet` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `AmbientPow` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `ScaffoldDistance` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `trade` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `Farmer` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `Dirt` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `MaxUpgrade` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `WorkerR` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `WorkerF` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `EventCollect` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `ForceHit` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `SkyDesaturate` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `TABMenuAlt` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `CineLinearWhite` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `DrawInstances` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `RenderEnvProbe` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `DrawSubset` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `InstanceSwitchLimit` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `DrawBlooms` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `PoryUpdate` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `TestWywalania` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `MSmoothness` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `MSensitivity` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `PoraTexture` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `PorySave` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `Pora` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `black` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `UpdateOM` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `DeleteWindows` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `Disable` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `DrawTextures` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `Demo` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `RecalculateOccluders` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `SkinmeshLightCoef` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `GameFX` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `unset` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `BezierCamera` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `UpdateTerrain` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `FarZ` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `PrintShakeScreenDistance` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `AT824` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `coffee` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `DrawStickMarkers` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `WideScreen` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `UpdateModels` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `RecalculateSkyLightEveryFrame` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `DrawSkylightLitObjects` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `DrawAmbientLitObjects` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `LoadOneLevelTextureOnly` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `CutScene` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `AT680` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `weight` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `UpdatePMgr` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `UpdateBezier` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `LightPowerMultiplier` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `SkinMeshSpeed` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `Anim` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `repair` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `UpdateFX` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `AT677` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `shovel` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `UseSkyLight` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `Mood` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `NumApprovedLights` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `Invisible` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `GlobalTimeSpeed` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `CorpseDisappearTime` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `DrawOpaque` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `EnhanceTrees` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `DrawTranslucent` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `Like` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `StartMenu` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `SystemDebug` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `FlySpeed` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `VersionFor` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `AT676` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `AA229` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `DropDebug` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `AA228` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `gameFX` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `Cutscene` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `RadioVolume` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `AlphaT` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `Crouch` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `action` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `poglos` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `if_not` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `UpdateWysokosci` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `if_set` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `grass` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `winter` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `Fireplace` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `if_hit` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `chapter` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `condition` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `ifdead` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `rocket` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `COLOR` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `Repair` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `source` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `prefab` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `advance` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `OldSave` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `PSPod` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `VSPod` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `credits` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `WifePajamas` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `PSNad` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `EventRebuild` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `rebuild_brick` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `furniture` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `VSNad` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `MultiServerOnLevelStart` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `grass_density` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `PTransX` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `PScaleZ` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `PScaleY` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `PScaleX` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `PTransZ` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `PTransY` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `CduLncd` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `dirt` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `PGrPS` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `GTPST` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `PoraTimeMultiplier` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `RepairMultiData` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `MCashS` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `ForceArd` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `BPS_I` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `BVS_I` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `PSRed` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `Water` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `AutoLoadGame` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |
| `loadmodels` | Chaîne du binaire ; rôle ou accessibilité console non établi | À déterminer |

## Suivi des découvertes

À chaque nouvelle commande validée : mettre à jour sa description, sa syntaxe exacte, ses arguments, son statut et si possible le comportement observé. Ne pas supprimer les entrées incertaines sans preuve. Documenter les risques des commandes destructives.

## Historique

- 2026-10-10 : création du catalogue initial, 351 chaînes candidates, à partir de l'inventaire extrait de l'EXE. Aucun fichier du jeu modifié.
