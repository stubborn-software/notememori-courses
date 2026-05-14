```yaml
id: solfege-fr
title: Apprendre le solfège
description: Apprendre le solfège
userName: notememori
```

# Accueil

## Les bases du solfège

```yaml
lessonType: tutorial
gameType: find
lessonId: tuto-intro
```

### slide 1

#### Options

**Langue de l'application :**

```yaml @block
type: languageSelector
```

**Type de notation musicale :**

```yaml @block
type: notationSelector
```

**Thème d'affichage :**

```yaml @block
type: themeSelector
```

### slide 2

#### La portée

Ceci est une **portée**:

```yaml @block
type: musicScore
scoreExpression: "{G2}[]"
vfConfig:
  hideClefs: true
  hideConnectors: true
  stretchLastLine: true
  topMargin: -36
  bottomMargin: 10
```

Elle est composée de 5 lignes horizontales.

#### Les notes

On écrit les **notes de musique** sur les **lignes** et les **intervalles** de la portée.

```yaml @block
type: musicScore
scoreExpression: "{G2}[(G2:w:D/5)@G2:left:Sur une ligne][(G2:w:F/4)@G2:center:Sur un intervalle]"
vfConfig:
  hideClefs: true
  hideConnectors: true
  stretchLastLine: true
  topMargin: -16
  bottomMargin: 30
```

### slide 3

#### La hauteur

Les lignes et intervalles sont numérotées du bas vers le haut.

```yaml @block
type: image
src: /assets/line-intervals-numbers.svg
alt: Les lignes et intervalles de la portée numérotées
height: 85
width: 160
align: center
```

Plus une note est placée haute sur la portée, plus elle est aiguë.

```yaml @block
type: musicScore
scoreExpression: "{G2}[(G2:w:E/4)@G2:left:Plus grave][(G2:w:F/5)@G2:center:Plus aiguë]"
vfConfig:
  hideClefs: true
  hideConnectors: true
  stretchLastLine: true
  topMargin: -10
  bottomMargin: 40
```

#### Lignes supplémentaires

Les notes peuvent aussi déborder de la portée. On ajoute alors des **lignes supplémentaires**, comme ceci:

```yaml @block
type: musicScore
scoreExpression: "{G2}[(G2:w:D/4)(G2:w:C/4)(G2:w:B/3)(G2:w:A/3)][(G2:w:G/5)(G2:w:A/5)(G2:w:B/5)(G2:w:C/6)]"
vfConfig:
  hideClefs: true
  hideConnectors: true
  stretchLastLine: true
  topMargin: -10
  bottomMargin: 40
```

### slide 4

#### Les clés

C’est la **clé**, placée en début de portée, qui indique quelles notes seront lues.

La **clé de Sol** indique que la note sur la **deuxième ligne** est un **Sol**.

```yaml @block
type: musicScore
scoreExpression: "{G2*2*}[(G2:w:G/4)]"
vfConfig:
  hideConnectors: true
  stretchLastLine: true
  topMargin: -20
  bottomMargin: 30
```

La **clé de Fa** indique que la note sur la **quatrième ligne** est un **Fa**.

```yaml @block
type: musicScore
scoreExpression: "{F4*4*}[(F4:w:F/3)]"
vfConfig:
  hideConnectors: true
  stretchLastLine: true
  topMargin: -30
  bottomMargin: 20
```

# Les premiers points de repères

## Lire

```yaml
lessonType: tutorial
gameType: read
lessonId: tuto-game-read
```

### slide 1

#### Exercice de lecture

Bienvenue dans le premier type d'exercice: l'**exercice de lecture**.

Nous allons commencer avec **4 points de repères** et nous entraîner à les reconnaître.

```yaml @block
type: tutoLandmarks
```

```yaml @block
type: youtube
videoId: f1QgGXwtGk4
title: Lecture du Solfège
width: 560
height: 315
align: center
```

### slide 2

#### À vous de jouer !

```yaml @block
type: tutoGameConfig
gameType: read
completeTitle: Félicitations !
completeMessage: Vous avez terminé l'introduction à NoteMemori. De nouveaux niveaux et tutoriels sont maintenant débloqués. Bon entraînement !
scoreBuilders:
  - type: landmarks
    level: 1
  - type: highlight
```

## Repères 1

```yaml
lessonType: game
gameType: read
lessonId: ae28b497
```

Game description

```yaml @block
type: gameIntroConfig
previewNames: all
scoreBuilders:
  - type: landmarks
    level: 1
  - type: highlight
  - type: flatten
```

