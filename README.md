# CompassLinux-Aws

ssh -i ChaveSSH ec2-user@ip

sudo dnf install httpd // instalar apache

sudo systemctl enable --now httpd.service 

sudo systemctl status httpd //ve o status do apache

-----------------------------------------------------------------

mkdir ~/efs-mount-point 

sudo mount -t nfs -o nfsvers=4.1,rsize=1048576,wsize=1048576,hard,timeo=600,retrans=2,noresvport mount-target-DNS:/   ~/efs-mount-point  //troca o mount-tarfeg-DNS pelo dns da EFS criado na aws

cd ~/efs-mount-point  

sudo chmod go+rw .

mkdir matheusReato
