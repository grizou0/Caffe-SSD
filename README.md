# Caffe-SSD
Installation caffe ubuntu 
Installation caffe ubuntu 16.04.(ne fonctionne pas sur la version 18)

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
Depuis une nouvelle installation Ubuntu16.04, on install caffe en mode CPU
Ubuntu 16.04 ne compile pas en mode CPU , mais c'est un premier pas....