```yaml @block
type: gameConfig
limitInput: true
scoreBuilders:
  - type: landmarks
    level: 1
  - type: highlight
  - type: fillTicks
    amount: 30
  - type: shuffleTicks
  - type: splitMeasures
    notesByMeasure: 4
```

## Chercher

```yaml
lessonType: tutorial
gameType: find
lessonId: tuto-game-find
```

### slide 1

#### Exercice de recherche

Voici le deuxième type d'exercice: l'exercice de **Recherche**.

Le but est de vous entraîner à reconnaître les points de repères et autre patterns parmis d'autres notes aléatoires.

Il vous suffit de trouver les points de repères et de cliquer dessus, dans n'importe quel ordre, pour tous les révéler.

```yaml @block
type: tutoLandmarks
```

### slide 2

#### À vous de jouer !

```yaml @block
type: tutoGameConfig
gameType: find
completeTitle: Félicitations !
completeMessage: Vous avez terminé l'introduction à NoteMemori. De nouveaux niveaux et tutoriels sont maintenant débloqués. Bon entraînement !
scoreBuilders:
  - type: landmarks
    level: 1
  - type: highlight
  - type: ranges
    nbExtraNotes: 1
  - type: fillTicks
    amount: 7
  - type: splitMeasures
    notesByMeasure: 4
```

## Repères 1

```yaml
lessonType: game
gameType: find
lessonId: e238348d
```

Game description

```yaml @block
type: gameIntroConfig
previewNames: highlighted
scoreBuilders:
  - type: landmarks
    level: 1
  - type: highlight
  - type: ranges
    nbExtraNotes: 1
  - type: merge
```

```yaml @block
type: gameConfig
scoreBuilders:
  - type: landmarks
    level: 1
  - type: highlight
  - type: ranges
    nbExtraNotes: 1
  - type: fillTicks
    amount: 28
  - type: shuffleTicks
  - type: splitMeasures
    notesByMeasure: 4
```

## Réciter

```yaml
lessonType: tutorial
gameType: recite
lessonId: tuto-game-recite
```

## Gamme ascendante

```yaml
lessonType: game
gameType: recite
lessonId: 4fd0dab0
```

Game description

```yaml @block
type: gameIntroConfig
previewNames: all
scoreBuilders:
  - type: notes
    notes: C/4,D/4,E/4,F/4,G/4,A/4,B/4
```

```yaml @block
type: gameConfig
scoreBuilders:
  - type: notes
    notes: C/4,D/4,E/4,F/4,G/4,A/4,B/4
  - type: shuffleTicks
    keepFirst: true
  - type: scales
    step: 1
    direction: up
```

## Repères 1 + voisines ascendantes

```yaml
lessonType: game
gameType: read
lessonId: ba155670
```

Game description

```yaml @block
type: gameIntroConfig
previewNames: all
scoreBuilders:
  - type: landmarks
    level: 1
  - type: highlight
  - type: sequences
    direction: up
    step: 1
  - type: fillMeasures
    amount: 2
  - type: merge
```

```yaml @block
type: gameConfig
scoreBuilders:
  - type: landmarks
    level: 1
  - type: highlight
  - type: sequences
    direction: up
    step: 1
  - type: fillMeasures
    amount: 10
  - type: shuffleMeasures
limitInput: true
```

## Gamme descendante

```yaml
lessonType: game
gameType: recite
lessonId: 90ce9184
```

Game description

```yaml @block
type: gameIntroConfig
previewNames: all
scoreBuilders:
  - type: notes
    notes: C/5,B/4,A/4,G/4,F/4,E/4,D/4
```

```yaml @block
type: gameConfig
scoreBuilders:
  - type: notes
    notes: C/6,B/5,A/5,G/5,F/5,E/5,D/5
  - type: shuffleTicks
    keepFirst: true
  - type: scales
    step: 1
    direction: down
```

## Repères 1 + voisines descendantes

```yaml
lessonType: game
gameType: read
lessonId: 81717f6b
```

Game description

```yaml @block
type: gameIntroConfig
previewNames: all
scoreBuilders:
  - type: landmarks
    level: 1
  - type: highlight
  - type: sequences
    direction: down
    step: 1
  - type: fillMeasures
    amount: 2
  - type: merge
```

```yaml @block
type: gameConfig
scoreBuilders:
  - type: landmarks
    level: 1
  - type: highlight
  - type: sequences
    direction: down
    step: 1
  - type: fillMeasures
    amount: 10
  - type: shuffleMeasures
limitInput: true
```

