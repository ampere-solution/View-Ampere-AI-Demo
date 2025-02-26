# View-Ampere-AI-Demo
## Managing and Running Demo

* Enable firewall for public access
    + Install firewall application:
      
       ```$ sudo apt update```
      
       ```$ sudo apt install firewalld```


    + Open ports:

      ```$ sudo firewall-cmd --zone public --permanent --add-port 5000-5010/tcp```
      
      ```$ sudo firewall-cmd --reload```

* Install docker application
  
  ```$ sudo apt-get update```
  
  ```$ sudo apt-get install ca-certificates curl gnupg```

  ```$ sudo install -m 0755 -d /etc/apt/keyrings```

  ```$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg```

  ```$ sudo chmod a+r /etc/apt/keyrings/docker.gpg```

  ```$ echo "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null```
         
  ```$ sudo apt-get update```

  ```$ sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin```

   + Make sure docker is installed properly:

      ```$ sudo docker run hello-world```

* Add user to the docker group:

  ```$ sudo usermod -aG docker $USER```

   + Logout and login back to the machine
   + Check docker is added to your groups:

     ```$ groups```
  
