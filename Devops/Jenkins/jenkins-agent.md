### launch two instances 
<img width="1903" height="640" alt="image" src="https://github.com/user-attachments/assets/b4d4233e-caa9-4310-b143-46b86859efe8" />
<img width="1912" height="1071" alt="image" src="https://github.com/user-attachments/assets/29915655-49ef-4bc8-ba00-f85bb9f5a5b6" />

### on master node generate ssh keypair 

<img width="1487" height="151" alt="image" src="https://github.com/user-attachments/assets/df352f50-f9b7-4d56-80ac-f8369cdd0d49" />

### now copy this public key to worker node .ssh/autorized_keys file
````
vim .ssh/authorized_keys
````
<img width="1916" height="962" alt="image" src="https://github.com/user-attachments/assets/7b4b6877-589b-4513-a674-96b66ad5c812" />

- create dir and assign 777 perm
- also install java
  
````
sudo apt update
sudo apt install fontconfig openjdk-21-jre -y
````
<img width="1063" height="118" alt="image" src="https://github.com/user-attachments/assets/4c7cfd9f-9602-4681-a3a1-a99b3e16cd9e" />

### go to jenkins click on manage jenkins(settings) and add creds
<img width="1650" height="906" alt="image" src="https://github.com/user-attachments/assets/5ebaf5c5-040b-4072-a4c4-c756a003ea27" />
<img width="1303" height="301" alt="image" src="https://github.com/user-attachments/assets/228eba05-025b-41e9-955b-84699b89eb80" />
<img width="706" height="820" alt="image" src="https://github.com/user-attachments/assets/66e013ae-0d4b-4eca-a140-b1600763947e" />

### add new node
<img width="1648" height="812" alt="image" src="https://github.com/user-attachments/assets/9488a4af-5003-4c08-a842-2b59d18bd93c" />
<img width="1522" height="472" alt="image" src="https://github.com/user-attachments/assets/5560018e-517b-4104-b552-a63dc02ac544" />
- node: in host section add worker node ip

<img width="1546" height="226" alt="image" src="https://github.com/user-attachments/assets/310fcc1c-2ac8-4e48-840c-4f8976cbb33f" />
