# Créer une clé d'installation windows depuis Linux

## Trouver l'image ISO Windows Corespondante
https://www.microsoft.com/fr-fr/software-download/

## Obtenir l'utilitaire woeusb-v.v.v.bash
https://github.com/WoeUSB/WoeUSB/releases <br/>
chmod +x path/to/woeusb-N.N.N.bash <br/>

## Installer la dependance Wimlib
sudo add-apt-repository ppa:nilarimogard/webupd8 <br/>
sudo apt-get update <br/>
sudo apt-get install wimtools <br/>

## Utiliser la clé entière
(iso et .bash dans le même doosier )<br/>
sudo bash woeusb-v.v.v.bash --device Win11_22H2_French_x64v1.iso /dev/sda1<br/>

## Utiliser une partition de la clé
sudo bash woeusb-v.v.v.bash --partition $PWD/Win11_22H2_French_x64v1.iso /dev/sda1<br/>
<br/>
L'operation prend plusieurs minutes<br/>
