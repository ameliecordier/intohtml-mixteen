.. include:: commondefs.rst.inc

====================
Premiers pas en HTML
====================

HTML signifie `HyperText Markup Language`:eng:\. C'est donc un langage à **balises** !

.. index:: HTML, balise


Élements de base du HTML
========================

La balise
---------

Les balises permettent d'encadrer des parties de documents pour les mettre en forme.

Par exemple, la balise :html:`<strong>` permet de mettre un mot en évidence dans une phrase.

Exemple de code HTML :

.. code-block:: html

   Dans la phrase suivante, je vais mettre le mot <strong>surprise</strong> en évidence. 

Résultat obtenu :

.. raw:: html

   <section class="rendered">
     Dans la phrase suivante, je vais mettre le mot <strong>surprise</strong> en évidence. 
   </section>


Balise ouvrante, balise fermante
--------------------------------

La plupart du temps, les balises fonctionnent par paires : une balise ouvrante pour marquer le début de l'encadrement, et une balise fermante pour marquer la fin.

Les balises sont toujours construites de la même façon : chevron ouvrant, nom de la balise, chevron fermant.

Pour les balises fermantes, on met un "/" avant le nom de la balise.

Certaines balises n'ont pas besoin d'être fermées... mais nous verrons cela plus tard.

  .. todo faire un schéma

.. index:: balise

Organisation d'une page web
---------------------------

Toutes les pages web sont strucutrées de la même façon :

* L'entête du document (:html:`<head>`), dans laquelle on met des informations utiles, mais qui seront invisibles dans le navigateur,

* Le corps du document (:html:`<body>`), dans lequel on mettra le contenu de la page web. 

  .. todo faire le schéma d'une page web 

.. index:: body, head

Exercice : votre toute première page web !
``````````````````````````````````````````

#. Créez un fichier nommé ``page.html``.

#. Recopiez le code suivant dans le fichier.

#. Sauvegardez votre fichier. 

#. Ouvrez le fichier avec un navigateur web (Firefox, Chrome, etc.)

.. code-block:: html

   <!DOCTYPE html>
   <html>
    <head>
      <title>Ma première page web</title>
      <meta charset="UTF-8">
    </head>
    <body>
      Yes! J'ai fait ma première page web ! 
    </body>
   </html>

.. warning:: Veillez bien à sauvegarder votre fichier au format ``html`` et non au format ``txt``. 


Structure minimale d'une page, ligne par ligne
----------------------------------------------

* :html:`<!DOCTYPE html>` : renseigne le navigateur sur la version du langage HTML utilisé. 
* :html:`<html>` : début du document.
* :html:`<head>` : début de l'entête du document.
* :html:`<title>` : titre du document (recherchez où il apparaît !).
* :html:`<meta charset="UTF-8">` : encodage du document. 
* :html:`<body>` : début du corps du document (partie visible).

.. index:: meta, title, charset, encodage

   
Quelques balises
----------------

Il est temps de découvrir quelques balises qui vont vous permettre d'organiser votre page web.

============================  ======================
 :html:`<h1>` à :html:`<h6>`  niveaux de titres 
 :html:`<em>`                 emphase faible
 :html:`<strong>`             emphase forte         
 :html:`<p>`                  paragraphe
 :html:`<ol>`                 liste ordonnée
 :html:`<ul>`                 liste non-ordonnée
 :html:`<li>`                 item d'une liste
============================  ======================    

.. index:: h1, h2, h3, h4, h5, h6, em, strong, p, ol, ul, li 

Le fonctionnement des listes
----------------------------

Exemple de code HTML :

.. code-block:: html

   <ul>
     <li>Pain</li>
     <li>Beurre</li>
     <li>Sucre</li>
   </ul>

   <ol>
     <li>Manger</li>
     <li>Boire</li>
   </ol>
                
Résultat obtenu :

.. raw:: html

   <section class="rendered">
   <ul>
     <li>Pain</li>
     <li>Beurre</li>
     <li>Sucre</li>
   </ul>

   <ol>
     <li>Manger</li>
     <li>Boire</li>
   </ol>

   </section>


Exercice : utiliser des balises
```````````````````````````````

#. Téléchargez le fichier minimal disponible ici__ (cliquez avec le bouton droit, puis "enregister sous" ou "enregistrer la cible du lien sous).

#. Sauvegargez-le dans le même répertoire que votre premier exercice. Attention à bien enregistrer au format ``html``. 

#. Utilisez les balises que vous venez de découvrir pour enrichir le texte et obtenir un résultat qui ressemble à l'image ci-dessous.

.. figure:: _static/exercice-raw.png
    :width: 200px
    :align: center
    :alt: Résultat attendu
    :figclass: align-center

__ _static/exercices/exercicesBalises.html


Ajoutons des images
-------------------

Voici une nouvelle balise : :html:`<img>`.

Cette balise permet d'inclure des images dans vos pages web.

Le code suivant permet d'inclure l'image nommée ``html5.png``, située dans le répertoire ``images`` dans votre page web.

.. code-block:: html

   <img src="images/html5.png" alt="Logo HTML 5">


Les éléments ``src`` et ``alt`` sont appelés des *attributs*. Les attributs permettent de préciser le comportement d'une balise. Ici, ``src`` (pour *source*) indique où trouver l'image, et ``alt`` (pour *alternative*) indique quel texte alternatif doit s'afficher en cas d'impossibilité d'affichage de l'image. 

.. index:: img, attribut


Exercice : utiliser des balises
```````````````````````````````

#. Créez un répertoire ``images`` au même endroit que vos pages web.

#. Récupérez les trois images suivantes et enregistez-les dans le répertoire images :
    - html5.png__
    - css3.png__
    - w3c.png__

#. Utilisez la nouvelle balise que vous venez de découvrir pour inclure ces trois images au bons endroits dans votre page web. Vous devriez voir le résultat suivant.

.. figure:: _static/exercice-raw-with-image.png
    :width: 200px
    :align: center
    :alt: Résultat attendu
    :figclass: align-center
      
__ _static/html5.png
__ _static/css3.png
__ _static/w3c.png



Ajoutons des liens
------------------

Encore une nouvelle balise !

Pour faire des liens entre les pages, on utilise la balise :html:`<a>`.

Par exemple, le code suivant permet de faire le lien vers le fichier nommé ``page2.html`` qui se trouve dans le même répertoire que le fichier courant :

.. code-block:: html

   <a href="page2.html">Lien vers une autre page</a>

.. index:: a, lien 

   
Exercice : ajouter des liens dans la page
````````````````````````````````````````` 

À vous de jouer : essayez de créer des liens pour pouvoir naviguer entre les deux pages que vous venez de réaliser. 

Quand vous aurez fini, vous pourrez passer à la section suivante !

