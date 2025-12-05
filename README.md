# Lab : Comparaison JSON, XML et Protobuf

Ce laboratoire démontre les différences entre les formats de sérialisation JSON, XML et Protobuf en termes de taille de fichiers et de performances d'encodage/décodage.

## Objectifs pédagogiques

À la fin du lab, vous serez capable de :
- Créer un projet Node.js minimal pour des tests de sérialisation
- Utiliser JSON.stringify pour générer un fichier JSON
- Utiliser xml-js pour créer un fichier XML à partir d'un objet JavaScript
- Définir un schéma Protobuf dans un fichier .proto
- Utiliser protobufjs pour encoder des données en binaire Protobuf
- Comparer la taille de fichiers JSON, XML et Protobuf
- Comparer les temps d'encodage et de décodage

## Prérequis

- Node.js installé (v14+ recommandé)
- Connaissances de base en JavaScript côté serveur (Node)
- Notion d'objet JSON

## Installation

1. Installer les dépendances :
```bash
npm install
```

## Exécution

Lancer le script :
```bash
npm start
```

ou

```bash
node index.js
```

## Résultats attendus

Le script génère trois fichiers :
- `data.json` : Format JSON
- `data.xml` : Format XML
- `data.proto` : Format Protobuf (binaire)

Le script affiche également :
- Les temps d'encodage pour chaque format
- Les temps de décodage pour chaque format
- Les tailles de fichiers en octets

## Structure du projet

```
json-xml-protobuf-lab/
├── package.json          # Configuration npm
├── employee.proto        # Schéma Protobuf
├── index.js              # Script principal
├── README.md             # Ce fichier
├── data.json             # Généré après exécution
├── data.xml              # Généré après exécution
└── data.proto            # Généré après exécution
```

## Extensions possibles

Pour aller plus loin :
- Ajouter plus de champs dans Employee (email, date d'embauche, etc.) et observer l'effet sur les tailles
- Changer les options de JSON.stringify (ajout d'indentation) et mesurer l'impact
- Lire data.proto et le décoder à nouveau en objet JavaScript pour vérifier la symétrie encodage/décodage
- Intégrer ce mécanisme dans un projet gRPC pour voir la continuité entre sérialisation et communication réseau

