 # SonarQube README


## Run 

``docker-compose up -d``

 - **UNIX**
 If error: **Max virtual memory areas vm.max_map_count [65530] is too low, increase to at least [262144] appears, solve it by:**

 `` sysctl -w vm.max_map_count=262144 ``

 is correct, however, the setting will only last for the duration of the session. If the host reboots, the setting will be reset to the original value.
 If you want to set this permanently, you need to edit **/etc/sysctl.conf** and set vm.max_map_count to 262144
 
 When the host reboots, you can verify that the setting is still correct by running ``sysctl vm.max_map_count``

 
 - **MS Windows**
 For MS Windows users, using wsl subsystem
 Open powershell, run

  ``wsl -d docker-desktop``

 then

  ``sysctl -w vm.max_map_count=262144``


  ## References

 - [max-virtual-memory-areas-vm-max-map-count-65530-is-too-low-inc](https://stackoverflow.com/questions/51445846/elasticsearch-max-virtual-memory-areas-vm-max-map-count-65530-is-too-low-inc)
 - [instalacion-de-sonarqube-con-docker](https://aprenderdevops.com/instalacion-de-sonarqube-con-docker/) 

 ## Restart admin 

 ``
 update users set crypted_password='100000$t2h8AtNs1AlCHuLobDjHQTn9XppwTIx88UjqUm4s8RsfTuXQHSd/fpFexAnewwPsO6jGFQUv/24DnO55hY6Xew==', salt='k9x9eN127/3e/hf38iNiKwVfaVk=', hash_method='PBKDF2', reset_password='true', user_local='true' where login='admin';
``