## Repères 1 + voisines

```yaml
lessonType: game
gameType: read
lessonId: fb932641
```

Game description

```yaml @block
type: gameIntroConfig
previewNames: all
scoreBuilders:
  - type: landmarks
    level: 1
  - type: highlight
  - type: sequences
    direction: either
    step: 1
  - type: fillMeasures
    amount: 2
  - type: merge
```

```yaml @block
type: gameConfig
scoreBuilders:
  - type: landmarks
    level: 1
  - type: highlight
  - type: sequences
    direction: either
    step: 1
  - type: fillMeasures
    amount: 10
  - type: shuffleMeasures
limitInput: true
```

## Repères 1 + progressions de voisines

```yaml
lessonType: game
gameType: read
lessonId: 8846c318
```

Game description

```yaml @block
type: gameIntroConfig
previewNames: all
scoreBuilders:
  - type: landmarks
    level: 1
  - type: multiSequences
    step: 1
    maxNbNotes: 6
  - type: shuffleMeasures
  - type: fillMeasures
    amount: 2
  - type: merge
```

```yaml @block
type: gameConfig
scoreBuilders:
  - type: landmarks
    level: 1
  - type: multiSequences
    step: 1
    maxNbNotes: 6
  - type: fillMeasures
    amount: 10
  - type: shuffleMeasures
limitInput: true
```

# Nouveaux points de repères

## Les points de repères niveau 2

```yaml
lessonType: tutorial
gameType: find
lessonId: tuto-landmarks-2
```

## Repères 2

```yaml
lessonType: game
gameType: read
lessonId: 6e8bb5af
```

Game description

```yaml @block
type: gameIntroConfig
previewNames: all
scoreBuilders:
  - type: landmarks
    level: 2
  - type: highlight
  - type: fillTicks
    amount: 4
  - type: splitMeasures
    notesByMeasure: 4
```

```yaml @block
type: gameConfig
scoreBuilders:
  - type: landmarks
    level: 2
  - type: highlight
  - type: fillTicks
    amount: 40
  - type: shuffleTicks
  - type: splitMeasures
    notesByMeasure: 4
```

## Repères 2

```yaml
lessonType: game
gameType: find
lessonId: cd92cb53
```

Game description

```yaml @block
type: gameIntroConfig
previewNames: all
scoreBuilders:
  - type: landmarks
    level: 2
  - type: highlight
  - type: ranges
    nbExtraNotes: 1
  - type: merge
  - type: splitMeasures
    notesByMeasure: 4
```

```yaml @block
type: gameConfig
scoreBuilders:
  - type: landmarks
    level: 2
  - type: highlight
  - type: ranges
    nbExtraNotes: 1
  - type: fillTicks
    amount: 40
  - type: shuffleTicks
  - type: splitMeasures
    notesByMeasure: 4
```

## Repères 2 + voisines ascendantes

```yaml
lessonType: game
gameType: read
lessonId: a75d8951
```

Game description

```yaml @block
type: gameIntroConfig
previewNames: all
scoreBuilders:
  - type: landmarks
    level: 2
  - type: highlight
  - type: sequences
    direction: up
    step: 1
  - type: fillMeasures
    amount: 2
  - type: merge
```

```yaml @block
type: gameConfig
scoreBuilders:
  - type: landmarks
    level: 2
  - type: highlight
  - type: sequences
    direction: up
    step: 1
  - type: fillMeasures
    amount: 10
  - type: shuffleMeasures
```

## Repères 2 + voisines descendantes

```yaml
lessonType: game
gameType: read
lessonId: c69c4fd1
```

Game description

```yaml @block
type: gameIntroConfig
previewNames: all
scoreBuilders:
  - type: landmarks
    level: 2
  - type: highlight
  - type: sequences
    direction: down
    step: 1
  - type: fillMeasures
    amount: 2
  - type: merge
```

```yaml @block
type: gameConfig
scoreBuilders:
  - type: landmarks
    level: 2
  - type: highlight
  - type: sequences
    direction: down
    step: 1
  - type: fillMeasures
    amount: 10
  - type: shuffleMeasures
```

## Repères 2 + deux voisines

```yaml
lessonType: game
gameType: read
lessonId: 82a5e64d
```

Game description

```yaml @block
type: gameIntroConfig
previewNames: all
scoreBuilders:
  - type: landmarks
    level: 2
  - type: highlight
  - type: sequences
    direction: either
    step: 1
  - type: fillMeasures
    amount: 2
  - type: merge
```

