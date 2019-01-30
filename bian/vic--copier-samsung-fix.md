# Samsung Xpress M2885FW
### unpack

+ **doas root:staff**
  
  ```
  tar -xzvf uld_V1.00.39_01.17.tar.gz
  ```


### install

+ **script pakage location**  
  - [x] rather
  
  ```
  sudo mkdir -pv /usr/local/src/samsung/
  sudo mv uld/ /usr/local/src/samsung/
  ```
  
  - [ ] than
  
  ```  
  sudo mkdir -pv /opt/samsung/src/
  sudo mv uld/ /opt/samsung/src/
  ```


+ **printer**  
  `ipp://SEC30CDA7A77B34.local:631/ipp/print`  
  `socket://SEC30CDA7A77B34:9100`


+ **scanner-fix** _« \(Ubuntu18.04<sup>Mint19.1</sup>\)_  
  [ :arrow_up_small: https://bugs.launchpad.net/ubuntu/+source/sane-backends/+bug/1728012 ](https://bugs.launchpad.net/ubuntu/+source/sane-backends/+bug/1728012)
  
  ```
  cd /usr/lib/x86_64-linux-gnu/sane/
  ```
  ```
  sudo ln -s ../../sane/libsane-smfp.so.1.0.1 libsane-smfp.so.1.0.1 \  
  && sudo ln -s libsane-smfp.so.1.0.1 libsane-smfp.so.1 \  
  && sudo ln -s libsane-smfp.so.1 libsane-smfp.so
  ```