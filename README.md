# View-Ampere-AI-Demo
## Managing and Running Demo

* Enable firewall for public access
    + Install firewall application:
      
       ```$ sudo apt update```
      
       ```$ sudo apt install firewalld```


    + Open ports:

      ```$ sudo firewall-cmd --zone public --permanent --add-port 5000-5010/tcp```
      
      ```$ sudo firewall-cmd --reload```
