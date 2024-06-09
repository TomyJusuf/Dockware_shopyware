## Dockerware & Shopyware

You can find many tutorial, but many of them had problem for you to load/starting the project?
If yes, I found solution with chatGTP.

Change the port/ports, it must be like that, here:

        services:
        shopware:
         # use either tag "latest" or any other version like "6.5.3.0", ...
        image: dockware/dev:6.5.8.10
        container_name: shopware
        ports:
          - '8081:80'
          - '3302:3306'
          - '2022:22'
          - '8802:8888'
          - '9902:9999'

Ensure no other services are using port 8081. You can check with:

    sudo lsof -i :8081

You have to run the project like that:
You must have installed docker.io

-type command

    docker-compose -up -d

Open you browser and use/run which one u want:

        http://localhost:8081/admin  <-- HERE YOU MOSTLY WILL WANT WORK
        http://localhost:8081/logs/
        http://localhost:8081/mailcatcher
        http://localhost:8081/adminer.php

Open in browser

    https://docs.dockware.io/use-dockware/default-credentials

    The login is for http://localhost:8081/admin
    User: admin
    Password: shopware

Please, forgive me my poor english and keep the docu as cheatsheet and not as solution for everything.

Here I share also good tutorial where you can learn:

    https://youtube.com/playlist?list=PLIunO7UzbF_qGzdtiKPALExSeGho0FOy1&si=wgdSKh3dU69IQJ4u

---

The cheatsheed is Created be Tomas Matusek.



docker exec -it bbecf51af4e1 bin/console
