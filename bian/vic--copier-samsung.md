# Samsung Xpress M2885FW

### doas root:staff

tar -xzvf uld_V1.00.39_01.17.tar.gz


### install

a) rather  
sudo mkdir -pv /usr/local/src/samsung/  
sudo mv uld/ /usr/local/src/samsung/


b) than  
sudo mkdir -pv /opt/samsung/  
sudo mv uld/ /opt/samsung/


### printer

ipp://SEC30CDA7A77B34.local:631/ipp/print  
socket://SEC30CDA7A77B34:9100


### scanner — fix (mint 19.1 that is ubuntu 18.04)

cd /usr/lib/x86_64-linux-gnu/sane/

sudo ln -s ../../sane/libsane-smfp.so.1.0.1 libsane-smfp.so.1.0.1 \  
&& ln -s libsane-smfp.so.1.0.1 libsane-smfp.so.1 \  
&& ln -s libsane-smfp.so.1 libsane-smfp.so  