```yaml @block
type: gameConfig
scoreBuilders:
  - type: landmarks
    level: 2
  - type: highlight
  - type: sequences
    direction: either
    step: 1
  - type: fillMeasures
    amount: 10
  - type: shuffleMeasures
```

## Repères 2 + progressions de voisines

```yaml
lessonType: game
gameType: read
lessonId: 66de8b32
```

Game description

```yaml @block
type: gameIntroConfig
previewNames: all
scoreBuilders:
  - type: landmarks
    level: 2
  - type: multiSequences
    step: 1
    maxNbNotes: 5
  - type: fillMeasures
    amount: 2
  - type: merge
```

```yaml @block
type: gameConfig
scoreBuilders:
  - type: landmarks
    level: 2
  - type: multiSequences
    step: 1
    maxNbNotes: 5
  - type: fillMeasures
    amount: 10
  - type: shuffleMeasures
```

# Les tierces

## Les Tierces

```yaml
lessonType: tutorial
gameType: find
lessonId: tuto-thirds
```

## Tierces ascendantes

```yaml
lessonType: game
gameType: recite
lessonId: cd5ae5f1
```

Game description

```yaml @block
type: gameIntroConfig
previewNames: all
scoreBuilders:
  - type: notes
    notes: C/4
  - type: scales
    step: 2
    direction: up
```

```yaml @block
type: gameConfig
scoreBuilders:
  - type: notes
    notes: C/4
  - type: scales
    step: 2
    direction: up
```

## Repères 2 + tierces ascendantes

```yaml
lessonType: game
gameType: read
lessonId: 5465fde4
```

Game description

```yaml @block
type: gameIntroConfig
previewNames: all
scoreBuilders:
  - type: landmarks
    level: 2
  - type: highlight
  - type: sequences
    direction: up
    step: 2
  - type: fillMeasures
    amount: 2
  - type: merge
```

```yaml @block
type: gameConfig
scoreBuilders:
  - type: landmarks
    level: 2
  - type: highlight
  - type: sequences
    direction: up
    step: 2
  - type: fillMeasures
    amount: 10
  - type: shuffleMeasures
```

## Tierces descendantes

```yaml
lessonType: game
gameType: recite
lessonId: f843d10a
```

Game description

```yaml @block
type: gameIntroConfig
previewNames: all
scoreBuilders:
  - type: notes
    notes: C/5
  - type: scales
    step: 2
    direction: down
```

```yaml @block
type: gameConfig
scoreBuilders:
  - type: notes
    notes: C/6
  - type: scales
    step: 2
    direction: down
```

## Repères 2 + tierces descendantes

```yaml
lessonType: game
gameType: read
lessonId: dfc48645
```

Game description

```yaml @block
type: gameIntroConfig
previewNames: all
scoreBuilders:
  - type: landmarks
    level: 2
  - type: highlight
  - type: sequences
    direction: down
    step: 2
  - type: fillMeasures
    amount: 2
  - type: merge
```

```yaml @block
type: gameConfig
scoreBuilders:
  - type: landmarks
    level: 2
  - type: highlight
  - type: sequences
    direction: down
    step: 2
  - type: fillMeasures
    amount: 10
  - type: shuffleMeasures
```

## Repères 2 + tierces

```yaml
lessonType: game
gameType: read
lessonId: abdedf0e
```

Game description

```yaml @block
type: gameIntroConfig
previewNames: all
scoreBuilders:
  - type: landmarks
    level: 2
  - type: highlight
  - type: sequences
    direction: either
    step: 2
  - type: fillMeasures
    amount: 2
  - type: merge
```

```yaml @block
type: gameConfig
scoreBuilders:
  - type: landmarks
    level: 2
  - type: highlight
  - type: sequences
    direction: either
    step: 2
  - type: fillMeasures
    amount: 10
  - type: shuffleMeasures
```

## Repères 2 + progressions de tierces

```yaml
lessonType: game
gameType: read
lessonId: c5a886f7
```

Game description

```yaml @block
type: gameIntroConfig
previewNames: all
scoreBuilders:
  - type: landmarks
    level: 2
  - type: multiSequences
    step: 2
    maxNbNotes: 5
  - type: fillMeasures
    amount: 2
  - type: merge
```

```yaml @block
type: gameConfig
scoreBuilders:
  - type: landmarks
    level: 2
  - type: multiSequences
    step: 2
    maxNbNotes: 5
  - type: fillMeasures
    amount: 10
  - type: shuffleMeasures
```
