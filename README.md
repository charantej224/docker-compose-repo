# docker-compose-repo

PRE-REQUISITES:
1. docker 
2. docker-compose to be installed in the machine.
3. ensure below ports are un-used : 
    a. port for employee service mysql database - 3307 
    b. port for event service mysql database - 3308
    c. RabbitMQ message broker uses :- 5672 & 15672 
    d. Employee Service endpoints hosted on  - 9094
    e. Event Service endpoints hosted on - 9095
    f. Integration tests port - 52310, 51010

Step to start the process: 
This is the repository for the required docker compose files to create containers.
containers required :-
1. mysql - Employee MicroService dedicated database. 
2. mysql - Department MicroService dedicated database.
3. rabbitmq - message broker between employee and department micro services.

step1: clone the repository
git clone https://github.com/charantej224/docker-compose-repo.git

step2: change the directory
cd docker-compose-repo/

step3: run docker compose using command below (-d to start as demon process)
docker-compose -f consolidated/docker-compose.yml up -d

NOTE : if containers are already running run the below command to stop and remote the containers.
docker-compose -f consolidated/docker-compose.yml down

Note: Please ensure the containers are healthy and running using (docker ps)
