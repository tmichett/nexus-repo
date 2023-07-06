# nexus-repo
Nexus Repository and Registry

docker volume create --name nexus-data
docker run -d -p 8081:8081 --name nexus -v nexus-data:/nexus-data quay.io/tmichett/nexus-registry:3.43-ubi

or

podman volume create --name nexus-data
podman run -d -p 8081:8081 --name nexus -v nexus-data:/nexus-data quay.io/tmichett/nexus-registry:3.43-ubi


Then you need to get the admin password:

$ docker exec -it nexus /bin/bash
bash-4.4$ cd /nexus-data/
bash-4.4$ cat admin.password
