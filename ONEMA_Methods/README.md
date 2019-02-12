# Metabarcoding : projet ONEMA-methods

* Rédacteurs: Emilie Chancerel, Alain Franc, Jean-Marc Frigerio
* Contributeurs: Agnès Bouchez, Maria Kahlert, Franck Salin
* contact: alain.franc@inra.fr 
* page crée le 12 février 2019  


Cette section contient les données produites dans le cadre du projet ONEMA-méthodes soutenu par l'ONEMA, puis l'AFB (2017-2018). Les fichiers suivants sont disponibles pour téléchargement :  
* le rapport technique produit à l'issue du projet (attente de l'autorisation de l'AFB pour le rendre public sur ce site)
* un bref tutoriel qui parcourt l'ensemble des étapes pour mener à bien un projet de metabarcoding, de la phase d'extraction de l'ADN à la phase de traitement des données
* les fichiers de résultats produits lors de ce projet


## Tutoriel

Le tutoriel est téléchargeable, et est en format pdf (``Tutoriel_pour_le_metabarcoding_v1.pdf``)

## Rapport technique

Le rapport technique est téléchargeable, et est en format pdf (``xxxx.pdf``)

### Résumé


L’estimation en routine de la qualité des eaux douces (rivières, lacs) s’effectue selon un protocole bien défini qui passe par la construction d’un inventaire des communautés de diatomées benthiques 
(biofilms sur les rochers submergés). Cet inventaire sert ensuite à la construction d’un indice de qualité des eaux, selon une formule de moyenne pondérée de la valeur indicatrice de chacune des 
espèces présentes. Un goulot d’étranglement de cette méthode en termes de temps de travail et d’expertise est  l’identification des espèces de diatomées présentes par microscopie optique. 
Une alternative a été proposée sous le nom de métabarcoding, où les inventaires sont réalisés avec des outils de bio-informatique sur des jeux de séquences ADN de régions amplifiées reconnues 
comme d’intérêt taxonomique (bonne résolution notamment). Ces méthodes sont assez récentes, et comportent une partie dite ici « technologique » qui consiste à extraire l’ADN, amplifier la région 
d’intérêt, et envoyer les produits de cette amplification dans un séquenceur. Il existe plusieurs protocoles à chacune de ces étapes et ces protocoles évoluent assez rapidement. Dans cette étude, 
nous évaluons l’influence du choix de deux protocoles de construction de librairies et d’une étape de bio-informatique (dite de contigage des séquences produites) sur la composition des inventaires.    


Pour cela, nous avons étudié 47 échantillons environnementaux, avec cinq constructions d’inventaires : une par la technique de séquençage PGM, et quatre par la technique de séquençage MiSeq. Pour 
le séquençage MiSeq, nous avons comparé (et croisé) deux méthodes de construction des librairies et testé l’effet d’un contigage (assemblage des segments dits forward et reverse issus du 
séquençage) avec ou sans filtre de qualité. Pour une profondeur de séquençage quasi équivalente entre les deux méthodes de construction de librairies testées, nous montrons que la méthode 
utilisée a une influence forte sur le nombre de séquences affecté à une espèce de la base de référence, avec des chiffres qui vont souvent du simple au double, voire au triple, pour les espèces 
dominantes. Nous montrons que souvent, une espèce peut être reconnue avec une des méthodes, mais pas avec une autre. Nous montrons que, en revanche, l’application ou non d’un filtre de qualité 
dans le contigage a peu d’effet sur les inventaires produits. Enfin, nous montrons que ces distorsions sont estompées quand on compare non pas les fréquences absolues des reads affectés à telle 
ou telle espèce, mais les fréquences relatives au sein de l’ensemble des reads affectés à au moins une espèce.   


Dans la mesure où des différences importantes dans les inventaires découlent du choix de la méthode de préparation de librairies et de la technologie de séquençage utilisée, nous suggérons qu’en 
l’état actuel des connaissances, il peut être prématuré de s’engager vers une normalisation des protocoles de biologie moléculaire, et qu’il faut encourager le développement d’études à caractère 
plus méthodologique, en amont, pour mieux comprendre les déterminants de la qualité des inventaires produits. 



## Fichiers de résultats et graphiques

Dans cette étude, nous avons construit 5 inventaires différents sur un ensemble de 47 échantillons environnementaux (voir le rapport technique ou le tutoriel pour comprendre les différences 
entre les technologies) 

* un séquençage par la technologie Ion-Torrent (PGM)
* un séquençage  par la technologie Illumina (MiSeq), avec deux façons de construire les librairies (dénommées Ligation et Tailed)
* pour chaque façon de construire les librairies, la réalisation du contigage selon une procédure standard ou en appliquant une procédure plus exigeante en terme de qualité 
(dénommée sans ou avec, soit without et with).     


Un inventaire a été construit pour chaque jeu de séquences fasta (5 = 1 + 2 x 2 par échantillon) par comparaison des séquences avec la base de référence R-Syst::diatoms. L'ensemble des inventaires est 
téléchargeable en haut de cette page, dans l'encart des fichiers téléchargeables (fichier compressé ``inventories.zip``).   

Pour chaque échantillon, deux graphiques ont été produits. Pour chaque graphique, un point représente une espèce reconnue au moins une fois pour au moins une technique. Le nombre de séquences de 
l'échantillon attribuées à cette espèce lors du séquençage PGM est en abscisse, et pour une des combinaisons technologies/contigage sur MiSeq en ordonnée. Il y a donc quatre points pour chaque espèce par échantillon. 
Les combinaisons de technologie x contigage sont indiquées par des couleurs. La diagonale (identité entre les inventaires PGM et MiSEQ est soulignée par une ligne verte. Il y a deux figures par 
échantillon : une pour le nombre de séquences, une pour les fréquences. L'ensemble des figures est téléchargeable en haut de cette page, dans l'encart des fichiers téléchargeables  
(fichier ``plots.zip``).

## Programmes et données

Le programme ``diagno-syst`` écrit en python utilisé pour réaliser les inventaires est téléchargeable à https://github.com/r-syst/tools/tree/master/diagno-syst    


Ce site contient
* le programme, téléchargeable
* une notice pour l'installation et l'utilisation de ce programme
* un jeu de données tests pour l'exécuter









