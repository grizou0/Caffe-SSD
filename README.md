# NCSDK V2 obselete, on utilise openvino. A partir de ssd-caffe, on convertit les fichiers caffemodel avec openvino.
(voir python mo-caffe.py)


        
Pour l'installation de ssd-caffe, on se refère au pack sur ce github.                     
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
voir reference :http://caffe.berkeleyvision.org/installation.html#compilation
On télécharge les fichiers caffe-master
                  

Depuis une nouvelle installation Ubuntu16.04, on installe ensuite caffe en mode CPU                           
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

Step 3
------
Après avoir installé ncsdk v2, on peut utiliser les examples NCAPPZOO V2                                                     
git clone -b ncsdk2 https://github.com/movidius/ncappzoo.git                                

