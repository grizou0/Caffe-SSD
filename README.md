# Caffe-SSD
Utilisant le sitck usb movidius, j'utilise la librairie ncsdk pour compiler le caffemodel en fichier graph (utilisable pour le module).
Les applications movidius ne fonctionnent pas si caffe et ssd-caffe sont installées en premier (probleme de PYTHONPATH);
Pour l'installation de caffe et ssd-caffe , le pack ncsdk v2 les installe après automatiquement dans le répertoire: opt/movidius/.

Installation caffe ubuntu 16.04.(ne fonctionne pas sur la version 18)
On installe simplement les pack par:
git clone -b ncsdk2 https://github.com/movidius/ncsdk.git
l'installation se fait par
make install
make examples.

Apres installation on retrouve mvNCCompile pour transformer le caffemodel en fichier graph (utilisable avec movidius).
Pour l'installation de ssd-caffe
https://github.com/grizou0/Caffe-SSD/blob/master/Installation%20CPU
https://github.com/grizou0/Caffe-SSD/blob/master/Installation%20GPU 


Tester avec Ubuntu 16.04 et modele caffe-ssd (fonctionne avec le modele caffe) 

Reference youtube installation mode CPU 
https://www.youtube.com/watch?v=DnIs4DRjNL4 
(le fichier ssd_pacal.py, .... et le train ne fonctionne qu'en mode GPU (utiliser CUDA par apres) 
Suivre les instructions d'installations. 
Le model caffe-ssd est en upload: 
https://github.com/weiliu89/caffe/tree/ssd 
Plusieurs essais son concluant avec le modele SSD, MobileNet-SSD..... 
Le but étant de créer un modelcaffe utilisable avec la compilation du fichier graph et le module Movidius USB.

First step
----------
Télécharger ncsdk v2, le pack movidius installe également le pack caffe et ssd-caffe en /opt/movidius/

Depuis une nouvelle installation Ubuntu16.04, on install caffe en mode CPU
En mode CPU, le training (ssd_pascal.py) est très lent mais fonctionnel.

ssd_pascal_webcam.py fonctionne moyennant la modification mais est très lent.
ligne 102 solver_mode = P.Solver.CPU

Pour ssd_pascal.py pour le training, on modifie 
ligne 341 solver_mode = P.Solver.CPU

https://github.com/grizou0/Caffe-SSD/blob/master/Installation%20CPU

Second Step
-----------
On ajoute cuda. Cela permet de faire tourner caffe en mode GPU
https://github.com/grizou0/Caffe-SSD/blob/master/Installation%20GPU


