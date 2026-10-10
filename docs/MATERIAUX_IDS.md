# Matériaux et identifiants — Farmer's Dynasty 2

Source : [`scripts/material_defs.txt`](../scripts/material_defs.txt), lu sur la branche `main` le 10 octobre 2026.

**20 matériaux déclarés** (ID `-1` exclu : configuration de réparation). **14** possèdent un prefab `source` pour une palette ; **6** n'en possèdent pas. Les IDs sans prefab ne sont **pas** des palettes garanties pour `AddPallet`.

## Commande console

```text
AddPallet <ID>
```

Exemples : `AddPallet 1` (bois neuf), `AddPallet 4` (briques neuves), `AddPallet 27` (peinture). `AddDryPallet <ID>` utilise également un ID de matériau. Pour le bois, une deuxième valeur numérique de `AddPallet` concerne l'humidité, **pas** l'essence.

## Liste complète

| ID | Matériau | Palette définie (`source`) | Prix déclaré | Choix de couleur |
|---:|---|---|---:|---|
| `0` | Vieux bois | Non | — | Non |
| `1` | Bois neuf | Oui | 10 | Non |
| `3` | Vieilles briques | Non | — | Non |
| `4` | Briques neuves | Oui | 220 | Non |
| `5` | Vieux plâtre | Non | — | Non |
| `6` | Plâtre neuf | Oui | 470 | Oui (`color_picker`) |
| `10` | Papier peint | Oui | 70 | Non |
| `12` | Vieux verre | Non | — | Non |
| `13` | Bitume de toiture | Oui | 200 | Non |
| `14` | Toiture — bardeaux rouges | Oui | 200 | Non |
| `15` | Toiture — tôle verte | Oui | 200 | Non |
| `16` | Toiture — tuiles céramiques rouges | Oui | 200 | Non |
| `17` | Toiture — tôle galvanisée | Oui | 200 | Non |
| `18` | Vieux métal | Non | — | Non |
| `19` | Métal neuf | Oui | 240 | Non |
| `21` | Ancien carrelage céramique | Non | — | Non |
| `23` | Parquet | Oui | 120 | Non |
| `27` | Peinture | Oui | 20 | Oui (`color_picker`) |
| `28` | Toiture solaire | Oui | 300 | Non |
| `29` | Verre neuf | Oui | 200 | Non |

## Prefabs et objets associés

| ID | Prefab `source` | Objet `item` |
|---:|---|---|
| `0` | — | — |
| `1` | `prefabs\buildings\buildings_materials\pallet_wood_new_nocenter.x` | `rebuild_wood` |
| `3` | — | — |
| `4` | `prefabs\buildings\buildings_materials\pallet_brick_new_nocenter.x` | `rebuild_brick` |
| `5` | — | — |
| `6` | `prefabs\buildings\buildings_materials\pallet_plaster_new_nocenter.x` | `rebuild_plaster` |
| `10` | `prefabs\buildings\buildings_materials\pallet_wallpaper2_new_nocenter.x` | `rebuild_wallpaper2` |
| `12` | — | — |
| `13` | `prefabs\buildings\buildings_materials\pallet_bitumen_new_nocenter.x` | `rebuild_bitumen` |
| `14` | `prefabs\buildings\buildings_materials\pallet_roof_1_new_nocenter.x` | `rebuild_roof_1` |
| `15` | `prefabs\buildings\buildings_materials\pallet_roof_2_new_nocenter.x` | `rebuild_roof_2` |
| `16` | `prefabs\buildings\buildings_materials\pallet_roof_3_new_nocenter.x` | `rebuild_roof_3` |
| `17` | `prefabs\buildings\buildings_materials\pallet_roof_4_new_nocenter.x` | `rebuild_roof_4` |
| `18` | — | — |
| `19` | `prefabs\buildings\buildings_materials\pallet_metal_new_nocenter.x` | `rebuild_metal` |
| `21` | — | — |
| `23` | `prefabs\buildings\buildings_materials\pallet_parquet1_nocenter.x` | `rebuild_parquet1` |
| `27` | `prefabs\buildings\buildings_materials\pallet_paint_new_nocenter.x` | `rebuild_paint` |
| `28` | `prefabs\buildings\buildings_materials\pallet_solar_new_nocenter.x` | `rebuild_solar` |
| `29` | `prefabs\buildings\buildings_materials\pallet_glass_new_nocenter.x` | `rebuild_glass` |

## Remarques et vérifications

- Les IDs `0`, `3`, `5`, `12`, `18` et `21` sont des matériaux anciens, sans `source` de palette dans ce fichier.
- `6` (plâtre) et `27` (peinture) disposent de `color_picker` : le choix de couleur existe dans les définitions, **mais** la commande `AddPallet` ne permet pas, à ce stade, de choisir une couleur par un paramètre vérifié.
- `1` (bois neuf) ne correspond pas à une essence précise : l'essence de bois d'une palette créée par la console est aléatoire selon l'analyse précédente.
- Le prix indiqué provient de `price` dans le fichier de définition ; ce n'est **pas** un prix de revente confirmé.
- La présence d'un prefab ne garantit pas à elle seule le bon fonctionnement de la palette en jeu.

## Historique

- 2026-10-10 : première extraction des 20 matériaux, IDs, prefabs, prix et options de couleur.
