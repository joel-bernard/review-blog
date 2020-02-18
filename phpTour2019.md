---
---layout: post
---title:  "PHP tour 2019"
---image: /img/posts/php-tour-2019/forumphp-2019.png
---author: Jojo
---date:   2019-10-24 09:00:00 +0200
---categories: event PHP-tour
---

# Le PHP tour 2019 de Paris c'est terminé !
Nous y étions et pour ceux qui n'ont pu assister aux diverses conférences, nous vous partageons notre compte rendu des talks auquels nous avons assistés.

## 1. PHP pragmatic develpment

> Pragmatisme : Qui favorise la pratique et l'expérience

### Pourquoi structure t'on notre code ?
Pincipalement parce qu'on code pour les autres (et accessoirement pour soit). 
Il est donc indispensable de faire du code compréhensible facilement et rapidement par les autres humains.

> Le code c'est comme une blague, si on doit l'expliquer c'est qu'elle est mauvaise.

### L'approche par le pragmatisme [YAGNI](https://www.martinfowler.com/bliki/Yagni.html)

Choisir la solution la plus adaptée à votre context :
Pour ce faire, il est possible de recourir à une matrice de décition.

Une des pratique que l'on entend souvent en programmation est  le DRY (Don't repeat yourself).
Depuis quelques temps, une autre pratique est remis à l'ordre du jour le WET (Write Everything Twice).  
Pour aller plus loin, un article disponible [ici](https://dev.to/wuz/stop-trying-to-be-so-dry-instead-write-everything-twice-wet-5g33).

Dans l'approche du pragmatisme, éviter d'aller trop vite dans la mise en place d'abstraction est une des clés. 

Pour conclure : **Rendre le code comprehensible par tous; des jumiors aux experts.**

Le respect de la [PSR 12](https://www.php-fig.org/psr/psr-12/) est indispensable pour avoir un code compréhensible par tous.

Retrouvez toutes les details sur le talk [ici](https://afup.org/talks/3087-php-pragmatic-development).

## 2. PHP 8, just in time compilation
Retrouvez toutes les details sur le talk [ici](https://afup.org/talks/3015-php-8-et-just-in-time-compilation).

## 3. Neuroatypie en IT : quelques conseils
Retrouvez toutes les details sur le talk [ici](https://afup.org/talks/3070-neuroatypie-et-it-quelques-conseils).

## 4. Agressive php quality assurance in 2019

> Présentation des différents outils du talk

### Outil pour l'aide à la prise de décision et le de la qualité du code :
- [ADR (Architecture Decision Record)](https://github.com/joelparkerhenderson/architecture_decision_record) 

### Outils pour la qualité du code :
- DEPTRAC
- phpstan
- phan 
- psalm

### Outils pour le testing :
- phpspec
- behat
- phpunit
- infection for mutation testing

### Outils pour la gestion de la qualité des dépendances d'un projet 
- roave-backwards-compatibility-check 
- roave/security-advisories
- maglnet/composer-requier-check
- maglnet/composer-unused

Retrouvez toutes les details sur le talk [ici](https://afup.org/talks/3181-aggressive-php-quality-assurance-in-2019).

## 5. Tout pour se préparer a PHP 7.4

> Liste des nouveautés abordées durant le talk

### les deprecated
- les ternaires imbriqués sans parenthèse (toujours autant déconseillé)
- exit les short tag 
- préséance + et . (obligation des parenthèses )
- accès aux tableaux avec des accolades
- accès aux tableaux aux scalaire
- plus d'entier (real) -> uniquement des float
- array_key_exists() ne fonctionnera plus sur les objets -> ajout du \ nampe

### Modernisation
- séparateur numérique
- propriétés typées
- spread pour les array
- arrow function (une seule instruction possible donc pas de return)
- contravariant / covariant
- ??=
- array_merge() accepte le null 
- références faibles
- strip_tags()
- proc_open()
- preg_unmached_as_null constante pour preg_match()
- nouvelle sérialisation
- preloading
- foreign function interface pour faire du c dans du php

> Tips : Nombre d'erreur que le code source de php est capatble de retourner : ~500

Retrouvez toutes les details sur le talk [ici](https://afup.org/talks/3120-tout-pour-se-preparer-a-php-7-4).

## 6. Architecture progressive
> Architecture progressive : Une **approche** plutôt qu'une solution.

### Les 3 aspects à prendre en compte dans l'architecture progressive :
1. **Métier** : Dans le context du métier, il y a différent niveau de compléxités et de criticités.Pour coder le métier, la compléxité technique doit être inférieur ou égale à la complexité métier.
2. **Business** : Le code légacy c'est une chose qu'on a été confronté. Mais il faut garder à l'esprit que si le légacy existe c'est aussi parce qu'un projet a réussi. 
    Courbe des différentes phases d'un projet : 
    <img src="/img/posts/php-tour-2019/graph-x3.png">
3. **Humain** : Les personnes sont des **Humains**. Les compétences sont différentes et tous différents.

### Découplage/découpage en bounded context (module)
**Comment identifier les bounded context ?**
 - metiers différents 
 - acteurs et usages différents

### Découpler les modules
**Comment découpler les bounded context ?**
 - Évenements (de préférence asynchrone avec un système de `queuing` (exemple: [aws sqs](https://docs.aws.amazon.com/fr_fr/AWSSimpleQueueService/latest/SQSDeveloperGuide/welcome.html))
 - Abstractions
 - Dependances unidirectionnelles 
 - Duplication de l'information dans les bounded context en fonction des besoins du modèle.
 - Duplication du modèle sans dupliquer l'information. Privilégier l'utilisation de DTO, vue mysql (si vous utilisez doctrine ce sera une entity read only)

> Dans l'architecture progressive la cohérence n'est pas une priorité.

**L'architecture devient progressive, evolutive et adaptative**

> Le talk a été fait par [Matthieu NAPOLI](https://twitter.com/matthieunapoli) le fondateur de [bref](https://bref.sh/).

Retrouvez toutes les details sur le talk [ici](https://afup.org/talks/3121-l-architecture-progressive).

## **On more thing**
Toutes les conférences du PHP tour 2019 sont disponibles [ici](https://afup.org/talks/?q=&hPP=7&idx=afup_talks&p=1&dFR%5Bhas_video%5D%5B0%5D=true&fR%5Bevent.title%5D%5B0%5D=Forum%20PHP%202019&is_v=1).